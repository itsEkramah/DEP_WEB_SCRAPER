#WEB_SCRAPER

## Objective
The primary objective of this project is to demonstrate a simple web scraping application that extracts book details (title, price, and availability) from the "Philosophy" category of the "Books to Scrape" website. The extracted data is then saved to a CSV file for further use or analysis.

## Purpose
This project serves as a practical example of how to:
- Use Python's `requests` library to make HTTP requests and retrieve web page content.
- Utilize `BeautifulSoup` for parsing HTML and extracting specific data from web pages.
- Save the extracted data into a structured CSV file for easy access and analysis.

## Working of the Code
1. **HTTP Request:** The script sends an HTTP GET request to the target URL (Philosophy category page) using the `requests` library, with headers to mimic a legitimate browser request.
  
2. **HTML Parsing:** The retrieved HTML content is parsed using `BeautifulSoup`, making it easier to navigate the HTML tree and find the necessary elements.

3. **Data Extraction:** The script identifies and extracts the following details for each book:
   - Title
   - Price
   - Availability
  
4. **Data Storage:** The extracted data is stored in a list of lists and then written to a CSV file named `books.csv`. The CSV file is saved in an `output` directory.

5. **Output:** The script prints a confirmation message indicating where the data has been saved.

## How to Use This Code

### Prerequisites
- Python 3.x
- Required Python packages: `requests`, `beautifulsoup4`

### Installation
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/itsEkramah/DEP_WEB_SCRAPER.git
   cd books-to-scrape
   ```

2. **Install Required Packages:**
   If you don't have the required packages installed, you can install them using:
   ```bash
   pip install -r requirements.txt
   ```
   Ensure you have a `requirements.txt` file listing `requests` and `beautifulsoup4`.

### Running the Script
To run the script and scrape the data, simply execute:
```bash
python scrape_books.py
```
This will create an `output` directory if it doesn't exist and save the scraped book data to `output/books.csv`.

### CSV File
- **Output Location:** The output CSV file is saved in the `output` directory with the name `books.csv`.
- **Contents:** The CSV file will contain the following columns:
  - Title
  - Price
  - Availability

### Important Notes
- **Ethical Scraping:** Ensure you are allowed to scrape the website and respect the website's `robots.txt` file. Be cautious not to overload the server with requests.
- **Error Handling:** The script is basic and does not include advanced error handling. Consider adding try-except blocks to handle potential errors, such as network issues or changes in the website structure.
- **Customization:** The script is currently set to scrape only the "Philosophy" category of that website. To scrape other categories, modify the `url` variable with the desired category URL.

---

Enjoy scraping!
