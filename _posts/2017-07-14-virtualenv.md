---
layout: post
title: 가상환경 설정
---

먼저 Python3가 설치되어 있고 버전이 3.6 이상임을 확인한다.
![python version]({{ site.baseurl }}/images/virtualenv/python-version.png)
`Stock`이라는 이름의 가상환경을 만들려고 한다면, 다음 명령을 실행하면 된다.

```python3 -m virtualenv Stock```

파이썬에서 `-m <module-name>` 옵션은 인자로 주어진 모듈을 실행한다. 위 명령은 `virtualenv` 모듈을 실행해서 `Stock`이라는 가상환경을 만들라는 뜻이다.
![install virtualenv]({{ site.baseurl}}/images/virtualenv/install-virtualenv.png)
스크린샷에서 볼 수 있듯이, `Stock`이라는 디렉토리가 만들어졌다.
![install virtualenv]({{ site.baseurl}}/images/virtualenv/install-virtualenv.png)
