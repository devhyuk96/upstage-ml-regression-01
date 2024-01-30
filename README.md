[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/g6ZC_OOE)
# 집값 미래를 내 손에! 예측 전략 대방출

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

![(Template)  패스트캠퍼스  Upstage AI Lab 1기_경진대회 발표자료 pptx의 사본 pptx](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/147508048/5d9c6ab4-dbe3-4f19-afea-ad6f20295be6)

![(Template)  패스트캠퍼스  Upstage AI Lab 1기_경진대회 발표자료 pptx의 사본 pptx (4)](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/147508048/aacd6d1b-aa6a-408b-b51b-6ec9d08dee90)

![(Template)  패스트캠퍼스  Upstage AI Lab 1기_경진대회 발표자료 pptx의 사본 pptx (3)](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/147508048/85150fdf-4106-4da0-a3a6-974592f16511)

![(Template)  패스트캠퍼스  Upstage AI Lab 1기_경진대회 발표자료 pptx의 사본 pptx (2)](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/147508048/752ce1e3-e684-4f46-a12c-60dc2eca35f6)

![(Template)  패스트캠퍼스  Upstage AI Lab 1기_경진대회 발표자료 pptx의 사본 pptx (1)](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/147508048/d5961dc0-bc64-44c4-b9f6-ffdc529d6dad)

- Strategy I

![(Template)  패스트캠퍼스  Upstage AI Lab 1기_경진대회 발표자료 pptx의 사본 pptx (5)](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/147508048/b3211fe9-ad74-4630-bfa0-72dc53b5c4fa)

- Strategy II
  
![(Template)  패스트캠퍼스  Upstage AI Lab 1기_경진대회 발표자료 pptx의 사본 pptx (6)](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/147508048/eb924a68-51c5-41bc-acad-ca33d926ae42)


### Data Preprocessing

- Strategy I

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/ed9f511a-4b41-4f04-a172-e35ae2082fcb)

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/6fd35ee5-e4d6-4591-bb33-633b56ce8b5b)

- Strategy II

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/e9ccdf76-1c6e-4afb-a642-5a4786ffeda1)
 
![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/6786f014-1c70-4fda-a32d-7c4cbcbe035a)

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/0eaa7c86-9cdd-47fe-8dbe-47d8403c6e8f)


### Feature engineering

- Strategy I
  
![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/e45843f4-8716-49c9-a2f9-a7adb8cdafdb)

- Strategy II

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/91efe0d5-429a-440b-b2de-f721b13da539)

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/b4329e18-621e-4cd7-af7c-6967d237b880)


## 4. Modeling

### Model description

- Strategy I

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/ec35b877-7333-4bb3-b500-4c05a8d4478d)

- Strategy II

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/d725ff11-f1f5-4a01-beca-e6fc6c2039d7)

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/aa61677a-f8e0-4d24-b482-73b38930dc74)


### Modeling Process

- Strategy I

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/8679f49f-7fce-42c6-a304-359c9f291d79)


- Strategy II

![image](https://github.com/UpstageAILab/upstage-ml-regression-01/assets/94885063/a707928f-81e2-4a46-9c2b-b3f539585884)


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
