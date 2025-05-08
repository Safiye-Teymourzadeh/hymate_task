# EV Charging and Billing System

## Overview
This project simulates an Electric Vehicle (EV) charging and billing system for a small residential building with 5 electric vehicles (EVs) and 3 charging ports. It schedules charging sessions based on the availability of cars, their maximum charging rate, and the electricity prices, and computes the cost for each session.

## Assumptions
- Charging starts only when the car is available, but can contunue over nitght.
- The last day of the week foes not have requirements, therefore no specific schdule is needed.
- Each port can charge only one car at a time.
- Each car has a maximum charging rate and a specific capacity.
- Charging step is 1 hour.
- Charging efficiency is assumed to be 95%.
- Cars must reach to a target state of charge (SoC) by a specific time.

## Files
- `cars.json`: Contains information about 5 cars, including their ID, capacity, maximum charging rate, and efficiency.
- `availability.csv`: A car x hour matrix showing the availability of cars for each hour.
- `requirements.json`: Contains the target SoC for each car on each day.
- `prices.csv`: Hourly electricity prices in €/kWh for 7 days.

## Structure
- **charging_schedule.py**: The main Python script containing the logic for scheduling charging, calculating costs, and generating the charging plan.
- **requirements.json**: Contains the target SoC for each car on each day.
- **availability.csv**: Provides the availability of cars for each hour.
- **prices.csv**: Contains the hourly electricity prices.

## Setup Instructions
1. Ensure you have Python 3.x installed on your system.
2. Install necessary Python libraries:
    ```bash
    pip install numpy pandas
    ```
3. Download or clone the repository.
4. Place the following data files in the project directory:
   - `cars.json`
   - `availability.csv`
   - `requirements.json`
   - `prices.csv`
5. Run the script:
   ```bash
   python charging_schedule.py
