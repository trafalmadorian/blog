---
layout: post
title: 02. 플라스크 설치
---
**목표**: 가상환경에서 파이썬 웹 프레임워크 Flask를 설치한다.

가상환경을 이용하면 파이썬 패키지를 편리하게 설치 및 관리할 수 있다.
첫 예제로 [Flask](http://flask.pocoo.org)라는 웹 프레임워크를 설치해본다.

먼저, [이전에 만들었던]({{ site.baseurl}}/_post/2017-07-14-01_virtualenv.md) `Stock` 가상환경을 실행한다. 해당 디렉토리로 가서 `source` 명령을 이용한다.
```bash
source bin/activate
```
가상환경이 실행되면서 `(Stock)`이라는 글자가 쉘 프롬프트 앞에 나온다.

이제 `pip3` 명령을 이용하여 `Flask` 패키지를 설치한다.

```bash
pip3 install flask
```

![install flask]({{ site.baseurl}}/images/flask/install-flask.png)

위 스크린샷과 같은 화면이 나오면서 관련 패키지들이 자동으로 설치된다.

설치된 패키지 목록을 확인하려면 `pip3` 명령에 `list` 인자를 주면 된다. 원하는 패키지가 제대로 설치되었는지 확인하기 위해 다음 명령을 실행한다.
```bash
pip3 list —format=columns
```

위 명령에서 `--format=columns` 옵션은 패키지 이름과 버전을 column으로 구분해서 보여주라는 뜻.

![check flask]({{ site.baseurl}}/images/flask/check-flask.png)

`Flask` 패키지가 제대로 설치되었으면 파이썬에서 `import flask` 명령으로 불러올 수 있다.

## 참고: 가상환경의 영향 범위
Flask 패키지는 `Stock`이라는 가상환경에 설치되었다. 그러므로 Flask와 관련된 패키지는 `Stock` 가상환경 밖에는 영향을 미치지 못한다.

`Stock` 가상환경을 끝내려면 `deactivate` 명령을 이용한다.

```bash
deactivate
```

가상환경이 끝났으므로 `(Stock)` 이라는 글자가 쉘 프롬프트 앞에서 사라졌다. 이제 `pip3` 명령으로 설치된 패키지 목록을 보면 Flask 패키지가 없는 것을 알 수 있다.

![no-virtualenv]({{ site.baseurl}}/images/flask/no-virtualenv.png)

파이썬에서 `import flask` 명령으로 Flask 패키지를 불러보면 그런 이름의 모듈을 찾을 수 없다는 에러가 난다.
