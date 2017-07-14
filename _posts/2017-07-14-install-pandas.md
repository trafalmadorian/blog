---
layout: post
title: Pandas 설치
---

**목표**: 가상환경을 이용하여 데이터 처리 패키지 Pandas를 설치한다.

먼저, 이전에 만들었던 `Stock` 가상환경을 실행한다. 해당 디렉토리로 가서 `source` 명령을 이용한다.
```bash
source bin/activate
```
가상환경이 실행되면서 `(Stock)`이라는 글자가 쉘 프롬프트 앞에 나온다.

이제 `pip3` 명령을 이용하여 `Pandas` 패키지를 설치한다.

```bash
pip3 install pandas
```

![install flask]({{ site.baseurl}}/images/pandas/install-pandas.png)

Pandas 뿐 아니라 연관 패키지도 모두 설치되었다. 자세한 목록은 아래 명령으로 확인할 수 있다.

```bash
pip3 list --format=columns
```

![install flask]({{ site.baseurl}}/images/pandas/check-list.png)

Pandas에서 파생된 패키지 중에서 ```pandas_datareader```를 설치한다.

```bash
pip3 install pandas_datareader
```

마찬가지로 관련된 패키지도 설치되었다. 정확한 목록은 아래와 같다.

![install flask]({{ site.baseurl}}/images/pandas/check-list-again.png)

