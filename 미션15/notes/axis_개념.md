# axis_개념

## 질문 이력
- 2026-08-11

## 핵심 개념
pandas/numpy에서 `axis`는 작업 방향을 뜻한다. `axis=0`은 행(위아래) 방향, `axis=1`은 열(좌우) 방향. `df.drop('컬럼명', axis=1)`은 "열 방향에서 그 이름을 찾아 지워라"는 뜻.

## 예시 코드
```python
X = df.drop('Performance Index', axis=1)  # 컬럼 삭제
```

## 헷갈렸던 부분
(없음, 한 번에 맞춤)
