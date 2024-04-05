# predict-delinquency
포스코 Ai·Big data 아카데미 24기 1차 프로젝트 

## Feature Engineering
+ CustomerId: 고객 ID
+ Gender: 성별
+ Age: 연령(년)
+ Education: 교육수준
+ MaritalStatus: 결혼상태
+ FamilyCount: 가족수
+ ChildCount: 자녀수
+ IncomeType: 수입 형태(유형)
+ IncomeClass: 수입등급(년)
+ Occupation: 고객 직업군
+ OrgType: 직장유형
+ EmployedYears: 근속년수(년)
+ HouseOwnerdYN: 주택 소유 여부(Y,N)
+ ResideneClass: 주거등급
+ HouseAge 주택 나이(년) - 결측치 많음
+ CarOwnerdYN: 대출신청 차량 외 자동차 소유 여부
+ LoadId: 고객대출ID
+ Default: 대출 상환여부(Y,N)
+ ActiveLoanYN: 대출 신청 당시 활성 대출 유무
+ LoanType: 대출유형(할부금융,오토론)
+ ApplWeek: 대출신청요일(월~금)
+ ApplHour: 대출신청시간대
+ Accompany: 대출 신청시 동행자
+ CarPrice: 차량 가격
+ Deposit: 현금비율
+ LoanTerm: 대출기간
+ LoanRemainTerm: 대출잔여기간
+ InterestType: 금리유형(고정, 변동, 혼합)
+ InterestRate: 대출금리
+ LoanAmount: 대출금
+ InstallAmount: 월납입액
+ LoanRemainAmount: 대출잔액
+ HomeAddMatchedYN: 집주소 일치 여부
+ WorkAddMatchedYN: 직장주소 일치 여부
+ InquiryCount: 대출 전년도 문의건수(건)
+ IdChangedYears: 신분증 변경 후 경과기간
+ InfoChangedYears: 고객정보 변경 후 경과기간
+ PhoneChangedYears: 휴대전화 변경 후 경과기간
+ ScoreA: 신용점수(A사)
+ ScoreB: 신용점수(B사)
+ ScoreC: 신용점수(C사)

## 핵심 Model
+ category feature의 전처리가 필수적으로 중요
+ **CatBoost**를 활용하여 category feature들을 지정하여 모델의 성능을 높힘
+ LightGBM, XGBoost와 비교 후 더 나은 성능을 보임

## Hyperparameter 전략
+ Lightgbm, XGBoost, CatBoost 경우 조기 중단 예측 파라미터 튜닝 
+ RandomForest와 GradientBoosting 모델은 직접 하이퍼파라미터 튜닝
+ 최단시간에 최고효율이 나오게끔 함

## 신용평가 모델 구축 전략
+ DT 모델 기반 변수 중요도 결과 기반 변수 가중치 설정
+ DT 그래프 구조 분석으로 변수별 값에 대한 가중치 설정 

## Award
Passion-Award
