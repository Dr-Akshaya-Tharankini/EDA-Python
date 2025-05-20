# No-Show Medical Appointments Analysis

This project analyzes **medical appointment no-shows** using a real-world dataset. The goal is to explore demographic and behavioral factors that influence whether a patient attends their scheduled medical appointment.

---

## Dataset Overview

The dataset contains **110,527 records** of patient appointments in Brazil, with features such as:

- **Demographics**: Gender, Age, Neighbourhood
- **Health Indicators**: Hypertension, Diabetes, Alcoholism, Handicap
- **Behavioral Flags**: SMS Received, Scholarship
- **Target Variable**: `No-show` (Yes/No)

---

## Key Questions Explored

- What patient factors are associated with missed appointments?
- Does age or gender influence no-show behavior?
- What role do chronic conditions (like diabetes or hypertension) play?
- Do SMS reminders or scheduling day impact attendance?

---

## Key Steps & Techniques

### 1. **Data Cleaning**
- Converted `ScheduledDay` and `AppointmentDay` to `datetime` objects
- Extracted `Weekday` from both date fields
- Handled incorrect age values (e.g., negative ages)
- Dropped unnecessary columns like `PatientID`, `AppointmentID`, and `Neighbourhood`

### 2. **Feature Engineering**
- Created **Age Groups** (1–21, 21–41, etc.)
- Created **weekday bins** for both scheduled and appointment days
- Converted categorical variables into dummy variables

### 3. **Exploratory Data Analysis (EDA)**
- Distribution of gender, SMS received, scholarship, and age group
- Comparison of health conditions with `NoShow` status
- Weekday-wise appointment behavior
- Correlation matrix to assess predictors of `NoShow`

### 4. **Visualization**
- Count plots segmented by `NoShow` across predictors
- Correlation bar chart and heatmap
- Log-scaled bivariate bar plots for categorical features

---

## Key Findings

- **SMS Reminder Effectiveness**: Surprisingly, patients who received SMS reminders were **less likely to show up (72%)** than those who didn’t (84%).
- **Age Influence**: Patients in the **41–61 age group** showed the highest appointment adherence.
- **Hypertension & Diabetes**: Patients with chronic conditions like hypertension and diabetes were more likely to attend their appointments.
- **Weekday Impact**: Very few appointments were scheduled for **Saturdays**, and **none for Sundays**.
- **Gender**: Female patients made more appointments overall, but no significant difference in no-show rate by gender.

--- 

## Author

**Dr. Akshaya Tharankini A**  
Healthcare Data & AI Specialist | SQL | Python | Power BI  
*Email: drakshayatharankini@gmail.com*  
*LinkedIn: https://www.linkedin.com/in/dr-akshaya-tharankini/*
