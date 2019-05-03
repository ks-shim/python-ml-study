# DIMENSION-REDUCTION

* 다차원 데이터의 차원을 축소 -> 새로운 차원의 데이터 생성
    * 좀 더 직관적 데이터 해석 가능
* 차원숙소는 ...
    * Feature Selection
        * 불필요한 Feature는 제거
    * Feature Extraction
        * 저차원의 중요 피처로 압축 = Latent Feature
* 차원축소 알고리즘
    * PCA (Principal Component Analysis)
        * 주성분 분석
        * 여러 변수간의 상관관계를 기반으로 주성분(Principal Component)을 추출하여 차원 축소
            * 상관관계 : 공분산
        * 분산을 최대한 유지하면서 서로 직교하는 새 기저(축)를 찾아 저차원 공간으로 변환
            * https://ratsgo.github.io/machine%20learning/2017/04/24/PCA/
        * 정보 유실 최소화
        * 분산이 가장 높은 데이터 축을 찾아 차원 축소
    * LDA
    * SVC
    * NMF