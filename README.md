# GIS Team Data Challenge

## 👋 Hi there

Welcome to the GIS team's Data Challenge! This small data challenge is designed to help us evaluate and for you to showcase your skills in geospatial data processing and project management. You can take an automated approach with python or another coding language, or a manual approach using GIS tools you have access to. The use of GitHub is optional. The challenge will go from easy to difficult.  There's no pressure to finish all the tasks; just try your best and get as far as you can! 

## Getting started

There are two ways for you to get started and submit your results for this challenge:

**1) Zipped folder**

If you have not used GitHub before or are unfamiliar with it, that's okay.  Please store your source data, files, outputs and documentation/readme in a folder, zip it up, and email the zipped folder to Matt (mcroswe@planning.nyc.gov), Casey (csmith@planning.nyc.gov), and Jack (jrosacker@planning.nyc.gov).

**2) GitHub**

If you've used GitHub and would like to demonstrate your GitHub skills, start this challenge by creating a new **private** repo under your github username. We would like you to include all the code, notes, visualizations, and data inside of the repo. When you are done with the challenge, please provide read access to your repo by inviting `@caseysmithpgh`, `@jackrosacker`, `@croswell81`, and `@AmandaDoyle`.
> ⚠️ Note: **the repo has to be <ins>private</ins>, otherwise you will be automatically <ins>disqualified</ins>**.


## What we are looking for

You will be evaluated based on your repo or folder, so make sure all files are stored in your repo or folder. Specifically we are looking at:

- **Project scaffolding**: How you name, manage, and organize your files.
- **Documentation**:
  - A comprehensive `README` document on anything that we should know about how you completed the tasks.
  - Clear instructions on process steps or commands to run code (optional), and what to expect.
  - Clear documentation for functions/processes.
- **Reproducibility**:
  - Ideally if your code runs on your machine, it would also run on mine (optional).
  - Make sure you document any software dependencies and installation processes.
- **Code** (optional):
  - Clean
  - Readable
  - DRY (Don't Repeat Yourself)
- **Project Management (Optional GitHub specifics)**:
  - We want to see how you manage a multi-part project and how you break down the tasks.
  - Feel free to open up issues for yourself / make pull requests and etc so that your code progress is captured and documented.
  - We highly **discourage** lumped commits.
- **Creativity**:
  - If you do not know how to complete a task in Python, for example, but you do know how to complete the task using another tool, like Excel, Carto, or ArcGIS, please feel free to use the tools you know to complete the task and document what tools were used, and your methodology, in the readme file.  


## Table of Content

- [Introduction](#introduction)
  - [Task 1: Data Download](#task-1-data-download)
  - [Task 2: Data Aggregation](#task-2-data-aggregation)
  - [Task 3: Data Visualization](#task-3-data-visualization)
  - [Task 4: Spatial Data Processing](#task-4-spatial-data-processing)
- [Resources](#resources)

## Introduction

We love the NYC 311 service and the open data products that come with it. In this challenge, you will use **[311 Service Requests from 2010 to Present](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9)** on NYC Open Data, write an ETL pipeline, and produce some data insight.

### Task 1: Data Download

Download all service request records created in the **last week** (7 days) that have **HPD** as the responding agency, and store the data in a csv named `raw.csv` in a folder called `data`.
You can do this by 1) writing a python script/notebook or 2) manually filtering and downloading the data using the Open Data tools.

### Task 2: Data Aggregation

Create a time series table based on the `data/raw.csv` file we created from **Task 1** that has the following fields

- `created_date_hour`: the timestamp of request creation by date and hour
- `complaint_type`: the type of the complaint
- `count`: the count of service requests by `complaint_type` by `created_date_hour`

Store this table in a csv under the `data` folder with a csv file name of your choice.

### Task 3: Data Visualization

Create a multi-line plot to show the total service request counts by `created_date_hour` for each `complaint_type`. Make sure you store the image of the plot in the `data` folder as a `.png` or `.html` file.  

### Task 4: Spatial data processing

Naturally, in the GIS team we work with a lot of spatial data and we enhance datasets with geospatial attributes, such as point locations and administrative boundaries. To help us better understand the data from **Task 1**, we would like you to join the initial raw data to the **[2020 NTA (Neighborhood Tabulation Area) boundaries](https://www1.nyc.gov/site/planning/data-maps/open-data/census-download-metadata.page)** and create a choropleth map of 7 day total count by NTA of a specific `complaint_type` of your choice.

Depending on how you generate the map, you can store the map as a `.png` or `.html` under the `data` folder. Let us know if you do not have access to any mapping software.

## Resources

- Reach out to Matt (mcroswe@planning.nyc.gov), Casey (csmith@planning.nyc.gov), and Jack (jrosacker@planning.nyc.gov) if you have any questions. We love people who ask questions.
