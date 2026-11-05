# Formula 1 Vehicle Performance Analysis

I started with the 2025 British Grand Prix at Silverstone to see where the quickest qualifying laps differed. I compared lap and sector times, aligned Verstappen's and Piastri's speed and control traces by distance, and examined how tyre choice and weather coincided with changes in race pace. The race prediction experiment uses six events across 2024 and 2025.

## Project files

| File | What it covers |
| --- | --- |
| [Analysis notebook](F1_Vehicle_Performance_Analysis.ipynb) | Data preparation, telemetry alignment, model fitting, evaluation and the original plots. |
| [Technical report](F1_Vehicle_Performance_Report.pdf) | Methods, figures and results for lap-time prediction, longitudinal speed modelling, PCA and the simulator surrogate. |
| [Interactive Tableau workbook](F1_Vehicle_Performance_Dashboards.twbx) | Four dashboards, 16 worksheets and the bundled data. |
| [Tableau presentation](F1_Tableau_Presentation.pptx) | A slide walkthrough of four dashboards covering vehicle performance, telemetry, tyres and weather, and model diagnostics. |

## What I found

- Verstappen set the quickest eligible qualifying lap at **84.892 s**, with Piastri **0.103 s** behind. Piastri recovered time in the final sector. The distance-aligned telemetry covered the shared observed range and ended with a gap of about **0.050 s**.
- The random forest had the lowest validation MAE. Across the two held-out 2025 races, the **prior three-lap median** gave the lowest MAE at **0.728 s**. **Ridge regression** gave the lowest RMSE at **1.356 s**.
- Over held-out five-second qualifying windows, the longitudinal model recorded **2.218 m/s** speed MAE, versus **12.423 m/s** for constant speed. Each window started at measured speed.

The race analysis is observational. Tyre compound, weather, fuel load and traffic can change together, and the prediction results cover eligible completed laps in two held-out races.

## Open the Tableau dashboards

Download the [packaged workbook](F1_Vehicle_Performance_Dashboards.twbx) and open it in Tableau Desktop. The workbook was built in Tableau Desktop 2026.2.3 and includes the CSV used by the dashboards.

