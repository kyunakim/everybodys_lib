- [모두의 도서관: 서울시 자치구별 문화프로그램 시행 현황 및 제언](#-------------------------------------)
  * [1. 시작](#1---)
  * [2. 분석 주제](#2------)
  * [3. 이용 데이터: (몇건인지도 추가하면 좋을듯)](#3-------------------------)
  * [4. 분석방법](#4-----)
  * [5. 분석 결과](#5------)
  * [6. 결론](#6---)
  * [프로젝트 타임라인](#---------)
  * [활용 기술 & 프로그램](#------------)
    + [사용 언어](#-----)
    + [자연어 전처리](#-------)
    + [시각화](#---)
  * [셀프 평가 & 의의](#----------)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>

## 모두의 도서관: 서울시 자치구별 문화프로그램 시행 현황 및 제언
-[2022 데이터안심구역 활용 경진대회](https://youtu.be/4qty40r2EBo?t=2982) 우수상 수상- 

### 1. 시작 
👶<b>"도서관에는 왜 어린이들이 많을까?"</b>👶

사소한 의문에서부터 시작한 도서관 문화프로그램 주제 찾기 프로젝트입니다. 
<br>공공 도서관이 시민 공동체의 역할을 강화하기 위해 어떤 점을 보완할 수 있을까요? 


**성인의 도서관 이용률은 2013년부터 꾸준히 감소해 지금은 10% 후반대를 기록하고 있습니다(KOSIS).** 도서관을 이용하지 않는 이유로는 ▲책을 읽지 않는다 ▲도서관을 이용할 필요를 못 느낀다가 꼽혔습니다. 한편 도서관을 이용하는 성인들은 도서관에서 ▲책을 읽거나 빌리고 ▲공부 및 자료조사를 위해 도서관을 찾는다고 합니다. 도서관을 찾는 이유도, 찾지 않는 이유도 '책'입니다. 즉, 우리 인식 속 도서관은 자료 이용을 하는 공간입니다. 

사실 도서관에서는 책만 읽을 수 있는 게 아닙니다. 도서관은 온 국민의 ‘평생교육의 장’으로서 모두에게 보편적인 교육기회를 제공하고, 지역 커뮤니티 허브로서의 역할을 수행하고 있습니다. 그중 대표적으로 **문화프로그램**이 있습니다. 문화프로그램의 역할을 강화할 수 있다면 도서관이 자료 이용 중심의 공간에서 더 확장된 개념으로 우리에게 다가올 수 있지 않을까요? 

<img width="368" alt="Screen Shot 2023-02-02 at 4 32 46 PM" src="https://user-images.githubusercontent.com/107484982/216260224-d9f7fd57-3b3c-4538-84ea-a0cff7df4eb0.png">

문제는, 현재 시행되고 있는 문화프로그램의 주제와 대상이 다양하지 않다는 점입니다. 2022년 10월 기준, 서울시 전체 공공도서관에서 시행되는 문화프로그램의 절반이 미성년을 대상으로 합니다. 성인 대상 프로그램조차도, 가족이나 육아를 주제로 하는 경우가 많습니다. 

### 2. 분석 주제 
구체적으로, 우리의 질문은 다음과 같습니다. 

#### ☝️ 첫째, 도서관의 문화프로그램이 우리 사회의 다양한 집단을 수용하고 있는가?
이때 다양한 집단이라 함은 시니어, 사회 초년생, 국내 이주민을 의미합니다. 노인인구와 국내이주민은 꾸준히 증가하고 있으며, 청년 고용은 지속적으로 감소 중입니다. 인구 구조의 변화와 고용문제를 고려해 이들 집단을 분석의 대상으로 선정했습니다. 이들을 대상으로 하는 프로그램이 얼마나 되는지 살펴보았습니다. 

#### ✌️ 둘째, 각 집단의 관심사에 맞는 프로그램을 시행하고 있는가?
물론 한 집단의 구성원이 모두 같은 것을 바라지는 않습니다. 하지만 집단을 정의하는 사회적 맥락을 고민해 본다면, 공통된 관심사는 있을 것입니다. 예를 들어보자면 시니어에게는 건강이, 사회초년생에게는 커리어가, 국내이주민에게는 정착이 중요한 화두일 것이라 짐작해 볼 수 있습니다. 이 점에 착안해, 트위터와 뉴스 데이터로 집단별 관심사를 읽어보려 시도했습니다. 

### 3. 이용 데이터: (몇건인지도 추가하면 좋을듯)

|분류|데이터|기간|출처|
|---|---|---|---|
|1. 인구 통계 |자택직장정보|2021|KCB(데이터안심구역)|
|2. 문화프로그램 데이터|문화 어쩌고 이름|2021|국립중앙도서관|
|| 문화프로그램 데이터|2021.01~2022.10|서울시 구별 도서관 홈페이지|
|3. 집단별 관심사 데이터 |청년, 시니어 관련 트윗|2021.01~2022.10|트위터|
||청년, 시니어, 국내이주민 관련 뉴스기사|2021.01~2022.10|네이버뉴스|

### 4. 분석방법
1. 인구데이터의 요약통계
2. 문화프로그램 데이터 전처리, 키워드 추출, 요약통계 
3. 집단별 관심사 데이터 전처리, 키워드 추출, 키워드에 해당하는 프로그램 도출 및 요약통계
4. GAP시각화

### 5. 분석 결과
발표자료 임베딩 

### 6. 결론
도서관 이용자집단을 확대할 필요가 있으며, 집단별 문화적 수요를 반영한 프로그램이 기획,시행되어야 합니다. 분석 결과를 토대로, 0000, 0000과 같은 프로그램을 제안해 봅니다. 배경을 조사하는 과정에서 알게 된 사실이 있습니다. 사서 인력의 한계로 프로그램이 원활히 기획되고 시행되지 못한다는 점입니다. 

<hr>

### 팀

|                            김영선                            |                            양주희                            |                           이명진                             |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| <img src='https://avatars.githubusercontent.com/u/108660426?v=4' height=80 width=80px></img> | <img src='https://avatars.githubusercontent.com/u/90437704?v=4' height=80 width=80px></img> | <img src='https://avatars.githubusercontent.com/u/107484982?v=4' height=80 width=80px></img> |
| [![Git Badge](http://img.shields.io/badge/-Github-black?style=flat-square&logo=github)](https://github.com/kyunakim) | [![Git Badge](http://img.shields.io/badge/-Github-black?style=flat-square&logo=github)](https://github.com/YANGJUHEE521) | [![Git Badge](http://img.shields.io/badge/-Github-black?style=flat-square&logo=github)](https://github.com/palesaltedcaramel) | 

### 프로젝트 타임라인 (날짜 업데이트 하기!)
- 주제 구체화 
- 데이터 수집 
- 데이터 전후처리 
- 데이터 통계적 분석 & 해석
- 프레젠테이션 자료 제작 
- 최종 발표 

### 기술 스택
#### 사용 언어 
<img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=Python&logoColor=white"></a>
<a>

#### 웹 스크래칭과 자연어 처리
<a href="https://github.com/JustAnotherArchivist/snscrape"><img src="https://img.shields.io/badge/SNScrape-808080?style=for-the-badge&logo=BeautifulSoup&logoColor=white"></a> <a href = "https://beautiful-soup-4.readthedocs.io/en/latest/#"><img src="https://img.shields.io/badge/BeautifulSoup-3E3E3E?style=for-the-badge&logo=BeautifulSoup&logoColor=white"></a> <a href="https://github.com/konlpy/konlpy"><img src="https://img.shields.io/badge/koNLPy-D00000?style=for-the-badge&logo=koNLPy&logoColor=white"></a>


#### 시각화
<img src="https://img.shields.io/badge/tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white"> <img src="https://img.shields.io/badge/numbers-71D754?style=for-the-badge&logo=numbers&logoColor=white"> <img src="https://img.shields.io/badge/goodnotes-5CC8FA?style=for-the-badge&logo=goodnotes&logoColor=white">

### 셀프 평가 & 의의 
- 데이터로부터 사회적 가치가 있는 인사이트를 이끌어냄 
- 충분히 다양한 집단을 대상으로 이루어지지 않고 있다는 점 발견 
- 시행현황과 집단별 수요의 gap 발견 
- 관심사 키워드로부터 프로그램 주제 도출 
- 공공도서관의 공동체적 기능을 강화할 방안 제시
- 등등등 더 써보시요 
