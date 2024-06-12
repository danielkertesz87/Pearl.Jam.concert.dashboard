# Pearl Jam Concert Setlist Scraper

This repository contains a Python script that scrapes Pearl Jam concert setlists from the Setlist.fm website. The script extracts details such as the date, location, tour name, and songs played during each concert and saves the data into an Excel file.

## Features

- **Web Scraping**: Utilizes the requests library to fetch web pages and BeautifulSoup for parsing HTML content.
- **Date Formatting**: Converts date elements from the web page into a standard YYYY-MM-DD format.
- **Location Extraction**: Extracts the venue/location of each concert.
- **Tour Name Extraction**: Identifies and extracts the tour name associated with each concert.
- **Song Extraction**: Retrieves the list of songs played during the concert, organized by setlist parts (Main, Encore, Encore2).
- **Data Storage**: Stores the extracted data into a Pandas DataFrame and exports it to an Excel file.

## Script Overview

1. **Dictionary for Month Conversion**: A dictionary to convert month abbreviations to numeric format.
2. **Function `get_soup(url)`**: Fetches and parses the HTML content of the given URL.
3. **Function `extract_date(soup)`**: Extracts and formats the concert date.
4. **Function `extract_location(soup)`**: Extracts the location (venue) of the concert.
5. **Function `extract_tour_name(soup)`**: Extracts the name of the tour.
6. **Function `extract_songs(soup)`**: Extracts the list of songs played during the concert.
7. **Function `scrape_setlists(base_url)`**: Main function to iterate through multiple pages of setlists, extract relevant information, and compile it into a list of dictionaries.
8. **Data Storage**: Converts the data into a Pandas DataFrame and saves it as an Excel file.

## Usage

1. **Install Dependencies**: Ensure you have `requests`, `beautifulsoup4`, and `pandas` installed. You can install them using:
   ```sh
   pip install requests beautifulsoup4 pandas
2. **Run The Script**: Ensure you have `beautifulsoup4`, and `pandas` installed. The script was written in Jupiter Notebook.
3. **Output**: The scraped data will be saved into an Excel file named setlist.xlsx.
  
