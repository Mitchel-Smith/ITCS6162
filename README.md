<h1>Group 11 Members</h1>
Mitchel Smith, Revanth Tiruveedhula, Anuhya Bharathy Uppalapati, Sai Nihanth Vanam, Shruthi Vasalamarri, Chaitanya Chennupati, Sowmya Deepthi

<h1>General Area Of Investigation</h1>
We plan to investigate NFL game data to determine if passing yards or rushing yards are more relevant for determining the winning team during an NFL regular season game.

<h1>Current Research</h1>
While research on this topic for soccer and basketball are reasonably prevalant, Lepschy (2018) and Otten (2015), studies on results in football are not nearly as popular.
One notable exception is Arkes (2011), but it is a decade old which means current trends may be different and 
he was not able to leverage the amount of data we have available in today's world. 

<h1>Our Question</h1>
From Arkes (2011) we came up with 2 main questions</br>
1) What statistics are most important in determining the winning team in an NFL game?</br>
2) What level of data is most relevant for NFL games?

Arkes posed that you cannot view a football game as a single unit but should instead view it in terms of halves. His paper clearly demonstrated that the first half stats meaningfully impacted the second half stats. 
We plan to explore if his view was granular enough. Football is not a game of halves, but of plays and drives. We plan to investigate if viewing the game at the play-by-play 
level (a feat now acheivable that was not feasable in 2011) yields different results. We will use data from the NFL obtained via nflscrapR
and available at [this link](https://www.kaggle.com/maxhorowitz/nflplaybyplay2009to2016)

<h1>Our Data</h1>
The data we chose to use is play-by-play data from NFL Regular season games between the 2009 and 2016 seasons. This data comes from the NFL website and is scraped using nflscrapR. There are a couple of benefits to using this data. First is the sheer amount of data we are able to collect. Instead of the 512 lines of data used by Arkes, we have over 350 thousand lines.<br>

Second, our data is play-by-play and psuedo-pre-cleaned. Since it is hosted on the official NFL website, and is uploaded as part of someone's job, we know that it is, at least at the highest level correct. Further, nflscrapR takes care of cleaning out some of the erroneous data that we don't need from the webpage and getting it into a nice format. This means that as far as cleaning data, we only have to clean out extra data and some of our outliers. The most notable outlier that we want to clean out of our data are tied games. Since the data scraped only covers through regulation, we can't see which team won the game and those games are not relevant to our analysis. There are relatively few NFL games that end in a tie each season, so pruning that data is not a major loss. 

One aspect of our data that we are also pruning that many people would argue has an impact on the offense are defensive scoring plays. These plays are often said to have a significant impact on the game as they can change the mommentum a team has, negate long drives that would otherwise have scored, or simply give a team that is already winning or losing some additional points. However, the focus of this exploration is measuring offensive statistics and since defensive scores do not DIRECTLY impact those, we will remove them along with other defensive statistics. 

That brings us to our main downfall of this data. There is just too much of it. Many of the features are either redundant (time and TimeSecs) or irrelevant for our purposes (Date). The other downfall of the data is that many features we do want are simply not there. For example, there is no feature that actually tells us in binary terms whether a team won or lost the game. So we will have to create that. We created many of our own features, Cumulative Time of Possession, a binary column for Winning/Losing Team (Technically ternary before Ties are eliminated), Rushing/Passing Yards/Time per Drive per Half/Whole to name a few. These are all derived from the data source but serve as a more condensed version of the play-by-play data that is easier to analyze. 

<h1>Results</h1>
Many of the results of our analysis indicate that there is not a clear and meaninful difference between the results of a Winning and Losing team. The features where the averages are clearly distinguishable are timePerDriveWhole values (both rushing and Passing) , RushingTimePerDrive values (Both half and whole), and the PassingYardsPerDrive. It's interesting to note that the only statistic (other than number of plays) that the losing team beats the winning team in is RushingTimePerDriveHalf. This seems to indicate that winning teams on average want to get their run plays off quicker during the first half. Whether this is that their coaches playcall faster, or they settle on the line and snap more quickly, or something else entirely is impossible to tell from this. This changes in the second half where the winning team tends to average 10 additional seconds per rush. <br>

Looking only at our Yardage statistics, the most noticeable different is between the PassingYardsPerDriveHalf where winning teams average 32 and losing teams only average 26. While this doesn't seem like a huge difference, when you consider that across all drives in the first half (generally about 6), thats a difference of about 30 yards in a half. That can be the difference in a scoring drive or not. So indication is that teams that have a more successful first half passing game are more likely to win.

Finally, it is interesting to note that both teams spend much more time rushing in the second half, doubling the average time spent on rushing plays per drive. 

<h1>Future Work</h1>
There are several places where this work could be extended. One is to analyze the outliers in the data, which we can assume exist due to the high standard deviation in our average rushing and passing games. It would be interesting to analyze whether having a few huge plays has a high impact on a game, or if consistency is more important.
Further, analysis of Special Teams and Defense would be interesting. Often it is assumed that teams that have large defensive plays, such as interceptions and fumble recoveries, are more likely to win. While this is likely true, an investigation into whether it has a measurable impact when analyzed across all games is worth while when many teams have to decide between drafting a defensive or offensive prospect.<br>

Another area worth exploring would be the impact of penalties on a game. Many people, especially on the internet, talk about how "refs decide games". The data used here provides penalty statistics and it would be interesting to see if the number/yardage of penalties does have a significant impact on likelihood to win. Perhaps it is worth training players to play an extremely clean game in addition to other parts of training. 

Finally, now that we have shown further evidence supporting Arkes's conclusion that the Passing squad has a larger impact that the Rushing squad, further analysis into target selection (which receiver and location to pass to) could yield interesting results. For example, are teams that have a powerful duo (e.g. Roethlisberger + Ward) more likely to win or is it important to have a large receiving core so that many options are available. Or perhaps it doesn't matter.

<h1>Citations</h1>
1) Lepschy, Hannes & Wäsche, Hagen & Woll, Alexander. (2018). How to be Successful in Football: A Systematic Review. 
  The Open Sports Sciences Journal. 11. 3-23. 10.2174/1875399X01811010003. </br>
3) Otten, M. P., & Miller, T. J. (2015). A Balanced Team Wins Championships: 66 Years of Data from the National Basketball Association and the National Football League. 
 Perceptual and Motor Skills, 121(3), 654–665. https://doi.org/10.2466/30.26.PMS.121c25x4</br>
3) Arkes, J. (2011). Is Controlling the Rushing or Passing Game the Key to NFL Victories? The Sports Journal. 

<h1>Questions about this Work</h1>
Contact: Mitchel Smith at https://www.linkedin.com/in/mitchel-smith/
