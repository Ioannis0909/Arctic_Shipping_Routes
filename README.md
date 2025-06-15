README.txt
----------------------------------------------------------------------------------------------------
PROJECT: Arctic Shipping Routes Analysis and Forecasting

This project analyzes the navigability of key Arctic shipping routes under different ice concentration thresholds using historical and forecasted ice data. The workflow leverages a series of Jupyter Notebooks, each dedicated to a specific part of the analysis pipeline. 

A paper was created along with this work titled 'Forecasting Arctic Shipping Routes Under Climate Change: A Network Approach'. This work was done as part of the 20599 Simulation and Modeling within the MSc Data Science and Business Analytics course at Università Bocconi. 

Submission date: 2025-05-30

----------------------------------------------------------------------------------------------------
NOTE: This full pipeline may take a considerable amount of time to run, especially for all risk thresholds (150, 225, 300, 375, and 450). Additionally, intermediate and final outputs (e.g., forecasted ice rasters, navigable days per threshold, plots) will collectively exceed 50GB in size. Ensure adequate computational resources and disk space.

----------------------------------------------------------------------------------------------------
CONTENTS:

SUBMISSION_Forcasting_Ice.ipynb  
   - Generates daily forecasted Arctic ice concentration rasters for 2025–2050 based on historical data and a linear decay model.

SUBMISSION_Merging_Forcasted_Ice_with_N_Hemisphere.ipynb  
   - Merges the forecasted ice data with a northern hemisphere base map, filling in gaps and standardizing to a common projection (EPSG:3411).  
   - Prepares a consistent raster dataset for downstream navigability analysis.
   
SUBMISSION_Getting_passable_days.ipynb  
   - Uses the A* algorithm to compute shortest maritime routes between four port pairs: Shanghai ↔ New York, Shanghai ↔ Rotterdam, Singapore ↔ New York, Singapore ↔ Rotterdam.  
   - Determines the number of “Arctic-navigable” days each year (2025–2050) for each risk threshold, considering dynamic ice conditions and route distance thresholds.  
   - Outputs a CSV file of navigable days per year for further analysis.

SUBMISSION_Final_Graphs.ipynb  
   - Reads the compiled navigable days data (one CSV per threshold).  
   - Produces visualizations:  
     - Annual navigable days by threshold  
     - Average route lengths by threshold  
     - Sensitivity of navigability to ice concentration thresholds.  
   - These final plots support analysis and conclusions in the research report.

----------------------------------------------------------------------------------------------------
KEY FEATURES:
- Use of A* pathfinding for optimal shipping routes across dynamic sea ice maps.  
- Integration of forecasted ice data with baseline topography.  
- Handles multiple ice concentration thresholds to reflect different vessel risk tolerances.  
- Considers real-world geography and constraints (e.g., Panama and Suez Canals carved into maps).  
- High-resolution daily data analysis for robust, fine-grained outputs.

----------------------------------------------------------------------------------------------------
CONTACT:
For questions or issues related to this project, please reach out to:

- Ioannis Thomopoulos   --> ioannis.thomopoulos@studbocconi.it  
- Jacopo D'Angelo       --> jacopo.dangelo@studbocconi.it  
- Max Rienth            --> maximilian.rienth@studbocconi.it  
- Luca Milani           --> luca.milani2@studbocconi.it  

----------------------------------------------------------------------------------------------------
END OF FILE