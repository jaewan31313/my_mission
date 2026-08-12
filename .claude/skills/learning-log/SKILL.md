---
name: learning-log
description: Use this skill automatically whenever the user is learning or being taught a coding concept — no need to wait for an explicit save request. Works together with coding-teacher. Two jobs — (1) BEFORE teaching a topic: check notes/ for an existing note on it, and if found, remind the user when they last asked about it. (2) AFTER a concept is understood: automatically save/update a note under notes/, organized by topic, so forgotten concepts are easy to look back up later.
---

# 학습 기록 (자동)

사용자가 배운 개념을 나중에 다시 찾아볼 수 있게 `notes/` 폴더에 주제별로 자동 정리한다. 사용자가 요청하지 않아도 항상 동작한다.

## 언제 실행하나

- **새 주제를 가르치기 시작하기 전**: `notes/` 에 관련 파일이 이미 있는지 확인한다.
- **개념 하나가 끝날 때마다**: 자동으로 기록/갱신한다. 요청을 기다리지 않는다.
- **세션이 끝날 때**: 사용자가 "오늘은 여기까지", "그만할래", "다음에 이어서" 등으로 마무리 신호를 주면 `notes/학습_일지.md`에 오늘 날짜로 항목을 추가한다.

## 가르치기 전 체크

1. 지금 다루려는 주제와 겹치는 `notes/<주제명>.md` 가 있는지 확인한다.
2. 있으면:
   - 언제 이 주제를 처음/마지막으로 물어봤는지 한 줄로 짧게 알려준다. (예: "이거 8/5에도 물어봤었네")
   - 질문 이력에 오늘 날짜를 추가한다.
   - 같은 개념을 3회 이상 물어본 경우, "계속 헷갈리는 부분인가봐" 정도로 자연스럽게 한 번 짚어준다. 통계나 표로 만들지 않는다.
3. 없으면 평소대로 바로 가르치기 시작.

## 파일 구조

- `notes/INDEX.md` — 전체 주제 목록. 주제명과 한 줄 설명만.
- `notes/<주제명>.md` — 주제별 노트. 파일명은 주제를 짧게 한글로 (띄어쓰기는 `_`).
- `notes/학습_일지.md` — 날짜별 세션 로그. "언제 뭘 했는지, 어디까지 했는지"를 시간순으로 훑어보는 용도.

## 노트 파일 형식

```markdown
# <주제명>

## 질문 이력
- YYYY-MM-DD
- YYYY-MM-DD (다시 물어봄)

## 핵심 개념
(2~4문장. 이게 뭐고 왜 쓰는지)

## 예시 코드
(방금 대화에서 나온 실제 예시. 짧게)

## 헷갈렸던 부분
(실제로 막혔거나 헷갈려했던 지점만. 없으면 생략)
```

## 개념이 끝난 뒤 자동 기록 순서

1. 방금 다룬 개념(주제)이 뭔지 파악한다.
2. `notes/<주제명>.md` 가 있으면 내용을 이어서 갱신한다 (덮어쓰지 않음: 질문 이력에 날짜 추가, 핵심 개념 보강, 새로운 헷갈림 포인트 추가). 없으면 새로 만들고 `notes/INDEX.md`에 한 줄 추가한다.
3. 기록했다는 사실만 한 줄로 짧게 알려준다. 기록 내용을 화면에 다시 풀어서 출력하지 않는다.

## 세션 종료 시 학습 일지 기록

1. 오늘 세션에서 다룬 주제들을 모은다 (오늘 날짜로 새로 만들거나 갱신된 `notes/<주제명>.md` 목록).
2. `notes/학습_일지.md`에 오늘 날짜(`## YYYY-MM-DD`) 항목을 추가한다:
   - 다룬 주제: 오늘 다룬 노트 파일들을 링크로 나열
   - 다음에 이어갈 것: 끝내지 못하고 남은 부분이 있으면 한 줄로 (없으면 생략)
3. 기존 날짜 항목은 건드리지 않고, 새 날짜 항목만 이어서 추가한다 (덮어쓰지 않음).

## 하지 말 것

- 노트 내용을 장황하게 쓰지 않는다 — 나중에 훑어보는 용도이지 완전한 설명이 아니다.
- 대화 전체를 옮겨적지 않는다. 핵심만 압축한다.
- 반복 질문을 지적하거나 평가하는 톤으로 말하지 않는다. 사실만 짧게.
