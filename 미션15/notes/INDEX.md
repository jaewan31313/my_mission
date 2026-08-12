# 학습 노트 목록

- [train_test_분할](train_test_분할.md) — train/test를 나누는 이유 (오버피팅 방지, 일반화 성능 확인)
- [pandas_csv_읽기](pandas_csv_읽기.md) — read_csv로 불러온 데이터는 print로 직접 출력해야 보임
- [결측치_확인](결측치_확인.md) — df.info()의 Non-Null Count로 결측치 여부 확인
- [괄호_vs_대괄호](괄호_vs_대괄호.md) — []는 꺼내기(인덱싱), ()는 실행하기(함수/메서드 호출)
- [딕셔너리_기초](딕셔너리_기초.md) — {}는 키:값 대응표(딕셔너리), replace()에 대응표로 넘길 때 사용
- [점_표기법](점_표기법.md) — .은 객체가 가진 것을 꺼내 쓰는 소속 표기, _는 이름에 쓰는 문자일 뿐
- [범주형_인코딩](범주형_인코딩.md) — Yes/No 같은 문자열을 replace()로 0/1 숫자로 변환
- [회귀_target_dtype](회귀_target_dtype.md) — 회귀 target이 float인 건 정상, 문제 없음
- [describe_기초](describe_기초.md) — df.describe()로 컬럼별 통계 요약 확인, 예상 범위 검증
- [target_vs_feature](target_vs_feature.md) — Performance Index가 target인 이유: test.csv에 없는 컬럼이라 예측 대상
- [EDA의_목적](EDA의_목적.md) — EDA는 feature 선택뿐 아니라 모델 결과 검증용 기준점, 보고서 근거로도 쓰임
- [X_y_분리](X_y_분리.md) — X엔 target 넣으면 컨닝(데이터 누수), fit(X, y)로 따로 전달
- [axis_개념](axis_개념.md) — axis=0은 행 방향, axis=1은 열 방향
