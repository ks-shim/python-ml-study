# EVALUATION

* Accuracy (정확도)
    * = 예측 결과가 동일한 데이터 건수 / 전체 예측 데이터 건수
    * 불균형한 레이블 값 분포에서는 적합한 평가 지표가 아님
* Confusion Matrix (오차 행렬)
    * 이진 분류의 성능 지표
    * TN, TP, FN, FP
* Precision (정밀도)
    * TP / (FP + TP)
* Recall (재현율)
    * TP / (FN + TP)
    * Positive를 Negative로 판단하면 큰 영향이 발생하는 곳에서 중요 지표로 사용
* Precision과 Recall은 Trade-off 관계