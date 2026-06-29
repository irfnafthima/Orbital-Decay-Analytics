# Orbital Decay Analytics

## Project Overview

The rapid growth of satellite deployments and commercial space activities has significantly increased the number of objects orbiting Earth. Monitoring these objects is essential for understanding global space activities, managing orbital congestion, and supporting long-term space sustainability.

This project performs exploratory data analysis (EDA) on orbital object data containing more than 14,000 records representing satellites, rocket bodies, and orbital debris. The objective is to identify trends in launch activities, analyze orbital characteristics, and understand the distribution of space infrastructure using data analytics techniques.

---

## Problem Statement

The increasing number of objects in Earth's orbit has introduced challenges related to:

- Space debris accumulation
- Orbital congestion
- Collision risks for operational satellites
- Space traffic management
- Long-term sustainability of orbital environments

Analyzing orbital datasets provides valuable insights for governments, research organizations, and commercial space operators involved in mission planning and satellite operations.

---

## Objectives

The objectives of this project are:

- Perform data cleaning and preprocessing on real-world orbital datasets.
- Identify major contributors to global space activities.
- Analyze launch trends over time.
- Study the distribution of launch infrastructure.
- Understand the composition of orbital objects.
- Explore relationships between orbital parameters.
- Generate meaningful insights through visualization and exploratory analysis.

---

## Why is this Dataset Important?

Orbital datasets play an important role in modern aerospace operations and research.

These datasets are useful for:

- Monitoring active satellites and inactive objects.
- Understanding the growth of space debris.
- Supporting satellite collision avoidance systems.
- Planning future satellite launches.
- Managing space traffic and orbital resources.
- Studying long-term trends in global space activities.

As the number of satellites continues to increase due to commercial constellations and private space companies, data-driven analysis of orbital environments becomes increasingly important.

---

## Dataset Description

The dataset contains information on more than **14,000 orbital objects** and includes the following attributes:

| Feature | Description |
|---------|-------------|
| OBJECT_NAME | Name of the orbital object |
| COUNTRY_CODE | Country associated with the object |
| OBJECT_TYPE | Type of object (Payload, Rocket Body, Debris) |
| LAUNCH_DATE | Date of launch |
| SITE | Launch facility code |
| APOAPSIS | Maximum orbital distance from Earth |
| PERIAPSIS | Minimum orbital distance from Earth |
| PERIOD | Time required to complete one orbit |
| INCLINATION | Orbital inclination angle |
| ECCENTRICITY | Shape of the orbit |
| DECAY_DATE | Date of atmospheric re-entry |
| SEMIMAJOR_AXIS | Average orbital radius |

---

## Data Cleaning and Preprocessing

The following preprocessing steps were performed:

- Missing value analysis using `isnull().sum()`
- Duplicate record detection using `duplicated().sum()`
- Missing categorical values replaced with `Unknown`
- Missing RCS values imputed using mode
- Records with missing launch dates removed
- Datetime conversion for launch dates
- Feature extraction for launch year analysis

An important observation was that missing values in `DECAY_DATE` represented objects that are still active in orbit rather than missing information.

---

## Exploratory Data Analysis

### 1. Country-wise Analysis
Analyzed the number of orbital objects contributed by each country to identify major participants in global space activities.

**Finding:**
Space activities are concentrated among a relatively small number of countries with established launch capabilities.

---

### 2. Launch Site Analysis
Analyzed launch facilities to identify the most active launch locations worldwide.

**Finding:**
A limited number of launch sites account for the majority of global launches, indicating centralized launch infrastructure.

---

### 3. Object Type Distribution
Studied the distribution of payloads, rocket bodies, and debris within Earth's orbit.

**Finding:**
The orbital environment contains both operational satellites and non-operational objects, highlighting the importance of orbital sustainability.

---

### 4. Launch Trend Analysis
Examined how launch activity has evolved over time.

**Finding:**
Launch frequency has increased significantly in recent decades due to commercial satellite deployments and private space initiatives.

---

### 5. Correlation Analysis
Explored relationships among orbital parameters.

Parameters analyzed:

- Semi-major axis
- Orbital period
- Apoapsis
- Periapsis
- Inclination
- Eccentricity

**Finding:**
Several orbital parameters exhibit strong positive correlations due to their physical relationships in orbital mechanics.

---

## Visualizations Included

The project includes the following visualizations:

- Top Countries by Number of Orbital Objects
- Distribution of Object Types
- Top Launch Sites
- Launch Trends Over Time
- Orbital Parameter Correlation Heatmap
- Active vs Decayed Object Distribution
- Average Orbital Period by Object Type
- Average Orbit Height by Country

---

## Major Findings

- Global space activity is dominated by a small number of countries.
- Launch operations are concentrated among a limited number of launch facilities.
- The number of orbital objects has increased significantly over time.
- Earth's orbit contains a substantial amount of inactive hardware and debris.
- Orbital characteristics show strong statistical relationships.
- Missing decay dates often indicate active orbital objects rather than incomplete data.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Git
- GitHub

---

## Future Enhancements

Potential future improvements include:

- Orbital decay prediction using machine learning.
- Collision probability estimation.
- Real-time satellite tracking integration.
- Interactive dashboard development.

---