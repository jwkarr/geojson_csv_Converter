JSON/GeoJSON to CSV Converter for Jupyter Notebooks
A flexible Python-based tool for converting JSON and GeoJSON files into CSV format, designed to work seamlessly in Jupyter Notebook environments.
Features

Multiple Format Support: Handles both GeoJSON and regular JSON files
Batch Processing: Convert multiple files at once
Robust Error Handling: Continues processing even if individual files fail
Flexible JSON Handling:

GeoJSON files with features and geometry
JSON arrays of objects
Single JSON objects
Nested JSON structures (automatically flattened)


Geometry Processing:

Point geometries extracted to longitude/latitude columns
Complex geometries (LineString, Polygon, etc.) converted to WKT format
Support for elevation data in Point geometries


Data Preview: Displays sample data from each converted file
Summary Statistics: Provides row and column counts for each conversion

Requirements
pythonimport json
import csv
import os
import glob
from IPython.display import display, HTML
import pandas as pd
import traceback
These libraries are typically included in standard Jupyter notebook installations.
Quick Start Guide
Step 1: Import Required Libraries
pythonimport json
import csv
import os
import glob
from IPython.display import display, HTML
import pandas as pd
import traceback
Step 2: Copy the Function Definitions
Copy all the function definitions from the provided code into a cell in your Jupyter notebook.
Step 3: Set Your File Paths
python# Directory containing your JSON/GeoJSON files
input_directory = "./my_json_files"

# Directory where CSV files will be saved
output_directory = "./Converted_Json_Files"
Step 4: Run the Conversion
python# Convert all JSON and GeoJSON files to CSV
dataframes = batch_convert_files_to_csv(
    input_directory, 
    output_directory,
    file_patterns=["*.geojson", "*.json"]
)
Troubleshooting
Common Issues and Solutions
See the full README above for detailed troubleshooting steps including permission errors, path issues, and import problems.
