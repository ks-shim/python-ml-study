# DIMENSION-REDUCTION

* 다차원 데이터의 차원을 축소 -> 새로운 차원의 데이터 생성
    * 좀 더 직관적 데이터 해석 가능
* 차원 축소는 ...
    * Feature Selection
        * 불필요한 Feature는 제거
    * Feature Extraction
        * 저차원의 중요 피처로 압축 = Latent Feature
* 차원축소 알고리즘
    * PCA (Principal Component Analysis)
        * 주성분 분석
            * 각각의 축은 하나의 주성분에 해당
            * 데이터 차원 수만큼의 주성분이 존재
            * 어느 축이 더 중요한지 우선 순위를 구하는 것임
        * 여러 변수간의 상관관계를 기반으로 주성분(Principal Component)을 추출하여 차원 축소
            * 상관관계 : 공분산 행렬
            * 공분산 행렬의 고유 벡터는 수직
        * 분산을 최대한 유지하면서 서로 직교하는 새 기저(축)를 찾아 저차원 공간으로 변환
            * https://ratsgo.github.io/machine%20learning/2017/04/24/PCA/
        * 정보 가장 높은 데이터 축을 찾아 차원 축소
    * LDA (Linear Discriminant Analysis)
        * 분산 유실 최소화
        * 분류에 사용
        * 개별 클래스를 분별할 수 있는 기준을 최대한 유지
        * PCA는 변동성이 가장 큰 축을...
        * LDA는 결정 값 클래스를 최대한 분리할 수 있는 축을 찾음.
        * 공분산 행렬을 사용하지 않음
            * 클래스 간 분산 + 클래스 내부 분산 행렬 사용
            * 위 행렬에 기반해 고유벡터 구하고 데이터 투영
    * SVD (Singular Value Decomposition)
        * PCA는 정방행렬만 분해 가능, but SVD는 행과 열의 크기가 달라도 가능
        * 특이값 분해
        * 특이벡터는 서로 직교
    * NMF (Non-Negative Matrix Factorization)
        * 행렬 내 모든 원소 값이 양수라는 게 보장되면 간단한 행렬 분해 가능
* 행렬
    * 정방 행렬(Square Matrix)
        * 행과 열의 크기가 동일
        * 모든 정방행렬은 고유벡터를 가짐
    * 선형 변환(Linear Transformations)
        * Av = b (행렬 A, 벡터 v, 벡터 b)
            * = 행렬 A를 이용해 벡터 v를 벡터 b로 변환/매핑
    * 고유 벡터
        * 선형 변환 시, 그 방향이 변하지 않는 벡터
        * https://skymind.ai/kr/wiki/eigenvector
