# 생각하고, 행동하고, 고쳐 쓰는 기계

**ReAct에서 LLM Wiki까지, Agentic AI 논문 읽기** · 일요일은 AI · 에이전트 스터디 · 권보원 엮음 · 1.1판(2026. 10. 23.)

- [화면본(HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/agentic-ai-reading/)
- [인쇄본(PDF, 453쪽)](agentic-ai-reading-v1.1.pdf)
- English edition: [*Machines That Think, Act, and Revise*](#english-edition)

GitHub에서 `index.html` 을 누르면 책 대신 코드가 보이거나 파일이 커서 표시되지 않습니다. 책은 위 화면본 링크로 여십시오.

「일요일은 AI」 스터디가 매주 한 시간씩 Agentic AI 논문을 읽으려고 엮은 자습서입니다. 확률·통계·선형대수와 프로그래밍 기초가 있으면 읽기 편합니다. 자연어처리와 강화학습이 처음이면 0장(사전 자습)부터 읽으면 됩니다. 이용할 때 유의할 점과 만든 방식은 책 앞의 「이 책의 사용법」과 끝의 간기에 있습니다.

짝이 되는 실전편 『[고삐를 쥐고 기계에게 일을 맡기는 법](../agentic-ai-practice/README.md)』(2026. 10. 13.)은 같은 부품을 Claude Code·Codex에 직접 붙여 보는 사전 과제 중심의 자습서입니다.

## 차례

| | 주제 |
|---|---|
| 사용법 · 0장 | 이 책의 사용법 / 사전 자습: 언어모형·토큰·문맥 내 학습·강화학습 용어 |
| 1~3회 | 에이전트란 무엇인가 / 에이전트의 머리(Agentic Reasoning 서베이) / 몸과 울타리(하네스 서베이) |
| 4~6회 | Chain-of-Thought / Tree of Thoughts / ReAct |
| 7~10회 | 도구 사용과 표준 규약 / RAG / Lost in the Middle과 컨텍스트 엔지니어링 / Self-RAG |
| 11~14회 | RARR와 Reflexion / MemGPT / MetaGPT / SWE-agent |
| 15~16회 | 간접 프롬프트 인젝션 / 정렬 |
| 17~19회 | 에이전트 평가의 지도 / 평가 결과를 통계학의 눈으로 / HarnessFix |
| 20회 | 종합: LLM Wiki, 지식을 컴파일하는 에이전트 |
| 부록 | 기호표, 용어 통일표, 서지·링크 목록, 영상 목록 |

## 인용

권보원(Bowon Kwon) 엮음, 『생각하고, 행동하고, 고쳐 쓰는 기계: ReAct에서 LLM Wiki까지, Agentic AI 논문 읽기』, 1.1판(2026. 10. 23.), https://github.com/BowonKwon/AI-Assisted-Handbooks

## 판 이력

| 판 | 날짜 | 내용 |
|---|---|---|
| 1.0 | 2026. 10. 5. | 첫 공개판 |
| 1.0 정정 | 2026. 10. 13. | 이용 허락 문구를 고쳤다(권리가 있는 범위, 추가 제한 금지, 요약의 지위, 제3자 자료 제외). 화면본 차례에 회차 번호를 붙이고, 휴대전화에서 가로로 넘치던 것을 고쳤다. 현행 조판 도구로 다시 만들어 인쇄본이 411쪽이 됐다. 본문 내용은 같다 |
| 1.1 | 2026. 10. 23. | 디자인 개편(시리즈 디자인 B: 세리프 본문, 굵은 제목, 인쇄본 머리글에 회차 번호와 짧은 제목). 영문판을 번역·대조하는 중에 확인된 사실·인용·서지 정정 34건과 조판 정정 3건 반영 |

## 이용 허락

글은 [CC BY-NC 4.0](../LICENSE)입니다(엮은이에게 권리가 있는 범위에서). 원문에서 옮기거나 다시 그린 표·인용·그림은 이 라이선스의 대상이 아니며 각 원저작자의 권리를 따릅니다. 논문 PDF는 링크로만 안내합니다. 화면본·인쇄본에 쓴 글꼴(`fonts/`)은 Source Serif 4·Source Sans 3·Source Code Pro·Noto Serif KR·Noto Sans KR 을 줄이고 이름을 바꾼 수정본으로, SIL Open Font License 1.1 을 따릅니다(같은 폴더의 라이선스 파일).

## English edition

*Machines That Think, Act, and Revise: Reading Agentic AI Papers, from ReAct to LLM Wiki* · Sunday AI agent study · edited by Bowon Kwon · edition 1.0-en (October 22, 2026), translated from Korean edition 1.0 (October 5, 2026, including the correction of October 13)

- [Read online (HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/agentic-ai-reading/en/)
- [Print edition (PDF, 540 pages)](en/agentic-ai-reading-v1.0-en.pdf)

The editor translated the book working with Claude Code. Quotations that were originally in English were restored from the original papers, posts and specifications rather than translated back from Korean; where a passage could not be found in the original, the quotation marks were removed. Korean-language sources are kept and marked "(in Korean)." Before publication, OpenAI Codex, given only the Korean and English texts and the sources they cite, compared the two editions sentence by sentence; each finding was rechecked against the originals. Details are in the colophon at the end of the book.

**Citation:** Bowon Kwon (ed.), *Machines That Think, Act, and Revise: Reading Agentic AI Papers, from ReAct to LLM Wiki*, edition 1.0-en (October 22, 2026), https://github.com/BowonKwon/AI-Assisted-Handbooks

**License:** To the extent the editor holds rights in it, the text is licensed under [CC BY-NC 4.0](../LICENSE). Tables, quotations, and figures reproduced or redrawn from original works are not covered by this license and remain subject to the rights of their authors. Papers are linked, not redistributed. The fonts in `en/fonts/` are modified (instanced, subset and renamed) versions of Source Serif 4, Source Sans 3, Source Code Pro and Noto Sans KR, licensed under the SIL Open Font License 1.1 (license files in the same folder).
