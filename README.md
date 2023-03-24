<h1>Uncovering the Role of Structural Properties in Food Association Networks</h1>
<em>Kianté Fernandez<sup>1</sup>, Uma R. Karmarkar<sup>3</sup>, Ian Krajbich<sup>1,2</sup></em></br>1 Department of Psychology, The Ohio State University; 2 Department of Economics, The Ohio State University; 3 Rady School of Management, University of California, San Diego </br> </br>

Preference-based decisions, like choosing what to eat, often depend on associations between the options. For example, when selecting a fruit basket for the holidays, the relations between fruits contribute to the overall attractiveness of a basket. However, quantifying the relations between options is a non-trivial task. Ideally, the relations between options should relate to how they’re organized in a person’s memory. In this poster, I introduce a novel approach that utilizes semantic network modeling to quantify relations between groups of food options. By extracting descriptive measures of network organization, I showcase how the structure of knowledge representations of preferences can produce behavioral phenomena like choice, response times, and similarity judgments. In this study our goals are </br>

1. to investigate a new application of modeling knowledge representations as networks to quantify relations, between groups of options within preferential decision-making </br>
2. to examine how the structure of knowledge representations of preferences produces behavioral phenomena like choice, response times, and similarity judgments </br>

<img src="food_network_icon.png" alt="food association network" title="knowledge representation of liking preferences">

<b>Keywords</b>: decision making, centrality, network analysis, knowledge representations

<h2>Background</h2>
<details>
  <summary>Definitions</summary>
   
  **Centrality**</br>
    By constructing a network representation, we are developing a measurement instrument to subsequently investigate its structure. Network modeling approaches allows us to examine different properties of nodes and edges, most commonly focusing on quantifying the “importance” of a node in the graph representation via centrality measures (Borgatti, 2005). That is, the centrality of nodes within a network can be used to inspect the structural importance of different nodes. Prior work suggests that network structure explains a range of behavioral phenomena like language processing (Vitevitch et al., 2014) and creative problem solving (Kenett et al., 2014), as well as in clinical settings like autism spectrum disorder (Kenett et al., 2016) and major depressive disorder (Boschloo et al., 2016). Node centrality, in particular, has been shown to influence decision-making (Dalege, Borsboom, van Harreveld, Waldorp, & van der Maas, 2017).

  **Subgraph**</br>
    We also interested in characterizing how sets of food items are related to one another. Thus, we need to select groups of food items from our larger food association network. More specifically in graph theory terms we are creating induced subgraphs of our association network. Let's say we have a graph $G=(V,E)$, where $V$ is the set of nodes, and $E$ denotes the edges between them. An induced subgraph of $G$ is any graph $S=(V^{*},E^{*})$ such that $V^{*} \subseteq V$ $V$ and $E^{*} \subseteq E$ that also satisfies the additional constraint that the subgraph of $G$ induced by $S$ is a graph that has $S$ as its set of nodes and all the edges of $G$ that have both endpoints in $S$. In words, we are creating sets of induced subgraphs that are formed from a subset of the food items of the food association network while retaining and all of the edges connecting pairs of food items in that subset.
</details>

<h2>Tasks Description</h2>

<details>
    <summary>Exposure and Ratings</summary>
    Participants first passively observed images of 60 individual snack foods. Each food was presented for 750 ms. Then, for each individual snack food, participants were asked to rate how much they would like to eat this food right now. Participants used a mouse to rate their desire to consume each of the 60 snack foods on a scale. The scale appeared to participants to be continuous, and the data was captured in increments of 1 (ranging from 1 to 100). Participants were be told to make the rating on a scale from “Not at all” to a rating of “Very much!” indicating that they really would like to eat the food item right now. Participants were able to revise their rating as many times as they liked before finalizing it. Participants clicked the “continue” button to finalize their value rating response and proceed to the next screen. This process continued for all 60 items.
 </details>

 <details>
    <summary>2AFC</summary>
    Participants completed a binary choice task using the generated arrays of snack foods from the constructed food association network. In each trial, participants were presented with two arrays of food items, one array on each side of the screen, and were instructed to choose their preferred array of food items that they would most prefer to eat right now. Participants used the F key to choose the array of food items on the left side of the screen and the J key to choose the array of food items on the right side of the screen. Participants were instructed to make selections at their own pace. Each trial was designed so that the two arrays of food items differ in centrality. In addition, no pair of food item arrays were shown more than once. Each trial consisted of two arrays from the set of 100 presented in random order. Participants completed a total of 99 trials.
