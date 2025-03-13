# AI Web Scraper Using Crawl4AI  

## Use Cases  
- **AI Data Enrichment** – Enhance and categorize scraped data using LLMs for better insights.  
- **Research & Analysis** – Extract structured data for business or academic studies.  
- **Lead Generation** – Collect business emails, phone numbers, and addresses for outreach.  
- **Market Research** – Gather industry data to analyze trends and customer behavior.  
- **Competitor Analysis** – Track pricing, services, and reviews to maintain a competitive edge.  


## Project Structure  

```
.
├── main.py            # Main script to run the scraper
├── config.py          # Configuration settings (LLM models, base URL, CSS selectors, etc.)
├── models
│   └── business.py    # Defines the Local Business data model using Pydantic
├── src
│   ├── utils.py       # Helper functions for processing and saving data
│   └── scraper.py     # Functions to configure and execute the scraper
└── requirements.txt   # List of required Python packages
```

## How to Run  

### Prerequisites  

Ensure you have the following installed:  

- Python 3.11+  
- LLM provider API key (OpenAI, Gemini, Claude, etc.)  
- Required Python libraries (`requirements.txt`)  

### Setup  

#### Clone the Repository  
```bash
git clone https://github.com/kaymen99/llm-web-scraper
cd llm-web-scraper
```

#### Create and Activate a Virtual Environment  
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

#### Install Required Packages  
```bash
pip install -r requirements.txt
playwright install
```

#### Configure Environment Variables  

Create a `.env` file in the root directory and add your credentials:  

```ini
# API keys for LLM providers
OPENAI_API_KEY=""            
GEMINI_API_KEY=""            
GROQ_API_KEY=""              
```

## Running the Scraper  

Run the following command to start the scraper:  

```bash
python main.py
```

This will extract data from the specified website, page by page, and save the results in a `businesses_data.csv` file. After scraping, the script will display statistics on LLM usage.  

## Configuration  

Modify the `config.py` file to customize the scraper's behavior:  

- **LLM_MODEL**: AI model used for data extraction (`gpt-4o`, `claude`, `deepseek-chat`, `gemini-2.0-flash`).  
- **BASE_URL**: Website URL to scrape (default: dentists in Toronto on Yellow Pages).  
- **CSS_SELECTOR**: HTML selector to extract business details.  
- **MAX_PAGES**: Number of pages to scrape (default: `3`).  
- **SCRAPER_INSTRUCTIONS**: Custom LLM prompt defining the data extraction rules.  



## Key Features  

- **Business Data Extraction** – Scrape business names, contact details, and other relevant information.  
- **AI-Powered Data Processing** – Utilize LLMs to clean, structure, and enhance extracted data.  
- **Customizable Scraper** – Modify it to work with different websites and data types.  
- **Flexible LLM Integration** – Supports AI models like GPT-4, Claude, and DeepSeek.  
 

