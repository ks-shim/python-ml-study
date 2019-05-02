# REGRESSION

* 여러 개의 독립변수와 한 개의 종속변수 간의 상관관계 모델링. 최적의 회귀계수를 찾는 것
    * 독립변수
        * 아파트의 방 개수, 크기, 주변 학군 ...
    * 종속변수
        * 아파트 가격
    * 회귀계수
    
* 선형회귀
    * 실제값과 예측값의 오류 제곱 값을 최소화하는 직선형 회귀선을 최적화
    * RSS(Residual Sum of Square)
    * Regularization 방식에 따라 아래와 같이 나뉨
        * 일반 선형 회귀
            * Regularization을 적용하지 않음
        * 릿지(Ridge)
            * L2 규제를 추가한 회귀모델.
            * L2는 상대적으로 큰 회귀 계수 값의 예측 영향도를 감소
        * 라쏘(Lasso)
            * L1 규제를 추가한 회귀모델
            * 예측 영향력이 작은 Feature의 회귀 계수를 0으로 만들어 Feature가 선택되지 않게 함.
            * = Feature 선택 기능
        * 엘라스틱넷 (ElasticNet)
            * L1,L2 규제를 함께 적용
            * 주로 Feature가 많은 데이터 세트에 적용
            * L1으로 Feature의 개수를 줄이고, L2로 계수 값의 크기를 조정
        * 로지스틱 회귀 (Logistic Regression)
            * 분류 선형 모델

* 경사하강법(Gradient Descent)
    * 비용 최소화
    * 전체 데이터를 기준으로 가중치 계산 : 속도가 느림
    * Steps
        1. 임의로 가중치 설정
        2. 손실 함수 계산
        3. 가중치 업데이트
        4. 손실 함수 계산. 함수 값이 감소했으면, 2부터 반복. 감소하지 않으면 Stop

* 확률적 경사 하강법(Stochastic Gradient Descent)
    * 일부 데이터로만 가중치를 업데이트 : 속도가 빠름
    
* 회귀 평가 지표
    * 실제 값과 예측 값의 차이를 기반으로 한 지표가 중심
    * 지표들
        * MAE (Mean Absolute Error)
            * 실제값과 예측값의 차이를 절대값으로 변환해 평균한 것
        * MSE (Mean Squared Error)
            * 실제값과 예측값의 차이를 제곱해 평균한 것
        * RMSE (Root Mean Squared Error)
            * MSE에 Root를 씌운 것
        * R^2
            * 분산 기반의 예측 지표
            * 실제 분산 대비 예측값의 분산 비율