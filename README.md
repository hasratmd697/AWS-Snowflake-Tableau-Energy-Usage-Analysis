# AWS + Snowflake + Tableau Project

## Project Overview
This project showcases the full workflow of cloud data management and visualization using **Amazon S3**, **Snowflake Data Warehouse**, and **Tableau**.  
It involves data ingestion, transformation, and the creation of interactive dashboards to analyze energy usage and cost savings by various dimensions.


## Steps and Workflow

### 1. Amazon S3 Setup
- Created an **Amazon S3 bucket** to store raw energy usage data.
- Uploaded data files into the S3 bucket.

### 2. IAM Role Creation
- Created a new IAM Role named **`tableau.role`**.
- Granted **AmazonS3FullAccess** permission to the role.
- Updated the trust relationship to integrate securely with Snowflake.

### 3. Snowflake Data Warehouse Setup
- Created an **Integration Object** in Snowflake to establish connection with Amazon S3.
- Updated the trust policy to enable secure access.
- Loaded the raw data from the S3 bucket into **Snowflake tables**.

### 4. Data Transformation in Snowflake
- Performed **SQL-based transformations**:
  - Updated **Monthly Usage (kWh)**:
    - Increased by **10%** for **Low Income** level.
    - Increased by **20%** for **Medium Income** level.
    - Increased by **30%** for **High Income** level.
  - Updated **Cost Saving (USD)**:
    - Decreased by **10%** for **Low Income** level.
    - Decreased by **20%** for **Medium Income** level.
    - Decreased by **30%** for **High Income** level.

### 5. Data Visualization with Tableau
- Imported the transformed data into Tableau using the **Snowflake Connector**.
- Built several visualizations for energy usage and cost savings:

  #### Visualizations Created:
  - **Bar Chart** for **kWh by Country**
  - **Bar Chart** for **Cost Saving (USD) by Country**
  - **Bar Chart** for **kWh by Region**
  - **Bar Chart** for **kWh by Energy Source**
  - **Bar Chart** for **Cost Saving (USD) by Energy Source**
  - **Bar Chart** for **Cost Saving (USD) by Region**

### 6. Dashboard and Publishing
- Assembled all visualizations into a single **Energy Usage Analysis Dashboard**.
- Published the final dashboard to **Tableau Cloud** for online access and sharing.


## Tech Stack

- **Cloud Storage**: Amazon S3
- **Data Warehouse**: Snowflake
- **Cloud IAM & Security**: AWS IAM
- **Data Visualization**: Tableau + Tableau Cloud


## Project Structure

aws-snowflake-tableau-project/
│
├── data/                  # Amazon S3 bucket data files
├── sql/                   # Snowflake SQL scripts for transformations
├── tableau/               # Tableau workbook (.twb/.twbx) files
├── documentation/         # IAM role setup, Snowflake integration configs
├── README.md              # Project documentation


## Future Enhancements
- Set up automated data refresh between S3, Snowflake, and Tableau.
- Add predictive modeling (e.g., future cost-saving projections) inside Tableau.
- Integrate with Snowflake Streams & Tasks for near real-time update

## Screenshot

![Screenshot 2025-04-28 125032](https://github.com/user-attachments/assets/e60ce6f6-2995-44fc-8193-8cb92a55932c)

## 🚀 How to Access
- The dashboard is available on Tableau Cloud.(https://prod-apsoutheast-b.online.tableau.com/t/hasratmd697-e30a26bb8b/views/Book2/TableauDashboard)
