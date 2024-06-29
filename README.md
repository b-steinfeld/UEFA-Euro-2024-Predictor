# 2024-Euros-Predictor
Goal: Trying to predict the 2024 Euros using webscrapping and machine learning.

Webscrapping: Extracted match data from the last five years of international soccer through FBref. However, within those five years, did not extract any data from friendly matches. Why? Friendly matches don't track signficant statistics, while also being considered to be less competitive games.

Model Predictor: The train data included matches prior to the 2022 World Cup, while the test data included the 2022 World Cup till matches prior to the 2024 Euros. However, my model (currently) does not predict draws. 

No Draws vs. With Draws: When games that involve draws are a part of the test data, the algorithm has a precision of about 70%; just enough to be classifed as a useful model. On the other hand, when games that involve draws are NOT a part of the test data, the algorithm has a precision of about 88%; very much can be considered to be a useful model. It should be noted that for both algorithms, drawn games ARE a part of the TRAIN data as it strengthens the precision of the model.

As my model (currently) does not predict draws, I decided not to try to predict the group stages as draws are possible. Furthermore, because the round of 16, quarter-finals, semi-finals, and finals, must all end with a win or loss for each team, in this scenario it is fair to say the model has a precision closer to 88% than that of 70%. 

Future Predictor: The train data included matches prior to the 2024 Euros, while the test data would be each round of the tournament (besides the group stages). I did not utilize past rounds in the train data (ex. using the round of 16 results I predicted to influence the model when predicting the quarter-finals) as these are future matches with no data. Additionally, as these are future matches, we cannot webscrape. Therefore, each CSV file (for each round) was manually created based on the outcome predicted for the prior round. (See the "Train+Test Data for Future Predictions" folder).
   - Originally my test data included only matches prior to the 2024 Euros as I had originally 
     planned to predict the group stage. However, I did also seperately utilize the group 
     stages within my test data alongside prior matches. Results can be found in the "Group 
     Stages in Train Data" folder.

My Predicted Winner: Spain

This is my first ever major ML project. I'm proud of what I've done and learned along the way, and hope to continue learning and creating more!

-----------------------------------------------------------------------------------------------

For the future, I do want to come back to this project in order to:
1. Remodel my algorithm in order to predict draws (which would allow me to try to predict the group stages and potentially gain better precision in my model).
2. Not have to manually create CSV files for each part of the tournament I'm predicting (so, build code that automatically does this process).
3. Did not predict both sides (team becomes opponent, opponent becomes team); possible conflicting results (and what to do about them)?
4. Finishing adding notes to each part of the code in order to convey each lines/blocks purpose.
5. Potentially figure out other ways to grow precision (more data, different reference, new model, strength of team/how much team is worth, etc)?
6. Should I consider group stage games as I couldn't predict them originally?
   - Considered group stage games apart of train data. Results are different, but winner 
     stays. Check out "Group Stages in Train Data" for results.
8. When the tournament is over, compare results.
   - Group stage precision results now compared. Both with and without draws involved.
     - Should I include each result (actual vs predicted)?
