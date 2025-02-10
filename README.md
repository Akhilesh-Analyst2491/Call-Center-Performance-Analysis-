# Call Center Performance Analysis - Power BI 


## Project Overview
This project analyzes call center performance using Power BI. The dataset consists of call records from 2021, including details on agents, call topics, response times, resolutions, and customer satisfaction ratings. The goal is to generate meaningful insights and visualizations to improve operational efficiency and customer service.

## Dataset
The dataset consists of the following columns:
- **CALLER ID**: Unique identification number of each caller
- **AGENT**: Names of call center agents
- **DATE**: Date on which the call was received
- **TIME**: Time of the call (hh:mm:ss format)
- **TOPIC**: Subject of the call
- **ANSWERED**: Whether the call was answered or abandoned (Y/N)
- **RESOLVED**: Whether the issue was resolved (Y/N)
- **SPEED OF ANSWER IN SECOND**: Time taken to answer the call
- **AVG. TALK DURATION**: Average talk duration per call
- **SATISFACTION RATE**: Customer rating of agent performance

## Data Preprocessing
Before analysis, the following preprocessing steps were performed:
1. Replaced all null/blank values with 0.
2. Changed data types where necessary.
3. Extracted seconds and minutes from `AVG. TALK DURATION` and created a new column **Duration on Calls**.

## KPIs and Analysis
The analysis focuses on the following KPIs to assess call center performance:
- **Total number of calls**
- **Total answered and rejected calls**
- **Percentage of answered and rejected calls**
- **Total resolved and unresolved calls**
- **Top agent who answered the most calls**
- **Top agent with the highest satisfaction rate**
- **Total number of calls by topic**
- **Call duration by agent**
- **Total calls by days and months for 2021**
- **Overall 2021 performance rating**

## Visualizations
The following visualizations have been created:
- **Bar Chart**: Total number of calls by topic
- **Line Chart**: Calls by days and months in 2021
- **Slicers**: Interactive filtering by month and day
- **Custom Chart**: Overall performance satisfaction rating

## DAX Queries Used
Below are some of the key **DAX** queries used in this project:
```DAX
Total Calls = COUNT(Call_Center[CALLER ID])

Answered Calls = CALCULATE(COUNT(Call_Center[CALLER ID]), Call_Center[ANSWERED] = "Y")

Rejected Calls = CALCULATE(COUNT(Call_Center[CALLER ID]), Call_Center[ANSWERED] = "N")

Resolved Calls = CALCULATE(COUNT(Call_Center[CALLER ID]), Call_Center[RESOLVED] = "Y")

Unresolved Calls = CALCULATE(COUNT(Call_Center[CALLER ID]), Call_Center[RESOLVED] = "N")

Satisfaction Rate = AVERAGE(Call_Center[SATISFACTION RATE])
```

## Screenshots
Here are some screenshots of the Power BI Dashboard:

### Overview Dashboard
![Overview Dashboard](screenshots/overview_dashboard.png)

### Calls by Topic
![Calls by Topic](screenshots/calls_by_topic.png)

### Agent Performance
![Agent Performance](screenshots/agent_performance.png)

## Power BI Dashboard Link
You can access the Power BI dashboard using the following link:
[Power BI Dashboard]()

## Tools Used
- **Power BI** for data visualization and dashboard creation
- **Excel** for initial data cleaning and formatting

## Files in Repository
- **Call-Center-Dataset.xlsx**: The raw dataset
- **Call Centre Performance.pbix**: The Power BI report file
- **Analyzation (CALL CENTRE).docx**: The analysis document detailing KPIs and approach
- **README.md**: Project documentation (this file)
- **screenshots/**: Folder containing dashboard screenshots

## Conclusion
This project provides an interactive analysis of call center operations, helping identify areas for improvement. Further refinements can be made by integrating real-time data and advanced analytics.

## Future Enhancements
- Implementing predictive analytics for customer satisfaction trends
- Analyzing call center performance across multiple years
- Adding AI-powered insights for sentiment analysis



