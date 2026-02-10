# Azure-Sentinel-Lab

# Azure Sentinel SIEM & SOC Automation Lab

## Project Overview
This project demonstrates a functional Cloud SIEM (Security Information and Event Management) implementation using **Microsoft Azure Sentinel**. 

The goal was to build a centralized log monitoring system to detect, alert, and respond to simulated threats in real-time. This lab replicates a SOC environment where raw data is ingested, normalized, and analyzed to identify attack vectors such as Brute Force attempts and Unauthorized Privilege Escalation.

## Architecture & Configuration
* **SIEM Core:** Azure Sentinel
* **Log Management:** Azure Log Analytics Workspace
* **Data Sources:**
    * Virtual Machines (Windows/Linux)
    * Azure Activity Logs
    * Network Security Groups (NSGs)
* **Orchestration:** Logic Apps for automated incident response

## Key Objectives
* **Ingestion:** Configured data connectors to aggregate raw logs from simulated network endpoints.
* **Detection:** Developed custom KQL (Kusto Query Language) rules to tune alerts and reduce false positives.
* **Triage:** Simulated attack scenarios (e.g., RDP Brute Force) to test incident mapping and severity classification.
* **Visualization:** Created workbooks to visualize geographic login attempts and failed authentication spikes.

## Skills Demonstrated
* **Blue Team Operations:** Log analysis, threat hunting, and incident triage.
* **Query Logic:** Writing KQL for specific threat signatures.
* **Security Hardening:** Identifying gaps in "Least Privilege" configurations.
