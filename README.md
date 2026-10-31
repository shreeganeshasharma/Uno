# Uno
- **Author**: sparedOstrich

## File UNO.ods - Raw data.
- An ODS file containing scores of 5300 online Uno games against AI players. Use a spreadsheet software to open the file.
- **Purpose**: To track the progress in online UNO.
- **Method**: The author created a fresh account on the host platform and recorded the data after each game.
- **Game settings** (Always)
  - Cards in hand at the start = 11
  - Game speed = Very fast
  - Automatically sort your cards = TRUE.
  - **Host**: [Play-uno.com](https://www.play-uno.com/newgame.php)
## File UnoClean.xlsx - Cleaned data.

## Code book (Common)
- Accuracy statement: Date, Opponents, Rank, and Score are accurate/truth and were of interest.
- **Date**: Date of the match.
  - Unstructured, mostly MMDDYY or MDD for convenience.
  - 17/Mar/2017 to 10/Mar/2019. Includes time if many sessions in a day from 26/Mar/2019.
  - Inlcudes NA/text values in cells 2009, 2191, 4631, 4707.
  - These NA, text and times are removed while cleaning. Repetitions are retained in cleaning as new session of the same day.
- **Opponents**: Number of AI adversaries.
  - First 27 values are missing, but were mostly 1.
  - Mostly 1 or 2. Maximum = 9. It ain't no fun if there are too many homies.
- **Rank**: Author's rank in the leaderboard.
  - Removed Rank 3069 and 3070 to clean. These values were not recorded and imputed.
- **Score**: Points won(positive) or lost(negative) in a game.
  - Values 2009 and 3069 were not recorded and are missing in both files.

- The following variables are derived or were recorded once in a while. They are NOT accurate in raw data.
- **Global Score**: Cumulative sum of Score.
  - Raw: Recorded from website. As the order of magnitude grew, only four digits were retained. See 'Correction' below.
  - Used =SUM($D$3:$D$cell, $J$cell) to clean.
- **Best Score in one try**: Most points won in a single game till date.
  - First 105 values are empty.
  - Used =MAX($D$3:$D$cell) to clean.
- **Worst Score in one try**: Most points lost in a single game till date.
  - First 290 values are empty.
  - Used =MIN($D$3:$D$cell) to clean.
    
- These two variables were updated once in a while and retained as they are in raw.
  - **Best Rank in one try**: Rank in 'Best Score in one try'
  - **Worst Rank in one try**: Rank in 'Worst Score in one try'.
  - These change less frequently compared to Rank which changes every game.
  - Ranks in one try change if any other player wins or loses large scores in their games, and this is common when number of opponents is large.
  - These Ranks give a very safe, conservative and bad estimate for the number of people using the host platform.
- **Correction**: Reduce 'Global score' by 10,000 every time if crossed to retain 4 digits. See 'Caution' below.

## Comments
- The leaderboard is dynamic as new players join and players remove their accounts.
- Inactive users retain their account and their Rank in the leaderboard changes as other players progress.
- **Caution**: Unethical game endings/sign-out adds penalty and the host sometimes corrects score by a point or two after a prolonged absence.
- **Caution**: There are some large spurious corrections in raw data that can not be explained by the author and were retained as is.
- **Disclaimer**: The raw data is provided **as-is** and is not machine readable due to spurious NA/text values in columns.

## More info
- Report an issue to report an issue and to discuss access to the mood and strategies of the player and about 2000 more games till 2026 :).

## Current leaderboard
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/1db89970-abc4-4b05-b8d1-e4bb93893b54" />


## Player profile, 2017
### Points
<img width="1129" height="529" alt="image" src="https://github.com/user-attachments/assets/980cbe9f-ab3c-452f-8cc2-2444ac617261" />

### Games
<img width="1129" height="529" alt="image" src="https://github.com/user-attachments/assets/531ce102-e97d-4fc5-85ed-6cd56ef40437" />

## Player profile, 2018
### Points
<img width="1129" height="531" alt="image" src="https://github.com/user-attachments/assets/62228516-b154-4d6f-9e49-5d04f1e95bf6" />

### Games
<img width="1128" height="530" alt="image" src="https://github.com/user-attachments/assets/4836ed84-ac77-4290-beb7-d64391bf526b" />

## Player profile, 2019
### Points
<img width="1129" height="532" alt="image" src="https://github.com/user-attachments/assets/227a62ba-385c-40a4-862d-5aebc579d43b" />

### Games
<img width="1127" height="528" alt="image" src="https://github.com/user-attachments/assets/2990ea4a-d088-4c65-8380-880de69ed3d3" />
