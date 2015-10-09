# Python Scripts

This folder contains the scripts used to scrape and obtain data about the NYC traffic cameras. To run these scripts, you need Python 2.7+

* **js_selectall.js:** is the jQuery used to select all the checkboxes on NYC page and obtain the feed of all cameras
* **cams.html:** is the scrapped page obtained using the previous script AFTER having the non-relevat HTML tags removed
* **crawler.py:** a Python script used to scrape the previous page, keeping just the address and the URL of each camera
* **cameras.txt:** the output of the previous script. Contains (*camera_address*\n<camera_url>\n)*
* **addresses.txt:** a list with the addresses of each camera. As latlongs, these lines doesn't corresponds to the lines on *cameras.txt*, as this file is generated by iterating a Python's dictionary
* **latlongs.txt:** contains the latitude and longitude of each camera. Notice that these lines doesn't corresponds to the lines on *cameras.txt*, as this file is generated by iterating a Python's dictionary
* **jsonFormatter.py:** another Python script that takes as input the file generated by the crawler and creates a formatted JSON file with the cameras data (including lat-long)
* **cameras.json:** finally, the json file with all cameras and their locations, URLs, lat-longs