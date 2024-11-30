
# Synthetic Time Series Data Generation and Anomaly Detection

## Project Overview

This project demonstrates how to generate a large-scale synthetic multivariate time series dataset of hardware metrics and perform anomaly detection using Python. The dataset includes metrics such as CPU temperature, CPU usage, memory usage, and battery level, with random anomalies introduced to simulate unusual system behavior. Anomaly detection is implemented using the Interquartile Range (IQR) method.

## Project Workflow

1. **Data Generation**: 
   - Data is collected using the `psutil` and `wmi` libraries for hardware metrics such as CPU temperature, usage, and memory usage.
   - The data is sampled at 10 samples per second for a duration of 600 minutes (~1GB of data).
   - Random anomalies are introduced (e.g., high CPU usage, elevated temperatures) to simulate abnormal behavior.
   
2. **Anomaly Detection**:
   - Anomalies are detected using the Interquartile Range (IQR) method, which flags data points that are unusually high or low compared to the rest of the dataset.
   - Anomalies are identified in the CPU temperature, CPU usage, and memory usage columns.

3. **Output**:
   - The generated dataset is saved as `synthetic_hardware_monitor_data.csv`.
   - The anomaly detection results are saved as `synthetic_data_with_anomalies.csv`.

## Files in this Project

- `data_generation.py`: Python script that generates the synthetic dataset and injects random anomalies.
- `anomaly_detection.py`: Python script that performs anomaly detection using the IQR method.
- `synthetic_hardware_monitor_data.csv`: CSV file containing the generated time series data.
- `synthetic_data_with_anomalies.csv`: CSV file containing the data with flagged anomalies.
- `synthetic_data_anomaly_detection_presentation.pptx`: PowerPoint presentation summarizing the project.
- `README.md`: This file.

## How to Run

### Step 1: Install Dependencies

Make sure you have the necessary Python libraries installed. You can do this by running the following command:

```bash
pip install psutil wmi pandas
```

### Step 2: Run Data Generation

To generate the synthetic data, run the `data_generation.py` script:

```bash
python data_generation.py
```

This will save the generated data to `synthetic_hardware_monitor_data.csv`.

### Step 3: Perform Anomaly Detection

Once the data is generated, run the `anomaly_detection.py` script to detect anomalies:

```bash
python anomaly_detection.py
```

This will save the data with anomalies flagged in `synthetic_data_with_anomalies.csv`.

## Key Features

- **Large-scale data generation** (~1GB) of system hardware metrics.
- **Random anomalies** to simulate real-world issues.
- **Anomaly detection** using the robust IQR method.

## Conclusion

This project provides a comprehensive demonstration of time series data generation and anomaly detection. The methods used can be applied to real-world system monitoring and data anomaly detection.


