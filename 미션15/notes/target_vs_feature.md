# target_vs_feature

## 질문 이력
- 2026-08-11

## 핵심 개념
지도학습(supervised learning)에서 "특성(feature)"은 이미 알고 있어서 입력으로 쓰는 컬럼들, "목표변수(target)"는 우리가 예측하고 싶은 컬럼이다. 이 미션에서는 `Performance Index`가 target이고 나머지 5개 컬럼이 feature다. train.csv에는 target이 포함되어 있어 모델을 학습시킬 수 있지만, test.csv에는 target이 빠져있어서 모델이 예측해야 하는 대상이 된다.

## 예시 코드
```python
# test.csv 헤더 확인 결과: Performance Index 컬럼 없음
Hours Studied,Previous Scores,Extracurricular Activities,Sleep Hours,Sample Question Papers Practiced
```

## 헷갈렸던 부분
왜 Performance Index를 예측 대상으로 삼는지 헷갈려함 → test.csv에 그 컬럼이 없다는 걸 직접 확인하고 이해함.
