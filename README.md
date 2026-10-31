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
## File Uno.xlsx - Cleaned data.

## Code book (Common)
- Accuracy statement: Date, Opponents, Rank, and Score are accurate/truth and were of interest.
- **Date**: Date of the match.
  - Unstructured, mostly MMDDYY or MDD.
  - 17/Mar/2017 to 10/Mar/2018. Sometimes includes time if many sessions in a day.
  - Inlcudes a few NA/text values.
- **Opponents**: Number of AI adversaries.
  - Mostly 1 or 2. Maximum = 9.
- **Rank**: Author's rank in the leaderboard.
  - Removed Rank 3069 and 3070 to clean. These values were not recorded and imputed.
- **Score**: Points won(positive) or lost(negative) in a game.

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
- **Correction**: Reduce 'Global score' by 10,000 every time if crossed to retain 4 digits. See 'Caution' below.

## Comments
- The leaderboard is dynamic as new players join and players remove their accounts.
- Inactive users retain their account and their Rank in the leaderboard changes as other players progress.
- Caution: Unethical game endings/sign-out adds penalty and the host sometimes corrects score by a point or two after a prolonged absence.
- Caution: There are some large spurious corrections in raw data that can not be explained by the author and were retained as is.
- Disclaimer: The raw data is provided as-is and is not machine readable due to spurious NA/text values in columns.

## More info
- Report an issue to report an issue and to discuss access to the mood and strategies of the player and about 2000 more games till 2026 :).
