# DS4400-final-project
Vivek Divakarla, Travis DeBruyn

## Introduction
### NFL Sports Betting:
- What is the best information upon which NFL bets should be based?
- It is impossible to predict the outcome of an NFL game with perfect accuracy, but are there patterns that we can identify to help improve our accuracy? The volatile nature of an NFL game makes it difficult to predict its outcome, but with the help of machine learning, we can find the best ways to spend our money in the process of predicting NFL games/scores.

### Approach:
- We tested different classifiers and compared their results to help us find the most important features in relation to winning an NFL game.
- After identifying the most important features to winning an NFL game, we intend to improve upon our investigation by then inspecting which features are most important to predicting the outcomes of different types of lines (ex. which features are most important in predicting that the home team will cover the spread?).
- We want to be able to draw conclusions from the similarities and differences between the different important features that we find between our two investigations, and we know that classifiers will be the best for this. We believe that our best results will come from Linear Discriminant Analysis because of the linear decision boundary. We are hoping to find generalizations across the NFL, and not team by team.
- Finally, we hope (if time allows) to create ML models to predict an NFL win/loss ratio as well as the outcomes of certain betting lines.


### Limitations:
- The main limitations of our results are time and computing power. The datasets that we are using are massive and needed to be trimmed for the purposes of this project.
- Our other limitation is the lack of player data. Teams are comprised of players and a coaching staff. In a perfect world where we have infinite time, we could create models to grade players. It would then be possible to create models that, based on player grades, predict the level of a team. We simply do not have the time or data to accomplish this at the moment.

## Setup
### Data:
- The first look at our dataset after cleaning is as follows: ![basicstats](https://user-images.githubusercontent.com/71042338/231732408-4a6026bb-f1e7-4a2c-a963-f5459caac0ea.png)
- This is just the first 5 rows of our dataset. As we can see, there are a multitude of statistics that help describe the playstyle and efficacy of each team in the NFL. Then, we looked at some visualizations of our data.![offypplay](https://user-images.githubusercontent.com/71042338/231737240-c92e601e-82aa-43a1-a057-9fd2bed00d1e.png)![pointdiff](https://user-images.githubusercontent.com/71042338/231736734-2d83cc75-38e5-4aee-b0bc-8d878fb736a7.png)


### Experiment Setup:
- As mentioned previously, we tested different classifiers and compared their results to find the features that are most important to winning an NFL game. LDA resulted in the lowest test error.
- We are using a collaborative .ipynb file through Datalore to complete the majority of this project.
- We are going to use LDA to understand the features of our data better, and then likely use Logistic Regression to create a model to predict NFL win/loss ratio by team.

## Results
- The following shows our tests of classifiers in an attempt to find that which fits our data best.![classifiers](https://user-images.githubusercontent.com/71042338/231737731-407f5297-0794-42b0-adb7-fa6c159dec90.png)
- Looking at the test error of each, LDA performs the best on our dataset. This makes sense as we want a general rule that can be applied to the whole NFL, and not one that fluctuates based on team.
- This left us with the following feature importance graph (when applying a random forest classifier to the data).![featureimportancegraph](https://user-images.githubusercontent.com/71042338/231738385-c30af62b-af83-44bc-ab6e-a618d1f82b65.png)

## Discussion
- We found it interesting that offensive stats seemed to be the most important metric, and defensive stats seemed to have very little importance. This could be explained by the common observation that teams are generally more consistent on offense, and their defensive performance fluctuates based on the strength of their opponent.
- Also, turnover percent has a low correlation as well. We believe that this is similar to defense in that a team's turnover percent is generally not consistent.

## Conclusion
In this project, we have taken a deeper look into what causes NFL teams to win or lose games. What are the statistics that bettors should be most wary of when choosing to spend their money on a team's perceived chance at victory? We have found that bettors should look at a team's offensive capabilities as their primary source of information. The expected points and yards per play features are important pieces of the puzzle, as well as the scoring of a team's offense.

## References
- [[https://topfunky.com/2021/logistic-regression-nfl-win-probability/]]

