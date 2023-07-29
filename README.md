# Web scraping

This project gets information from the website:
https://books.toscrape.com/

## Description

The code runs into each book URL and gets the following data:
1. book_item['url']
2. book_item['title'] 
3. book_item['upc'] 
4. book_item['product_type'] 
5. book_item['price_excl_tax']
6. book_item['price_incl_tax']
7. book_item['tax']
8. book_item['availability']
9. book_item['num_reviews']
10. book_item['stars']
11. book_item['category']
12. book_item['description']
13. book_item['price']

The file **pipelines.py** cleans and transforms the data (string to numbers), making it easier to manipulate the numbers later.

The output is the **booksdata.json** file inside the *bookstoscrape* folder.

In order to orchestrate the data extraction, this code can also be scheduled in an online server like [Digital Ocean](https://cloud.digitalocean.com/).
You just need to configure the libraries **scrapyd** and **scrapydweb** to work properly.

## Getting Started

### Dependencies

* Python 3.11.3
* Scrapy 2.9.0

### Installing

You must run the code below in the root folder where the repository was cloned.
```
pip install virtualenv
virtualenv venv
```
If you're using Linux/Mac: 
```
source venv/bin/activate
```
If you're using Windows:
```
venv\Scripts\activate.bat
```
Last command to install scrapy:
```
pip install scrapy
```
### Executing program

* How to run the program
```
scrapy crawl books
```

## License

This project is licensed under the MIT License - see the LICENSE file for details
