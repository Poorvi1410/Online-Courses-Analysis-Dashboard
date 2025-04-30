# Online Courses Analysis Dashboard


## Problem Statement

This dashboard provides an analysis of the online course landscape, drawing insights from a dataset covering various course offerings. It aims to help users understand trends in course categories, sub-categories, languages, skills taught, duration, viewership, and instructor ratings.

By visualizing this data, the dashboard allows potential learners, educators, or platform providers to identify popular course types, in-demand skills, prominent languages, and correlations between factors like duration, subtitle availability, and viewership, thereby facilitating informed decisions about course selection or offering strategies.

## Steps followed

-   **Step 1 : Load Data:** Loaded data into Power BI Desktop from the provided Excel file containing details about various online courses.
-   **Step 2 : Data Exploration & Cleaning (Power Query):** Opened Power Query Editor. Checked data integrity using view tab options ("column distribution", "column quality", "column profile"). Removed unwanted columns, changed data types where necessary, and handled null values appropriately.
-   **Step 3 : Data Profiling Scope:** Ensured column profiling was based on the entire dataset.
-   **Step 4 : Data Transformation (Power Query):**
    *   Added a new column to count the number of skills listed for each course.
    *   Added a new column to count the number of subtitle languages available for each course.
    *   Transformed the course `Duration` column (originally in approx. months) into a numeric column representing `Duration (Hours)`.
-   **Step 5 : Create Measures (DAX):** Developed various DAX measures to calculate aggregated values needed for visualizations (e.g., Total Viewers, Average Rating, Total Instructors, Counts of Languages/Subtitles).
-   **Step 6 : Theme Selection:** Selected a dark, space-themed background/theme for the report in the View tab.
-   **Step 7 : Add Slicers:** Added slicers for `Category` and `Sub-Category` to allow filtering of the dashboard.
-   **Step 8 : Create Dashboard Visuals:**
    *   Added KPI Cards for `Total no of Instructors`, `Total Languages`, `Total Subtitle Languages`.
    *   Added a Bar Chart showing `Courses as per Language and sub-category`.
    *   Added a Bar Chart showing `Course Type Popularity` (Course vs. Specialization).
    *   Added a Line Chart showing `Viewership on the Basis of learning duration (in hrs)`.
    *   Added a Line Chart showing `Number of Viewers as per Subtitle Count`.
    *   Added a Pie Chart showing `Most Prominent Languages` based on course count or viewership.
    *   Added a Bar Chart visualising `Instructors by Rating` distribution .
    *   Added a Bar Chart showing the count of `Total Subtitle Languages`.
    *   Added a Word Cloud visual displaying the frequency of `Demanding Skills`.
    *   Added a Table visual summarizing key metrics (Avg Rating, Avg Duration, Viewers, Course Count) by `Category`.
-   **Step 9 : Implement Drill-down:** Configured drill-down capabilities on the `Courses as per Language and sub-category` Bar Chart, allowing users to explore sub-courses within categories and languages, and see viewership for those specific combinations.
-   **Step 10 : Add Titles:** Added a text box for the main dashboard title "ONLINE COURSES ANALYSIS".


# Report Snapshot (Power BI Desktop)

![Image](https://github.com/user-attachments/assets/c0f47b23-f780-436e-9c95-d4161fad0fab)


# Insights

The dashboard reveals several insights into the online course landscape:

### [1] Course Landscape Overview
-   A wide variety of courses are available across categories like Data Science, Business, Computer Science, Health, Language Learning, etc.
-   Key metrics show a total of **988** instructors, **7** primary course languages, and **301** subtitle languages offered across the analyzed courses.

### [2] Popularity & Viewership
-   **Course Type:** Standalone 'Courses' (3.1K entries) are significantly more numerous than 'Specializations' (0.9K entries).
-   **Duration & Viewership:** The line chart indicates viewership peaks at certain course durations (e.g., sharp peaks around 25-30 hrs and 60+ hrs), suggesting popular standard course lengths.
-   **Subtitles & Viewership:** There appears to be a positive correlation initially between the number of subtitle languages offered and viewership, with viewership peaking when around 15-20 subtitle languages are available, before potentially declining.
-   **Language:** English is the overwhelmingly dominant primary language for courses.

### [3] Skills & Content Focus
-   **Demanding Skills:** The word cloud highlights skills like "Data Science", "Machine Learning", "Python", "Data Analysis", "Cloud Computing", "Big Data", "SQL", and "Business Analysis" as highly prevalent in course descriptions.
-   **Category Performance:** The table shows variations across categories; for instance, 'Information Technology' has a high average rating (4.0) and viewership (7513), while 'Health' has fewer courses but comparable average duration.

### [4] Interactivity Benefits
-   **Filtering:** Slicers allow users to narrow down the analysis to specific categories (e.g., Data Science) and sub-categories (e.g., Python Programming) of interest.
-   **Drill-down:** Enables users to explore the specific sub-courses offered within broader categories and languages, along with their respective viewership numbers, directly from the main bar chart.

These insights can guide learners towards popular and relevant courses, and help content creators or platforms identify high-demand skill areas, optimal course formats, and language/subtitle strategies to maximize reach.
