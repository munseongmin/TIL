# 벅스뮤직 차트 스크래핑

벅스뮤직 차트에서 1~100위까지 가수와 곡명 스크랩핑 해서 엑셀 파일로 저장하기

### webdriver, BeautifulSoup, pandas 불러오기
```python
from selenium import webdriver
from bs4 import BeautifulSoup
import pandas as pd
```

### Chrome 실행시켜 벅스뮤직 사이트로 이동
```python
browser=webdriver.Chrome()
browser.get(https://music.bugs.co.kr/chart)
```

### 페이지 소스에 접근하기
```python
html=browser.page_source
BeautifulSoup(html, 'html.parser')
```