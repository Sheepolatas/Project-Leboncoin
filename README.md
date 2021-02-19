# Project-Leboncoin

Bonjour machin 
 ghgh
 
 ohlala le stage
 
 
 
URL = 'http://bj.xiaozhu.com/fangzi/37609773603.html'

URL1 = 'http://bj.xiaozhu.com/fangzi/40280014403.html'

headers = {
'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/69.0.3497.100 Safari/537.36'
}

wb_data = requests.get(URL, headers=headers)

soup = BeautifulSoup(wb_data.content, 'lxml')

#print(soup)

HouseName = soup.select('div > div > div > h4 > em')

HouseAdress = soup.select('div.wrap > div > div > p > span')

HousePrice = soup.select('#pricePart > div.day_l > span')

HousePicture = soup.select('#curBigImage')

WannerPicture = soup.select('#floatRightBox > div.js_box.clearfix > div.member_pic > a > img')

WannerName = soup.select('#floatRightBox > div.js_box.clearfix > div.w_240 > h6 > a')


WannerSex = soup.select('#floatRightBox > div.js_box.clearfix > div.member_pic > div')

if WannerSex[0]['class'][0] == 'member_ico':
    WannerSex = ‘M’
elif WannerSex[0]['class'][0] == 'member_ico1':
    WannerSex = ‘F’
    
else:
    WannerSex = ‘inconnu
    
vpn
print('title：%s' %HouseName[0].string)

print('adree：%s' %HouseAdress[0].get_text().strip())

print('price：'+HousePrice[0].text)

print('picture：'+HousePicture[0]['src'])

print('name：'+WannerName[0].text)

print('sex：'+WannerSex)

import requests


# fichier excell
import pandas as pd

Annonce=pd.DataFrame({"Article":Article,"Prix":Prix,"link":link})

Annonce.to_excel(r'C:/Users/Alioune Badara NDAO/Documents/Unistra/Semestre2/Programmation/projet.xlsx')

