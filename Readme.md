# Google Maps Scraper

A Python tool for extracting business information from Google Maps based on search criteria such as location and business type.

## Overview

This tool uses Selenium WebDriver to automate searches on Google Maps and extract relevant business information including:

- Business name
- Address
- Phone number
- Website
- Category
- Rating
- Number of reviews

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/AhmedOsamaMath/google-maps-scraper.git
   cd google-maps-scraper
   ```

2. Install required packages:
   ```
   pip install -r requirements.txt
   ```

3. Download ChromeDriver from [https://sites.google.com/chromium.org/driver](https://sites.google.com/chromium.org/driver) and ensure it's in your PATH or in the same directory as the script.

## Usage

Run the script from the command line:

```
python scraper.py
```

You will be prompted to enter:
1. The country to search in (e.g., United States)
2. The query type (e.g., companies, restaurants, hotels)
3. The maximum number of results to scrape (default is 15)

The script will then:
1. Open a Chrome browser window
2. Navigate to Google Maps
3. Perform the search
4. Extract information from each result
5. Save the data to a CSV file named `{country}_{query_type}.csv`

## Configuration

You can modify the following aspects of the scraper by editing the code:

- To run in headless mode (no visible browser), set `headless=True` when creating the `GoogleMapsScraper` instance in the `main()` function
- Adjust the wait time by modifying the `wait_time` parameter when initializing the scraper
- Change the maximum scroll attempts in the `_process_search_results` method

## CSV Output

The output CSV file will contain the following columns:
- name
- country
- address
- phone
- website
- category
- rating
- num_reviews

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for more details.
