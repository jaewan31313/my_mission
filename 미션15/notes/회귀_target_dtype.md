# 회귀_target_dtype

## 질문 이력
- 2026-08-11

## 핵심 개념
회귀(regression) 모델은 연속적인 값을 예측하므로, 목표변수(target)가 float 타입인 건 정상이고 문제되지 않는다. 입력 특성(feature)들이 int이고 target이 float이어도 dtype을 맞출 필요 없음 (분류 문제의 클래스 라벨과는 다름).

## 예시 코드
Performance Index 컬럼이 float64인 것 → 그대로 둬도 됨.

## 헷갈렸던 부분
다른 컬럼은 int64인데 target만 float64라 문제가 되는 줄 헷갈려함 → 회귀는 연속값 예측이라 상관없다는 걸로 정리.
