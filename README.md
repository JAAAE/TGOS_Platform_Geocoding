# TGOS_Platform_Geocoding
Automatically geocoding via Python on the TGOS platform(https://map.tgos.tw/TGOSCloudMap) 

* Motivation：The TGOS platform allows individuals to geocode addresses to coordinates, offering an alternative method to the official TGOS geocoding service, which has a limit of ten thousand addresses per day.
* objective: Enter an address in the search box, automatically utilize geocoding, and repeat the process n times.
* challenge: 
The API key (**kestr**) on the platform (https://gis.tgos.tw/TGLocator/TGLocator.ashx?format=jsonp&input=&srs=EPSG:4326&ignoreGeometry=false&pnum=1&keystr=xwX1jHXL3NnG5rbVMs9zH%2F0NWItJYrtxFG%2F%2BeA59MJY%3D&jsonp=TGOS.getJSON%5B%27sn0%27%5D) changes approximately every twenty minutes."
* Result:
1. Automate web control using the **selenium.webdriver** library.
2. Extract the coordinates from the geocoding result using the **requests** library
3. Save the geocoded coordinates to a CSV file using the **csv** library
