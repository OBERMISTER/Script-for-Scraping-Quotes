# Script-for-Scraping-Quotes
Python Script for Scraping Quotes from a Website
import requests
from bs4 import BeautifulSoup

url = 'https://quotes.example.com'
response = requests.get(url)
soup = BeautifulSoup(response.text, 'html.parser')

for quote in soup.find_all('blockquote'):
    print(quote.get_text())
