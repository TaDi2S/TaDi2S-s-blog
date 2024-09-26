---
# Front Matter
title: "[Python] import와 from의 차이"
categories: pythonInfo
tags: python, python-import, python-from
date: YYYY-MM-DD HH:MM:SS +09:00

# 목차
toc: true  
toc_sticky: true 
---

# import와 from의 차이
- import와 from import 구문은 각각 모듈(파이썬 파일)을 가져오는 방법.
- 각 방법은 모듈의 전체 또는 일부를 사용한다.

## import 구문
- 전체 모듈을 가져오는 데 사용.
- 모듈 내의 모든 함수를 호출할 때마다 모듈 이름을 명시한다.

#### 기본 사용법

```python
import module_name
```
#### 사용 예시
math 모듈에서 sqrt 함수를 사용하는 방법
```python
import math

result = math.sqrt(16)  # 모듈 이름을 통해 sqrt 함수 호출
print(result)
```
- 장점
    - 모듈 이름을 통해 명확한 코드 작성가능 : 어떤 모듈의 함수를 사용하는지 명확하게 파악 가능.
    - 네임스페이스 충돌 방지 : 모듈 이름을 항상 사용해야 하므로, 다른 모듈에 동일한 이름의 함수가 있어도 충돌이 발생하지 않음.
- 단점
    - 긴 코드: 모듈 이름이 길 경우, 반복적으로 사용해야 하므로 코드가 길어질 수 있음.

## from import 구문
from import 구문은 특정 모듈에서 일부 함수나 클래스만 가져오는 데 사용된다.    
이렇게 하면 모듈 이름 없이 직접 해당 함수나 클래스를 사용할 수 있다.

기본 사용법
```python
from module_name import function_name
```
또는 여러 함수와 클래스를 한 번에 가져올 수도 있다.

```python
from module_name import function1, function2
```

#### 사용 예시
math 모듈에서 sqrt 함수만 가져오려면 다음과 같이 작성.

```python
from math import sqrt

result = sqrt(16)  # 직접 sqrt 함수 호출
print(result)
```
- 장점
    - 짧고 간결한 코드: 모듈 이름 없이 함수나 클래스를 직접 사용할 수 있으므로 코드가 더 간결해진다.
    - 메모리 효율성: 특정 함수나 클래스만 가져오기 때문에, 큰 모듈의 모든 내용을 메모리에 로드할 필요가 없다.
- 단점
    - 네임스페이스 충돌 가능성: 동일한 이름의 함수가 다른 모듈에서도 존재할 경우, 네임스페이스 충돌이 발생할 수 있다.
    - 코드 가독성 감소: 코드에서 함수나 클래스가 어느 모듈에서 온 것인지 명확하지 않을 수 있다.

### from module import * 구문

이 구문은 모듈의 모든 내용(함수, 클래스 등)을 현재 네임스페이스로 가져온다.    
모듈이 여러개면 꼬일 수도 있을 것 같아서 프로젝트가 커지면 좋은 사용방법이 아닌 것 처럼 보인다.

#### 기본 사용법

```python
from module_name import *
```

#### 사용 예시

```python
from math import *

result = sqrt(16)  # math 모듈의 모든 것을 가져와서 sqrt 함수를 직접 사용
print(result)
```

- 프로젝트가 커지면 불편할 거 같다.

### 마무리

1. 전체 모듈을 가져오는 경우에는 `import module_name`를 사용 하는 것이 더 가독성이나 사용자 측면에서도 모듈들을 관리하기 편해 보인다.

2. 특정 함수나 클래스만 가져오는 경우에는 `from module_name import function_name`도 괜찮은 선택일 수도 있겠지만 여러 모듈을 부러왔을때 함수명드으이 네임스페이스가 충돌하여 예기치 못 한 결과를 얻을 수도 있으니 조심해서 사용하도록 하자.

#### 요약
- import module_name
    - 모듈 전체를 가져오며, 모듈 이름을 통해 함수와 클래스에 접근한다.
    - 네임스페이스 충돌이 적고 코드가 명확해진다.
- from module_name import function_name
    - 모듈의 특정 함수나 클래스만 가져오며, 더 간결한 코드가 가능.
    - 하지만 네임스페이스 충돌 가능성이 매우 거슬림.
- from module_name import *
    - 모듈의 모든 내용을 가져온다.
    - 일반적으로 네임스페이스 충돌 위험이 크므로 왠만하면 쓰지 말자.
