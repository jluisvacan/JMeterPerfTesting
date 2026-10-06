# 🚀 JMeter Performance & API Testing Suite

![JMeter](https://img.shields.io/badge/Apache%20JMeter-5.6%2B-orange.svg?style=for-the-badge&logo=apachejmeter&logoColor=white)
![Testing Type](https://img.shields.io/badge/Testing-API%20%7C%20Performance-blue?style=for-the-badge)

---

## 📌 Executive Summary

This repository demonstrates a **comprehensive end-to-end performance and API testing framework** engineered using **Apache JMeter 5.6.3**. It simulates realistic user traffic scenarios, validates system stability under load, and enforces Service Level Agreements (SLAs).

---


## 🛠️ Key Technical Features & Best Practices

- **Dynamic Data Correlation:** Extraction and passing of dynamic response tokens and IDs using RegEx / JSON Extractors.
- **Robust Assertions:** Automated validation of HTTP Status Codes, Response Body payloads, and Latency Thresholds.
- **CLI & GUI Ready:** Standardized for interactive debugging (GUI) and continuous integration/headless runs (Non-GUI / CLI).
- **Rich Dashboard Reporting:** Automated HTML report generation featuring detailed metrics (Throughput, Latency, Error %, Response Time Percentiles).

---

## 💻 Prerequisites & Environment Setup
Ensure the following prerequisites are installed before executing the test scripts:

- **Java Development Kit (JDK)**: Version 8 or higher (java -version)

- **Apache JMeter**: Version 5.0 or higher (Download Apache JMeter)

---

## 🚀 Execution Guide
Ensure the following prerequisites are installed before executing the test scripts:

- **Opcion 1: Interactive Execution (GUI Mode)**: 
1. Launch Apache JMeter:
2. Open the desired .jmx test script (File > Open).
3. Click the Start button (Green Play Icon) to run the test plan.

- **Opcion 2: Headless Execution & HTML Report Generation (CLI Mode)**:
1. Execute the test suite from the command line and automatically build an HTML performance dashboard:
    - Command Arguments Breakdown:
`-n`: Runs JMeter in non-GUI (headless) mode.
`-t`: Specifies the file path of the .jmx test script.
`-l`: Specifies the output .jtl file for raw execution logs.
`-e`: Triggers the generation of an interactive HTML report upon completion.
`-o`: Specifies the output folder for the HTML dashboard.

```
jmeter -n -t <YourTestPlanName>.jmx -l reports/test_results.jtl -e -o reports-html
```