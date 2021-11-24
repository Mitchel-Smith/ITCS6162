<h1>Group 11 Members</h1>
Mitchel Smith, Revanth Tiruveedhula, Anuhya Bharathy Uppalapati, Sai Nihanth Vanam, Shruthi Vasalamarri, Chaitanya Chennupati

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

Arkes posed that you cannot view a football game as a single unit but should instead view it in terms of halves. His paper clearly demonstrated that the first half stats meaningfully
impacted the second half stats. We plan to explore if his view was granular enough. Football is not a game of halves, but of plays and drives. We plan to investigate if 
viewing the game at the play-by-play level (a feat now acheivable that was not feasable in 2011) yields different results. We will use data from the NFL obtained via nflscrapR
and available at [this link](https://www.kaggle.com/maxhorowitz/nflplaybyplay2009to2016)

<h1>Data Preprocessing</h1>
We are able to rely on the fact that the data is scraped from the NFL's website and so is check by the crowd of NFL fans. That means we can expect most of the data to be accurate. 
This means I began with checking the data to make sure that every team had played the correct number of games. That turned up an issue that 4 teams had played a strange number of games. 
Upon further analysis, it became obvious that it was because 2 teams had changed their names which was causing issues.</br>
After that I checked for unusual values in the data. One of the 
obvious areas was Special Teams plays. Values in special team, specifically kickoffs, made many aspects of the data strange. Further, we know that most often the kick returner plays a 
second position on the team, whether on special teams, offense, or defense, and very rarely is a player signed specifically for returning. This means that we can remove these plays without
having a huge effect on our end recommendations for which squads are most important in determining wins. </br>
Following this, I split the data into 3 sections: Passing, Rushing, General. One of the arguments Arkes made was that teams in the second half are more likely to run while ahead in order to 
manage time of possession. This means that we should be able to see a difference in the time of possession between the first and second half of games. Rushing and Passing are simply clear areas to split for 
analysis. </br>
One note is that there is no column for who won the game or cumulative tracking of many of our variables, such as passing yardage or play time. I lightly processed the data to add these for initial
looks into the data. 

<h1>Data Understanding and Exploration</h1>
After splitting and preprocessing the data it was time to dive a little more into which features were usefull. I removed many of the features as they are outside the scope of the exploration we are
performing: for example, we aren't going to look at point after completions because player's aren't drafted for that (the kicker's main job is field goals and they are expected to make points after). </br>


<h1>Citations</h1>
1) Lepschy, Hannes & Wäsche, Hagen & Woll, Alexander. (2018). How to be Successful in Football: A Systematic Review. 
  The Open Sports Sciences Journal. 11. 3-23. 10.2174/1875399X01811010003. </br>
3) Otten, M. P., & Miller, T. J. (2015). A Balanced Team Wins Championships: 66 Years of Data from the National Basketball Association and the National Football League. 
 Perceptual and Motor Skills, 121(3), 654–665. https://doi.org/10.2466/30.26.PMS.121c25x4</br>
3) Arkes, J. (2011). Is Controlling the Rushing or Passing Game the Key to NFL Victories? The Sports Journal. 
