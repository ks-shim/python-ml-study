# CLASSIFICATION

* Decision Tree
    * 장점
        * 정보의 균일도만 신경쓰면 됨
        * 대부분 스케일링이 필요하지 않음
    * 단점
        * 트리가 깊어 질수록 과적합 가능성이 높아짐
    * 최대한 균일한 데이터 세트를 구성해야 함
        * 균일도를 측정하는 방식
            * Information Gain
            * 지니 계수
    * Information Gain
        * 균일하지 못하면 Entropy가 높음
        * IG = 1 - Entropy 지수
    * 지니 계수
        * 불평등 지수를 나타내는 계수
        * 0이 가장 평등, 1이 불평등
        * 1일 수록 균일함
  
* Ensemble (앙상블)  
    * Voting
        * 서로 다른 알고리즘을 가진 모델 결합(Voting)
        * Hard Voting
            * 다수결
        * Soft Voting
            * 확률 평균
    * Bagging
        * 같은 유형의 알고리즘, 그러나 데이터 샘플링이 상이한 모델 결합(Voting)
        * Random Forest
            * Bootstrapping 방식으로 샘플링
                * 데이터 세트를 중첩되게 분리
            * 단점
                * Hyper Parameter가 너무 많음 = 튜닝 노력이 많이 듦
    * Boosting
        * 다수의 Weak Learner를 순차 학습
        * 전 모델의 예측이 틀린 데이터는 Weight를 부여하여 후 모델의 학습 진행
        * Gradient Boosting Machine
            * Random Forest보다 대체적으로 좋은 성능, but 더 긴 수행시간
            * AdaBoost
            * Gradient Boost
                * 가중치 업데이트를 경사하강법으로 진행
        * XGBoost
            * 분류에 있어서는 뛰어남
            * 장점
                * GBM 대비 빠른 수행시간
                * 과적합 규제(Regularization)
                * Tree Pruning : 과분할 방지
                * 내장된 교차 검증, 조기 중단 기능
                * 결손값 자체 처리
        * LightGBM
            * 장점
                * XGBoost보다 훨씬 수행시가니 빠름
                * XGBoost와 유사한 성능
                * 더 적은 메모리 사용
                * GPU 지원
            * 리프 중심 트리 분할 방식 사용
                * 불균형 트리 분할 방식 = 예측 오류 손실 최소화 목적
    * Stacking
        * 메타모델 : 개별 알고리즘이 예측한 데이터를 기반으로 다시 예측 수행
        
* Sampling
    * 극도로 불균형한 레이블 값 분포로 인한 문제점 해결 필요
        * Over Sampling
            * 적은 레이블을 가진 데이터 세트를 증가 시킴
            * 원본 Feature를 약간만 변형하여 증식
                * SMOTE(Synthetic Minority Over-sampling Technique)
                    * K Nearest Neighbor를 찾아서 일정값 차이가 나는 새로운 데이터 생성
        * Under Sampling
            * 많은 레이블을 가진 데이터 세트를 감소 시킴
            * 정상 레이블에 대한 학습을 제대로 수행할 수 없다는 단점을 지님 = 잘 쓰지 않음

* Outlier(데이터 이상치)
    * 전체 데이터 패턴에서 벗어난 데이터
    * 모델의 성능에 영향을 주는 경우 있음
        * 이상치 제거 후, 학습/예측/평가 진행 필요
    * IQR (Inter Quantile Range)
        * 사분위 값의 편차를 이용하는 기법
        * Box Plot으로 시각화 가능
        
* 성능 올리기
    * Scaling -> 이상치 제거 -> (Optional) 불균형 데이터일 경우 Over Sampling ...