# Netflix Data Analysis
![Description of Image](https://github.com/th-ayyush/SQL/blob/c79682f5182d32b1d3de2a8d348a215882f650fc/logo.png)


This project focuses on analyzing Netflix metadata using SQL and CSV data. It includes:

- A CSV file containing Netflix titles metadata.
- An SQL script with table creation and analysis queries.

## Files

### 1. `netflix_titles.csv`
This file contains metadata about Netflix shows and movies.

#### Summary:
- **Total Rows**: 8,807
- **Columns**:
  - `show_id` (string): Unique identifier for each title.
  - `type` (string): Specifies whether the title is a Movie or TV Show.
  - `title` (string): Name of the title.
  - `director` (string): Director of the title.
  - `cast` (string): Main cast members.
  - `country` (string): Country of origin.
  - `date_added` (string): Date the title was added to Netflix.
  - `release_year` (integer): Year of release.
  - `rating` (string): Content rating (e.g., PG, R).
  - `duration` (string): Duration of the title (e.g., 90 min or 2 seasons).
  - `listed_in` (string): Genres/categories the title falls into.
  - `description` (string): Brief summary of the title.

### 2. `netflix_SQL_Analysis.sql`
This SQL script provides the structure and queries for analyzing the Netflix dataset.

#### Key Sections:
1. **Table Creation**: Creates a table named `netflix` with appropriate data types for each column.
2. **Basic Queries**:
   - Retrieves all data from the `netflix` table.
   - Counts the total number of entries.
   - Lists distinct types of content (Movies and TV Shows).
3. **Analysis Problems**:
   - A total of **15 business problems** have been solved using SQL queries, including:
     - Counting the number of Movies vs. TV Shows.
     - Identifying the most common genres.
     - Analyzing the distribution of content by country.
     - Exploring temporal trends in content additions.

## Usage

### Prerequisites
- A relational database system (e.g., MySQL, PostgreSQL).
- Python (optional for preprocessing or additional analysis).

### Steps
1. **Load the CSV Data**:
   - Use the CSV file to populate the `netflix` table in your database.
   - Tools like SQL Server Management Studio, MySQL Workbench, or Python can help with importing the data.
2. **Run SQL Queries**:
   - Execute the queries in `netflix_SQL_Analysis.sql` to explore and analyze the dataset.

### Example Queries
- Count the number of Movies vs. TV Shows:
  ```sql
  SELECT type, COUNT(*) as count
  FROM netflix
  GROUP BY type;
  ```
- Find the most common genres:
  ```sql
  SELECT listed_in, COUNT(*) as count
  FROM netflix
  GROUP BY listed_in
  ORDER BY count DESC;
  ```

## Potential Applications
- Content distribution analysis.
- Insights into popular genres, countries, or ratings.
- Temporal analysis of content additions.

## Acknowledgments
This dataset was sourced from Netflix and analyzed for educational and research purposes.

