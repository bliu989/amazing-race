# The Amazing Race team archetypes

A good reality TV show needs a variety of interesting archetypes. The Amazing Race, which first aired in 2001, is airing its 36th season in March 2024. Throughout its long history, there have been a lot of different teams from various backgrounds and with various relationships with one another. Discovering themes within the teams of the cast can help inform future casting decision. The aim of this project is to find out what are the underlying team archetypes in the Amazing Race. To achieve this, we use the team biographies from the Amazing Race Wiki. 

I first scraped the teams' biographies from the wiki. Since these biographies were ultimately from different sources from season to season and the format of the biographies varied from season to season, I cleaned the data to avoid teams from the same season from being too similar when processed through the models. For example, some of the biographies from certain seasons have the same questions within the biographies. Since these questions are in bold, I simply removed all words in the biographies that are within bold tags. 

I looked at three different types of Natural Language Processessing (NLP) algorithms for the task of grouping similar teams together based on their biographies. I looked at tf-idf + k-means, non-negative matrix factorization (NMF), and latent Dirichlet allocation (LDA) with various number of groups. The grouping that made the most sense came from the NMF algorithm with 8 groups. The 10 teams that are most representative of each group and words that are most representative of each group are visualized below. While some teams in these groups don't necessarily fall into the group they were assigned to, the overall archetypes agree with my experience watching the show.

Group 1 - Twins/siblings in their 20s

![](word%20clouds/cluster%200.png)

Group 2 - Friends/dating in their 30s

![](word%20clouds/cluster%201.png)

Group 3 - Competitive friend/family teams who want to experience other cultures

![](word%20clouds/cluster%202.png)

Group 4 - Retired married couples and police officers

![](word%20clouds/cluster%203.png)

Group 5 - Students in their 20s

![](word%20clouds/cluster%204.png)

Group 6 - Dating teams

![](word%20clouds/cluster%205.png)

Group 7 - Parent/child teams

![](word%20clouds/cluster%206.png)

Group 8 - Military teams and Davids

![](word%20clouds/cluster%207.png)
