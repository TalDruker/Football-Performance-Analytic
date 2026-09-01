# Football-Performance-Analytics

# Project Objective
 Project Objective: Establishing a data-driven infrastructure to serve as a tactical decision-making engine for professional football coaching staffs.
 The project aims to transform raw statistical data into actionable tactical insights, enabling coaches and technical staff to prepare optimally for specific opponent matchups, identify key threats, and manage the roster efficiently.

 ## Data Loading and Initial Inspection
The first step involves loading the football match data from a tab-separated file using Pandas. The dataset contains 1,000 entries with 12 columns, including unique player identifiers, player names, teams, positions, match dates, age, minutes played, goals, assists, yellow cards, red cards, and total distance covered (`Distance_KM`). Initial inspection using methods like `head()`, `info()`, and `describe()` provides a clear overview of data types, memory usage, and initial distribution ranges.

## Data Cleaning & Outlier Treatment
The dataset undergoes comprehensive cleaning to ensure high data integrity:
* **Missing Values & Imputation:** Missing distance values and match dates were handled and imputed using realistic baselines.
* **Outlier Capping:** Unrealistic distance values exceeding 14 KM were capped at a physical limit of 12 KM. Age boundaries and disciplinary metrics were restricted to professional limits.
* **Disciplinary Validation:** Rules ensuring that two yellow cards automatically incur a red card were enforced.
* **Standardization:** Tactical positions (such as Hebrew terms and abbreviations like 'FWD') were normalized into standard English roles (`Defender`, `Goalkeeper`, `Midfielder`, `Forward`). Team names were standardized to proper title case, removing whitespaces and fixing typos.
* **Metric Correction:** Erroneous negative values in goals and assists were converted to absolute positive values.

## Advanced Analysis, Statistical Profiling & Visualizations
This section covers the core research questions, advanced groupings, and professional visualizations:

### 1. Key Players Identification
Grouping data by player and summing goal contributions identifies the most dominant player for each club in the league, highlighting key offensive contributors.

### 2. Seasonality & Time Trends Analysis
By extracting month components from match timestamps, the analysis tracks monthly performance spikes and identifies peak offensive months for each team across the seasonal timeline.

### 3. Physical Fitness vs. Age
Using scatter plots to analyze the relationship between player age and average distance covered (`Distance_KM`), the project uncovers a distinct non-linear pattern, showing how physical workloads shift across career stages.

### 4. Statistical Profiling
Aggregating core metrics provides a comparative view of total goals scored, mean age, and average physical distance covered across all major clubs in the league.

### 5. Risk & Aggression Analysis
Evaluating disciplinary records by summing yellow and red cards highlights team-level tactical discipline, identifying clubs that exhibit higher levels of match aggression and disciplinary liability.

## Conclusion
The Football Analytics project provides valuable, data-driven insights into player dominance, seasonal performance windows, age-related physical workloads, and disciplinary risks. This structured framework equips technical staff and coaches with the necessary metrics to optimize match preparation, manage squad rotations, and make informed tactical decisions
