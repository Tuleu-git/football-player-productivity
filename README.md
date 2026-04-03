# Ball Progression and Player Productivity Across European Leagues

## Project Overview
This project investigates the relationship between different methods of ball progression, progressive passes `(prg_p)` and progressive runs `(prg_r)`, and their impact on player productivity, measured by goals and assists `(G+A)`.<br/>
The study tests the hypothesis that in modern football, individual ball-carrying actions (runs) might be more effective at predicting scoring contributions than passing, particularly under different tactical conditions across the top five European leagues.

## Dataset
The analysis uses a dataset of 2,176 players from the 2025-2026 football season.
* Source: Kaggle (originally sourced from FBref).
* Scope: Premier League, La Liga, Serie A, Ligue 1, and Bundesliga.
* Key Variables:
  * G+A: Total goals and assists (Dependent variable).
  * prg_p: Passes that move the ball significantly toward the opponent's goal.
  * prg_r: Carrying the ball a significant distance toward the opponent's goal.
  * min: Total minutes played (Control variable).
  * age: Player age.
  * pos: Player position (Forward, Midfielder, Defender, Goalkeeper).
