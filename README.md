# **Log Analyzer with SIEM Tool Integration**

An advanced log analysis tool designed to help cybersecurity professionals and system administrators detect anomalies in log files, visualize activities, and export data for further analysis. This tool supports a variety of log formats and integrates seamlessly with Elasticsearch.

## **Table of Contents**
- [About](#about)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

---

## **About**

**Log Analyzer** is a Python tool that parses various log formats (e.g., Zeek, EVTX, SMB, and SSH) and detects potential security threats, such as ransomware and rootkits. It also provides capabilities to generate visualizations of SMB activity trends and integrates with Elasticsearch for storing and analyzing SSH log data.

---

## **Features**

- **Log Parsing**: Supports multiple log formats, including Zeek, EVTX, SMB, and SSH logs.
- **Malware Detection**:
  - Detects ransomware-related activities in SMB logs.
  - Identifies potential rootkit usage via EVTX logs.
- **Beacon Detection**: Analyzes HTTP traffic logs to detect beaconing behavior.
- **SMB Activity Visualization**: Generates bar charts to analyze SMB activity trends.
- **Elasticsearch Integration**: Export SSH log data to Elasticsearch for advanced querying and visualization.
- **Command Line Interface**: Easy-to-use menu-based interface for executing different log analysis tasks.

---

## **Requirements**

To run this project, you will need the following:
- Python 3.7 or later
- Required Python packages:
  - `Evtx`
  - `matplotlib`
  - `elasticsearch`
  - `pyfiglet`

These dependencies are listed in the `requirements.txt` file, which can be installed using `pip`.

---

## **Installation**

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/akilan-kj/log-analyzer.git
   cd log-analyzer
   ```
2.Install the required Dependence: 
```bash
pip install -r requirements.txt
```
3.Ensure Elasticsearch is running on http://localhost:9200 for exporting SSH logs.

---

## **Usage**
Run the tool by executing the following command in your terminal:

```bash
python log_analyzer.py
```
Main Menu Options
Once the tool is running, you will be presented with a menu:

Detect Malicious Rootkit: Analyze EVTX logs for rootkit activity using rundll32.
Detect Beacons: Analyze Zeek connection and HTTP logs to detect beaconing behavior.
Detect Ransomware Activity: Scan SMB logs for ransomware-like file activity.
SMB Activity Timeline Analysis: Visualize SMB activity trends using bar charts.
Elasticsearch Analysis: Export SSH log data to Elasticsearch for further analysis.
Exit: Exit the program.

---

## **License**
This project is licensed under the MIT License. See the LICENSE file for more information.


