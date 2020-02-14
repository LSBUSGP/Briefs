# Offline Ranking Table

A single player arcade game requires the generation of offline ranking tables showing the top 5 places for 60 different game levels. Each level has an expected average score and [standard deviation](https://en.wikipedia.org/wiki/Standard_deviation). As input you will take a list of three letter initials (you may randomly pick from the list to populate the rankings) a list of 60 average scores and 60 standard deviations. The generated scores must be integer value multiples of 10 distributed over the range and stored in a persistent file when the program first runs. You will also receive three letter initials and scores from players as they play the game. These scores should be sorted into their correct place in the rankings and overwrite those stored in the persistent file.

![Image of an arcade game high score table](http://www.howdesign.com/wp-content/uploads/arcade-high-scores1.jpg "high score table")

You must include the following in your Unity package:

1. ranking table generator script
2. a scene to reset the ranking tables
3. an example program allow generated ranking tables to be viewed
4. a test scene where new scores can be added
5. documentation
