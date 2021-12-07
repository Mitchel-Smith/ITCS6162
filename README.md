<h1>Group 11 Members</h1>
Mitchel Smith, Revanth Tiruveedhula, Anuhya Bharathy Uppalapati, Sai Nihanth Vanam, Shruthi Vasalamarri, Chaitanya Chennupati, Sowmya Deepthi

<h1>General Area Of Investigation</h1>
We plan to investigate NFL game data to determine if certain statistics, such as passing yards or rushing yards, are more relevant than others for determining the winning team.

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
Our data is play-by-play data covering regular season games in the NFL from the 2009 to 2016 seasons. One of the immmediate issues with this data is that it is extremely noisy.
Not only are there just too many features to be relevant, some of the features are so strongly correlated as to be effectively duplicate values. In addition to those two issues that come from having too many features, we are missing some important features that we would want, such as who won the game, so in this project we deal with all of those issues to improve the clarity and usefullness of the data for our purpose. 

<h1>Results</h1>
Our results support those found by Arkes in 2011 and extend them to be accurate and meassures at a drive-by-drive level rather than a first half-second half measure. While winning teams on average do outperform losing teams in both rushing and passing plays, the most significant difference is in the passing plays. 

<h1>Citations</h1>
1) Lepschy, Hannes & Wäsche, Hagen & Woll, Alexander. (2018). How to be Successful in Football: A Systematic Review. 
  The Open Sports Sciences Journal. 11. 3-23. 10.2174/1875399X01811010003. </br>
3) Otten, M. P., & Miller, T. J. (2015). A Balanced Team Wins Championships: 66 Years of Data from the National Basketball Association and the National Football League. 
 Perceptual and Motor Skills, 121(3), 654–665. https://doi.org/10.2466/30.26.PMS.121c25x4</br>
3) Arkes, J. (2011). Is Controlling the Rushing or Passing Game the Key to NFL Victories? The Sports Journal. 
