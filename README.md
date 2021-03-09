Link to Google Colab: https://github.com/pellehol/DataScienceProject.git

1. Firstly read the results.csv file
2. Remove all rows which don't contain words FIFA or UEFA.
3. Make different data possibilities taking into account the time(games from 2000-2020 and another 2010-2020).
4. Run method weightOfYear(will give every game it's weight) and chooseDataToUse(returns matches model data).
5. Training with data and implementing Poisson regressioon on it. 
6. Run method getMatchProbability, which calculates match participants winning chances and how big is the probability that the match will end up in a draw. 
It also calculates the most likely match end result.
7. Run method get_match_result which returns the match winner (which is denoted by the variable result), loser, and score. 
(if match ends in a draw then both result and loser are equal to draw)
8. Run the part of the code where groups are declared.
9. Run the main code.
In the main code we have methods get_group_result which calculates every group game result and adds up every team points, scored goals. This method return group ranking.

    1) Method choose3rd chooses the 3rd winner from group stage if there are 3 options. 
    2) Method choose3rdv2 chooses the 3rd winner from group stage if there are 4 options. 
    3) We have for-loop to run the groupstages and knockout stage as much as we want. 
    4) Inside this for-loop firstly we use another for-loop to get every group ranking which uses method get_group_result.
    5) When that for-loop is done we use another for loop to decide which groups 3-rd places can go through to knockout stage.
    6) Then we add every game to separately lists, so we get 8 matches, then we add this into another list so we get a 2D array 
    (so it consist from 8 games and every game consists of 2 teams).
    7) We are going to loop that 2D array through and use on every match method get_match_result which is going to decide the winner of the match. 
    8) We add that winner to new list which is going to include the next round participants.
    9) So we do all that again but instead of 8 matches we have 4 matches and so on until we have only one game remaining and thats the final.
    
    Basically steps vi-viii will be reapeated until the end.

10. After the main code we take all the info and make 2 bar charts. One about each participating country scored and conceded goals. 
Another about how many times which country won(if there isn't some of the countries on the bar chart then it's because they didn't win this tournament a single time).(PS code about the first bar chart must be run 2 times, then it will be in normal size).
