# ETL Server Access Log Processing DAG

## Overview

This repository contains a Python script that defines an Apache Airflow DAG (Directed Acyclic Graph) named "ETL_Server_Access_Log_Processing." The DAG is designed to perform a series of ETL (Extract, Transform, Load) tasks on a server access log file. The tasks include downloading the log file, extracting specific fields, transforming data, and loading the results into a compressed file.

## Problem Statement

The goal of this DAG is to create a DAG that accomplishes the following tasks:

1. Download the server access log file from a this [URL](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0250EN-SkillsNetwork/labs/Apache%20Airflow/Build%20a%20DAG%20using%20Airflow/web-server-access-log.txt).
2. Extract specific fields from the log file (timestamp and visitorid).
3. Transform the extracted data by capitalizing the visitorid.
4. Load the transformed data into a compressed file.


## DAG Structure

The DAG is structured as follows:

1. **Imports Block**: Imports necessary libraries and modules for Airflow.

2. **DAG Arguments Block**: Defines default DAG arguments such as owner, start date, and email settings.

3. **DAG Definition Block**: Defines the DAG with a name, default arguments, description, and scheduling interval (daily).

4. **Task Definitions**:
   - **download**: Downloads the server access log file from the specified URL.
   - **extract**: Extracts specific fields (timestamp and visitorid) from the log file.
   - **transform**: Transforms the extracted data by capitalizing the visitorid.
   - **load**: Loads the transformed data into a compressed file.

5. **Task Pipeline Block**: Specifies the task dependencies, defining the order in which tasks should be executed.

## Installation and Running

To run the DAG, follow these steps:

1. Ensure you have Apache Airflow installed.

2. Create a Python file named `ETL_Server_Access_Log_Processing.py`.

3. Copy the code from this repository's script to `ETL_Server_Access_Log_Processing.py`.

4. Place the Python script in the DAGs directory of your Apache Airflow installation.

5. Start the Apache Airflow scheduler and web server.

6. Access the Airflow web interface and trigger the DAG to initiate the ETL process.



## Technologies

This project leverages the following technologies:


- **Apache Airflow**: An open-source platform used to programmatically author, schedule, and monitor workflows.
- **Python**: The programming language used to create `ETL_Server_Access_Log_Processing.py`, the DAG definition script.
- **Bash**: The scripting language used to perform the tasks.


## Contributing

Contributions to this project are welcome! If you have suggestions or would like to report issues, please open an issue or create a pull request.

## Acknowledgments

This project was completed as part of an educational assignment and is based on the provided datasets from the Chicago Data Portal.
It serves as an assignment for `ETL and Data Pipelines with Shell, Airflow and Kafka` course which is part of `IBM Data Engineer` Professional Certificate on Coursera. 

## License

This project is licensed under the [MIT License](LICENSE).
