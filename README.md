# ScrapeFinnBoligMongoDB
# Scrape finn.no bolig information by use of MongoDB


This script is trying to scrape the real estate information from www.finn.no.

For this script, Python package *requests* and *BeautifulSoup* are used for information scraping.

When this information is collected, each real estate is saved in **MongoDB** with a unique finnkode.

After all the pages are scraped, and all real-estate information is saved in **MongoDB**, the titles of each real-estate will be fetched to a text file.

All the words from this text file will be read out and the frequencies of each word will be calcualted.

Some common stopwords like "av", "en", "og" etc. will be excluded for sorting.

By scraping the first 100 pages of real estate information, the 10 most frequent words that Norwegian real estate client would like to use are:

Norwegian Word | English Meaning | Appearance
--- | --- | ---
leilighet | apartment | 2672
3-roms | 3-rooms | 2037
enebolig | detached home | 2027
beliggenhet | position | 2634
utsikt | overview | 1584
flott | great | 1416
soverom | bedroom | 1241
balkong | balcony | 1171
meget | very | 1159
gode | good | 1044

All this words will in the end masked in a map of Norway, by using a Python package wordcloud.

![alt text](https://github.com/qiangwennorge/ScrapeFinnBoligMongoDB/blob/master/norwaymap_mask_output.png "norwaymap_mask_output")
