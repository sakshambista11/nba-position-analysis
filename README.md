# NBA Player Position Classifier 🏀

## Project Overview
This project uses machine learning (Random Forest Classifier) to analyze NBA player statistics and predict their on-court positions. The goal was to determine if traditional position labels (PG, SG, SF, PF, C) are still statistically distinct in the modern era of basketball.


## The Business Problem
Modern basketball has shifted towards a "position-less" style of play. Players like LeBron James or Nikola Jokić play roles that defy traditional definitions. This project uses data to quantifiably test how distinct these positions really are in the 2024 season.

## Key Findings & Insights
The model achieved an accuracy of approximately **45%**, which provides strong statistical evidence for the "Position-less" theory.

1.  **The "Wing" Ambiguity:** The model frequently confused Shooting Guards (SG) and Small Forwards (SF). This confirms that in the modern NBA, "Wings" share nearly identical statistical profiles regardless of their assigned label.
2.  **The Power Forward Identity Crisis:** Power Forwards (PF) had the lowest prediction scores. This suggests the PF position is the most versatile role, blending traits of both Centers (interior defense) and Wings (perimeter scoring), making it mathematically difficult to define.
3.  **Feature Engineering Impact:**
    * **Assist-to-Turnover Ratio:** Helped isolate pure playmakers (Point Guards).
    * **3PA/TRB Ratio:** Attempted to separate perimeter players from interior players, though the overlap remains high.

## Methodology
1.  **Data Cleaning:** Handled traded players (duplicates) and standardized position labels.
2.  **Feature Engineering:** Created custom ratios (AST/TOV, 3PA/TRB) to capture player efficiency and playstyle.
3.  **Modeling:** Trained multiple Random Forest Classifiers, iterating on features to improve class separation.
4.  **Evaluation:** Used Confusion Matrices and Precision/Recall reports to identify where the model failed, providing insights into player versatility.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, Scikit-Learn, Matplotlib
* **Environment:** Jupyter Notebook

## How to Run
1.  Clone the repository.
2.  Ensure you have the required libraries installed.
3.  Run the `NBA_position_analysis.ipynb` notebook.
