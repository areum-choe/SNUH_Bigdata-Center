### 프로젝트 내용

미국 중환자실 데이터(MIMIC) 과 원내 데이터(CDM)을 이용한 해열 목적으로 IV propacetamol/acetaminophen 투여한 환자들 중 혈압이 떨어지거나 승압제 투여 시작 또는 요구량이 늘어난 환자들의 사망률 예측하여 논문 작성하고자 합니다. (테이블 생성 진행 중)

Population :
해열목적으로 Acetaminophen IV , Propacetamol IV 투여 이후,
6시간 이내 혈압이 떨어지거나 승압제 투여 시작 또는 요구량이 늘어난 환자

- ***세부조건***
    1. 체온>37.1 인 발열환자
    2. AAP, PPA 투여는 IV, 발열 후 6시간 이내
    3. AAP, PPA 투여 이후 6시간 이내 혈압측정값이 있는 환자
    4. 승압제 : Norepinephrine, Epinephrine, Dopamine, Dobutamine, Vasopressin
    5. mimic인 경우 ICU입실 중 AAP, PPA IV 투여
    6. 혈압측정방법 : mimic에서 다루는 혈압측정방법 전체
- ***5기준 중 1개 이상 만족하는 경우 hypotension***
    1. 이전 24시간 승압제 X, AAP iv 이후 6시간 이내 승압제 O
    2. 이전 24시간 승압제 O, AAP iv 이후 6시간 이내 승압제 O, 요구량 증가
    3. AAP iv 이후 6시간 이내 첫측정 SBP < 90mmHg
    4. AAP iv 이후 6시간 이내 첫측정 MBP < 65mmHg
    5. AAP iv 직전 SBP - AAP iv 이후 6시간 이내 첫측정 SBP ≥ 30mmHg

### 담당 업무

1️⃣ SQL을 이용한 CDM & MIMIC 데이터 추출 

1.1 위 세부 조건에 맞는 MIMIC데이터 추출 

1.2 위 세부 조건에 맞는 CDM데이터 추출(진행중)

2️⃣  Python을 이용한 폐혈증(SEPSIS) 환자 판단 함수 작성

2.1 SOFA SCORE, QSOFA SCORE 계산

2.2 +SAPS2 SCORE계산 함수 작성

3️⃣ R을 이용한 PS matching(Propensity Score matching) 성향 점수 매칭진행

3.1 혈압이 떨어진 그룹과 떨어지지 않은 그룹의 PSM진행(matchit함수 사용)
