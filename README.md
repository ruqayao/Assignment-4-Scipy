# Assignment-4-Scipy
# Purpose
The purpose of this project is to analyze NBA player statistics using Python. The program loads a CSV dataset containing seasonal player statistics and performs statistical and mathematical analysis on regular season data. The project identifies the player with the most regular seasons played, analyzes that player’s three-point shooting accuracy over time, performs linear regression, computes an average accuracy using integration, estimates missing seasons using interpolation, calculates descriptive statistics, and performs hypothesis testing.
# Dataset / Input File Requirements
The program requires a CSV file named:
players_stats_by_season_full_details.csv

The dataset must contain the following columns:
- Player
- Season
- Stage
- FGM (Field Goals Made)
- FGA (Field Goals Attempted)
- 3PM (Three-Point Makes)
- 3PA (Three-Point Attempts)

The Stage column must contain the value "Regular_Season" because the program filters only regular season data.

The Season column must be formatted like:
- 1999 - 2000

so the starting year can be extracted for regression and interpolation.
# Class Design and Implementation
The project is implemented using one class:
NBADataAnalysis

The class organizes the entire workflow of the program. Each method performs one specific step of the analysis, which keeps the code structured and modular.
# Class Attributes
- file_path

Stores the path to the dataset file.

- data

Stores the full dataset loaded from the CSV file.

- regular_season_data

Stores filtered data containing only regular season rows.

- most_seasons_player

Stores the name of the player with the most regular seasons played.

- player_data

Stores all regular season data for the selected player.
