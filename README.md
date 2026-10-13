# Crime-analysis-of-chicago
An interactive Tableau dashboard that explores Chicago crime data from 2017 to 2022. It helps users spot crime patterns by type, time of day, day of week and location, and tracks how crime has changed over the years.
## 📌 Project Overview

Understanding when, where and what kind of crimes happen is the first step toward
making communities safer. This project turns raw Chicago crime records into a single
interactive dashboard that answers questions such as:

- What are the most common types of crime?
- At what time of day and on which weekdays does crime peak?
- How has the crime rate changed from year to year?
- What share of cases end in an arrest?
- How many incidents are domestic vs. non-domestic?
- How many crimes happened recently, and which community areas are affected?

## 📊 Dashboard Features

| Visualization | What it shows |
|---|---|
| **Total Cases** | Overall number of recorded crimes (KPI) |
| **Live Feed of Crimes / Recent Crimes** | Crimes from the last N months (user-selectable) |
| **Top N Crime Types** | Most frequent crime categories (user picks top 3 / 5 / 10) |
| **Crimes by Time Block** | Morning, Afternoon, Evening and Night distribution |
| **Crimes by Week Day** | Which days see the most incidents |
| **Change in Crime Rate Over Years** | Year-over-year trend |
| **Arrested vs. Not Arrested** | Arrest rate across cases |
| **Domestic vs. Non-Domestic Cases** | Share of domestic-related incidents |
| **Severity Analysis** | Proportion of cases flagged as severe |
| **Community Areas Affected** | Count of distinct community areas with incidents |

### Interactive Controls
- **"Recent months back" parameter** – choose 3, 6, 12 or 18 months to view recent crime.
- **"Top" parameter** – choose the top 3, 5 or 10 crime types.
- **Dashboard filter actions** – click one chart to filter the others.

## 🧮 Key Calculated Fields

- **Time Block** – groups the hour of the crime into Morning (6–12), Afternoon (12–17), Evening (17–21) and Night.
- **Day of Week** – extracted from the crime date.
- **Percentage of Arrested** – arrests divided by total cases.
- **Domestic / Non-Domestic** and **Arrested / Not Arrested** – readable labels from boolean flags.
- **Is Severe** – flags a crime as severe or not severe.
- **Recent Crime / Total Recent Crime** – uses a `FIXED` LOD on the latest date to find crimes within the selected number of months.
- **Current Year** – compares each record's year with the latest year in the data.
- **Distinct Community Areas Affected** – `COUNTD([Community Area])`.

## 🗂️ Dataset

- **Source:** Chicago crime records (`Crime_data.xlsx`, extracted into a Tableau `.hyper` file)
- **Period:** 2017–2022
- **Key fields:** Case Number, Date, Primary Type, Description, Location Description, Arrest,
  Domestic, District, Ward, Community Area, Beat, Latitude/Longitude, Year, UCR

## 🛠️ Tools & Skills Used

- **Tableau Desktop** (version 18.1 workbook)
- Calculated fields, parameters and LOD expressions
- Pie charts, KPI cards, trend views and dashboard actions
- Data cleaning and feature engineering for time-based analysis

- ## 📁 Repository Structure

├── project_2.twbx # Packaged Tableau workbook (data included)
├── README.md # Project documentation
└── screenshots/ # Dashboard images (add yours here)


## 🚀 How to Use

1. Download `project_2.twbx`.
2. Open it in **Tableau Desktop** or **Tableau Public** (free).
3. Open **Dashboard 1** and use the parameters and filters to explore.

## 🔍 Key Insights
*(Fill in with your own findings, for example:)*
- Which crime type is the most frequent?
- Which time block and weekday record the most incidents?
- Whether crime is trending up or down across the years.
- What the overall arrest rate is.

## 👤 Author

**[Your Name]**
[LinkedIn] • [Tableau Public] • [Email]

⭐ If you found this project useful, please star the repository!
