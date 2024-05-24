# Navigating-the-Data-Science-Job-Landscape
## Web Scraping by Selenium

## Data Science Jobs Scraping Summary:

    - Scraped job information, including Job Title, Company Name, Experience, Location, Salary, and Skills.
    - Established a DataFrame to organize and store the collected data.
    - Visualized the number of jobs per company using a Bar Chart, Distribution of Experience,
      Distribution of Job Title, Top 10 Skills in Demand and Distribution of Joblistings across Locations.

    Technical Documentation:

    1. Dependencies:
        - Pandas
        - Matplotlib
        - Seaborn

    2. User-defined Functions:
        - create_dataframe(titles, companies, experiences, locations, salaries, skills):
          Takes lists of job-related information and returns a DataFrame.

        - visualize_data(df):
          Plots a bar chart of the number of jobs per company using Matplotlib.

    3. Visualization Functions:
        - visualize_data(df):
          Bar chart showing the number of jobs per company.

        - plt.figure(figsize=(10, 8))
          sns.histplot(df['Experience'], bins=20, color='green', kde=True)
          Histogram showing the distribution of experience.

        - plt.figure(figsize=(12, 10))
          sns.countplot(y='Job Title', data=df, order=df['Job Title'].value_counts().index, palette='viridis')
          Count plot showing the distribution of job titles.

        - plt.figure(figsize=(12, 8)
          sns.barplot(x=top_skills.values, y=top_skills.index)
          Horizontal Bar Chart showing top 10 demanding skills for Data-Science jobs.

        - plt.figure(figsize=(12, 10))
          sns.countplot(y='Location', data=df, order=df['Location'].value_counts().index, palette='viridis')
          Countplot showing the number of jobs across locations.

    4. How to Use:
        - Call create_dataframe() with the lists of job-related information.
        - Call visualize_data() with the created DataFrame for data visualization.
