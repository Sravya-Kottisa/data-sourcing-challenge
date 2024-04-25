# NYT and TMDB API Data Collection and Merge

## Project Overview

This project demonstrates a comprehensive data collection and merging process by leveraging the New York Times Article Search API and The Movie Database API. The goal is to retrieve movie reviews from the New York Times and corresponding movie details from The Movie Database, merge the data, and export it to a CSV file for future analysis.

### Part 1: New York Times API Data Collection
-  **Filtering and Sorting:**   Retrieves movie reviews with "love" in the headline, sorts results by newest, and selects specific fields to return.
- **Pagination and Error Handling:** Loops through 20 pages of results (starting from page 0), extends the query_url to include the page parameter, and implements a try-except clause to handle errors.
- **Rate Limiting:** Adds a 12-second interval between queries to stay within the New York Times API's rate limits.

### Part 2: The Movie Database API Data Collection
- **Search and Retrieval:** Searches for movies by title, extracts the movie ID, and retrieves full movie details using the movie ID.
- **Data Extraction:** Extracts genre names, spoken languages, and production countries from the movie details.
- **Data Storage:** Creates a dictionary with the results and appends it to a list.

### Part 3: Data Merging and Export
- **Dataframe Creation:** Converts the New York Times reviews and TMDB data into separate DataFrames.

- **Merging:** Merges the two DataFrames on the title column.

- **Data Cleaning:** Fixes the genres, spoken_languages, and production_countries columns by converting them to strings and removing list characters.

- **Export:** Deletes duplicate rows, resets the index, and exports the merged data to a CSV file without the DataFrame's index.

### Additional Considerations
- **API Keys:** Ensure environment variables are set up properly, and API keys are correctly referenced.
- **Debugging:** Use print statements to debug and verify data collection and merging processes.
- **Version Control:** Regularly commit and push changes to GitHub or GitLab to maintain a record of progress and collaborate with others.
  
### Repository Structure
- README.md (this file)
- .env (API keys)(Not checked in to repository)
- retrieve_movie_data.ipynb (Python script)
- output.csv (exported data)

This project showcases a thorough data collection and merging process, demonstrating the ability to work with multiple APIs, handle errors, and clean data for analysis.
