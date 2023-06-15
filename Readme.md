# Web Scraping with Autoscraper

This app was designed to make web scraping automatic and simple. It receives a URL or the HTML code of a web page along with a list of sample data that we wish to scrape from that website. This information may take the form of text, a link, or any value for an HTML tag on the page. It picks up the scraping guidelines and returns similar components. Then you may utilize the newly acquired object along with the new URLs to access the same or substantially the same content on the new sites. In this project I have used packages like autoscraper

## Installation

For this project we have to install Autoscraper using pip:

$ pip install Autoscraper

## How to Use

In this project we will do scraping on www.Amazon.in for Iphone.First we have to create a variable of Url.Then we have to create list of the data which we want for example:- "price", "Name", "size","Reviews". etc after the we have to scrape the data with the help of AutoScraper than we have to save the result in a variable then print the result 👍

'''url = "https://www.amazon.in/s?k=Iphones"
scraping_list =[ "1,19,999","Apple iPhone 14 Pro (128 GB) - Silver","491"]
scraper = AutoScraper()
result = scraper.build(url,scraping_list)
print(result) '''

Then to get similer result user "get_result_similer" and group it 👍

'''scraper.get_result_similar(url,grouped=True)'''

Take the Aliases information into keyword format and keep rules then save so that we can use this rule for any products on Amazon example

'''results=scraper.get_result_similar('https://www.amazon.in/s?k=samsung+mobile+above+20000',group_by_alias=True)
results['Price']'''

NOTE:- There will be a change in group Names.