</details>

 <details>
    <summary>Similarity judgments</summary>
    In experiment two, after preforming the rating and choice task, for each of the 100 previously shown groups of items, subjects were asked to assess the preference similarity for each group of foods. For each group of items, subjects were asked to rate: if someone likes one of the foods, how likely is it that they also similarly like the other foods? Subjects were told to make the rating on a scale from “Not at all likely” to “Very likely”. Subjects used a mouse to rate each item on a scale. The scale appeared to be continuous, and the data was captured with integers ranging from 1 to 100.
</details>

<h2>Association Network Construction</h2>
    Because we required an association network to create the experimental stimuli, we estimated a network from previously collected rating data from Lee & Holyoak, 2021. Using the rating data from our analysis of Lee & Holyoak, we: estimated an association network, removed spurious connections using model selection procedures, and partitioned the graph into clusters. Then using the estimated network structure, we extracted subgraphs of items with different network organization to create our stimulus set. All network measures in this study used the Lee & Holyoak network to compute relevant statistics (e.g., degree, or edge density). </br></br>
    We implemented the Network Estimation Method and Community Detection Algorithm below by conducting Exploratory graph analysis (EGA), a recently developed method to estimate the number of communities in multivariate data using undirected network models (Golino & Epskamp, 2017; Golino et al., 2020). EGA first applies a network estimation method (in our case EBICglasso) followed by a community detection algorithm for weighted networks (in our case, the Walktrap algorithm). EGA has been shown to be as accurate or more accurate than more traditional factor analytic methods (Christensen, Garrido, & Golino, 2021; Golino et al., 2020; Merritt & Christensen, 2022).</br></br>

<details>
  <summary>Network estimation</summary>
</details>
    To estimate the network structure, we applied the graphical least absolute shrinkage and selection operator (GLASSO; Friedman, Haste, & Tibshirani, 2008, 2014), which estimates a Gaussian Graphical Model (GGM; Lauritzen, 1996) where nodes (food items) represent variables and edges (partial correlations) represent the conditional dependence between nodes given all other nodes in the network. The least absolute shrinkage and selection operator (LASSO; Tibshirani, 1996) of the GLASSO is a regularization technique that reduces parameter estimates, with some estimates becoming exactly zero. The LASSO uses a parameter called lambda ($\lambda$), which controls the sparsity of the network. When $\lambda$ = 0, the estimates equal the ordinary least squares solution for the partial correlation matrix. Based on previous work in the network psychometrics literature, we computed network models across one hundred values of $\lambda$ and select the model that minimizes the extended Bayesian information criterion (EBIC; Chen & Chen, 2008; Epskamp & Fried, 2018). The EBIC model selection uses a hyperparameter gamma ($\gamma$) to control how much it prefers simpler models (i.e., models with fewer edges; Foygel & Drton, 2010). Larger $\gamma$ values lead to simpler models, while smaller $\gamma$ values lead to denser models. When $\gamma$ = 0, the EBIC equals the Bayesian information criterion. This study follows recommendations from previous work and set $\gamma$ to 0.5 (Epskamp & Fried, 2018).</br></br>
<details>
  <summary>Community Detection Algorithm</summary>
    To partition the estimated network into subsets of nodes that are 1) well connected among themselves and 2) relatively well separated from the remaining nodes. We apply the the Walktrap algorithm (Pons & Latapy, 2006; Fortunato, 2010), a commonly applied community detection algorithm in the psychological network literature (Golino & Epskamp, 2017; Golino et al., 2020). The algorithm begins by computing a transition matrix where each element represents the probability of one node traversing to another (based on node strength or the sum of the connections to each node). Random walks are then initiated for a certain number of steps (e.g., 4) using the transition matrix for probable destinations. Using Ward's agglomerative clustering approach (Ward, 1963), each node starts as its own community and merges with adjacent communities (based on squared distances between each community) to minimize the sum of squared distances between other communities. Modularity (Newman, 2006) is then used to determine the optimal partition of communities.</br></br>
</details>

