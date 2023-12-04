# 세계 테러 데이터 분석 프로젝트

## 프로젝트 개요

이 프로젝트는 전 세계 테러 데이터를 종합적으로 분석하는 것을 목표로 합니다. 주요 목적은 테러 활동의 추세, 패턴 및 영향을 이해하는 것입니다. 분석은 연도별 테러 공격 빈도, 가장 영향을 받은 국가들, 공격 유형, 그리고 이러한 사건들로 인한 사상자 수 등 다양한 측면을 다룹니다.

## 데이터 출처

이 프로젝트에서 사용된 데이터셋은 Kaggle의 [Terrorism Around the World](https://www.kaggle.com/code/ash316/terrorism-around-the-world)에서 가져왔습니다. 이 데이터셋에는 1970년부터 2017년까지의 테러 활동에 대한 자세한 기록이 포함되어 있습니다.

## 분석의 주요 특징

- **데이터 선택**: 방대한 데이터셋에서 전 세계 테러 추세의 거시적인 관점을 제공하기 위해 21개의 주요 변수를 선택했습니다.
- **연도별 추세**: 연간 테러 사건 수를 분석하여 패턴 및 활동 증가를 파악합니다.
- **지리적 초점**: 테러로 가장 큰 영향을 받은 상위 10개국을 식별하고 지역별 테러 차이를 분석합니다.
- **사상자 분석**: 테러 공격으로 인한 사망자 및 부상자 수를 전 세계적으로 및 특정 국가별로 조사합니다.
- **공격 유형**: 테러리스트들이 사용하는 다양한 공격 방법을 탐색합니다.
- **10년 단위 분석**: 1970년대부터 2010년대까지 테러가 어떻게 변화해 왔는지 살펴봅니다.

## 사용된 도구 및 라이브러리

- **Python**: 데이터 분석을 위한 주요 프로그래밍 언어.
- **Pandas & NumPy**: 데이터 조작 및 분석을 위함.
- **Matplotlib & Seaborn**: 정적 플롯 및 시각화 생성을 위함.
- **Plotly**: 인터랙티브 플롯을 위함.
- **Folium**: 지리적으로 테러 활동을 매핑하기 위함.
- **WordCloud**: 가장 두드러진 테러 그룹을 시각화하기 위함.

## 결과 요약

- 2011년 이후 테러 활동이 급격히 증가, 특히 중동, 북아프리카 및 남아시아에서 두드러짐.
- 폭탄 테러와 무장 공격이 가장 일반적인 테러 유형임.
- 테러로 가장 큰 영향을 받은 상위 10개국은 공격 유형과 사상자 수에서 다양한 패턴을 보임.

## 사용 방법

분석을 실행하기 위해서는:

1. Python이 설치되어 있고 필요한 라이브러리가 준비되어 있는지 확인하세요.
2. 저장소를 클론하고 프로젝트 디렉토리로 이동하세요.
3. Jupyter Notebook을 실행하여 분석을 확인하세요.

## 기여

제안, 토론 및 기여를 환영합니다. 저장소를 포크하고 풀 리퀘스트를 제출하세요.

## 참고자료

- [Kaggle Dataset: Global Terrorism Database](https://www.kaggle.com/datasets/sandeep04201988/worldcountries)
- [Stanford University: Mapping Militant Organizations](https://cisac.fsi.stanford.edu/mappingmilitants/profiles/islamic-state)
- [Wilson Center: Timeline of the Islamic State](https://www.wilsoncenter.org/article/timeline-the-rise-spread-and-fall-the-islamic-state)
