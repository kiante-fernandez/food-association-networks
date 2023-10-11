<h1>Uncovering the Role of Structural Properties in Food Association Networks</h1>
<em>Kianté Fernandez<sup>1</sup>, Uma R. Karmarkar<sup>2</sup>, Ian Krajbich<sup>1</sup></em></br>1 Department of Psychology, University of California Los Angeles; 2 Rady School of Management, University of California, San Diego </br> </br>

**Research Question**: How do people choose between menus of options, like when choosing which restaurant to dine in or which store to shop in? Such decisions involve comparing sets of items, whose value may relate to the cohesiveness of their options. A shop with similar items may be more appealing than one with dissimilar items. Thus, a major challenge in testing such questions is identifying similarity. Here, we define similarity as the degree to which items are associated with each other. We study the associations between items using network models, where relations between items (nodes) are represented as connections (edges). In these models, items that fit together are more closely and densely connected. Across two studies, we use network models to understand how individual items relate to each other and how those relations affect choices between sets. </br>

**Methods**: To quantify relations between items, we estimated an association network using a study where subjects rated a variety of food items (N = 267; Lee & Holyoak, 2021). From this network, we extracted several measures of node importance and connectedness, to see how those features might affect choices between sets of those foods.  </br>
In our new studies, subjects chose repeatedly between two sets of six foods each; the studies varied on whether subjects would receive all the items or only one item from a chosen set.  Subjects also provided liking ratings for each individual food; in the second study they also provided similarity judgments for the sets of foods.  </br>

**Results**: Our network analysis yielded seven communities, which clearly mapped onto distinct categories like fruit, chocolate, and chips. Within communities, foods that would have been predicted to be similar, like raspberries and blackberries, were indeed closely related. Building on this, across two studies (N = 30; N = 75), we found that network structure played a significant role in choosing between sets (Study 1: beta = 0.16, 95% HDI [0.05, 0.26], Study 2: beta = 0.11, 95% HDI [0.04, 0.18]). Controlling for individual items’ liking ratings, subjects were more likely to choose sets containing items with high node strength and clustering coefficient. Moreover, subjects’ similarity judgments in the second study correlated with the strength of connectivity between foods in the set (rho = 0.42, 95% HDI [0.25, 0.55]).</br>

**Conclusions**: Unlike previous work deriving semantic memory representations from statistical regularities in text (Bhatia & Aka, 2022) or semantic fluency tasks (Zemla & Austerweil, 2018), we show that relational representations can be derived from preference data, and that they align well with subjective measures of similarity. Moreover, we demonstrate that these relations affect people’s choices between sets – people prefer sets with more well-connected items. Our work highlights the usefulness of network science in the study of preferences and provides a new tool for assessing how well sets of items fit together.</br>

<img src="food_network_icon.png" alt="food association network" title="preference representation of liking preferences">

<b>Keywords</b>: decision making, centrality, network analysis, preference representations

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
   Participants completed a binary choice task using the generated sets of foods from the constructed food association network. In each trial, participants were presented with two sets, one on each side of the screen and were instructed to choose their preferred set that they would most prefer to eat. Participants used the F key to choose the set on the left side of the screen and the J key to choose the set on the right side of the screen. Participants were instructed to make selections at their own pace. Each trial was designed so that sets differed in centrality. In addition, no pair of sets was shown more than once. Each trial consisted of two sets from the set of 100 presented in random order. Participants completed a total of 99 and 100 trials in Experiments 1 and 2 & 3 respectively. 
</details>

 <details>
    <summary>Similarity judgments</summary>
    In Experiment 2 and 3, after preforming the rating and choice task, for each of the 100 previously shown sets, participants were asked to assess the preference similarity for each set. For each set, participants were asked to rate: if someone likes one of the foods, how likely is it that they also similarly like the other foods? Participants were told to make the rating on a scale from “Not at all likely” to “Very likely”. Participants used a mouse to rate each item on a scale. The scale appeared to be continuous, and the data was captured with integers ranging from 1 to 100.
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

<h2>References</h2>

1) Evers, E. R. K., Inbar, Y., & Zeelenberg, M. (2014). Set-fit effects in choice. Journal of Experimental Psychology: General, 143(2), 504–509. https://doi.org/10.1037/a0033343

2) Lee, D. G., & Holyoak, K. J. (2021). Coherence shifts in attribute evaluations. Decision, 8(4), 257. https://doi.org/10.1037/dec0000151

3) Collins, A. M., & Loftus, E. F. (1975). A spreading-activation theory of semantic processing. Psychological Review, 82, 407–428. https://doi.org/10.1037/0033-295X.82.6.407

4) Bhatia, S., & Mullett, T. L. (2018). Similarity and decision time in preferential choice. Quarterly Journal of Experimental Psychology, 71(6), 1276–1280. https://doi.org/10.1177/1747021818763054

5) Evers, E., Park, A., & Lakens, D. (2019). Low Complexity Drives Similarity Judgments Within Bundles of Products. ACR North American Advances.

6) Siew, C. S. Q., Wulff, D. U., Beckage, N. M., & Kenett, Y. N. (2019). Cognitive Network Science: A Review of Research on Cognition through the Lens of Network Representations, Processes, and Dynamics. Complexity, 2019, e2108423. https://doi.org/10.1155/2019/2108423

7) Christensen, A. P., & Golino, H. (2021). Estimating the Stability of Psychological Dimensions via Bootstrap Exploratory Graph Analysis: A Monte Carlo Simulation and Tutorial. Psych, 3(3), Article 3. https://doi.org/10.3390/psych3030032