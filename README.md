# ScrapeFinnBoligMongoDB
Scrape finn.no bolig information by use of MongoDB


This script is trying to scrape the real estate information from www.finn.no.
For this script, Python package requests and BeautifulSoup are used for information scraping.
When this information is collected, each real estate is saved in MongoDB with a unique finnkode.

After all the pages are scraped, and all real-estate information is saved in MongoDB, the titles of each real-estate will be fetched to a text file.
All the words from this text file will be read out and the frequencies of each word will be calcualted.
Some common stopwords like "av", "en", "og" etc. will be excluded for sorting.
By scraping the first 100 pages of real estate information, the 10 most frequent words that Norwegian real estate client would like to use are:
leiligheab2037 -> 3-rooms
enebolig: 2027 -> single-family detached home
beliggenhet:1624 -> position
utsikt: 1584 -> 
soverom: 1241 -> bedroom

 (u'flott', 1416), (u'soverom', 1241), (u'balkong', 1171), (u'Meget', 1159)]