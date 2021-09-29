# Data-Visualization-Group-Project

**Team Members:** 

Peishan Li(pl2772@columbia.edu), Shiying Lai(sl4849@columbia.edu), Tao Li(tl3020@columbia.edu), Xiaofan Liu(xl3042@columbia.edu)

## RPubs links

Our file is too large to publish in Rpubs as a whole, so we have four websites.

(If you want to see the whole file, please see the final_project.html in the final_project folder.)

Part 1: [Mail-in Voting & Covid Development](http://rpubs.com/LPS/peishanligrouphdv) (Leaflet map too large so that it takes a while to display)

Part 2: [The influence of large election events on Covid cases development in the county the events were held](https://rpubs.com/shiyinglai/758739)

Part 3: [The Relationship between Governors' tweets and COVID-19 Cases by State](https://rpubs.com/shiyinglai/section3)

Part 4: [Network analysis](https://rpubs.com/Lilian-Liu/Part4)

## Project description

This repository is for the group project for the Data Visualization Course of the Quantitative Methods in the Social Sciences program at Columbia University. We are interested in exploring the association of some election patterns and events with Covid-19 development and control. Specifically, the subtopics we explore are:

### 1. The relationship of Mail-in Voting and Covid cases development (line charts+interactive maps)

The overall pandemic situation before the voting period starts might lead to people’s preference of mail-in voting. This could be somewhat proved by the fact that people who are absence of in person voting could register for mail ballot and fill in “Covid” as the excuse.

To understand this, we plot a trend of mail-in voting percentage in elections since 2000 to see if there is an evidence of increasing favoritism in mail-in voting versus other voting modes.

The background knowledge suggests that Trump administration and its supporters oppose mail-in voting, so we’ll also be looking at the difference of mail-in voting preference change for Democrats and Republicans respectively.

We’ll then explore if different voting mechanisms could have an impact on number of cases. How does the percentage of mail-in voting affects the increase of Covid-19 cases? Do democratic states and republican states differ in the increase of Covid-19 cases during the whole voting period, since they might have different policies and preferences regarding in person vs mail-in voting at state government level?

To look at the influence of mail-in voting on covid cases in turn, we plot the mail-in voting percentage of 2020 Election as well as covid cases increase during voting period for each state on leaflet maps. The election day is November 3, and the earliest voting time is 46 days before the election day. The end of our observation date is 7 days after the election day. Each state is categorized as a typical Democratic state or a Republican state based on the percentage of Democrats and Republicans from the 2020 SPAE.
 
### 2. The influence of large election events on Covid cases development in the county the events were held (line charts+bar chart)

We collected 21 Trump's Election Rallies for 2020, and create 21 trend plots of confirmed Covid Cases for each rally event's county. By comparing the slope before one week and the slope of the week when the rally take place to see if the rallieis affect the Covid's Development. 

Here is the comparsion result:

*Covid 19's spread in Marathon(Mosinee), Wisconsin speed up after the rally.
*Election rally has no obvious effect on Blue Earth(Mankato), Minnesota.
*Covid 19's spread slows down after the rally in Saginaw(Freeland), Michigan.
*Covid 19's spread slows down after the rally in Winnebago(Oshkosh),Wisconsin.
*Election rally speed up the Covid 19's spread in Tulsa, Oklahoma. 
*Election rally speed up the Covid 19's spread in Maricopa(Phoenix), Arizona.However, the effect is not very obvious.
* Covid 19's spread in Tulsa, Oklahoma slightly speed up after the rally. 
* Covid 19's spread in Lackawanna(Old Forge), Pennsylvania speed up after the election rally
* Covid 19's spread in Rockingham(Londonberry),New Hampshire slightly has no obvious change after the election rally.
* Covid 19's spread in Westmoreland(Latrobe),Pennsylvania  has no obvious change after the election rally.
* Covid 19's spread slows down after the rally in Forsyth(Winston-Salem), North Carolina.
* Covid 19's spread in Douglas(Minden), Nevada speed up after the rally. 
* Covid 19's spread in Clark(Henderson), Nevada has no obvious change after the election rally.
* Covid 19's spread in Beltrami(Bemidji), Minnesota has no obvious change after the election rally.
* Covid 19's spread in Cumberland(Fayetteville), North Carolina has no obvio* us change after the election rally
* Covid 19's spread in Lucas(Swanton),Ohio has no obvious change after the election rally.
* Covid 19's spread in Vandalia, Ohio has no obvious change after the election rally.
* Covid 19's spread in Allegheny(Pittsburgh), Pennsylvania has no obvious change after the election rally.
* Etc.

Conclusion:among all the rallies, only 38.1%(8/21) cities might have increased Covid 19 spread speed. Thus, it is hard to conclude that rallies have negative effect on Covid 19 spread.

Then, we study whether being indoor rally or outdoor rally matters?

Conclusion: after all indoors' rally, the Covid 19's spread speed increase. However, the among the outdoor rallies, the situation is much better that more than 75% of cities' Covid 19 spread speed remain the same or even slow down. 

### 3. The Relationship between Governors' tweets and COVID-19 Cases by State (text analysis+sentiment analysis+interactive map)

Sentiment analysis:

We want to explore the sentiment of governors' tweets about COVID-19 and Election in 2020. We also comapared the sentiment score and COVID-19 cases by state to see whether there's correlation between them. The hypothesis is that there is a positive correlation between average sentiment scores of governors' tweets and Covid cases.

First, we cleaned governors' tweets and did a bunch of visualizations to get an overview of the tweets. From graph 1 (barplot of most frequent 20 words in governors' tweets), we can see that words like Covid, mask, vaccine and virus get the most frequencies. We can also see that words like test, vote, work and spread are pretty frequent as well. 

From the comparison word clouds of Democrats and Republicans, we can see both parties have the negative word cloud dominated by words like virus, spread, cases, lost, etc, and positive word cloud dominated by words like protect, mask, test, vaccine, etc.

Then we compared the two leaflet maps of average sentiment score by state and Covid cases by state to see the relationship between average sentiment score of governors' tweets about COVID19 and Confirmed COVID cases by state. We found no obvious correlation between sentiment score and Covid cases.

Conclusion: there is no obvious correlation between sentiment of governors' tweets and Covid cases.

### 4. The relationship of state governers' attitude with covid development (network analysis)

Network analysis：

We would like to investigate the relationship between governors and Biden/Trump. We collected around 1,000 tweets from Twitter from 2020.6 to now and focus on governors from each state who mention Biden/Trump on their Twitter accounts. 

The hypothesis is that governors from the same party with Biden/Trump will mention him more than governors from the opposite party. We also make a further assumption that states that governors mention Trump more will have higher number of COVID-19 cases than states that governors mention Biden more.

From graph 1 (The network of governors who mention Biden on Twitter), we can learn that most governors mentioned Biden on Twitter are Democrats, which are in the same party with Biden; From graph 2 (The network of governors who mention Trump on Twitter), we can learn that almost all governors mentioned Trump on Twitter are Republicans, which are in the same party with Trump. Comparing the two graphs, there are more edges in graph 2 than graph 1. It is indicated that compared with Biden, Trump is mentioned more by governors.

GavinNewsom (governor from California) have mentioned Biden the most times on Twitter while BrainKempGA (governor from Georgia) and KimReynoldsIA (governor from Iowa) have mentioned Trump the most times on Twitter. The COVID-19 cases in Georgia and Iowa are higher than that in California. To some extent, our hypothesis and assumption are proved.

## Data Sources

SAPE of each election Stewart, Charles, 2021, “2020 Survey of the Performance of American Elections”, https://doi.org/10.7910/DVN/FSGX7Z, Harvard Dataverse, V1, UNF:6:70KW4uouuTDT860MiPJq3A== [fileUNF]

[Covid cases by state by day--United States COVID-19 Cases and Deaths by State over Time](https://data.cdc.gov/Case-Surveillance/United-States-COVID-19-Cases-and-Deaths-by-State-o/9mfq-cb36)

[Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE](https://github.com/CSSEGISandData/COVID-19)

[Population estimate 2020](https://www.census.gov/programs-surveys/popest/technical-documentation/research/evaluation-estimates.html)

Twitter handles of the current governors from each state in the US (obtained from UCSD library).

Self collected data from news

## Directory

Group-H Final Project Proposal

Group-H Process Book

Codes and Datasets of Each Member
