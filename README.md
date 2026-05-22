SDS210 - Global Wildfire Hotspot Analysis with NASA FIRMS

Interactive spatial wildfire analysis project developed for the University of Zurich course SDS210: Programming with Spatial Data.
The project uses near real-time wildfire detections from the NASA FIRMS API and visualizes global fire activity using interactive clustering and temporal grouping techniques.

Course requirements emphasize reproducible workflows, modular Python programming, spatial visualization, and well-documented analysis pipelines.

Project Overview

This project explores the question:

How can near real-time wildfire detections be filtered and visualized to highlight major global fire hotspots on an interactive map?

The workflow combines:

NASA FIRMS API data acquisition
data cleaning and preprocessing
wildfire intensity classification
spatial KMeans clustering
temporal acquisition window grouping
interactive Folium-based visualization

The final result is an interactive multi-layer wildfire monitoring map.

Features
Interactive wildfire map
Global wildfire detections
Multiple basemap options
Satellite imagery support
Interactive popups and tooltips
Fire intensity classification

Detections are grouped into:

Low
Medium
High
Extreme

using Fire Radiative Power (FRP).

Pie-chart marker clustering

Cluster icons dynamically summarize local fire intensity composition.

Spatial KMeans hotspot analysis

Two spatial clustering resolutions:

k = 7 for broad continental hotspot regions
k = 30 for more detailed regional structure

Clusters are visualized using:

cluster center markers
transparent hotspot polygons
Temporal acquisition windows

Wildfire detections are grouped into approximate 4-hour satellite acquisition windows to highlight temporal collection patterns.

Example Outputs
All wildfire detections with pie-chart clusters
Broad spatial hotspot regions (k=7)
Detailed spatial hotspot regions (k=30)
Temporal acquisition windows


NASA FIRMS API:

VIIRS_SNPP_NRT
Near real-time global wildfire detections

https://firms.modaps.eosdis.nasa.gov/

The VIIRS source was selected because it provides high-resolution global wildfire detections suitable for interactive monitoring workflows.

Repository Structure
project/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── outputs/
│   ├── wildfire_final_interactive_map.html
│   ├── top_15_fires.csv
│   └── kmeans_cluster_summary.csv
│
├── wildfire_analysis.ipynb
└── README.md
Installation


Required Python Packages
pandas
numpy
folium
scikit-learn
requests
jupyter

Running the Project

Open the notebook:

jupyter notebook

Run all notebook cells from top to bottom.

The final interactive map will be exported to:

outputs/wildfire_final_interactive_map.html
Reproducibility

This repository was designed to be reproducible on another machine:

relative file paths are used
processed outputs are generated automatically
notebook cells run sequentially from start to finish
required packages are documented

These design decisions follow the SDS210 project guidelines for reproducible spatial programming workflows.

Challenges and Design Decisions

Some important project decisions included:

simplifying the visualization to avoid excessive layer complexity
tuning KMeans resolutions for interpretability
replacing overly dense temporal grouping with broader 4-hour acquisition windows
balancing visual clarity with global spatial coverage

The project evolved iteratively through multiple visualization refinements.

AI Usage Statement

AI tools were used during development to:

improve readability and structure
discuss visualization ideas
refine documentation and explanations

All code, analysis decisions, and final project outputs were reviewed and validated manually.

This follows the SDS210 AI usage guidelines.

Author

Tristan Hein
University of Zurich
SDS210 - Programming with Spatial Data

GitHub repository:
https://github.com/heintr/projectwildfire