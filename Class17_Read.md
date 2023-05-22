### What are the key differences between scraping static and dynamic websites?

1. JavaScript Execution: Dynamic websites heavily rely on JavaScript to manipulate the DOM and fetch data. Scraping dynamic websites may require using tools that can execute JavaScript, such as headless browsers (e.g., Puppeteer, Selenium) or browser automation frameworks (e.g., Playwright), to render the page and access the fully generated content.

2. Complexity: Dynamic websites tend to be more complex to scrape compared to static websites due to their reliance on JavaScript, asynchronous requests, and dynamic content generation. Extracting data from dynamic websites often involves interacting with the page, waiting for content to load, handling AJAX requests, and parsing the updated DOM.

3. Maintenance: Static websites generally require less maintenance for scrapers since the structure and content of the pages remain constant over time. Dynamic websites may undergo frequent changes to their HTML structure, APIs, or JavaScript code, necessitating regular updates to the scraping process to adapt to these modifications.

### Explain at least three techniques or best practices that can be employed to avoid getting blocked while scraping websites.

1. Respect Robots.txt :
   
    Web spiders should ideally follow the robot.txt file for a website while scraping. It has specific rules for good behavior, such as how frequently you can scrape, which pages allow scraping, and which ones you can’t. Some websites allow Google to scrape their websites, by not allowing any other websites to scrape. This goes against the open nature of the Internet and may not seem fair, but the owners of the website are within their rights to resort to such behavior. 

2. Make the crawling slower, do not slam the server, treat websites nicely


    Web scraping bots fetch data very fast, but it is easy for a site to detect your scraper, as humans cannot browse that fast. The faster you crawl, the worse it is for everyone. If a website gets too many requests than it can handle it might become unresponsive.

    Make your spider look real, by mimicking human actions. Put some random programmatic sleep calls in between requests, add some delays after crawling a small number of pages and choose the lowest number of concurrent requests possible. Ideally, put a delay of 10-20 seconds between clicks and not put much load on the website, treating the website nice.

3. Do not follow the same crawling pattern
   
    Humans generally will not perform repetitive tasks as they browse through a site with random actions. Web scraping bots tend to have the same crawling pattern because they are programmed that way unless specified. Sites that have intelligent anti-crawling mechanisms can easily detect spiders by finding patterns in their actions and can lead to web scraping getting blocked.

    Incorporate some random clicks on the page, mouse movements and random actions that will make a spider look like a human.


### What is Playwright, and how does it assist in web scraping tasks? Provide an example of a use case where Playwright would be particularly beneficial.

**What ?**

Playwright is an open-source browser automation framework developed by Microsoft. It provides a high-level API that allows developers to automate web interactions and perform tasks programmatically in various browsers, including Chromium, Firefox, and WebKit.

**How ?**
1. Browser Compatibility: Playwright supports multiple browser engines, enabling scraping across different browser environments. This versatility allows you to choose the most suitable browser for your scraping needs and ensures compatibility with a wide range of websites.

2. JavaScript Execution: Playwright can execute JavaScript code within the browser, making it effective for scraping dynamic websites that heavily rely on client-side rendering and AJAX requests. It can wait for elements to appear, interact with the page, and extract data after JavaScript has modified the DOM.

3. Headless and Headful Modes: Playwright offers both headless and headful modes. In headless mode, the browser runs in the background without a visible user interface, making it suitable for efficient and automated scraping. In headful mode, the browser's UI is visible, allowing you to observe and debug the scraping process interactively.

**Example:**

Imagine you want to scrape a Twitter website to monitor the content of a specific type of tweet. The website may have dynamic elements, require login credentials, and use JavaScript to load additional information.

### Describe the purpose of using Xpath in web scraping, and provide an example of an Xpath expression to select a specific HTML element from a webpage.

**Purpose:**

XPath stands for XML Path. It is W3C recommended technique used to identify and navigate nodes in an XML document. In automation, we use XPath to find elements on a webpage. Like any other language, Playwright supports XPath Selector and all its techniques and functions.

**Example:**
```
await page.locator("xpath=/html//button/i[contains(@class,'fa-search')]").click()

```