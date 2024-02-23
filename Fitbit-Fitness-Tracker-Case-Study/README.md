# FitBit Fitness Data Analysis (Capstone Design Project)

## 프로젝트 소개

이 프로젝트는 [Google Data Analytics Professional Certificate](https://www.coursera.org/professional-certificates/google-data-analytics) 과정의 최종 프로젝트인 캡스톤 스터디의 일환으로 진행되었습니다. 

### 프로젝트 목적: FitBit 유저 데이터 분석을 통한 유저 경험 개선 전략 수립

## 프로젝트 개요

### 1. 비즈니스 문제 (개념설계)
- 지금보다 한 단계 더 효율적인 마케팅 전략 수립을 위해 당사의 스마트 기기 사용 데이터를 분석하여 유저들의 서비스 이용에 대한 통찰을 얻고자 한다.
- 이를 위해 타사(FitBit)의 스마트 제품 사용 동향을 먼저 파악하고, 여기서 얻은 통찰을 당사의 제품에 적용하고자 한다.
    1) **유저들의 스마트 기기 사용 트렌드가 어떻게 되는가?**
    2) **이러한 트렌드를 당사 제품에 적용해 유저 경험을 어떻게 개선해볼 수 있을까?**

### 2. 데이터
- 본 프로젝트에서는 FitBit 피트니스 트래커([FitBit Fitness Tracker Data](https://www.kaggle.com/datasets/arashnic/fitbit))의 데이터를 사용한다.
- 이 데이터는 30명의 핏빗 유저들의 1분 당 활동기록, 심박수, 수면 모니터링 기록 등을 포함한다.

### 3. 데이터 처리
- 코드 본문 참조

### 4. 데이터 분석 결과

#### 결과 1. 유저들은 대부분의 시간을 '무활동' (Sedentary) 상태로 보낸다.
유저들의 활동 유형을 아래 네 가지로 분류해서 유형별 활동시간을 확인했다.

1. VeryActive: 고활동
2. FairlyActive: 중간활동
3. LightlyActive: 저활동
4. Sedentary: 무활동

무활동 (Sedentary) 시간이 가장 높은 것으로 확인된다 (그림1). 

<그림1. 네 가지 활동 유형별 시간>
![image](https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/46d9dce3-1c30-415f-a2be-a8497c56041c)

#### 결과 2. 활동 강도가 높을수록 칼로리 소모와 활동시간의 뚜렷한 상관관계가 확인된다.

활동 유형별로 사용되는 시간과 칼로리 소모량의 관계를 확인했다. 

- **칼로리 소모 ~ 고활동: 0.22**
- **칼로리 소모 ~ 중간활동: 0.58**
- 칼로리 소모 ~ 저활동: 0.06
- 칼로리 소모 ~ 무활동: -0.04

고활동, 중간활동 유형에서 활동시간과 칼로리 소모의 뚜렷한 상관관계가 확인되었다 (그림2).

걸음수와 칼로리 소모의 뚜렷한 상관관계를 고려할 때 (그림3), 칼로리 소모는 걸음수 + 걸음 강도(고활동 + 중간활동)와 관련이 있는 것으로 추정된다. 

<그림2. 네 가지 활동 유형별 칼로리 소모량과의 상관관계>
![image](https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/7b1a78c5-af43-4aa3-b6ab-06cfd107d43b)
![image](https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/6c7f928c-81b2-432a-b595-fdcc4e5634e8)

<그림3. 걸음수와 칼로리 소모의 상관관계>
![image](https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/09f010a6-71cd-4bac-b473-06190b5bb315)

#### 결과 3. '무활동' (Sedentary) 상태가 길어질수록 수면시간이 감소한다.

가만히 앉아있는 '무활동' (Sedentary) 시간과 총수면시간의 뚜렷한 부적 상관관계를 확인했다 (그림4).
- 수면시간 ~ 고활동: 0.16
- 수면시간 ~ 중간활동: 0.21
- 수면시간 ~ 저활동: 0.37
- **수면시간 ~ 무활동: -0.77**

<그림4. 네 가지 활동 유형별 수면 시간과의 상관관계>
![image](https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/dec21f00-076b-4da3-a339-d30fcc106170)
![image](https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/a1bafbcf-3e29-4a27-a5ea-ec2b9ce5d68f)

#### 결과 4. '누워있는 시간'에 비해 '수면시간'이 떨어지는 유저들이 존재한다.

수면의 질을 평가할 때 누워있는 시간 대비 실수면시간이 중요한 지표로 작용한다. 실수면시간이 떨어지는 경우, 불면증, 스트레스 등이 원인이 될 수 있기 때문이다. 
따라서 bed-to-sleep-ratio 라는 변수를 생성하여 수면의 질을 평가하는 지표로 사용하였다. 

누워있는 시간 대비 수면 시간이 낮은 사람들이 확인된다(그림5).
이들은(=8명/24명; 33.3%) 수면시간/누워있는시간 비율이 86% 이하인 경우를 의미한다. 8시간을 누워있다고 할 때 실제 수면시간은 대략 7시간 미만인 셈. 

<그림5. 누워있는 시간 대비 수면시간의 비율>

![image](https://github.com/dchlseo/Data-Science-Portfolio/assets/70427747/67dec453-91bd-44a6-90f1-aba779cf8bbb)


### 5. 액션플랜
활동 유형에 따라 유저별로 특화된 프로그램을 제안할 수 있다.

| 활동 유형별 집단  | 전략              |
|----------------|------------------|
| 고활동 (Very Active) | 고활동 시간 유지를 위한 활동 유지 챌린지 |
| 중간활동 (Fairly Active)   | 활동량 증가를 위한 목표 설정 및 루틴 제안, 모니터링 알림 서비스 |
| 저활동 (Lightly Active)             | 초기 운동습관 형성을 위한 건강 정보 및 가이드 제공  |
| 무활동 (Sedentary)             |운동부족으로 인한 체중 증가 위험 및 수면 시간 단축 데이터 제공 및 일상 속 간단한 활동 증가 유도 알림 서비스|


또한, bed-to-sleep-ratio가 낮은 집단(<= 0.7)을 위한 수면습관 설문지 및 수면의 질 개선 서비스도 고려해볼 수 있겠다.
- 수면 건강 정보 제공 (불면증 위험, 스트레스/불안 관리)
- 수면 시간 설정 알림 서비스
- 수면 전 명상 프로그램
- 수면 일기쓰기

