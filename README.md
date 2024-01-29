[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/g6ZC_OOE)
# Title (집값 미래를 내 손에! 예측 전략 대방출)

## Team
<table>
  <tr>
    <td> <div align=center> 👑 </div> </td>
    <td> <div align=center>  1 </div> </td>
    <td> <div align=center>  2 </div> </td>
    <td> <div align=center>  3 </div> </td>
  </tr>
  <tr>
    <td> <div align=center> <b>서상혁</b> </div> </td>
    <td> <div align=center> <b>김도연</b> </div> </td>
    <td> <div align=center> <b>김다운</b> </div> </td>
    <td> <div align=center> <b>신동혁</b> </div> </td>
  </tr>
  <tr>
    <td> <img alt="Github" src ="https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/a4dbcdb5-1d28-4b91-8555-1168abffc1d0" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/3d913931-5797-4689-aea2-3ef12bc47ef0" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/0f945311-9828-4e50-a60c-fc4db3fa3b9d" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/c4cb11ba-e02f-4776-97c8-9585ae4b9f1d" width="250" height="300"/> </td>
  </tr>
  <tr>
    <td> <div align=center> <a href="https://github.com/S-RSH"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href="https://github.com/d-yeon"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href="https://github.com/Daw-ny"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href="https://github.com/HyeokHam"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    </tr>
</table>
      
## 1. Competiton Info

### Overview

- 다양한 부동산 관련 의사결정을 돕고자 하는 부동산 실거래가를 예측하는 모델을 개발하는 것
- 서울시 한정 아파트 가격 예측
- 정확하고 일반화된 모델을 개발하여 아파트 시장의 동향을 미리 예측하는 것

### Timeline

- Jan 08 ~ 14, 2024 - Making A Group
- Jan 15, 2024 - Start Competition
- Jan 15 ~ 20, 2024 - Data Collection
- Jan 18 ~ 21, 2024 - Data EDA
- Jan 21 ~ 25, 2024 - Modeling & Tuning
- Jan 25 ~ 26, 2024 - Report Writing

### Evaluation

- RMSE 지표를 활용
  
  ![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/5cfa5fdc-7256-4972-98af-f15ad54f8361)


## 2. Components

### Directory

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/cc50aae1-aebd-4fe0-8d1e-30f6c576b236)


## 3. Data descrption

### Dataset overview

주요 데이터는 .csv 형태로 제공되며, 서울시 아파트의 각 시점에서의 거래금액(만원)을 예측하는 것이 목표입니다.

학습 데이터는 아래와 같이 1,118,822개이며, 예측해야 할 거래금액(target)을 포함한 52개의 아파트의 정보에 대한 변수와 거래시점에 대한 변수가 주어집니다.

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/9c3d2f9e-ac4c-4f1f-be3c-3f2447dfcc9a)

학습 데이터의 기간은 2007년 1월 1일부터 2023년 6월 30일까지이며, 각 변수 명이 한글로 되어있어 어떤 정보를 나타내는 변수인지 쉽게 확인할 수 있습니다.

예시)
> - 시군구 : “서울특별시 강남구 개포동” 과 같이 주소에 대한 정보입니다.
> - 아파트명 : “개포더샵트리에”와 같이 아파트명에 대한 정보입니다.
> - 전용면적(㎡) : “108.2017”와 같이 매매대상의 전용면적에 대한 정보입니다.
> - 건축년도 : “2021”과 같이 아파트의 건축 연도를 나타내는 정보입니다.

각 변수들은 아래와 같은 결측치 비율을 가지고 있습니다.

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/a4ba70e3-f9f2-47dd-8d3f-aae5ad104bac)

아파트의 매매가를 결정하는데에 교통적인 요소가 영향을 줄 수 있기에 추가 데이터로 서울시 지하철역, 서울시 버스정류장의 정보가 주어집니다. 

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/d1f86dad-e331-4a13-b010-bcb2cbd63312)

추가 데이터는 위도와 경도, 좌표 X와 좌표Y와 같이 거리에 대한 정보가 포함되어 있으며, 이를 활용하여 학습 데이터와 함께 사용할 수 있습니다. 

### EDA

- _Describe your EDA process and step-by-step conclusion_

### Feature engineering

- _Describe feature engineering process_

## 4. Modeling

### Model descrition

- _Write model information and why your select this model_

### Modeling Process

- _Write model train and test process with capture_

## 5. Result

### Leader Board

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/76687996/d687d43e-b43c-4ba3-abb3-cab2f925b939)


### Presentation

- [1조 minus의 ppt](https://docs.google.com/presentation/d/1LmVvBo0ZpkWONN22q8OppNOOL5F3Ds9N/edit)

## etc

### Meeting Log

- 전체적인 내용은 [Notion](https://www.notion.so/1-c35e90521c3e445888e2218d9871acf5)에서 확인하실 수 있습니다.
- Jan 21 ~ Jan 26 : Offline Meeting

### Reference

- [서울시 역사마스터 정보](https://data.seoul.go.kr/dataList/OA-21232/S/1/datasetView.do)
- [아파트 브랜드 top24](https://brikorea.com/bbs/board.php?bo_table=rep_1&wr_id=2584&sfl=wr_subject&stx=%EC%95%84%ED%8C%8C%ED%8A%B8&sop=and)
- [선거 지지율 기사](https://www.joongang.co.kr/article/25055110#home)
- [학군 기사](https://www.sentv.co.kr/news/view/669378)
- [학교별 학급수](https://www.schoolinfo.go.kr/ng/go/pnnggo_a01_l2.do)
- [서울시 지하철 유동인구](https://data.seoul.go.kr/dataList/OA-12252/S/1/datasetView.do)
