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

![Untitled](readme%20fdf84a16fd434dc2a8f37da4b4cc59d5/Untitled.png)

### Model Result

Result 요약

- Train : Test = 7 : 3 = 582 : 250
- 각 결과 Accuracy 요약

![Untitled](readme%20fdf84a16fd434dc2a8f37da4b4cc59d5/Untitled%201.png)

### Model result

![Untitled](readme%20fdf84a16fd434dc2a8f37da4b4cc59d5/Untitled%202.png)

![Untitled](readme%20fdf84a16fd434dc2a8f37da4b4cc59d5/Untitled%203.png)