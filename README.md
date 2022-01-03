# Mission-to-Mars

## Overview
My goal for this project is to dynamically scrape information from multiple websites and input that information onto my own site. To do this, I used Splinter to automate browser clicks to obtain the specific elements I wanted, BeautifulSoup to parse through HTML elements to find desired objects (images, index tags, etc.), MongoDB to store article titles and image URLs,  and Flask to host the website with all of the scraped information.

## Scraping file

**scrape_all function:** this function creates a browser instance and retreives all the data using all of the scraping functions I wrote.

![](https://github.com/mooshak21/Mission-to-Mars/blob/main/Resources/scrape_all.png)

**mars_news function:** this function visits the mars NASA news site and uses Splinter to navigate through the HTML elements to find the news title and paragraph. This will get the most up to date title and paragraph. 

![](https://github.com/mooshak21/Mission-to-Mars/blob/main/Resources/mars_news.png)

**featured_image function:** the goal of this function is to retrieve the featured image from the website URL listed. This will simply Splinter through to find the image that we know will be on the main page and then save the URL of that image.

![](https://github.com/mooshak21/Mission-to-Mars/blob/main/Resources/featured_image.png)

**mars_facts function:** this function goes to another part of the Mars website to get different facts about Earth and Mars. Our goal here is to manipulate the data into a Dataframe after retrieving it using Splinter. Once we do that, we convert that table to HTML to later display on our site. 

![](https://github.com/mooshak21/Mission-to-Mars/blob/main/Resources/mars_facts.png)

**scrape_mars function:** the goal of this function is to retrieve 4 images and their names. We are doing this in a fashion that doesn't hard-code the results, but rather will dynamically retrieve the most recent titles and images from the site because we are looking for the first 4 'img' tags rather than hard-coding the URLs in the 'img' tag. 

![](https://github.com/mooshak21/Mission-to-Mars/blob/main/Resources/scrape_mars.png)
