# 고삐를 쥐고 기계에게 일을 맡기는 법

**Claude Code·Codex로 내 일을 대신할 에이전트 짓기** · 일요일은 AI · 에이전트 스터디 · 실전편 · 권보원 엮음 · 1.1판(2026. 10. 23.)

- [화면본(HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/agentic-ai-practice/)
- [인쇄본(PDF, 127쪽)](agentic-ai-practice-v1.1.pdf)
- English edition: [*Harness in Hand*](#english-edition)

GitHub에서 `index.html` 을 누르면 책 대신 코드가 보이거나 파일이 커서 표시되지 않습니다. 책은 위 화면본 링크로 여십시오.

「일요일은 AI」 스터디가 원리편 『[생각하고, 행동하고, 고쳐 쓰는 기계](../agentic-ai-reading/README.md)』를 읽던 중에 엮은 실전편입니다. 원리편이 회차마다 논문 한 편으로 에이전트의 부품이 왜 그렇게 작동하는지를 읽는다면, 이 책은 회차마다 부품 하나를 내 컴퓨터의 Claude Code나 Codex에 직접 붙여 봅니다. 장마다 30분 안에 끝나는 사전 과제, 엮은이가 실제로 돌린 결과, 부품을 빼면 무엇이 깨지는지 보여 주는 「망가뜨려 보기」가 들어 있습니다. 본문은 Claude Code 기준이고, Codex는 장마다 대응표로 따라옵니다. 프로그래밍을 업으로 하지 않아도 0회부터 따라올 수 있습니다.

실습은 실습 전용 폴더에서, 공개되어도 문제없는 자료로만 하십시오. 이용할 때 유의할 점과 엮은이의 실행 결과를 읽는 법은 책 앞의 「이 책의 사용법」에 있습니다.

## 차례

| | 주제 |
|---|---|
| 사용법 · 0회 | 이 책의 사용법 / 설치와 첫 실행 |
| 1~2회 | 챗봇에서 에이전트로 / 지시문과 컨텍스트(규칙 파일) |
| 3~4회 | 도구와 MCP / 스킬 |
| 5~6회 | 훅: 가드레일과 재시도 / 메모리 |
| 7~8회 | 서브에이전트와 역할 분담 / 스펙과 사람의 검증 |
| 9~10회 | 보안·권한·비용 / 운영과 평가: 내 일 하나 끝까지 맡겨 보기 |

## 인용

권보원(Bowon Kwon) 엮음, 『고삐를 쥐고 기계에게 일을 맡기는 법: Claude Code·Codex로 내 일을 대신할 에이전트 짓기』, 1.1판(2026. 10. 23.), https://github.com/BowonKwon/AI-Assisted-Handbooks

## 판 이력

| 판 | 날짜 | 내용 |
|---|---|---|
| 1.0 | 2026. 10. 13. | 첫 공개판 |
| 1.0 정정 | 2026. 10. 13. | 이용 허락 문구를 고쳤다(권리가 있는 범위, 추가 제한 금지, 요약의 지위, 제3자 자료 제외). 인쇄본에서 쪽 너비를 넘던 표 둘(6회·7회)을 고치고, 화면본이 휴대전화에서 가로로 넘치던 것을 고쳤다. 본문 내용은 같다(118쪽) |
| 1.1 | 2026. 10. 23. | 디자인 개편(시리즈 디자인 B: 세리프 본문, 굵은 제목, 인쇄본 머리글에 회차 번호와 짧은 제목). 영문판을 번역·대조하는 중에 확인된 사실 정정 2건 반영(2회 4절 실행에 쓴 규칙 파일, 4회 8절 10회에서 다시 쓰는 자료) |

## 이용 허락

글은 [CC BY-NC 4.0](../LICENSE)입니다(엮은이에게 권리가 있는 범위에서). 원문에서 옮기거나 다시 그린 표·인용·그림은 이 라이선스의 대상이 아니며 각 원저작자의 권리를 따릅니다. 화면본·인쇄본에 쓴 글꼴(`fonts/`)은 Source Serif 4·Source Sans 3·Source Code Pro·Noto Serif KR·Noto Sans KR 을 줄이고 이름을 바꾼 수정본으로, SIL Open Font License 1.1 을 따릅니다(같은 폴더의 라이선스 파일).

## English edition

*Harness in Hand: Building AI Agents with Claude Code and Codex* · Sunday AI agent study · hands-on volume · edited by Bowon Kwon · edition 1.0-en (October 22, 2026), translated from Korean edition 1.0

- [Read online (HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/agentic-ai-practice/en/)
- [Print edition (PDF, 156 pages)](en/agentic-ai-practice-v1.0-en.pdf)

The editor translated the book working with Claude Code. The practice results were not translated: the agents were given the same tasks again with English instructions and English practice materials on October 22, 2026, and the text reports those runs, so results differ from the Korean edition in places. Quotations that were originally in English were restored from the original sources. Before publication, OpenAI Codex, given the two editions, the run records and the sources they cite, compared them; each finding was rechecked against the originals. Details are in the colophon at the end of the book.

**Citation:** Bowon Kwon (ed.), *Harness in Hand: Building AI Agents with Claude Code and Codex*, edition 1.0-en (October 22, 2026), https://github.com/BowonKwon/AI-Assisted-Handbooks

**License:** To the extent the editor holds rights in it, the text is licensed under [CC BY-NC 4.0](../LICENSE). Quoted originals and sentences from official documentation are not covered by this license and remain subject to the rights of their authors. The fonts in `en/fonts/` are modified (instanced, subset and renamed) versions of Source Serif 4, Source Sans 3, Source Code Pro and Noto Sans KR, licensed under the SIL Open Font License 1.1 (license files in the same folder).