<details>
  <summary>Principal component analysis (PCA)</summary>
    While a range of possible centrality measures is available, people likely do not track or utilize any exact measure of centrality per se but rather the variances reflected by centralities. Furthermore, as the number of centrality measures increases, interpreting each measure in isolation becomes challenging due to issues of multicollinearity and dimensionality. Principal component analysis (PCA) is a statistical technique that can help us understand the importance of any given node rather than relying solely on any single measure of centrality.</br></br>
    PCA linearly transforms input data into an equal number of linearly uncorrelated variables called Principal Components (PCs) that cumulatively account for an additional portion of the remaining data variance (Kambhatla et al., 1997). To reduce the dimensionality of the data, we consider the minimum set of largest PCs, i.e., the principal subspace, that accounts for at least some pre-defined variance threshold (usually in the range of 80%-95% of original data variance) for further analyses.</br></br>
    In our case, by transforming the data into a lower dimensional space, we can facilitate capturing higher-order notions of node importance. Thus, we conducted a PCA to decompose variances in the node metrics into components aligned with network measures. As PC 1 and PC 2 jointly account for more than 80% of the total variances in node parameters under consideration, the PCs act as our network statistic scores for our behavioral analysis. Using the PC scores, we assigned each food item two node importance scores and assessed the effect of node importance by PC 1 and 2 alone or by PCs 1 and 2 combined.</br></br>

</details>

<h2>Regression Tables</h2>
Here are the corresponding regression tables for each of the figures on the poster.</br></br>
<details>
    <summary>Table one</summary>
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax">&nbsp;&nbsp;&nbsp;<br>&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="font-weight:bold;color:white">Experiment one</span>&nbsp;&nbsp;&nbsp;</th>
    <th class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="font-weight:bold;color:white">Experiment two</span>&nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">left&nbsp;&nbsp;&nbsp;liking rating</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">0.90***&nbsp;&nbsp;&nbsp;[0.69, 1.11]</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">0.79***&nbsp;&nbsp;&nbsp;[0.68, 0.91]</span>&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">right&nbsp;&nbsp;&nbsp;liking rating</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">−0.75***&nbsp;&nbsp;&nbsp;[−0.96, −0.55]</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">−0.81***&nbsp;&nbsp;&nbsp;[−0.93, −0.70]</span>&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">left&nbsp;&nbsp;&nbsp;network estimate</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">0.16**&nbsp;&nbsp;&nbsp;[0.05, 0.26]</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">0.11**&nbsp;&nbsp;&nbsp;[0.04, 0.18]</span>&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">right&nbsp;&nbsp;&nbsp;network estimate</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">−0.23***&nbsp;&nbsp;&nbsp;[−0.33, −0.13]</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">−0.10**&nbsp;&nbsp;&nbsp;[−0.17, −0.03]</span>&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">left&nbsp;&nbsp;&nbsp;rating × network estimate</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">0.12*&nbsp;&nbsp;&nbsp;[0.01, 0.23]</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">−0.06+&nbsp;&nbsp;&nbsp;[−0.13, 0.01]</span>&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">right&nbsp;&nbsp;&nbsp;rating × network estimate</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">0.00&nbsp;&nbsp;&nbsp;[−0.11, 0.10]</span>&nbsp;&nbsp;&nbsp;</td>
    <td class="tg-0lax">&nbsp;&nbsp;&nbsp;<br><span style="color:black">0.04&nbsp;&nbsp;&nbsp;[−0.03, 0.11]</span>&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>
</details>

<h2>References</h2>

1) Evers, E. R. K., Inbar, Y., & Zeelenberg, M. (2014). Set-fit effects in choice. Journal of Experimental Psychology: General, 143(2), 504–509. https://doi.org/10.1037/a0033343

2) Lee, D. G., & Holyoak, K. J. (2021). Coherence shifts in attribute evaluations. Decision, 8(4), 257. https://doi.org/10.1037/dec0000151

3) Collins, A. M., & Loftus, E. F. (1975). A spreading-activation theory of semantic processing. Psychological Review, 82, 407–428. https://doi.org/10.1037/0033-295X.82.6.407

4) Bhatia, S., & Mullett, T. L. (2018). Similarity and decision time in preferential choice. Quarterly Journal of Experimental Psychology, 71(6), 1276–1280. https://doi.org/10.1177/1747021818763054

5) Evers, E., Park, A., & Lakens, D. (2019). Low Complexity Drives Similarity Judgments Within Bundles of Products. ACR North American Advances.

6) Siew, C. S. Q., Wulff, D. U., Beckage, N. M., & Kenett, Y. N. (2019). Cognitive Network Science: A Review of Research on Cognition through the Lens of Network Representations, Processes, and Dynamics. Complexity, 2019, e2108423. https://doi.org/10.1155/2019/2108423

7) Christensen, A. P., & Golino, H. (2021). Estimating the Stability of Psychological Dimensions via Bootstrap Exploratory Graph Analysis: A Monte Carlo Simulation and Tutorial. Psych, 3(3), Article 3. https://doi.org/10.3390/psych3030032