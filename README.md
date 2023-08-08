# Youtube Clone Coding
## Introduction
Project Title : Youtube Clone Coding

Goal : HTML,CSS,Javascript를 활용하여 기존 유튜브 디자인/기능 과 유사하게 개발하여 Front의 기본 역량 향상 및 팀 프로젝트 역량 향상


Team 7-eleven : 김유진  문길호  안소윤  이정민


Team Communication : Discord , Notion

## Design
##### Home, Channel, Video 3가지 화면으로 구성

<img src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/c4ba7602-f263-4d62-9886-c2f2825c8d8f.png" width="300" height="150"/>
<img src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/2e2238ca-a424-4e26-9456-618eac39a168.png" width="300" height="150"/>
<img src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/76c1503c-3e98-4b2e-8044-00f632be139f.png" width="300" height="150"/>


##### Figma를 활용한 HTML 구조 작성 및 CSS 디자인 작업
<img width="300" height="150" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/c99f876a-6d31-42cc-8f29-f14503f5868c">
<img width="300" height="150" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/f237d1b6-3ccb-4d25-a982-7b11f54a7fd0">
<img width="300" height="150" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/8303fe8f-1f62-4914-b8b6-c492195188e5">


#### Home
- API 통해 영상 목록 불러오기
- 상단 검색 기능, 음성 인식 검색 기능
- 영상 호버 자동 재생 기능
- 로고, HOME 버튼 클릭 시 Redirection 기능
- 왼쪽 사이드바 슬라이드 및 hidden 기능

#### Channel
- 채널 화면 내 검색 기능
- 구독 버튼 동작 기능
- 인기 동영상 노출 기능

#### Video
- 구독,좋아요,댓글 기능
- 우측 영상 목록 태그에 따른 영상 노출
- AI 유사도 측정에 따른 추천 영상 기능

## Implementation
#### Home
1. 동영상 목록 업로드

    fetchData() 함수를 통해 비디오 정보를 가져오는 API를 호출하여 비디오 목록 데이터를 가져오고, 가져온 데이터를 JSON 형식으로 파싱하여 VideoList_data에 저장하고 fetchPromises 배열을 만들어서 각 비디오 정보를 병렬로 가져온 후 HTML 구조화 후 메인 컨테이너에 데이터를 추가합니다.
<p align = center><img width="500" height="250" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/bba3a5e2-cf4b-479a-acd8-7cc79c6f9192"></p>


2. 검색

    전체 동영상 리스트에서 검색어가 title,channel 정보와 비교하여 filtering 과정을 통해 search 결과를 확인 할 수 있도록 구현


    마이크 장치를 통해 검색어를 입력 받아 기존에 구현되어있는 search 함수를 통해 검색기능 동작
<p align = center> <img width="500" height ="250" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/6d0fee84-bb76-4e18-85b8-34b8fd90150e"></p>



#### Channel
1. 구독 버튼 동작

    local storage를 활용하여 구독 버튼 클릭 시 구독 목록 추가 기능 구현
<p align = center><img width="500" height = "250" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/e435510e-c4c7-4589-9217-a1dadec9d82e"></p>



2. 해당 채널 영상 검색
 
    현재 채널 화면의 data 값을 활용하여 검색어를 포함한 영상 노출 기능 구현
<p align = center><img width="500" height = "250" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/a3e6dad6-db9c-4eeb-a5bb-6a05c9675b70"></p>


#### Video
1. 댓글

    local storage를 활용하여 구독 버튼 클릭 시 구독 목록 추가 기능 구현

<p align = center><img width="500" heigth = "250" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/c47fec57-a989-4888-ac5b-73e9314452ca"></p>


2. 연관 태그 영상 노출
   
    API를 통해 동영상 목록을 불러오며 해당 비디오와 동일한 채널, 포함 태그를 통한 filtering 과정을 통해 관련 태그와 영상 목록 노출

<p align = center><img width="500" height = "250" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/e177b9d9-0bc8-4662-a10a-8ad94cd64ef2"></p>


3. AI 추천 영상
   
    AI 를 통한 유사도 측정 API 를 활용하여 현재 영상 정보를 바탕으로 AI 기반 추천 영상 목록 노출
   <p align = center><img width="500" height = "250" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/7a95d05b-73ae-4f06-8193-bb676cae553c"></p>


## Trouble Shooting
1. Git
- Git을 통한 작업 중 conflict 문제 발생

    -> 팀원들이 함께 git 활용에 대한 학습과 소통 과정을 통해 문제 해결

2. API
- Video 정보, Channel 정보에 대한 독립적인 API 구성으로 검색 기능 및 영상 로드 과정에서의 문제 발생

  -> 초기 작성한 코드 구조를 유지하는 방식으로 수정 과정

## Result
HTML,CSS,Javascript 를 활용한 기존 유튜브의 주요 기능 구현 완료

##### [Home]
<p align = center><img width="700" height = "350" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/3609ae43-f601-4d7e-ba7c-02468342a140"></p>

##### [Channel]
<p align = center><img width="700" height = "350" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/7d15e753-c31e-4ad2-8f5b-4cdc340c4dee"></p>

##### [Video]
<p align = center><img width="700" height = "350" alt="image" src="https://github.com/jmlee0527/Youtube-Clone/assets/115601680/8ba68e9a-550e-4fc1-b06b-f2e169407a4d"></p>




