CricGame ia a video game which allows user to play a cricket match.
And along with playing match we will be able to view the score of that match ball by ball.

In the scorecard we will show the scores inning by inning

like for first inning we will show the score/wicket and overs. (98/6 20.5 Overs)

and then we will show the score of each player i.e. runs balls 4's 6's SR and if it is out then out by which player
and then the bowler's data like overs maiden runs wickets extras economy

similarly we will show for the second innings.

After this draw all the class and the UML diagram.

PlayerBattingController class is required to know which player is currenlty on strike and from the queue we will know who is 
the next player which will bat.

PlayerBowlingController class will tell us who is the current bowler and we will maintain a DeQueue so at the top we will have
the bowler who is going to ball next. and At the end we will have the bowler who bowls the last over.And we will 
also maintain a Map<Player, NoOfOversBowled>

As we know Cricbuzz updated the information bowl by bowl anf we have Bowling Scorecard and Batting Scorecard and these scorecard
need to be updated on every ball so we can use Observer Design pattern here.

We can create an interface ScoreUpdaterObserver and it will be implemented by two classes one is BowlingScorecardObserver and 
BattingScorecardObserver, both these classes will have update() method and in the Ball class we can take a 
List<ScorecardObserver> and there will be a notify method which will call both the class update method and in the Ball class 
we have bowlPlayedBy and for that Player we can update the information respectivley


