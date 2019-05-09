# CLUSTERING

* K-Means
    * 특정한 임의의 지점을 선택해 해당 중심에 가장 가까운 포인트들을 선택/군집
    * 데이터 세트가 원형의 범위를 가질수록 효율이 높음
        * 길쭉한 타원형일 경우 군집확 잘 되지 않음
    * 장점
        * 쉽고 간결
    * 단점
        * 속성의 개수가 많은 경우 군집화 정확도가 떨어짐
            * PCA로 차원 감소 적용 필요
        * 반복 횟수가 많을 수록 느려짐
        * 군집 개수 가이드가 어려움

* Mean Shift
    * K-Means는 거리 중심 이동
    * Mean Shift는 밀도가 가장 높은 곳으로 이동
    * 대역폭(Bandwidth) 내에서 밀도가 높은 곳으로 이동
    
* GMM (Gaussian Mixture Model)
    * 데이터가 가운시안 분포를 여러 모델을 섞어서 생성된 모델로 가정해서 수행
    * K-Means보다 유연, 다양한 데이터 세트에 잘 적용
        * but 느림
    * 모수 추정
        * 개별 정규 분포의 평균과 분산
        * 각 데이터가 어떤 정규 분포에 해당하는지의 확률

* DBSCAN (Density Based Spatial Clustering of Application with Noise)
    * 밀도 기반 군집화
    * 간단한 알고리즘에도 불구하고, 복잡하고 기하학적인 데이터의 분포를 가진 데이터 세트에서 잘 적용
    * Concept
        * Epsilon (입실론 주변 영역)
            * 개별 데이터를 중심으로 입실론 반경을 가지는 원형의 영역
        * min points (최소 데이터 개수)
            * 개별 데이터의 입실론 주변 영역에 포함되는 타 데이터의 개수
        * min points 충족 여부에 따라
            * Core Point (핵심포인트)
            * Neighbor Point (이웃포인트)
            * Border Point (경계포인트)
            * Noise Point (잡음포인트)
    
    
* 군집 평가 (Cluster Evaluation)
    * 비지도 학습의 특성상 정확한 평가는 힘듦
    * 실루엣 분석 (Silhouette analysis)
        * 군집 간의 거리가 얼마나 효율적으로 분리돼 있는지의 정도
        
    