# Django

# 📌목차

---

# 🟠웹의 동작 방식

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1848a85f-9836-46e1-8795-3eff9f43f933/c060f5cc-21db-4f0e-ac4b-51c3edf8b4bd/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1848a85f-9836-46e1-8795-3eff9f43f933/27c8dbf2-d956-49ba-9ac0-25f7719392dd/Untitled.png)

## 🔶Client

- 클라이언트
- 서비스를 **요청**하는 주체
    - 웹 사용자의 인터넷이 연결된 장치, 웹 브라우저

## 🔶Server

- 서버
- 클라이언트의 요청에 **응답**하는 주체
    - 웹 페이지, 앱을 저장하는 컴퓨터

---

# 🟠Frontend & Backend

## 🔶Frontend

- 사용자 인터페이스(UI)를 구성하고, 사용자가 애플리케이션과 상호작용할 수 있도록 함
    - HTML, CSS, JavaScript 등

## 🔶Backend

- 서버 측에서 동작하며, 클라이언트의 요펑에 대한 처리와 데이터 베이스와의 상호작용 등을 담당
    - 서버언어(Python, Java) 및 백엔드 프레임 워크, 데이터 베이스, API, 보안 등

# 🟠Famework

- “거인의 어깨 위에서 프로그래밍하기”
    - 하나부터 열까지 개발자가 모두 개발하는 것이 아닌 잘 만들어진 것들을 가져와 좋은 환경에서 내 것으로 잘 사용하는 것도 능력

## 🔶Web Framework

- 웹 애플리케이션을 빠르게 개발할 수 있도록 도와주는 도구
    - 개발에 필요한 기본 구조, 규칙, 라이브러리 등을 제공
- 파이썬 기반 대표 웹 프레임워크 - **Django**

---

# 🟠Django

- 다양성
    - Python기반으로 소셜 미디어 및 빅데이터 관리 등 광범위한 서비스 개발에 적합
- 확장성
    - 대량의 데이터에 대해 빠르고 유연하게 확장할 수 있는 기능 제공
- 보안
    - 취약점으로부터 보호하는 보안기능이 기본적으로 내장되어 있음
- 커뮤니티 지원
    - 개발자를 위한 지원, 문서 및 업데이트를 제공하는 활성화 된 커뮤니티
    

## 🔶가상 환경

- Python 애플리케이션과 그에 따를 패키지를 격리하여 관리할 수 있는 독립적인 실행 환경
- Global 환경이 아닌 격리된 환경을 사용

### 가상환경 venv 생성

```python
python -m venv venv
```

### 가상환경 활성화

```python
source venv/Scripts/activate
```

### 가상환경 비활성화

```python
deactivate
```

### 환경에 설치된 패키지 목록 확인

```python
pip list
```

### 패키지 목록 생성

- 의존성 패키지
- 한 소프트웨어 패키지가 다른 패키지의 기능이나 코드를 사용하기 때문에 그 패키지가 존재해야만 제대로 작동되는 관계
- 사용하려는 패키지가 설치되지 않았거나, 호환되는 버전이 아니라면 오류가 발생하거나 예상치 못한 동작을 보일 수 있음

```python
pip freeze > requirements.txt
```

- 개발환경에서는 각각의 프로젝트가 사용하는 패키지와 그 버전을 정확히 관리하는것이 중요
- 가상환경 & 의존성 패키지 관리

### 의존성 패키지 목록 설치

```python
pip install -r requirements.txt
```

### 장고 서버 실행

```python
python manage.py runserver
```

## 🔶LST(Long-Term Support)

- 프레임워크나 라이브러리 등의 소프트웨어에서 장기간 지원되는 안정적인 버전을 의미
- 기업이나 대규모 프로젝트에서는 소프트웨어 업그레이드에 많은 비용과 시간이 필요하기 때문에 안정적이고 장기간 지원되는 버전이 필요

## 🔶디자인 패턴

- 소프트웨어 설계에서 발생하는 문제를 해결하기 위한 일반적인 해결책
    - 공통적인 문제를 해결하는데 쓰이는 형식화된 관행
- 애플리케이션의 구조는 이렇게 구성하자 라는 관행

### MVC 디자인 패턴

- Model, View, Controller
- 애플리케이션을 구조화하는 대표적인 패턴
- 데이터, 사용자 인터페이스, 비즈니스 로직을 분리
- 시각적 요소와 뒤에서 실행되는 로직을 서로 영향없이, 독립적이고 쉽게 유지보수할 수 있는 애플리케이션을 만들기 위함

### MTV 디자인 패턴

- Model, Template, View
- Django에서 애플리케이션을 구조화하는 패턴
- 기존 MVC 패턴과 동일하나 단순히 명칭을 다르게 정의한 것
    
    ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1848a85f-9836-46e1-8795-3eff9f43f933/210a8d1f-8842-4b5a-890c-dbafa83fac1a/Untitled.png)
    

## 🔶Project & App

### Django Project

- 애플리케이션의 집합
    - DB설정, URL연결, 전체 앱 설정등을 관리

**프로젝트 생성**

```python
django-admin startproject 프로젝트명 .
```

### Django application

- 독립적으로 작동하는 기능 단위 모듈
    - 각자 특정한 기능을 담당하며 다른 앱들과 함께 하나의 프로젝트를 구성

### 앱을 사용하기 위한 순서

1. 앱 생성
    - 앱 이름은 복수형으로 지정하는 것을 권장
2. 앱 등록
    - 반드시 앱을 생성한 후에 등록해야 함
    - project/ settings.py의 INSTALLED_APPS에 맨 앞쪽에 등록
        
        ![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1848a85f-9836-46e1-8795-3eff9f43f933/deda6914-5470-4524-9d9d-2117685955bc/Untitled.png)
        

## 🔶프로젝트 구조

### settings.py

- 프로젝트의 모든 설정을 관리

### urls.py

- 요청 들어오는 URL에 따라 이에 해당하는 적절한 views를 연결

### manage.py

- Django 프로젝트와 다양한 방법으로 상호작용하는 커맨드라인 유틸리티

## 🔶앱 구조

- MTV모두 앱에 존재해야함

### admin.py

- 관리자용 페이지 설정

### models.py

- DB와 관련된 Model을 정의
- MTV 패턴의 M

### views.py

- HTTP 요펑을 처리하고 해당 요청에 대한 응답을 반환
- url, model, template과 연계
- MTV 패턴의 V

### apps.py

- 앱의 정보가 작성된 곳

## 🔶요청과 응답

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/1848a85f-9836-46e1-8795-3eff9f43f933/2d4065b8-d30e-4f73-9d4a-4d6fed729257/Untitled.png)

## 🔶templates

- **앱 아래에 존재**
- **폴더 이름은 templates여야만 함** - 필수

### templates불러오기

- views.py에 함수를 만들어야 함
    - 이때 함수에는 request를 꼭 인자값으로 넣어줘야하며
    - return시에는 render함수를 사용함
        - return render(request, ‘templates이후의 폴더, 파일 명’)
