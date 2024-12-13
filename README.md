Water Simulation Model

Overview

This Python script simulates the water stock of a lake over a specified period of time (in months), considering various factors such as human consumption, seasonal fluctuations in precipitation and evaporation, and groundwater inflow. The script also incorporates changes in water usage policies over time. Results are visualized through graphs and exported to a CSV file for further analysis.

Key Features

Simulates water stock changes in a lake over time.

Models seasonal fluctuations in evaporation, precipitation, and tourist activity.

Incorporates human water use based on population, tourists, and industrial use.

Visualizes water stock levels and tourist activity over time.

Exports simulation results to a CSV file for further analysis.

Dependencies

The script requires the following Python libraries:

math

matplotlib

numpy

pandas

Ensure these libraries are installed before running the script. You can install them using pip:

pip install matplotlib numpy pandas

Input Parameters

Time Steps:

dt: Time step in months (default is 1 month).

endtime: Total simulation period in months (default is 120 months).

Water Use Policy:

change_month: Month at which water usage policy changes.

rel_wateruse_before: Relative water usage before policy change (1 = 100%).

rel_wateruse_after: Relative water usage after policy change.

Lake Characteristics:

init_waterstock: Initial volume of the lake (m³).

max_waterstock: Maximum capacity of the lake (m³).

lake_surface: Surface area of the lake (m²).

Environmental Variables:

avg_evap: Average evaporation (converted to m³/month).

avg_precip: Average precipitation (converted to m³/month).

ground_water: Groundwater inflow into the lake (m³/month).

Human and Tourist Factors:

inhabitants: Population in the region.

avg_wateruse_pipd: Average water use per inhabitant per day (L/day).

init_avg_tourists: Average number of tourist nights spent per month.

avg_wateruse_ptpd: Average water use per tourist per day (L/day).

tourist_annual_gr: Annual growth rate of tourist nights spent.

other_wateruse: Industrial and agricultural water use (m³/month).

Script Functions

1. mm_to_m3(height)

Converts a height of water in millimeters to volume in cubic meters based on the lake surface area.

2. tourist_amt(month)

Calculates the number of tourists per month considering seasonal fluctuations and annual growth.

3. total_outflow(month, human_factor=1, nature_factor=1)

Calculates the total outflow of water from the lake, including human use and evaporation.

4. total_inflow(month)

Calculates the total inflow of water into the lake, including precipitation and groundwater.

Simulation Loop

The main loop iterates through each time step to:

Calculate water inflow and outflow.

Update the water stock of the lake.

Adjust water extraction based on policy changes.

Outputs

1. Graphs

Water Stock Over Time: Shows changes in the lake's water stock (in million m³).

Tourist Activity Over Time: Displays the number of tourists per month.

2. CSV File

The script exports the water stock data to simwaterdata.csv, with each row representing the water stock for a specific month.

How to Use

Configure Parameters: Update input parameters to match your simulation needs (e.g., lake size, population, policy change).

Run the Script: Execute the script using Python.

View Results: Inspect the generated graphs for a visual understanding of the water dynamics.

Export Data: Use the simwaterdata.csv file for further analysis in tools like Excel or Python.

Notes

Ensure the lake surface area (lake_surface) is accurate to maintain consistency in unit conversions.

Seasonal variations are modeled using sinusoidal functions; adjust coefficients if required.

The script is designed for generality and may need calibration for specific regions or lakes.

Contact

For questions or suggestions, contact us.

