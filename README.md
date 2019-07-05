# analysing-financial-transcripts
Text analytics on Verizon's financial transcripts

Code contains -
*Part I - READING IN DATA + BASIC PREPROCESSING
*Part II - DATA PROCESSING + FEATURE ENGINEERING
*Part III - PRELIMINARY DATA ANALYSIS 
*Part IV - FREQUENCY ANALYSIS
*Part V - LDA TOPIC MODELING
*Part VI - TOPIC SENTIMENT ANALYSIS
*Part VII - SPEAKER (CEO/CFO) SENTIMENT ANALYSIS


The analysis is over a total of 261 financial documents pertaining to Verizon (NYSE: VZ) over a 15-year period (2002 Q2 - 2017 Q3). The documents primarily consisted of quarterly earnings calls, press announcements, and investor conference calls. Using these documents, my primary goal was to reduce “noise” and optimize information extraction. To do this, I began by using topic modeling techniques to determine the most important themes to further analyze. I then performed a variety of sentiment analyses to evaluate the views and attitudes towards these important topics over time. Additionally, I focused on the sentiment of Verizon’s CEO and CFO since they are top-level management and tend to discuss significant, big-picture items that are inextricably linked to the overall health of the company. 
The analysis primarily focused on topic modeling and sentiment analysis.

### Topic Modeling 
I implemented LDA Topic Modeling over two document categories - Verizon Earnings and Verizon Conferences. The intuition behind implementing topic modeling and sentiment analysis separately for each of these document categories is that the nature of each category type is different and hence different document types lend to different topics. The topic number was determined through advanced topic modeling and then confirmed through manually examining the word distribution (beta values) and the contextual meaning of the words within the different topics. Topic modeling helped us determine a variety of topics that could be further examined through sentiment analysis to gain insights into events such as acquisitions, industry-wide metrics such as user retention, churn and Verizon products such as “Fios”, ”Verizon Cloud”, etc.

### Sentiment Analysis
I also examined the sentiment across speaker type, specifically the sentiment for Verizon’s CEO and CFO across different document types, and business segments, along with the important concepts identified through topic modeling.
The results of my sentiment analyses suggest that breaking down the documents into different types can help determine trends more clearly. For example, there seems to be a correlation between a sharp decrease in sentiment around 2011 and a workers strike that occurred in August of that year. An additional result of my analyses relates to the insight gained from examining the correlation between the CEO sentiment and stock prices. When examining this correlation I looked at the daily standard deviation of the sentiment to create a proxy of the movement because I wanted to look at the change in sentiment and how that impacts the stock value. I found that there is a positive correlation between CEO sentiment from the Verizon conference documents and Verizon’s stock prices.
 
For the topic-wise sentiment analysis, I explored the sentiment for 14 topics across three document types - Verizon Earnings, Conferences, and Announcements. Some of the topics analyzed are a result of my topic modeling analysis. I explored topics under various categories such as Verizon products or subsidiaries, industry-wide metrics reported by Verizon (User Retention, User Churn), industry related news (Spectrum Auction, Pension Strike), and acquisitions made by Verizon. The topic wise sentiment analysis was able to capture some interesting trends under the various topics. I observed that the sentiment for Verizon Fios, one of their flagship internet products has been declining for the last few years and that decline has remained consistent across all the three document types. I also extracted text pertaining to “User Retention” and User Churn” and analyzed the sentiment for these two attributes. User retention and churn are company-reported metrics and are widely tracked in the Telecom industry. My analysis showed that the sentiment on user retention picked up since 2015 and that trend remains consistent across the document types. This is in keeping with the trend of the Verizon stock that witnessed an uptick 2015 onwards. I also looked at the sentiment across some of the biggest acquisitions that Verizon has made over the years. The sentiment trend remains consistent across the document types and I observed that document of type - “Conference”, tend to have a slightly more positive sentiment compared to the “Earnings” documents, though it is also sensitive to more fluctuation in its sentiment. 


