# Asana Time Tracking Data Extractor

This script extracts time tracking entries from Asana tasks and exports them into a CSV file.

## Features

- Extracts time tracking data from multiple Asana projects
- Writes the data into a CSV file

## Dependencies

This script uses the following Python libraries:
- asana
- requests
- csv
- json

To install these libraries use pip:

pip install asana requests

## Usage

1. Set up your Asana Personal Access Token: The script uses Asana's Personal Access Token for authentication. Replace the `PERSONAL_ACCESS_TOKEN` variable in the script with your own Personal Access Token.

2. Add your project GIDs: The script extracts data from multiple projects. Add your project GIDs to the `project_gids` list in the script.

3. Run the script: Use Python 3 to run the script:

python3 asana_time_tracking.py

4. Check the output: The script creates a CSV file named `report.csv` in the same directory, which contains the extracted time tracking data.

## Output

The CSV file has the following columns:
- `time entry id`: The gid of the time entry
- `employee gid`: The Asana id of the user who created the task
- `employee name`: The name of the user who created the task
- `entered on`: The date the task was entered
- `project name`: The name of the project
- `project gid`: The project id
- `actual time minutes`: Logged time in minutes
- `company`: Taken from the Asana Team the project sits in
- `ns job id`: Taken from the Asana project description (notes in the API) field
