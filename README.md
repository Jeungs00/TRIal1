# TRIal1
import requests
from bs4 import BeautifulSoup, NavigableString, Tag

URL = 'https://web.archive.org/web/20200709231031/https://www.imdb.com/search/title/?sort=user_rating,desc&groups=top_100'
headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36'}
page = requests.get(URL, headers=headers)
import pandas as pd
soup = BeautifulSoup(page.text, 'html.parser')
