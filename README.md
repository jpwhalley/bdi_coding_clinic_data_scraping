# BDI Python Code Clinic - 29th April 2020

## Collecting disparate data online by web scraping using Selenium and BeautifulSoup in Python

Ideally the data we wish to work on can be downloaded in an easy to use format. Otherwise when we want only a small subset of a very big dataset, or the data is being constantly updated, hopefully the owner will provide an application programming interface (API) to automate the collection of the relevant data. However quite often the data cannot be downloaded and there is no API, but the data is publicly available, just dispersed across a website. When it would be too tedious and time consuming to navigate page by page to collect the data manually; we can use Selenium Webdriver and Beautiful Soup to automate navigating across the website and collecting of the relevant data. In this code clinic, I will go through the best practices (and what not to do!) when web scraping; using Selenium Webdriver to navigate around a website and then using Beautiful Soup to extract the data from the HTML.

### The following tools will be used in this code clinic:

+ Python3, I will be sharing a Python Notebook for everyone to work through with me.
 
+ Selenium: <https://selenium-python.readthedocs.io/> I usually use pip or conda to install packages:  
  
    pip install selenium
  
or  
  
    conda install -c anaconda selenium
  
+ Beautiful Soup: <https://www.crummy.com/software/BeautifulSoup/bs4/doc/>  
  
    pip install beautifulsoup4
  
or  
  
    conda install -c anaconda beautifulsoup4
  
+ Gecko drivers for my web browser <https://selenium-python.readthedocs.io/installation.html#drivers>  
You have to put the `geckodriver` binary in a path Python can see, if my case I have it in `~/⁨anaconda3⁩/bin⁩/`  
  
  
Once you have done that, hopefully running the following code snippet:  
  ````
from selenium import webdriver
browser = webdriver.Firefox() # Or which ever web browser you are using
browser.get("https://www.literaryclock.com/“)
````  

you should get a popup window (sorry!) of the Literary Clock website.
