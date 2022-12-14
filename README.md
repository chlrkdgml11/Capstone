# capstone
### The Design and Implementation of a Mobile Healthcare Application For Pregnants
**2020 Capstone Design, Dept. of Computer Science &amp; Engineering, Incheon National University**

# 요약

- 소개

    임산부 건강관리를 도와주는 어플리케이션

- 기여
    - 회원관리 기능 개발
    - 자세추정을 이용한 운동 관리 기능 개발
    - 식단 추천을 위한 추천 알고리즘 개발
- 졸업작품발표회 동상, KIPS 2021 온라인 춘계학술발표대회 논문게재
- 발표(youtube) : [https://www.youtube.com/watch?v=W2Rw1ElWoTE](https://www.youtube.com/watch?v=W2Rw1ElWoTE)
  
# 소개
### 임산부 건강관리의 필요성
  * 산모의 평균 연령이 높아짐에 따라 영양 관리 및 운동에 대한 중요성이 더욱 높아짐
  * 임산부는 건강관리가 중요함을 인지하고 있지만 관련 지식에 무지한 경우가 대부분임
### 스마트한 식단 관리와 요가 기능
  * 산모 나이와 출산예정일에 기반한 임산부 일일 영양소 섭취기준과 추천 알고리즘을 바탕으로 식단 관리
  * Tensorflow-Lite의 학습된 모델을 이용한 요가자세추정
### 임산부의 편의를 위한 기능
  * 인근 산부인과 검색(위치 기반)과 일정 관리

# 프로젝트 총평
### 리더로서 협업에 대해 많은 고민을 했다. DevOps에 관심을 갖게됐다.
1. 아쉬운 점
  * 팀원들의 역량을 최대로 이끌어내지는 못했다는 생각이 든다.
    * 비대면으로 프로젝트를 진행하는 게 어렵다고 생각했다.
    * 돌아보니 나의 문제였다. 더 명확히 지시하고, 더 체계적으로 계획했으면 됐다.
  * 두 명이 함께 서버를 맡는 데 어려움이 있었다.
    * 깃허브를 효율적으로 사용하는 방법을 고민해보는 게 좋겠다.
    * CI/CD와 DevOps에 대한 지식을 배우는 게 좋겠다.
2. 배운 점
  * 내가 가진 기술 스택을 좀 더 꼼꼼히 공부했다.
    * 이전 프로젝트에서는 남의 코드를 참고해서 기능을 구현하는 데만 힘을 썼다.
    * 이번 프로젝트에서는 코드를 한땀 한땀 이해하기 위해 노력했다. 특히 ES6 공부를 많이 했다.
  * 데이터 분석과 AI에 대해 경험했다.
    * 추천 알고리즘과 자세 추정을 구현했다.
    * 데이터 분석과 AI에 대해 좀 더 자세히 배워보고 싶다는 생각을 했다.

# 성과
### 졸업작품발표회 동상
![image](https://user-images.githubusercontent.com/67588446/122170063-1dd98b80-ceb9-11eb-8c92-b7ffec81d3dc.png)

발표(youtube) : https://www.youtube.com/watch?v=W2Rw1ElWoTE
### KIPS 2021 온라인 춘계학술발표대회 논문게재
논문 : https://manuscriptlink-society-file.s3-ap-northeast-1.amazonaws.com/kips/conference/kips2021spring/presentation/KIPS_C2021A0026.pdf

# 요구사항
<details>
  <summary>상세 내용 확인</summary>
  <div markdown="1">
    
| 기능 | 설명 |
| --------------- | -------------------------------------------------- |
|출산 예정일 등록|출산 주차에 따라 산모에게 필요한 정보를 제공|
|산모 나이 등록|산모의 나이에 따라 식단 정보를 제공|
|식단 추천|일일 영양소 섭취기준과 추천 알고리즘을 바탕으로 식단 추천|
|요가|임산부에게 도움이 되는 요가를 볼 수 있음|
|자세추정|카메라를 사용해 자세를 인식하고, 주어지는 요가 이미지와 일치하는지 판별|
|인근 산부인과 검색|인근 산부인과 검색을 통해 응급시 신속히 가까운 병원을 찾을 수 있음|
|병원 일정 알리미|다음 병원 선생님과의 예약날짜를 입력하여 일정을 잊지 않도록 알려줌|
|회원정보 관리|회원가입, 로그인, 회원정보 수정, 알림 설정|

  </div>
</details>

# 설계
<details>
  <summary>상세 내용 확인</summary>
  <div markdown="1">
    
### 1. 메뉴구성도
![image](https://user-images.githubusercontent.com/67616332/111997295-407c3280-8b5e-11eb-8b94-666d990624d1.PNG)
### 2. 식단 알고리즘
![image](https://user-images.githubusercontent.com/67616332/111997510-74575800-8b5e-11eb-8867-5c00447b25c1.PNG)
### 3. 요가 알고리즘
![image](https://user-images.githubusercontent.com/67616332/111996433-5d643600-8b5d-11eb-9273-1425dd1c0038.PNG)


  </div>
</details>

# 개발환경
<details>
  <summary>상세 내용 확인</summary>
  <div markdown="1">
       
### BE
| 구분 | 개발환경 | 개발도구 | 개발언어 |
| ----- | --------- | --------- | --------- |
|Server|VSCode|Node.js|JavaScript|
|DB|Robo 3T|MongoDB|MongoDB|
|\*HF|Pycharm|-|Python|

\*HF : Hybrid Filtering
  
### INFRA-AWS
| 구분 | 서비스 |
| --------- | ------------- |
|Computing|EC2 CentOS7|
|Storage|S3|
|CDN|CloudFront|
  
### FE
|구분|개발환경|개발도구|개발언어|
|--|--| -- |--|
|Front|Android Studio| - | Java & Kotlin |
  
  </div>
</details>


# API DOCS
<details>
  <summary>상세 내용 확인</summary>
  <div markdown="1">
    
* USERS
  * [[POST] 회원가입](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-회원가입)
  * [[POST] 로그인](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-로그인)
  * [[POST] 출산예정일수정](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-출산예정일수정)

* YOGAS
  * [[GET] 요가목록](https://github.com/owenyi/capstone/wiki/%5BGET%5D-요가목록)
  * [[GET] 요가자세](https://github.com/owenyi/capstone/wiki/%5BGET%5D-요가자세)

* CALENDARS
  * [[GET] 일정](https://github.com/owenyi/capstone/wiki/%5BGET%5D-%EC%9D%BC%EC%A0%95)
  * [[POST] 일정](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-%EC%9D%BC%EC%A0%95)

* DIETS
  * [[POST] 밥](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-%EB%B0%A5)
  * [[POST] 국, 찌개](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-%EA%B5%AD,%EC%B0%8C%EA%B0%9C)
  * [[POST] 반찬1](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-%EB%B0%98%EC%B0%AC1)
  * [[POST] 반찬2](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-%EB%B0%98%EC%B0%AC-2)
  * [[PATCH] 식단선택](https://github.com/owenyi/capstone/wiki/%5BPATCH%5D-식단선택)
  * [[POST] 식단평점초기화](https://github.com/owenyi/capstone/wiki/%5BPOST%5D-식단평점초기화)
  * [[GET] 모든식단](https://github.com/owenyi/capstone/wiki/%5BGET%5D-모든식단)
  * [[PATCH] 식단선호도선택](https://github.com/owenyi/capstone/wiki/%5BPATCH%5D-식단선호도선택)
  
  </div>
</details>
