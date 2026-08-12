---
name: quiz-me
description: Use this skill when the user asks to be quizzed or tested on what they've already learned (e.g. "퀴즈내줘", "테스트해줘", "복습시켜줘", "질문 좀 해줘"). Pulls topics from the notes/ folder built by learning-log and asks one question at a time, Socratic-style, to check retention. Also fine to gently suggest a quiz (never force one) when notes/ has topics that haven't been reviewed in a while or that show a lot of repeat questions in their 질문 이력.
---

# 퀴즈

`notes/` 폴더에 쌓인 기록을 바탕으로 사용자가 실제로 기억하고 있는지 확인하는 스킬.

## 언제 실행하나

- 사용자가 "퀴즈내줘", "테스트해줘", "복습시켜줘" 등으로 요청할 때.
- 가끔 자연스러운 타이밍에 먼저 제안할 수 있다 (예: `notes/`에 오래 안 본 주제나 질문 이력이 잦은 주제가 있을 때). 단, 강요하지 않고 제안만 하고 사용자 답을 기다린다.

## 출제 범위 고르기

1. `notes/INDEX.md`를 읽어서 전체 주제 목록을 파악한다.
2. 사용자가 특정 주제를 지정하면 그 주제에서만 출제.
3. 지정하지 않으면 아래를 우선순위로 1~2개 주제를 고른다:
   - 질문 이력에 재질문(반복)이 많은 주제 — 아직 안 익은 개념일 가능성.
   - 오래전에 기록되고 그 뒤로 다시 안 본 주제.
4. 한 세션에 3~5문제 정도로 제한한다. 사용자가 더 원하면 이어간다.

## 진행 방식

1. 노트의 "핵심 개념"과 "헷갈렸던 부분"을 바탕으로 질문을 하나 만든다. 노트 내용을 그대로 베끼지 말고, 이해했는지 확인할 수 있는 형태로 바꿔서 묻는다 (개념 설명 시키기, 짧은 코드 예측, 틀린 코드 찾기 등).
2. 질문은 한 번에 하나만 던진다.
3. 사용자 답을 기다린다.
4. 맞았으면 짧게 확인해주고 다음 문제로. 틀렸거나 막히면 coding-teacher와 같은 방식으로 힌트를 단계적으로 준다 (바로 정답을 알려주지 않는다).
5. 다 끝나면 뭘 잘했고 뭐가 아직 헷갈리는지 1~2문장으로만 짧게 정리한다. 점수표나 통계는 만들지 않는다.

## 결과를 노트에 반영

각 문제가 끝나면 해당 `notes/<주제명>.md`의 "질문 이력"에 한 줄 추가한다:
- 맞았으면: `- YYYY-MM-DD (퀴즈, 정답)`
- 틀렸거나 헷갈렸으면: `- YYYY-MM-DD (퀴즈, 오답 — 다시 볼 것)` 그리고 "헷갈렸던 부분"에 무엇 때문에 틀렸는지 짧게 추가.

## 하지 말 것

- 노트에 있는 문장을 그대로 질문으로 재활용하지 않는다 (외운 문장 맞추기가 되어버림).
- 한 번에 여러 문제를 몰아서 내지 않는다.
- 웹페이지나 표 형식으로 만들지 않는다 — 대화로 진행한다.
- 틀렸다고 평가하는 투로 말하지 않는다. coding-teacher와 같은 톤 유지.
