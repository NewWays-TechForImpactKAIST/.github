# 🥰
# 지역정치 다양성 시각화
저희 프로젝트는 자동 데이터 수집과 웹사이트 개발을 통해 지역정치의 다양성을 시각화하고 증진하는 데 주력하고 있습니다.
각 리포지토리의 작동방식은 리포지토리 README에서 확인하실 수 있어요!
## 🙋‍♀️ 0. 목적
지역 대표자들은 자치단체 내에서 예산, 규제, 행정 감독을 관리하는 중요한 역할을 합니다. 많은 정치인들은 전통적인 정치의 틀을 깨고 다양한 인구들의 복지를 위해 도전적으로 독립적으로 운영하거나 기존의 정치 구조에 도전하기 위해 출마합니다.

대략 226개 지방자치단체의 3,000명의 의회원과 17개 광역자치단체의 900명 대표는 우리 지역을 형성하는 데 중요한 영향력을 가지고 있습니다. 뉴웨이즈는 재산, 현재 정치 소속, 공식 출장 기록과 같은 영역에 초점을 맞추어 다양한 시민 단체들의 주목을 끌고자 합니다.

뉴웨이즈의 모토인 "다양한 개인들의 다양한 의사결정이 정치를 더 나게 만든다"는 우리의 미션을 이끌고 있습니다. 그러나 2010년부터 2022년까지의 네 차례의 지방 선거 결과를 분석해보면 당선된 정치인 중 48%가 50대, 72%가 남성이며 88%가 거대 양당 소속임을 알 수 있습니다. 뉴웨이즈는 특히 젊은 정치인의 부족에 중점을 두어 이것을 해결하고 시민들과 연결하여 플랫폼을 구축하고자 합니다.

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
- [실행 방법](https://github.com/NewWays-TechForImpactKAIST/API-scrap-and-analysis/pull/77)
  - API-scrap-and-analysis 외의 리포지토리는 모두 자동 실행 
  - 2개의 쉘 스크립트: `install.sh`, `run_scrap_scripts.sh`
  - `install.sh` 스크립트를 통해 파이썬 가상환경, Chromedriver 등 초기 셋업 진행
  - 이후 crontab에 `run_scrap_scripts.sh`를 등록해 스크랩 및 DB 연동 자동화
  - 예시: `0 3 * * 0 ~/API-scrap-and-analysis/run_scrap_scripts.sh`

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

# 링크 (Links)
- 현 테스트 링크 : https://diversity.tech4impact.kr/
- 백엔드 명세서 : https://diversity-api.tech4impact.kr/docs
- [DB다이어그램](https://dbdiagram.io/d/TFI-DB-Design-652b8164ffbf5169f0b3215b)
- [API 엔드포인트 명세서](https://tech4impact.notion.site/API-Endpoints-056e342c240b495390b71546af4ed5d3?pvs=4)
- [[뉴웨이즈] 기초의회 연령/성별 다양성 지수 평가](https://docs.google.com/document/d/1zDRcU9ytQJv-7DPrxgRqOsd4_tevCYVfspJO1eKLzfc/edit)
- [아이디어 미로보드](https://miro.com/app/board/uXjVNTg6e24=/)
- [Figma 파일](https://www.figma.com/file/Dh9nytTfbib9qGI56Ddw6F/NewWays-%EB%8B%A4%EC%96%91%EC%84%B1-%ED%8F%89%EA%B0%80-%EB%A6%AC%ED%8F%AC%ED%8A%B8?type=design&node-id=98-49&mode=design )
# 참여자 (Contributors)
| 📛 Name        | 📧 Email (@kaist) | 🐈‍⬛ GitHub     | 역할             |
|--------------|-------------------|----------------|------------------|
| 박건         | geon.park00       | Re-st          | 팀장(팀 외부 소통), 기초의원 크롤링, 정부API DB화, 나이통계, DB수정, 웹에 표현할 글 내용 설계  |
| 손성민        | soungmin          | happycastle114 | 백엔드 설계/포팅, 기초의원 크롤링, 직업통계, API 엔드포인트 구상, URL 라우팅, 히스토그램/맵셀렉터 제작, 웹디자인  |
| 송준혁        | songmhrm          | songc04        | 히스토그램/맵셀렉터 제작, 프론트엔드 구현 전반       |
| 이기연        | keonl             | keonly         | 기초의원 크롤링, 스크랩 → MongoDB 연동, 다양성지표 조사 및 수기 테스트, 크론잡, 실행마다 결과 정리해 웹훅으로 슬랙앱 알림되도록 제작, 코드 정리  |
| 이희원        | pingpingy         | pingpingy1     | 기초/광역/국회의원 크롤링, 다양성지표 비교, 다양성지수 및 순위 계산, DB 설계 및 수정, 백엔드서버 구축, API 엔드포인트 구상  |
| 정상         | withsang          | withSang       | 파이썬 가상환경 + 깃헙구조 + 자동배포 설계, 서버 + 웹 주소 제공 및 배포, API 엔드포인트 구상, 제품요구사항 정의, React 구조설정, 히스토그램 제작, 웹디자인, 웹에 표현할 글 내용 설계, 회의록 작성    |
## 컨설팅
- JAY (카카오 크루) : 기술적 조언, 진행방식 지도, 레퍼런스 권유
- 박혜민 대표님 (뉴웨이즈) : 유저 페르소나 공유, 방향 지도
- 류석영 교수님 : 방향 지도 

# 데모 (Demo)


Uploading diversity-demo.mp4…


# Visualizing Diversity in Local Politics
Our project is dedicated to visualizing and promoting diversity in local politics through automatic data collection and website development.
You can find the operation details of each repository in the respective repository README!
## 🙋‍♀️ 0. Purpose
Local representatives play a crucial role in managing budgets, regulations, and administrative oversight within their communities. Many politicians run for office to break the mold of traditional politics, advocating for the well-being of diverse populations, running as independents, and challenging established political structures.

With approximately 3,000 council members across 226 local government units and 900 representatives in 17 metropolitan regions, these officials have the power to shape our communities. NewWays seeks to draw attention from various civic organizations by focusing on areas such as property, current political affiliation, and official travel records.

Newways' motto, "Diverse decision-making by diverse individuals improves politics," drives our mission. However, analyzing the results of four local elections from 2010 to 2022 reveals that 48% of elected officials are in their 50s, 72% are male, and 88% belong to two major political parties. NewWays particularly emphasizes addressing the lack of young politicians, connecting them with citizens to bridge the gap and foster a platform where more people can share their concerns.

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
- [How to Run](https://github.com/NewWays-TechForImpactKAIST/API-scrap-and-analysis/pull/77)
  - Repositories other than API-scrap-and-analysis are fully automated.
  - Two shell scripts: `install.sh` and `run_scrap_scripts.sh`.
  - The `install.sh` script handles initial setup, including creating a Python virtual environment and installing Chromedriver.
  - Subsequently, `run_scrap_scripts.sh` is registered in crontab for automatic scraping and database integration.
  - Example crontab entry: `0 3 * * 0 ~/API-scrap-and-analysis/run_scrap_scripts.sh`

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
