# Milestone 1

### Title

Fake News : What ? When ? and Why ? Who can tell ?

### Abstract
A 150 word description of the project idea, goals, dataset used. What story you would like to tell and why? What's the motivation behind your project?

The theme of this year is "Data Science for social goods". We will try to follow this theme by helping people not believing everything they see by giving certain directional axes. In order to do so, we will first establish some facts drawn from the data to show how much fake news can affect us and how the crowd can easily be fooled. We will also try to show that some news (not necessarily false or true : we will use for example the false-true or barely true labels) are made to create doubt and decredibilize some people or organizations. We will try to give some directions by trying to find recurrent patterns of fake news, their features, their trends and how they are delivered in order to warn people to always cross check their references to avoid being fooled half of the time. 



### Research questions
A list of research questions you would like to address during the project. 

- Repartition of the provenance of these fake news. (LIAR)
- Repartition in time of the aggregation of fake news in total, and according to their provenance (LIAR)
- Make the connection between a fake news (LIAR) and the number of tweet (and retweets) by subject (IRA) :
Are there some subjects that have buzzing way more than others, why ?? If it is possible to know when it happened, try to find a justification for it.
- Do most of the fake news come from one particular political party ? Are there reason for it ? Is it the opposing party versus the ruling power ? Is it the other way around -> Propaganda ?
- Is it possible to draw some inferences from it ? Is it more likely to have fake news from either region, party ? How to identify them ? what ressources are mostly used for fake news ? Social media? Press release ? ....
- Can we identify them ? Can we classify some sources as reliable from the dataset , through some credit history ?


### Dataset
List the dataset(s) you want to use, and some ideas on how do you expect to get, manage, process and enrich it/them. Show us you've read the docs and some examples, and you've a clear idea on what to expect. Discuss data size and format if relevant.

We use two data sets :  The LIAR and IRA datasets.

- LIAR Data set :
10269 human labeled short statements s from POLITIFACT.COM’s API.
** labels : pants-fire, false, barelytrue, half-true, mostly-true, and true (distribution pretty-well balanced)
** other attributes : subject, author of the statement, what the author represent (media, government..), geographic origin (Us state), political party of the author, the credit history vector of the author (counts of pants fire, false, barelytrue...) and the where the statement was emitted. (campaign debate, press release, website...)

-  Data Set : 
8 CSV sheets of more than 370k rows + 1 sheet of 37k rows(sheets differ by their author). Each row represent Tweets of IRA (Internet Research Agency) trolls about U.S politics. 77% of the tweets are in english while 13% in Russian and other languages represent 11% of the data. We will only consider english tweets here.
Each tweet is described by its author, the content, the region it comes from, the language used, its publication and harvested date, the number of people following the author and the number of people he is following, the number of update of the current tweet(I think it is the number of retweets, likes.. ?), and the post category, is it an original tweet or a retweet ?

### A list of internal milestones up until project milestone 2
Add here a sketch of your planning for the next project milestone.

The milestone 2 is due for November 25, until then, here is a tentative schedule we will try to follow.

- November 11 : Data Exploration : Distribution of fake news among author/group/organisations, where do they come from, when are they released if possible. Exploration of the IRA data set, can we find patterns, clusters ?
- November 18 : Draw some inferences from the data. Make some links/connections between the two data sets and think about the best way to extract meaningful information from the combination of both.
- November 25 : Complete descriptive analysis of the two previous steps and plan the next steps for milestone 3 : which direction do we need to continue to follow, which one to remove and think if we will need extra informations/data to complete our story. 

Hand over this milestone.


### Questions for TAa
Add here some questions you have for us, in general or project-specific.

Among the directionnal axes given/proposed, which one are more/less feasible and relevant ?


# Milestone 2



The vision we have for our datastory is a guide for the average citizen to make him more critical about information. Indeed with the exponential spread of data accessible to everyone, the challenge of getting rightly informed is getting harder and harder. 
Our aim is to make the distinction between the 'safe' and 'unreliable' topics and sources of information.

In order do this we decided to focus only on the LIAR dataset. The feedback of Milestone 1 suggested the use of advanced natural language processing techniques which will recquire our full commitment.

We ran a first descriptive analysis of our data, and already discovered some insights on the final guide.

The next steps include feature engineering.
Here are the directions we wish to investigate: 

  - Tagging of the different grammatical value of the words (Pronouns, nouns, verbs, ...)
  - Comparing the term frequencies of the english language and the english of our list of statements
  - TF-IDF (Term Frequency - Inverse Document Frequency) values as a metric
  - Detrminig the relevance of our different features (geographical origin, political affiliation, topic)
  - Creating a credit history feature of the authors using the five given columns (finding an relevant metric from the 5)
  
We will run the interpretable machine learning techniques, Logit model and Random Forest most likely, in order to determine the relevant features so as to complete the guide.
We will verify our assumptions using the provided test set.

# Milestone 3

**Composition of the repository**

This repository contains : 
  - A notebook describing our full investigation with preprocessing tasks, descriptive analysis along with visualizations and results obtained.
   - A 4-page PDF file containing the report of our work
   - Plotted Visualizations of our random forest model

**Repartition of the work**
  - In Milestone 1, Thevie provided the backbone of descriptive analysis of the code, while  Timothee and Patrik investigated possible  directions of the project. 
  - In Milestone 2, Timothee came up with the data story of the project writing up textual descriptions and interpretations questioning our results, while Thevie did the preprocessing tasks and topics analysis and Patrik did descriptive analysis on contexts (sources) and geographical origin of the news.
  - Finally, in Milestone 3, Patrik came up with most of the machine learning code with their results, Thevie and Timothee focused on completing descriptive analysis tasks and writing up the report.

**Final Presentation**
The final presentation shall be done by the three members of the group.
