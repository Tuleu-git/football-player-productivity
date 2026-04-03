# Ball Progression and Player Productivity Across European Leagues

## Project Overview
This project investigates the relationship between different methods of ball progression, progressive passes `(prg_p)` and progressive runs `(prg_r)`, and their impact on player productivity, measured by goals and assists `(G+A)`.<br/>
The study tests the hypothesis that in modern football, individual ball-carrying actions (runs) might be more effective at predicting scoring contributions than passing, particularly under different tactical conditions across the top five European leagues.

## Dataset
The analysis uses a dataset of 2,176 players from the 2025-2026 football season.
* Source: Kaggle (originally sourced from FBref).
* Scope: Premier League, La Liga, Serie A, Ligue 1, and Bundesliga.
* Key Variables:
  * `G+A`: Total goals and assists (Dependent variable).
  * `prg_p`: Passes that move the ball significantly toward the opponent's goal.
  * `prg_r`: Carrying the ball a significant distance toward the opponent's goal.
  * `min`: Total minutes played (Control variable).
  * `age`: Player age.
  * `pos`: Player position (Forward, Midfielder, Defender, Goalkeeper).

## Methodology
The research employs a log-linear OLS regression model to allow for a percentage-based interpretation of results and to address the right-skewed nature of football performance data.

Model Specification: $`\ln(G + A + 1)_i = \beta_0 + \beta_1 \cdot Age_i + \beta_2 \cdot Min_i + \beta_3 \cdot Prg\_p_i + \beta_4 \cdot Prg\_r_i + \dots + \epsilon_i`$

* Baseline Categories: Midfielders and the Bundesliga were used as the reference groups for categorical dummy variables.
* Diagnostics: To ensure reliability, the model utilized robust (HC1) standard errors to account for confirmed heteroskedasticity. Multicollinearity was ruled out with a VIF test (all values below 2.5).

## Key Findings
* Dominance of Progressive Runs: Progressive runs were found to have a highly significant impact, with each additional run increasing goal contribution by approximately **1.38%**. This makes them roughly 7 times more valuable for predicting `G+A` than progressive passes in this model.
* Playing Time: Each additional minute played increases expected goal contribution by **0.063%**.
* Position Effects: Forwards contribute approximately **16.7%** more to scoring than midfielders, while defenders and goalkeepers contribute significantly less.
* Model Fit: The model achieved an adjusted R-squared of 0.38, explaining **38%** of the variation in player productivity.

## Conclusion
The results suggest that individual initiative through ball-carrying is a critical driver of offensive success in the world’s top leagues, regardless of specific league playing styles. While progressive passes are vital for team play, they depend more on teammate interaction, whereas runs represent direct individual impact.

## Tools Used
Gretl: Used for all statistical testing, OLS regression, and visual diagnostics (Q-Q plots, Kernel density estimations, etc.).

## References
* LTT Sports & World Football Summit (2024). Global football report.
* SkyQuest Technology Consulting (2024). Global football market size analysis.
* FBref / Kaggle (2025-2026 Season Data).
