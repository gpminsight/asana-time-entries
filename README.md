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

4. Check the output: The script creates a CSV file named `time_tracking_entries.csv` in the same directory, which contains the extracted time tracking data.

## Output

The CSV file has the following columns:
- `gid`: The gid of the task
- `resource_type`: The type of the resource
- `duration_minutes`: The duration of the task in minutes
- `created_by`: The name of the user who created the task
- `entered_on`: The date the task was entered

## Note

This script only extracts the 'name' field from the 'created_by' dictionary in the Asana API response. Modify the script if you need to extract more fields.
