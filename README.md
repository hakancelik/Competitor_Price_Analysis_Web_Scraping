# Web Scraping for Competitor and Price Analysis

This project is designed to scrape and analyze data for books in the **Travel** and **Nonfiction** categories from **books.toscrape.com**. Using **Selenium** and **BeautifulSoup**, the project extracts details about books, including prices and star ratings, and performs various analyses.

## Table of Contents

1. [Project Objective](#project-objective)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Code Explanation](#code-explanation)
5. [Visualization](#visualization)
6. [Authors](#authors)
7. [License](#license)

## Project Objective

The goal of this project is to scrape data for books in the **Travel** and **Nonfiction** categories, and to analyze the prices and star ratings. The obtained data will be used to create various charts and perform analysis.

## Installation

To run the project, you'll need to install the required libraries. Use the following commands to install the necessary packages:

```bash
pip install selenium beautifulsoup4 pandas matplotlib seaborn
```
Additionally, you need to download ChromeDriver and place it in a suitable location on your computer. Update the executable_path in the setup_driver function with the path to your ChromeDriver executable.

## Usage

### Start and Configure the Browser
Launch the browser and configure the necessary settings.

### Inspect the Homepage and Extract Category Links
Open the homepage and extract the links for the "Travel" and "Nonfiction" categories.

### Inspect the Category Page and Extract Book Links
On each category page, extract the links to the book detail pages. Manage pagination to gather all book links.

### Inspect the Product Detail Page and Extract Data
For each book detail page, extract the book title, price, star rating, description, and product information.

### Analyze and Visualize the Data
Convert the extracted data into a pandas DataFrame and analyze it with various charts.

### Close the Browser
After completing all tasks, close the browser and free up resources.

## Code Explanation
The project includes the following key functions:

- `setup_driver(): Configures and starts the browser.
- `get_category_urls(driver): Extracts the URLs for category pages.
- `get_book_urls(driver, category_url, max_pagination=3): Extracts the URLs for book detail pages from a category page.
- `get_book_details(driver, book_url): Scrapes details from a book's detail page.
- `scrape_books(driver): Scrapes all books and collects data.
- `visualize_data(df): Analyzes and visualizes the collected data.

## Visualization
The project produces the following visualizations:

- **Book Prices vs. Star Ratings: Shows the relationship between book prices and star ratings.
- **Price Distribution: Displays the distribution of prices across categories.
- **Star Rating Distribution: Illustrates the distribution of star ratings.
- **Authors
Hakan Çelik - Project Manager and Developer
## License
This project is licensed under the MIT License. See the LICENSE file for details.
