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
    