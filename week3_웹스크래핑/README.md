# OP.GG 웹스크래핑
**웹스크래핑**을 통하여 우리는 원하는 웹페이지의 데이터를 긁어올 수 있다.

이에 대해 간단히 설명하자면,</br>
웹 페이지에서 **HTML** 코드를 가져와서 우리가 원하는 데이터를 찾아서 활용할 수 있는 작업이다.</br>
일반적으로 **웹 크롤링**이라고도 한다.

*직접 다량의 데이터를 쌓기 힘든 환경*에서 유용하게 사용한다.

*공식적으로 제공하는 API가 없거나 상태가 좋지 않을 때*도 유용하다.

파이썬은 대표적으로 스크래핑 하는 두 가지 방법이 있다.
+ requests : 빠름 / javascript로 렌더링되는 element 못 가져옴
+ selenium : 느림 / javascript로 렌더링되는 element 못 가져옴

**My_OPGG_scrap.ipynb** 파일은 첫번째로 나의 OP.GG 전적에서 내가 했던 게임의 **챔피언 이름, 결과, 킬관여율**을 가져왔고</br>
두 번째로 **모스트 챔피언과 그 챔피언의 게임 수**를 가져왔다.

## selenium
웹 크롤링을 할 때 사용되는 프레임워크이며, 해당 파일에서도 셀레니움을 사용하였다.

Selenium은 **webdriver**라는 것을 통해 디바이스에 설치된 브라우저들을 제어할 수 있다.</br>
**webdriver api**를 통해 브라우저를 제어한다.

먼저, https://sites.google.com/a/chromium.org/chromedriver/downloads 에서 크롬 드라이버를 다운로드 해주어야 한다.</br>
꼭 크롬에서는 **현재 버전에 맞는 chromedriver**를 받도록 한다.</br>
*오른쪽 상단 점 3개 > 설정 > Chrome 정보*를 통해 크롬 버전 확인 가능

```python
driver = webdriver.Chrome("C:/chromedriver_win32/chromedriver.exe", options= options)
```
