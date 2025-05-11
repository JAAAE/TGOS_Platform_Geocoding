# TGOS_Platform_Geocoding
Automatically geocoding via Python on the TGOS platform(https://api.tgos.tw/TGOS_MAP_API/Docs/Example/99)

* `Motivation`：The TGOS platform enables individuals to geocode addresses to coordinates by inputting the address in the search box, providing an alternative method to the official TGOS geocoding service, which has a limit of ten thousand addresses per day.
  
* `Objective` : Enter an address in the search box, automatically utilize geocoding, and repeat the process n times.
* `Challenge` :
The API key (**keystr**) on the platform (https://gis.tgos.tw/TGLocator/TGLocator.ashx?format=jsonp&input=&srs=EPSG:4326&ignoreGeometry=false&pnum=1&keystr=xwX1jHXL3NnG5rbVMs9zH%2F0NWItJYrtxFG%2F%2BeA59MJY%3D&jsonp=TGOS.getJSON%5B%27sn0%27%5D) changes approximately every twenty minutes.

* `Results` :
1. Automate web control using the **selenium.webdriver** library.
2. Extract the coordinates from the platform using the **requests** library
3. Save the geocoded coordinates to a CSV file using the **csv** library

* `Libraries` : requests、json、csv、pandas、slenium、time（pip install requests pandas selenium）

* Customize the file path and the column name for the address：
  ```
    1. input_path = r'C:\Users\USER\Desktop\test.csv'
    2. output_path = r'C:\Users\USER\Desktop\Addresss_result.csv'
    3. df1 = df['商業地址']
  ```
  
