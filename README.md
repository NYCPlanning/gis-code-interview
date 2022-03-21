# GIS Team Code Interview

## 👋 Hi there

Welcome to the GIS team's code interview! This small data challenge is designed to help us evaluate and for you to showcase your skills in data processing, python, GitHub, and/or geospatial data processing. The challenge will go from easy to difficult.  There's no preassure to finish all the tasks; just try your best and get as far as you can!

## Getting started

There are two ways for you to get started and submit your results of this chanllenge:

**1) GitHub**
If you've you'd GitHub and would like to demostrate your skills, please follow the instructions below.
To start this challenge, create a new **private** repo under your github username. We would like you to include all the code, notes, visualizations, and data inside of the repo. When you are done with the challenge, please provide read access to your repo by inviting `@SashaWeinstein`, `@mbh329`, `@AmandaDoyle`, `@croswell81`, and `@td928`.
> ⚠️ Note: **the repo has to be <ins>private</ins>, otherwise you will be automatically <ins>disqualified</ins>**. Also we will check your commit timestamp to only account for the first 48 hours of coding activities.

**2) Zipped folder**
If you have not used GitHub before or are unfarmiliar with it, that's okay.  Please store your source data, files, and outputs in a folder, zip it up, and email the file to Matt (mcroswe @ planning.nyc.gov).

## What we are looking for

Your code interview will be evaluated based on your repo or folder, so make sure all files you have are stored in your repo or folder. Specifically we are looking at:

- **Project scafolding**: How you name, manage, and organize your files.
- **Reproducibility**:
  - Ideally if it runs on your machine, it would also run on mine.
  - Make sure you document any software dependency, and installation process.
- **Code**:
  - Clean
  - Readable
  - DRY (Don't Repeat Yourself)
- **Documentation**:
  - A comprehensive `README` on anything that we should know.
  - Clear instructions on commands to run code and what to expect.
  - Clear documentation for functions/processes in code.
- **Project Management (GitHub specific)**:
  - We want to see how you manage a multi-part project and how you break down the tasks.
  - Feel free to open up issues for yourself / make pull requests and etc so that your code progress is captured and documented.
  - We highly **discourage** lumpped commits.

## Table of Content

- [Introduction](#introduction)
  - [Task 1: Data Download](#task-1-data-download)
  - [Task 2: Data Aggregation](#task-2-data-aggregation)
  - [Task 3: Data Visualization](#task-3-data-visualization)
  - [Task 4: Spatial Data Processing](#task-4-spatial-data-processing)
  - [Task 5: SQL](#task-5-sql)
  - [Task 6: Spatial SQL](#task-6-spatial-sql)
- [Resources](#resources)

## Introduction

We love the NYC 311 service and the open data products that come with it. In this challenge, you will use **[311 Service Requests from 2010 to Present](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9)** on NYC Open Data, write an ETL pipeline, and produce some data insight.

### Task 1: Data Download

Download all service request records created in the **last week** (7 days) and has **HPD** as the responding agency, and store the data in a csv named `raw.csv` in a folder called `data`.
You can do this by 1) writing a python script/notebook or 2) manually filtering and downloading the data using the Open Data tools.

### Task 2: Data Aggregation

Create a time series table based on the `data/raw.csv` file we created from **Task 1** that has the following fields

- `created_date_hour`: the timestap of request creation by date and hour
- `complaint_type`: the type of the complaint
- `count`: the count of service requests by `complaint_type` by `created_date_hour`

Store this table in a csv under the `data` folder with a csv file name of your choice.

### Task 3: Data Visualization

Create a multi-line plot to show the total service request counts by `created_date_hour` for each `complaint_type`. Make sure you store the image of the plot in the `data` folder as a `.png` file.  

### Task 4: Spatial data processing

At Data Engineering, we enhance datasets with geospatial attributes, such as point locations and administrative boundaries. To help us better understand the data from **Task 1**, we would like you to join the initial raw data to the **[2020 NTA (Neighborhood Tabulation Area) boundaries](https://www1.nyc.gov/site/planning/data-maps/open-data/census-download-metadata.page)** and create a choropleth map of 7 day total count by NTA of a specific `complaint_type` of your choice.

Depending on how you generate the map, you can store the map as a `.png` or `.html` under the `data` folder.

## Resources

- Reach out to Sasha (aweinstein @ planning.nyc.gov) if you have any questions. We love people who ask questions.