# 처음 하는 개인 프로젝트 

# 프로젝트 주제 : 스마트 스토어 마케팅 전략 을 위한 어플 개발
## 기간 : 2023/03/01 ~ 2023/03/02
[PPT 자료](https://github.com/Kwanghyun97/YSedu_personal_Project/blob/289238620a151c276e82b5fef36dec811cb714e7/%ED%82%A4%EC%9B%8C%EB%93%9C%20%ED%8A%B8%EB%9E%9C%EB%93%9C%20%ED%8C%8C%EC%95%85%EC%9D%84%20%EC%9C%84%ED%95%9C%20API%20%EB%A7%8C%EB%93%A4%EA%B8%B0%20(1).pdf) <br/><br/>


## 목적
계약일 기준 2022년 1월 1일부터 현재까지의 **서울시 전/월세 실거래 데이터 기반 검색** 및 **전세 시세 예측** 웹 개발

## 데이터
서울 열린데이터 광장 - 서울시 부동산 전월세가 정보 공공 데이터를 이용하였습니다.

[서울시 부동산 전월세가 정보](https://data.seoul.go.kr/dataList/OA-21276/S/1/datasetView.do)

## ERD
![screensh](img/erd.png)

## 팀 구성
- 사용언어 : Python : 3.9.13v
- 작업툴 : VS code
- 인원 : 4명
- 주요 업무 : Streamlit 라이브러리를 이용한 웹개발 구현 코드 작성 및 머신러닝을 활용한 전세 시세 예측
- 기간 : 2023-01-30 ~ 2023-02-10
***

## 주요 기능
- 홈페이지
    - 실거래 현황(매일 갱신)
- 전월세 검색페이지
    - 해당구, 해당동, 전/월세 구분 검색
    - 보증금, 월세, 임대면적 슬라이더 검색
- 전세 예측페이지
    - 지역 선택 후 날짜에 따른 보증금 막대그래프로 시각화
    - 날짜 선택 후 지역구별 평균 실거래가 지도 시각화
    - 전세 월평균, 월세 월평균 추이 꺾은선그래프 시각화
    - 월세, 전세 실거래 수 지역 순위 막대그래프 시각화
    - 지역구 선택 후 전세 예측 모델 시각화
- 건의사항페이지
    - 게시판 작성자, 이메일, 제목, 내용 저장을 위한 db 구축
    - 문의 내용 작성칸 구축
    - 게시판 목록 구현
    - 관리자모드
        - 처리상태 변경

## 설치 방법
### Windows
+ 버전 확인
    - vscode : 1.74.1
    - python : 3.9.13
    - 라이브러리 :  pandas (1.5.3), numpy (1.24.1), plotly (5.13.0), matplotlib (3.6.3), streamlit (1.17.0), streamlit-option-menu (0.3.2), geopandas (0.12.2), pandas-gbq (0.19.1), pydeck (0.8.0), stqdm (0.0.5), prophet (1.1.2), seaborn (0.12.2), openai (0.26.5), streamlit_chat (0.0.2.1), requests (2.28.2v), tensorflow(2.9.0), scikit-learn(1.2.1)

- 프로젝트 파일을 다운로드 받습니다. 

```bash
git clone https://github.com/SeungKyu37/project2.git
```

- 프로젝트 경로에서 가상환경 설치 후 접속합니다. (Windows 10 기준)
```bash
virtualenv venv
source venv/Scripts/activate
```

- 라이브러리를 설치합니다. 
```bash
pip install -r requirements.txt
```

- streamlit 명령어를 실행합니다. 
```bash
streamlit run app.py
```

# 내방 어디? v2(2023.02.02~)

## 주요 기능 업데이트 내용
- 홈페이지
    - 실거래 현황(최근 한달순)
    - 전세 월평균, 월세 월평균 추이 꺾은선그래프 **시각화**
    - 월세, 전세 실거래 수 지역 순위 막대그래프 **시각화**
- 전월세 검색페이지
    - 전/월세 구분 검색 중 모두 검색할 수 있도록 **추가**
    - 보증금, 월세, 임대면적 최소/최대값 정해줄 수 있도록 **추가**
    - 보증금, 월세, 임대면적 최소/최대값과 슬라이더값 **동기화**

- 전세 예측페이지
    - 날짜 선택 후 지역구별 평균 실거래가 지도 **시각화**

- 건의사항페이지
    - 처리 상태 **추가**
    - 빈칸 입력시 에러메시지 **추가**
    - 관리자 기능
        - 처리 상태 변경 기능 **추가**
    - 검색 기능
        - 제목, 작성자명, 내용에 같은 내용 검색 기능 **추가**
        
# 내방 어디? v3(2023.02.07~)

## 주요 기능 업데이트 내용
- 홈페이지
    - 전세 월평균, 월세 월평균 추이 꺾은선그래프 **삭제**
    - 월세, 전세 실거래 수 지역 순위 막대그래프 **삭제**
    - 실거래 현황 매일 오후 10시 실제 데이터 **갱신**

- 전세 예측페이지
    - 전세 월평균, 월세 월평균 추이 꺾은선그래프 **시각화**
    - 월세, 전세 실거래 수 지역 순위 막대그래프 **시각화**
    - 날짜 선택 후 지역구별 평균 실거래가 지도 **시각화**
    - 지역구 선택 후 전세 예측 모델 **시각화**
        - Prophet 모델
        - LSTM 모델
    - 전월세 전환율 **추가**
        - 전세 -> 월세
        - 월세 -> 전세
        - 전환율 계산
    - 대출이자 계산기 **추가**
        - 원리금균등상환 계산
        - 원금균등상환 계산
        - 원금만기일시상환 계산
- 챗봇 
    - chat gpt api를 활용한 챗봇 **추가**
    - 부동산 데이터 연계해 챗봇 **활용**
- 건의사항
    - 자주 묻는 질문 **추가**
    - 게시글 수정 기능 **추가**
    - 게시글 삭제 기능 **추가**
- 업데이트
    - 최신 부동산 데이터 **업로드**
    - 매일 오후 10시 데이터 **갱신**
        - why? 서울 열린데이터 광장 데이터 오후 9시 갱신
        - 배치 파일 사용
- 평균 함수화
    - 구별 전세 일 평균 **함수화**
    - 구별 전세 월 평균 **함수화**
    - 구별 월세 일 평균 **함수화**
    - 구별 월세 월 평균 **함수화**
    - 동별 전세 일 평균 **함수화**
