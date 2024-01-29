# Class 17

## Scraping

Web scraping, web harvesting, or web data extraction is data scraping used for extracting data from websites. Web scraping software may directly access the World Wide Web using the Hypertext Transfer Protocol or a web browser. While web scraping can be done manually by a software user, the term typically refers to automated processes implemented using a bot or web crawler. It is a form of copying in which specific data is gathered and copied from the web, typically into a central local database or spreadsheet, for later retrieval or analysis.

### Static and Dynamic

In static webpages, all requested content is received on page load. Dynamic pages are able to update or load content after the inital load.

Due to this fact, scraping from dynamic webpages rquire a few more steps. That being said, the steps involve simply using some third-party tools like Selenium, Pyppeteer, or Playwright.

### Webcrawling 101

Scraping websites follows a certain etiquette that should be respected in order to make everyone happy.

1. Follow the rules a website gives on its robots.txt
2. Mimic human behavior as much as possible. Crawl slower, crawl randomly, etc.
3. Avoid suspicion. Rotate IP addresses, avoid traps, use headless browsers.

### Xpath

Addresses that you can use to locate any element or group of elements in an HTML page.

```
# Example xpath for targetting an input attribute with id='username'
//input[@id='username']
```

### Playwright

A test framework that allows developers to automate web browsers. Tasks like logging in, opening a specific product's buy page on Amazon, etc.

```
# Opening browser, page, and then going to a specific URL
with sync_playwright() as p:
  browser = p.chromium.launch(headless=False, slow_mo=3*1000)
  page = broswer.new_page()
  
  page.gogo(URL)
```

## Things I want to know more about