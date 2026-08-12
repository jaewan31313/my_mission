# pandas_csv_읽기

## 질문 이력
- 2026-08-11

## 핵심 개념
`pd.read_csv(파일명)`은 CSV를 DataFrame으로 읽어오기만 할 뿐, 화면에 자동으로 보여주지 않는다 (Jupyter와 달리 `.py` 스크립트는 마지막 줄이라도 자동 출력 안 됨). 변수에 담고 `print()`로 직접 출력해야 확인 가능.

## 예시 코드
```python
df = pd.read_csv('mission15_train.csv')
print(df)
```

## 헷갈렸던 부분
`.py` 스크립트를 실행했는데 터미널에 아무것도 안 떠서 당황함 → 변수 저장 + print 필요하다는 걸 확인.
