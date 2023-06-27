
Here I would like to write the things I find very helpful for extracting data based on web pages: 
Web scraping is often necessary for several reasons:



## Beautiful Soup
Beautiful Soup is a Python library used for web scraping and parsing HTML or XML documents. It provides convenient methods and functionality to extract data from web pages by navigating the HTML structure and locating specific elements based on tags, attributes, or CSS selectors.

With Beautiful Soup, you can parse HTML or XML content and extract the desired information, such as text, links, tables, or specific elements, from the structured document. It handles poorly formatted markup and provides a consistent interface for accessing and manipulating the data.

### import requests
The import requests statement is used in Python to import the requests library, which is a popular HTTP library for making requests to web servers and handling their responses. The requests library simplifies the process of sending HTTP requests and provides an easy-to-use interface for interacting with web services, APIs, and websites.

## example
import requests
    from bs4 import BeautifulSoup
    import re

    url = "yourURL.com"

    response = requests.get(url)
    html_content = response.text

    soup = BeautifulSoup(html_content, "html.parser")
    file_names = []
    pattern = r"\d{2}\.\d{2}\.\d{2}_\d{2}"

    for link in soup.find_all("a"):
        match = re.search(pattern, link.get("href"))
        if match:
            file_names.append(match.group())

    num_items = len(file_names)

    print("Number of items:", num_items)
    for file_name in file_names:
        print(file_name) 
