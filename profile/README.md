# 지역정치 다양성 시각화
저희 프로젝트는 자동 데이터 수집과 웹사이트 개발을 통해 지역정치의 다양성을 시각화하고 증진하는 데 주력하고 있습니다.
각 리포지토리의 작동방식은 리포지토리 README에서 확인하실 수 있어요!
## 🙋‍♀️ 0. 목적
지역 대표자들은 자치단체 내에서 예산, 규제, 행정 감독을 관리하는 중요한 역할을 합니다. 많은 정치인들은 전통적인 정치의 틀을 깨고 다양한 인구들의 복지를 위해 도전적으로 독립적으로 운영하거나 기존의 정치 구조에 도전하기 위해 출마합니다.

대략 226개 지방자치단체의 3,000명의 의회원과 17개 광역자치단체의 900명 대표는 우리 지역을 형성하는 데 중요한 영향력을 가지고 있습니다. 뉴웨이즈는 재산, 현재 정치 소속, 공식 출장 기록과 같은 영역에 초점을 맞추어 다양한 시민 단체들의 주목을 끌고자 합니다.

뉴웨이즈의 모토인 "다양한 개인들의 다양한 의사결정이 정치를 더 나게 만든다"는 우리의 미션을 이끌고 있습니다. 그러나 2010년부터 2022년까지의 네 차례의 지방 선거 결과를 분석해보면 당선된 정치인 중 48%가 50대, 72%가 남성이며 88%가 정당 소속임을 알 수 있습니다. 뉴웨이즈는 특히 젊은 정치인의 부족에 중점을 두어 이것을 해결하고 시민들과 연결하여 플랫폼을 구축하고자 합니다.

## 👩‍💻 1. API-scrap-and-analysis
### 1-1. 모든 선출단위에 대한 공직자 변동 자동 추적
- BeautifulSoup 및 Selenium을 사용한 웹 크롤링.
- 각 웹사이트에 대한 크롤링 함수 생성.
- 5815줄의 코드.
- BeautifulSoup
  - 각 웹사이트에 대한 개별 함수로 쉬운 유지보수.
  - 유사한 웹사이트는 하나의 함수를 여러 태그로 공유하여 쉬운 유지보수.
- Selenium
  - BeautifulSoup이 처리하지 못하는 부분을 처리.
- 자동 실행
  - (TKTKTK> 기연님 부탁해요!)
### 1-2. 나이 히스토그램 데이터 생성
- 나이를 기준으로 5개의 동일한 크기의 하위 그룹으로 그룹화하고, 첫 번째 및 마지막 백분위를 계산합니다.

## 🧙 2. Backend-python
React와의 호환성을 보장하기 위해 MongoDB 데이터를 백엔드에서 관리.

## 🌈 3. Frontend
- 빠른 비교 및 상호 작용을 위한 지도.
- 연도 및 지역에 대한 빠른 탐색을 위한 사용자 친화적인 드롭다운 메뉴.
- 종합적인 시각화를 위한 차트 및 텍스트의 결합.
- 시각적 명확성을 위한 연령 분할.

이 플랫폼을 자유롭게 탐험해 보세요. 우리는 지역 정치에 투명성과 다양성을 제공하기 위해 노력하고 있습니다!

# Visualizing Diversity in Local Politics
Our project is dedicated to visualizing and promoting diversity in local politics through automatic data collection and website development.
You can find the operation details of each repository in the respective repository README!
## 🙋‍♀️ 0. Purpose
Local representatives play a crucial role in managing budgets, regulations, and administrative oversight within their communities. Many politicians run for office to break the mold of traditional politics, advocating for the well-being of diverse populations, running as independents, and challenging established political structures.

With approximately 3,000 council members across 226 local government units and 900 representatives in 17 metropolitan regions, these officials have the power to shape our communities. NewWays seeks to draw attention from various civic organizations by focusing on areas such as property, current political affiliation, and official travel records.

Newways' motto, "Diverse decision-making by diverse individuals improves politics," drives our mission. However, analyzing the results of four local elections from 2010 to 2022 reveals that 48% of elected officials are in their 50s, 72% are male, and 88% belong to mainstream political parties. NewWays particularly emphasizes addressing the lack of young politicians, connecting them with citizens to bridge the gap and foster a platform where more people can share their concerns.

## 👩‍💻 1. API-scrap-and-analysis
### 1-1. Automated tracking of public official changes for all elected units.
- Web scraping using BeautifulSoup and Selenium.
- Creation of scraping functions for each website.
- 5815 lines of code.
- BeautifulSoup
  - Individual functions created for each website for easy maintenance.
  - Similar websites share one function with different tags for easy maintenance.
- Selenium
  - Handles what BeautifulSoup can't.
- Automated running
  - (TKTKTK> 기연님 부탁해요!)

### 1-2. Making age_histogram data
We group the age into 5 same-sized subgroups based on age, and compute the first- and last quantile too.
## 🧙 2. Backend-python
Backend management of MongoDB data to ensure compatibility with React.

## 🌈 3. Frontend
- Map for quick comparison and interactive features.
- User-friendly dropdown menus for quick exploration by year and region.
- Charts and text blended for a comprehensive view.
- Age segmentation for visual clarity.

Feel free to explore this platform, where we strive to bring transparency and diversity to local politics, one visualization at a time!
