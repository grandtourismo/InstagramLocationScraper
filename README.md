
# Instagram Location Crawler
A non API python program to scrape number of posts at a location, as well as locations in a city from Instagram  
I am coding this for use in my Seminar "Computational Social Sciences" to acquire data for my group
### Full usage:
```
usage: LocationCrawler.py [-h] [-l LOCATION] [-c CITY] [-fromFile FILE TYPE]
                          [-fromDir DIR SUFFIX] [-d DATE] [-t TIMEWINDOW]
                          [-dir DIRPREFIX] [-threads THREADCOUNT]
                          [-max MAXPOSTS] [-drv DRIVERPATH]
                          [-drvProfile DRIVERPROFILEPREFIX]

Instagram Location Scraper

optional arguments:
  -h, --help            show this help message and exit
  -l LOCATION, --location LOCATION
                        Location Number to scrape, eg. -l 214335386/ for
                        Englischer Garten
  -c CITY, --city CITY  City to scrape location links from, eg. -c c579270/
                        for Munich
  -fromFile FILE TYPE   File containing a list of locations/cities to scrape,
                        specify with c or l, eg. -fromFile cities.txt c
  -fromDir DIR SUFFIX   Directory containing files with lists of locations to
                        scrape with suffix to specify which files to scrape,
                        eg. -fromDir ./data/Locations _Locations.txt
  -d DATE, --date DATE  Date up till which to scrape, eg. -d
                        2017-06-01T10:00:00 ; default: now
  -t TIMEWINDOW, --timeWindow TIMEWINDOW
                        Timeframe to check number of posts in hours, eg. -t
                        1.0 ; default: 1.0
  -dir DIRPREFIX, --dirPrefix DIRPREFIX
                        directory to save results to, eg. -dir ./data/ ;
                        default: ./data/
  -threads THREADCOUNT, --threadCount THREADCOUNT
                        how many threads (each one instance of chromedriver)
                        to use, eg. -threads 4 ; default: 1
  -max MAXPOSTS, --maxPosts MAXPOSTS
                        maximum number of posts to scrape, mainly due to
                        performance reasons, eg. -max 1500 ; default: -1
                        (unlimited)
  -drv DRIVERPATH, --driverPath DRIVERPATH
                        path to chromedriver, eg. -drv ./chromedriver.exe ;
                        default: ./chromedriver.exe
  -drvProfile DRIVERPROFILEPREFIX, --driverProfilePrefix DRIVERPROFILEPREFIX
                        prefix for scraper chrome profiles, eg -drvProfile
                        ./Scraper ; default: ./Scraper
```

### Installation
download chromedriver here: https://sites.google.com/a/chromium.org/chromedriver/
either place chromedriver.exe in same directory as LocationCrawler.py, edit CHROMEDRIVER_PATH in LocationCrawler.py, or pass it as an argument with -drv (eg: "-drv ./chromedriver.exe")

then install the requirements (you need to have a python 3 distribution installed):
```
$ pip install -r requirements.txt
```
