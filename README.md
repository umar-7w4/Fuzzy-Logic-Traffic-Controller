## Fuzzy Logic-Based Traffic Light Control System

## Overview

Traffic congestion is a critical issue in urban environments, often exacerbated by inefficient traffic light systems that operate on fixed cycles or predetermined schedules. This project introduces a novel approach to traffic light control using fuzzy logic, designed to optimize traffic flow and minimize delays, particularly under varied and heavy traffic conditions. The system smartly prioritizes emergency vehicles at intersections, significantly reducing their waiting times and enhancing overall traffic management.

## Features

- **Adaptive Traffic Light Control**: Dynamically adjusts traffic light timings based on real-time traffic data, including vehicle count and the presence of emergency vehicles.
- **Prioritization of Emergency Vehicles**: Reduces waiting times for emergency vehicles, ensuring they pass through intersections with minimal delay.
- **Traffic Simulation**: Utilizes SUMO (Simulation of Urban MObility) for realistic traffic simulations.
- **Fuzzy Logic Implementation**: Leverages fuzzy logic principles to handle the uncertainties and partial truths inherent in traffic management.

## System Requirements

- **Python 3**
- **SUMO (Simulation of Urban MObility)**
- **SUMO-GUI** (Graphical User Interface for SUMO)

## Installation

## Step 1: Install Python 3

1. Verify if Python 3 is installed by running:
    ```bash
    python3 --version
    ```
2. If not installed, download and install the latest version from [python.org](https://www.python.org/downloads/).

## Step 2: Install SUMO and SUMO-GUI

For Unix-like systems:
```bash
sudo add-apt-repository ppa:sumo/stable
sudo apt-get update
sudo apt-get install sumo sumo-tools sumo-doc
```

For Windows:
- Download and install SUMO from the official SUMO website or compile it from the source using instructions from the SUMO GitHub repository.

## Step 3: Set Up Environment Variables

- Set the `SUMO_HOME` environment variable to point to your SUMO installation directory:
  - On Unix-like systems, add the following to your `.bashrc` or `.bash_profile`:
    ```bash
    export SUMO_HOME=/path/to/sumo
    ```
  - On Windows, set the environment variable in System Properties.

- Apply the changes:
  ```bash
  source ~/.bashrc
  ```
  or restart your terminal.

## Step 4: Install Python Dependencies

- Navigate to the project directory and create a virtual environment:
  ```bash
  python3 -m venv venv
  ```
- Activate the virtual environment:
  - On Unix-like systems:
    ```bash
    source venv/bin/activate
    ```
  - On Windows:
    ```bash
    venv\Scripts\activate
    ```
- Install the required Python packages:
  ```bash
  pip install -r requirements.txt
  ```

## Configuration

## SUMO Network Files

Ensure that the SUMO network files (`.net.xml`, `.rou.xml`, etc.) are correctly placed in the appropriate directories, typically within the `4-junction` folder.

## Running Test Simulation

Before running full simulations, it's recommended to run a test:
```bash
sumo-gui -c 4-junction.sumocfg
```
This will open the SUMO GUI with the sample configuration if everything is set up correctly.

## Running Simulations

## Starting SUMO GUI

To start the SUMO GUI:
```bash
sumo-gui
```

## Running the Fuzzy Logic-Controlled Simulation

1. Navigate to the `fuzzy controlled simulation` directory.
2. Run the simulation:
   ```bash
   python fuzzy_controlled_simulation.py
   ```

## Running the Uncontrolled Simulation

1. Navigate to the `uncontrolled simulation` directory.
2. Run the simulation:
   ```bash
   python uncontrolled_simulation.py
   ```

## Observing Results

- Monitor the number of vehicles moving and stopped at intersections.
- Pay special attention to the waiting times of emergency vehicles.
- Compare the performance of traffic lights with and without fuzzy logic control.

## Results and Analysis

## Generated Data Files

The simulation generates several data files providing insights into the system's performance:

- **MOVING VEHICLES**: Data on moving vehicles.
- **STOPPED VEHICLES**: Data on stationary vehicles at traffic lights.
- **COMBINED WAIT TIME**: Data on overall vehicle waiting times.
- **EMV WAITING TIME**: Data on emergency vehicle waiting times.

## Graphs and Visualization

To visualize the results:

1. Navigate to the `graphs` directory.
2. Run the provided scripts to generate graphs.

## Performance Metrics

Key metrics include:

- Average waiting time for all vehicles and emergency vehicles.
- Intersection throughput (vehicles passing per unit of time).
- Efficiency of traffic light switching.

## Comparative and Statistical Analysis

- Compare the results of controlled and uncontrolled simulations.
- Perform statistical tests using tools like Python's SciPy library to determine the significance of the results.

## Troubleshooting

## Common Issues

- **SUMO Not Found**: Ensure the `SUMO_HOME` environment variable is correctly set.
- **Python Module Not Found**: Activate your virtual environment and run `pip install -r requirements.txt`.
- **SUMO GUI Does Not Start**: Check for error messages and ensure configuration files are correct.
- **Incorrect Simulation Results**: Verify the integrity of network and route files, and check simulation parameters.

## Support

For further assistance or to report issues, please contact:

- Umar Mohammad: mohammadumar7w4@gmail.com

## Future Work

Future research could explore the scalability of this approach in varied urban settings and integrate it with other smart transportation technologies. Testing in real-world scenarios could further validate the system's effectiveness.
