# TGOS_Platform_Geocoding
Automatically geocoding via Python on the TGOS platform(https://api.tgos.tw/TGOS_MAP_API/Docs/Example/99)

* `Motivation`：The TGOS platform allows users to geocode addresses by entering them into the search box, offering an alternative to the official TGOS geocoding service, which has a daily limit of 10,000 addresses.
  
* `Objective` : Enter an address in the search box, automatically utilize geocoding, and repeat the process n times.
* `Challenge` :
The API key (**keystr**) on the platform (https://gis.tgos.tw/TGAddress/TGAddress.aspx?oAddress=%E8%87%BA%E5%8C%97%E5%B8%82%E4%B8%AD%E5%B1%B1%E5%8D%80%E6%9D%BE%E6%B1%9F%E8%B7%AF469%E5%B7%B74%E8%99%9F&oSRS=EPSG:3826&oResultDataType=jsonp&pnum=NaN&keystr=GcsaLeN61ur%2BRIdpQ6q%2B%2F6ko1AwBUfcmw4voRAh0AfU%3D&jsonp=TGOS.getJSON%5B%27sn3%27%5D) updates approximately every 20 minutes.

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
  
