# 2024-Euros-Predictor
Goal: Trying to predict the 2024 Euros using webscrapping and machine learning.

After webscrapping, the initial algorithm is created to use test and train data on past matches in the last five years (did not include friendles). The train data was matches prior to the 2022 World Cup, while the test data included the 2022 World Cup and forward. The algorithm had a precision of about 70%; just enough to be classifed as a useful model.

I decided not to try to predict the group stages as draws are possible; my model only predicts wins and loses. 

Then, a future predictor was created; in which, the test data would be each part of the tournament (round of 16, quarterfinals, semifinals, and the final). As these are future matches, each of these csv(s) were manually created based on the outcome predicted for each part.

For the future, I do want to come back to this project in order to:
1. remodel my algorithm in order to predict draws.
2. not having to manually create csv(s) for each part of the torunament I'm are predicing.
