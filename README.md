# Job Listings Web Scraper
https://roadmap.sh/projects/job-listings-scraper

This project demonstrates a small web-scraping workflow with Python, Requests, Beautiful Soup, and pandas. The notebook fetches the job listings from Real Python's [Fake Jobs](https://realpython.github.io/fake-jobs/) website, extracts selected fields, and exports the results to `job.csv`.

The source website contains intentionally fake data for learning and testing. The exported listings should not be treated as real job opportunities.

## Project Files

- `dataScrapper.ipynb`: Notebook containing the scraping and CSV-export workflow.
- `job.csv`: Generated dataset containing the scraped listings.

## Requirements

- Python 3
- Jupyter Notebook or VS Code with the Jupyter extension
- `requests`
- `beautifulsoup4`
- `pandas`

Install the Python packages with:

```bash
pip install requests beautifulsoup4 pandas
```

## How It Works

1. Sends an HTTP request to the Fake Jobs page with a browser-like User-Agent header.
2. Parses the returned HTML with Beautiful Soup.
3. Selects job titles, company names, locations, and job-detail URLs from the page.
4. Stores the values in a pandas DataFrame.
5. Writes the DataFrame to `job.csv` without adding an index column.

## Running the Notebook

1. Open `dataScrapper.ipynb` in Jupyter or VS Code.
2. Run the cells from top to bottom.
3. Check the resulting DataFrame in the notebook or open the refreshed `job.csv` file.

Running the export cell again replaces `job.csv` with the current results from the website. An internet connection is required, and changes to the source page's HTML structure may require updating the CSS selectors in the notebook.

## Output Columns

The generated CSV contains:

- `job title`
- `company name`
- `location`
- `Job detail page URL`