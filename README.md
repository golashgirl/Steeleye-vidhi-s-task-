# Steeleye-vidhi-task

Here summary of the code explained in points:

1. **Imports:** The code imports necessary modules including `requests` for making HTTP requests, `csv` for handling CSV files, and `logging` for logging messages.
  
2. **Logging Configuration:** It configures logging to log messages at the INFO level, allowing INFO level messages and higher to be captured and logged.

3. **Fetching Data:** The `fetch_data` function is defined to fetch JSON data from a given URL using the `requests.get()` method. It handles exceptions if the request fails and logs appropriate error messages.

4. **Get Country Name:** The `get_country_name` function retrieves the country name from a given country code by iterating through a list of countries data and matching the code.

5. **Processing Laureates Data:** The `process_laureates_data` function processes laureates data, extracting required information such as ID, name, date of birth, unique prize years, unique prize categories, gender, and country name for each laureate. It utilizes the `get_country_name` function to get the country name.

6. **Writing to CSV:** The `write_to_csv` function writes the processed data to a CSV file. It opens the file for writing, initializes a `csv.DictWriter` object with fieldnames, writes the header, and iterates through the data, writing each row to the CSV file. It logs success or failure messages accordingly.

7. **Main Function:** The `main` function specifies URLs for laureates and countries data, fetches the data, processes it, and writes to a CSV file if both data fetches are successful. It logs an error message if any data fetch fails. Finally, it calls the `main` function when the script is executed directly.
