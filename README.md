# NBA Player Position Classifier 🏀

Predicts NBA player positions (PG, SG, SF, PF, C) from box score statistics using a Random Forest Classifier. Achieves ~45% accuracy — which itself is the key finding, providing statistical evidence for the "position-less" era in modern basketball.

🔗 [View Notebook on nbviewer](https://nbviewer.org/github/sakshambista11/nba-position-analysis/blob/main/NBA_position_analysis.ipynb)

---

## The Business Problem
Modern basketball has shifted towards a "position-less" style of play. Players like LeBron James or Nikola Jokić play roles that defy traditional definitions. This project uses data to quantifiably test how distinct these positions really are in the 2024 season.

## Key Findings
1. **The "Wing" Ambiguity:** The model frequently confused Shooting Guards and Small Forwards, confirming that modern wings share nearly identical statistical profiles regardless of assigned label.
2. **The Power Forward Identity Crisis:** Power Forwards had the lowest prediction scores, suggesting PF is the most versatile role — blending traits of both Centers and Wings.
3. **Feature Engineering Impact:** Adding an Assist-to-Turnover ratio helped isolate Point Guards, while physical stats (rebounds/blocks) remained the strongest indicators for Centers.

## Methodology
1. **Data Cleaning:** Handled traded players (duplicates) and standardized position labels.
2. **Feature Engineering:** Created custom ratios (AST/TOV, 3PA/TRB) to capture player efficiency and playstyle.
3. **Modeling:** Trained multiple Random Forest Classifiers, iterating on features to improve class separation.
4. **Evaluation:** Used confusion matrices and precision/recall reports to identify where the model failed.

## Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib
- **Environment:** Jupyter Notebook

## How to Run
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Data source: [2023-2024 NBA Player Stats](https://www.kaggle.com/datasets/vivovinco/2023-2024-nba-player-stats) on Kaggle. `NBA.csv` is already included in this repo.
4. Run `NBA_position_analysis.ipynb`.