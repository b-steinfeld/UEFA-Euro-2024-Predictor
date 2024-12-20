# 2024-Euros-Predictor
Goal: Trying to predict the 2024 Euros using webscrapping and machine learning.

Webscrapping: Extracted match data from the last five years of international soccer through FBref. However, within those five years, did not extract any data from friendly matches. Why? Friendly matches don't track signficant statistics, while also being considered to be less competitive games.

Model Predictor: The train data included matches prior to the 2022 World Cup, while the test data included the 2022 World Cup till matches prior to the 2024 Euros. However, my model does not predict draws (rather draws are just considered as 0s, which are losses). My model uses a Random Forest Classifier and predictions always stay the same.

No Draws vs. With Draws: When games that involve draws are a part of the test data, the algorithm has a precision of about 70%; just enough to be classifed as a useful model. On the other hand, when games that involve draws are NOT a part of the test data, the algorithm has a precision of about 88%; very much can be considered to be a useful model. It should be noted that for both algorithms, drawn games ARE a part of the TRAIN data as it strengthens the precision of the model.

As my model does not predict draws, I decided not to try to predict the group stages as draws are possible and instead use the group stage results in the train data of the 'Future Predictor'. Furthermore, because the round of 16, quarter-finals, semi-finals, and finals, must all end with a win or loss for each team, in this scenario it is fair to say the model has a precision closer to 88% than that of 70%. 

Future Predictor: The train data included matches prior to the 2024 Euros AND the group stage of the 2024 Euros (originally, had train data without the group stages; was tested and had a prediction precision of 8/15 -> 53.3%, with Spain as the predicted winner), while the test data would be each round of the tournament (besides the group stages). I did not utilize past rounds in the train data (ex. using the round of 16 results I predicted to influence the model when predicting the quarter-finals) as these are future matches with no data. Additionally, as these are future matches, we cannot webscrape. Therefore, each CSV file (for each round) was manually created based on the outcome predicted for the prior round. (See the "How Future Matches were Tested" folder). 

My Predicted Winner: Spain -> Actual Winner: Spain!

Prediction Precision: 11/15 -> 73.3%

This is my first ever major ML project. I'm proud of what I've done and learned along the way, and hope to continue learning and creating more! I know there are some stuff I still need to work on and figure out, but I know this will also help me get deeper into the world of ML and computer science. I also utilized comments in the code to keep track of everything I did. NOTE: The comments in futurepredictor.ipynb correlate with the model predictor files; that's why they don't have any comments.

-----------------------------------------------------------------------------------------------

For the future (even after the tournament), I do want to come back to this project in order to (as a continued learning experience) improve or at least think about what else I could have done. These are listed in no specific order:
1. Not have to manually create CSV files for each part of the tournament I'm predicting (so, build code that automatically does this process).
   - Thought: get prediction, add back to data, iterate again till the final.
2. Did not predict both sides (team becomes opponent, opponent becomes team); possible conflicting results (aka both teams predicted to win/lose and what do I do about them)?
   - Main concern!
   - Also did not combine both sides of results to check precision in the model predictor and see if results did not conflict (one team wins, one team loses).
   - If both teams "won", for example, what decides who wins? 
3. Potentially figure out other ways to grow precision (more data, different reference, new model, strength of team/how much team is worth, etc)?
4. Remodel my algorithm in order to predict draws (which would allow me to try to predict the group stages and potentially gain better precision in my model).
