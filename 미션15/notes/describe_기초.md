# describe_기초

## 질문 이력
- 2026-08-11

## 핵심 개념
`df.describe()`는 각 숫자형 컬럼의 count, mean, std, min, 25%/50%/75% 분위수, max를 한 번에 보여준다. 데이터가 예상 범위(예: 문서에 적힌 min/max)와 맞는지 검증하는 용도로도 쓸 수 있다.

## 예시 코드
```python
df.describe()
```
확인 결과: Performance Index min=10, max=100 (미션 설명과 일치), Extracurricular Activities는 0/1만 존재 (인코딩 검증 완료).

## 헷갈렸던 부분
(없음)
