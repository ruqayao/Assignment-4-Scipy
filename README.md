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
# Class Methods
- filter_regular_season()

Filters the dataset to include only rows where Stage equals "Regular_Season".

- player_most_seasons()

Determines which player has played the most unique regular seasons.

- get_player_data()

Retrieves and sorts all regular season data for the selected player.

- calculate_three_point_accuracy()

Calculates three-point shooting accuracy (3PM / 3PA) while avoiding division by zero.

- linear_regression_accuracy()

Performs linear regression on three-point accuracy over time using SciPy.

- integrate_average_accuracy(years, slope, intercept)

Uses numerical integration to compute the average fitted accuracy from the regression line and compares it to the actual average.

- interpolate_missing_seasons()

Uses linear interpolation to estimate three-point accuracy for the 2002 and 2015 seasons.

- descriptive_statistics()

Calculates mean, variance, skewness, and kurtosis for FGM and FGA.

- perform_t_tests()

Performs both paired and independent t-tests comparing FGM and FGA.
# Limitations
- The dataset must contain properly formatted column names exactly as specified.
- The Season format must allow extraction of the starting year.
- If no regular season data exists, the program will raise an error.
- Interpolation is limited to linear estimation.
- The analysis depends entirely on the accuracy and completeness of the dataset.
