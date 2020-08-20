# orlando_gunshot_twitter_analysis
Please read the blog at [Initium Lab](http://initiumlab.com/blog/20160622-orlando-gunshot/)
## Methodology

We take advantage of twitter public API to scratch data by locations. We first selected each state’ s biggest city to represent that state. Then the tweet-created time was limited between  12:00, June 12, to 24:00, June 13 (36 hours). For each city (50 cities in total), our rooftop is 10000. No matter how many tweets the API returned in each city, they will be returned randomly by the created time in the period. Moreover, our searching keywords included: “#OrlandoShooting”, “#Orlando”, ” #OrlandoUnited”, “#TwoMenKissing” and  “#LoveIsLove”.  

As for the sentiment score calculation, we used the lexicon-based method. The dictionary comes from Liu Bing, Hu Minqing  and Cheng Junsheng (2005), Opinion Observer: Analyzing and Comparing Opinions on the Web. You can find the resource here. The higher the scores, the more positive words the tweet has; the lower the scores, the more negative words the tweet has. 

In the word cloud processing, we removed all retweeted tweets and only kept unique tweet text. “Orlando” actually appeared 5,1535 times which is the most frequent word. The size of “Orlando” was adjusted on purpose to fit the word cloud. 

In the last part of the analysis, we employed two independent coders to code the emotion, since the sentiment package in R is not reliable enough (only about 20%~40% accuracy compared to manually coding result). We selected the most retweeted tweets which had been retweeted more than 50,000 times in the limited period. And then filtered out duplicated texts. Our Cohen’s Kappa is 0.722 which achieved a substantial agreement in inter-coder reliability. 
