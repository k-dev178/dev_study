# 6.0 Introduction
## 웹 스크래퍼
웹사이트에 연결해 데이터를 추출하는 프로그램.

## 웹 스크래핑할 사이트
- https://weworkremotely.com
- https://remoteok.com
- https://www.wanted.co.kr

이 사이트의 데이터를 추출한 후, Excel에 넣을거임.

# 6.1
웹사이트는 업데이트를 자주하기 때문에, 지금하는 코드가 추후에도 작동하기 기대하면 안됨.

# 6.2 BeautifulSoup
## url 받기
```py
import requests

url = "https://weworkremotely.com/categories/remote-full-stack-programming-jobs"
response = requests.get(url)

print(response.content)
```
이제 이걸 조금씩 가공해볼거임.

## html vkdlf
```py
import requests
from bs4 import BeautifulSoup

url = "https://weworkremotely.com/categories/remote-full-stack-programming-jobs"
response = requests.get(url)

soup = BeautifulSoup(response.content, "html.parser")
jobs = soup.find("section", class_="jobs").find_all("li")

print(jobs)
```
이렇게 하면 jobs안에 있는 li들을 모두 파싱해서, jobs에 리스트로 저장함.
