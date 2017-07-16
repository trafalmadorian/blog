---
layout: post
title: 04. Pandas 설치
---

**목표**: 가상환경을 이용하여 데이터 처리 패키지 Pandas를 설치한다.

먼저, 이전에 만들었던 `Stock` 가상환경을 실행한다. 해당 디렉토리로 가서 `source` 명령을 이용한다.
```bash
source bin/activate
```
가상환경이 실행되면서 `(Stock)`이라는 글자가 쉘 프롬프트 앞에 나온다.

이제 `pip3` 명령을 이용하여 [Pandas](http://pandas.pydata.org/) 패키지를 설치한다.

```bash
pip3 install pandas --upgrade
```

이전과 달리 `--upgrade`라는 인자가 추가되었다. `pandas` 패키지가 이미 설치되었더라도 새 버전으로 업그레이드하라는 뜻이다.

![install flask]({{ site.baseurl}}/images/pandas/install-pandas.png)

Pandas 뿐 아니라 연관 패키지도 모두 설치되었다. 자세한 목록은 아래 명령으로 확인할 수 있다.

```bash
pip3 list --format=columns
```

![install flask]({{ site.baseurl}}/images/pandas/check-list.png)

Pandas에서 파생된 패키지 중에서 [pandas_datareader](https://pandas-datareader.readthedocs.io/en/latest/)를 설치한다.

```bash
pip3 install pandas_datareader
```

![install flask]({{ site.baseurl}}/images/pandas/install-pandas-reader.png)

마찬가지로 관련된 패키지도 설치되었다. 자세한 목록은 아래와 같다.

![install flask]({{ site.baseurl}}/images/pandas/check-list-again.png)

## 테스트: KOSPI 정보 가져오기
간단한 파이썬 스크립트를 이용해서 Pandas 패키지가 제대로 설치되었는지 테스트할 수 있다.
아래 파일 ```kospi.py```는 [Google Finance](https://www.google.com/finance)를 통해서 KOSPI 정보를 내려받는다.

```python
from pandas_datareader import data
from datetime import datetime

# set the time period
start, end = datetime(2017, 7, 3), datetime(2017, 7, 7)
# retrieve KOSPI index for given time period
web = data.get_data_google("KRX:KOSPI", start, end)

print(web)
```
다음과 같은 명령으로 실행할 수 있다.
```bash
python3 kospi.py
```

![install flask]({{ site.baseurl}}/images/pandas/kospi.png)

이 스크립트는 2017년 7월 3일부터 2017년 7월 7일까지 KOSPI 주가 정보를 다섯 개의 필드로 출력한다.

|일자|시가|최고가|최저가|종가|거래량|
|--|--|---|----|--|---|
|2017-07-03|2397.66|2399.90|2384.55|2394.48|310991000|
|2017-07-04|2395.24|2398.02|2376.41|2380.52|411776000|
|2017-07-05|2377.01|2390.29|2375.63|2388.35|333721000|
|2017-07-06|2390.31|2392.50|2380.82|2387.81|301472000|
|2017-07-07|2376.29|2385.02|2372.83|2379.87|314370000|
