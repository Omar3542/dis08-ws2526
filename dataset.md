# NBA Database

## Source
The dataset is available on Kaggle: [https://www.kaggle.com/datasets/wyattowalsh/basketball/data](https://www.kaggle.com/datasets/wyattowalsh/basketball/data)

## Dataset Description

| Criterion | Details |
| :--- | :--- |
| **Primary File Format** | SQLite database (`.sqlite` file) |
| **File Size** | 2.35 GB (compressed download) |
| **Scope (Rows)** | > 65,000 games, > 4,800 players, > 13 million play-by-play events |
| **Number of Tables** | 17 related tables (e.g., `game`, `player`, `team`, `box_score`, `play_by_play`) |
| **Geographic Coverage** | Teams based in the United States and Canada (NBA league) |
| **License** | **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)** |
| **Conditions for Reuse** | **Yes, the dataset is open.**<br>1. **Attribution required** (must credit creator).<br>2. **ShareAlike** (adapted datasets must be shared under the same license).<br>Commercial use is permitted. |

## Key Features
- **Comprehensive Coverage**: Includes every game since the inaugural 1946-47 NBA season
- **Daily Updates**: The dataset is maintained and updated regularly
- **Relational Structure**: Data is organized in 17 interconnected tables for efficient querying
- **Multiple Data Types**: Contains game statistics, player information, team details, and play-by-play events

## Potential Use Cases
- Sports analytics and performance analysis
- Historical trends in basketball statistics
- Player career trajectory studies
- Team performance comparisons over time
- Machine learning models for game outcome prediction

## Complementary Dataset: NBA Player Salaries (2020-2025)
- Source:[Kaggle](https://www.kaggle.com/datasets/omarsobhy14/nba-players-salaries)
- Format:CSV file (33.68kB)
- Content:Player salaries for NBA seasons 2022/2023 to 2024/2025,including projected salaries
  
## How the Two Datasets Could Be Linked  
The Datasets can be linked through two primary keys:
- 1.**Player Name**:The most direct connection between the salary datset(Player Name) and the Nba database (_player _name_ in the _player_ table)
- 2.**Season/Year**: The salary data is organized by season (2022/2023, etc.),wich can be matched with game dates in the Nba database by extracting the year from game_date

## Potential Research Questions
Combining these datasets enables salary-performance analysis:
- 1.**Efficiency Analysis**: Which players provide the best performance per salary dollar? (e.g., points, rebounds, or advanced metrics like Player Efficiency Rating per million dollars)
- 2.**Team Investment Strategy**: Is there a correlation between a team's total salary expenditure (payroll) and their regular season win percentage or playoff success?
- 3.**Contract Value Assessment**: Do players perform significantly better in contract years (final year before free agency) compared to other seasons?
- 4.**Positional Salary Trends**: How do salaries compare across different positions (guard, forward, center) relative to their statistical contributions?

## Data Inspection and Understanding
- 1.**Explore Schemas**: Examine the structure of both datasets. For the primary NBA database, list all tables (e.g., player, game, box_score) and their columns using SQL (PRAGMA table_info() in SQLite) or pandas. For the salaries CSV, review its columns (Player Id, Player Name, salary columns for each season).
- 2.**Identify Key Variables**: Determine the exact matching keys. The most reliable link is player_name, but you must verify the exact column names (e.g., player_name vs Player Name). A secondary link is season, which will need to be derived from the game_date in the games table.

## Data Cleaning and Standardization
 - ### 1. Prepare & Clean the Data
 - This foundational phase involves standardizing the datasets to make them compatible. Key actions include transforming the salary data from wide to long format (so each row is a player-season combination), cleaning player names in both datasets (correcting nicknames, punctuation, and case differences), and creating a common season key in the NBA dataset by extracting the year from game dates.

- ### 2. Link & Merge the Datasets
- Execute the technical merge using the cleaned keys. First, perform a player match by joining the cleaned player tables from both datasets on the standardized player name. Then, enrich the performance statistics by joining the game/box score data (which now has a season key) with the newly created player-salary lookup table based on player_id and season.

- ### 3. Validate & Structure for Analysis
- After merging, ensure data quality and prepare for use. Check the merge success rate to see what percentage of records were successfully linked and investigate mismatches. Finally, structure the final dataset into a clean, analysis-ready table that combines player performance metrics with their corresponding salary for each season. 

| Principle | Rating | Assessment & Evidence |
| :--- | :--- | :---
| **Findable** | **Very Good** | The dataset is highly findable. It is hosted on Kaggle, a major data platform, with a descriptive title ("NBA Database"), relevant tags (nba, basketball, sports), and a rich "About" section detailing its scope, tables, and update frequency.|
| Accessible| Good | The dataset is accessible with one minor barrier. It can be downloaded directly as a single file via a stable URL. However, a free Kaggle account is required to initiate the download, which is a common practice on the platform but still a technical barrier to completely anonymous access.|
| **Interoperable** | **Excellent** | The dataset scores excellently in interoperability. It is provided as a standard SQLite database (.sqlite), a universally machine-readable, open-source format. The data is highly structured across normalized relational tables (Game, Player, Team, etc.), allowing for immediate use with countless tools (Python, R, SQL browsers).|
| **Reusable** | **Very Good** | The dataset is highly reusable. Its Creative Commons Attribution-ShareAlike 4.0 (CC BY-SA 4.0) license is clear, standard, and explicitly permits commercial and academic reuse. The documentation on Kaggle is good, and the associated GitHub repository provides technical details on the data's generation, further supporting informed reuse.|

---

