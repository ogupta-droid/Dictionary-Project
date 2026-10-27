# Dictionary App

My Champions League Dictionary App lets users view, add, and delete teams, compare their stats, and rank teams and countries.

## Calculations

- **Lowest Stat:** After the user enters a team name, the app compares stat values to find the smallest number. It skips country, wins, losses, draws, goals, shots on target, and clean sheets during the loop. However, goals is still the starting value, so it can remain the result if none of the compared stats are lower.
- **Team Power Rankings:** The app calculates a weighted score for each team, then sorts teams from highest to lowest. Each win adds 10 points, draw adds 3, goal adds 4, shot on target adds 1, clean sheet adds 5, and save adds 1. Conversion rate is multiplied by 0.5, pass accuracy by 0.2, and defensive tackles by 0.5. Each loss subtracts 2 points.
- **Best Country:** Using the scores saved by the power rankings, the app adds up each country’s team scores and divides by its number of teams. It then adds a bonus of 5 points per team. The country with the highest final score wins.

## Challenges I Ran Into

- One bug happened when I used `int()` to convert the menu input into a number but still compared it to strings like `"1"`. Selecting an option did not run the function because the number `1` does not equal the string `"1"`. I fixed this by removing the quotation marks from the menu comparisons.

## What I'd Improve With More Time

- Improve the weakest-stat calculation so it compares performance fairly instead of just finding the smallest number.
- Record the same stats for every team so the power rankings are more balanced.
- Save changes to a file so added and deleted teams stay updated after the program closes.
- Make team searches work regardless of capitalization.
