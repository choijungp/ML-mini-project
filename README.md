## ML-mini-project

#### Step 1) Overfitting을 잡아라 !!

* 방법 1 : 단일 알고리즘 사용    
  RandomForest      
  DecisionTree   
  XGBoost    
  LGB    
  LightLGB     
  GradientBoost   
   
  
* 방법 2 : 단일 알고리즘에서 성능 좋은 것들을 뽑아 앙상블
  Stacking      
  Voting(soft)   
  GridSearch CV     
  Blending     
  
* 방법 3 : AutoML 사용


#### Step 2) 최고의 성능을 위한 데이터 가공
* 필요한 컬럼 추출
* 새로운 컬럼 창출


#### Step 3) 생성한 모델로 4월달 결과를 예측
----------------------------------------

### Dataset1.  (2022.04.19 14:00)
* 추가한 컬럼
  + 스타팅멤버 컬럼 추가 - 당 선수가 5세트 중 3세트 미만으로 참여할 시 0, 이상 참여할 시 1
  + 팀득점 - 해당 날짜에 해당 팀이 넣은 총 득점 수
  + 득점점유율 – 개인 득점수 / 팀득점
  + 참여게임수 – 해당 선수가 해당 팀에서 참여한 게임의 수
  + 승리횟수 – 해당 선수가 해당 팀에서 참여한 게임 중, 승리한 횟수
  + 개인 승률 – 참여게임수 / 승리횟수

* One Hot Encoding한 컬럼
  + 이름, 팀명, 포지션

* 경기날짜는 index로 변경
* 결과 : 8116 rows * 259 columns

### STep 2. 단일 알고리즘 돌리기
