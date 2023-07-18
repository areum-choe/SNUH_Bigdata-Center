# readme

# 2023 Datathon baseline model

### 대회 주제

COVID-19확진 환자의 기관내삽관 및 High Flow System (HFS) 시행여부를 예측하는 인공지능 모델 개발

### Data소개

Table

- id(n) : 871명 (id 800 – 코로나 음성이므로 제거)
- Category : 81개
Info(5)
O2demand(1)
Underlying(9)
Outcome(1)
Vital(6)
Lab(59)

### Model Structure

- 전처리 내용 - Table
Outcome 2인 8명 탈락 (id : 871 → 863)
Age, Sex → One-Hot encoding
결측치→ train data의 mean
값이 너무 적은 항목 탈락 (column : 81 → 76)

![Untitled](https://user-images.githubusercontent.com/81748349/229706759-df02bd17-3dc6-4841-9905-6cc98cfd3d6b.png)

### Model Result

Result 요약

- Train : Test = 7 : 3 = 582 : 250
- 각 결과 Accuracy 요약

![Untitled (1)](https://user-images.githubusercontent.com/81748349/229707036-d2b57ee0-bca6-40b3-9761-65c4bd8dec63.png)

### Model result

![Untitled (2)](https://user-images.githubusercontent.com/81748349/229707111-d16a606c-3208-40a6-abbf-7355efc5cfe3.png)
![Untitled (3)](https://user-images.githubusercontent.com/81748349/229707152-dc1445d5-2d9d-433d-8c77-d620f96a4b19.png)
