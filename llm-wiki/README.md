# 읽은 것이 사라지지 않는 서재

**법률가를 위한 LLM 위키 자습서 — 혼자서 처음부터 끝까지** · 권보원 엮음 · 2.1판(2026. 11. 7.)

- [화면본(HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/llm-wiki/)
- [인쇄본(PDF, 103쪽)](llm-wiki-v2.1.pdf)
- English edition: [*A Library That Remembers What You Read*](#english-edition)

GitHub에서 `index.html` 을 누르면 책 대신 코드가 보이거나 파일이 커서 표시되지 않습니다. 책은 위 화면본 링크로 여십시오.

Andrej Karpathy가 제안한 「LLM 위키」 — 읽은 자료를 AI 에이전트가 요약·연결해 내 컴퓨터의 마크다운 폴더에 쌓아 가는 방식 — 를 법률가가 혼자서 만들고 석 달 동안 운영할 수 있게 쓴 자습서입니다. 2026년 9월 2일 사법연수원 「2026년 AI 리터러시 슈퍼위크」 고급 실습 과정 중 「에이전틱 AI 및 바이브코딩 활용례 시연」 강의 자료집에서 출발해, 강의를 듣지 않은 독자도 설치부터 따라올 수 있도록 다시 썼습니다. 본문은 Claude Code 기준이고, 같은 방식을 다른 에이전트로 옮기는 법도 적었습니다.

되는 것과 안 되는 것을 같은 무게로 적었습니다. 이 방식에 대한 비판을 한 장(제19장)에 통째로 실었고, 무엇을 넣지 말아야 하는지와 데이터가 어디로 가는지(제18장), AI가 만든 인용을 다시 확인하는 습관(제20장)을 실습보다 앞에 둘 만큼 무겁게 다룹니다. **실습은 공개된 자료로만 하십시오.**

## 차례

| | 주제 |
|---|---|
| 들어가며 | 이 자습서를 쓰는 법 / 한 장 요약 — 30분 만에 만들기 |
| 제1부 준비 | 무엇을 만들게 되는가 · 계정과 준비물 · 설치와 첫 실행 · 에이전트가 일하는 방식 |
| 제2부 개념 | LLM 위키란 무엇인가 · 「AI에 파일 올리는 것」과의 차이 · 네 개의 층 · 이론적 배경 |
| 제3부 실습 | 위키 만들기 8단계 · 결과 읽기 · 세 가지 운영 · 검수하는 습관 |
| 제4부 심화 | 혼자 해볼 과제 · 규칙 파일 고치기 · 석 달 동안 일어날 일 · 규모·비용·자동화 · 여러 에이전트와 백업 |
| 제5부 지켜야 할 것 | 안전과 비밀유지 · 한계와 비판 · 인용을 믿지 않는 습관 |
| 제6부 참고 | 증상별 해결 · 더 배울 자료 |
| 제7부 | 이미 코드를 쓰시는 분께(B 트랙) |
| 부록 | `CLAUDE.md` 템플릿 · 프롬프트 모음 · 용어 사전 · 첫 30일 운영표 · 명령과 단축키 · `settings.json` 예시 |

## 인용

권보원(Bowon Kwon) 엮음, 『읽은 것이 사라지지 않는 서재: 법률가를 위한 LLM 위키 자습서』, 2.1판(2026. 11. 7.), https://github.com/BowonKwon/AI-Assisted-Handbooks

## 판 이력

2026년 9월 2일 사법연수원 「2026년 AI 리터러시 슈퍼위크」 고급 실습 과정의 강의 자료집에서 출발해 공개 저장소에 올리지 않은 자습서(판 1.0~1.3)를 거쳤습니다.

| 판 | 날짜 | 내용 |
|---|---|---|
| 2.0 | 2026. 10. 13. | 첫 공개판. Claude Code 관련 서술을 공식 문서로 다시 대조했다 |
| 2.1 | 2026. 11. 7. | 영문판을 만들며 찾아낸 것을 고쳤다. 원문과 어긋난 따옴표 인용을 원문대로 바로잡고 비판 ①의 출처를 밝혔다. Claude Code의 바뀐 사실(Ultra 요금제, 패키지 관리자 자동 업그레이드, 대화록 보존 기간, `AGENTS.md` 를 읽는 조건, 클라우드 업로드 조건)을 공식 문서로 고쳤다. 디자인 개편(시리즈 디자인 B, 주색 서가 녹색). Codex의 독립 대조를 반영했다 |

## 이용 허락

글은 [CC BY-NC 4.0](../LICENSE)입니다(엮은이에게 권리가 있는 범위에서). 원문에서 옮긴 표·인용은 이 라이선스의 대상이 아니며 각 원저작자의 권리를 따릅니다. 화면본·인쇄본에 쓴 글꼴(`fonts/`)은 Source Serif 4·Source Sans 3·Source Code Pro·Noto Serif KR·Noto Sans KR 을 줄이고 이름을 바꾼 수정본으로, SIL Open Font License 1.1 을 따릅니다(같은 폴더의 라이선스 파일).

## English edition

*A Library That Remembers What You Read: Building an LLM Wiki — A Self-Study Guide for Lawyers* · edited by Bowon Kwon · edition 2.1-en (November 7, 2026), translated from Korean edition 2.1 (November 7, 2026)

- [Read online (HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/llm-wiki/en/)
- [Print edition (PDF, 116 pages)](en/llm-wiki-v2.1-en.pdf)

A self-study guide for lawyers who want to build an LLM wiki on their own, following Andrej Karpathy's pattern: an AI agent summarizes and links what you read into a folder of Markdown files on your own computer. It starts with installation and covers three months of running the wiki. What works and what does not are given the same weight: a whole chapter sets out the criticisms of the method, and what must not go in, where the data goes, and the habit of rechecking AI-made citations come before the hands-on part. Korean examples (statutes, public databases) are kept; one box headed "Comparable cases elsewhere" adds an example from another jurisdiction.

The editor translated the book working with Claude Code. Quotations that were originally in English were restored from the original sources rather than translated back from Korean. Korean-language sources are kept and marked "(in Korean)." Before publication, OpenAI Codex, given only the Korean and English texts and the sources they cite, compared the two editions paragraph by paragraph; each finding was rechecked against the originals. Details are in the colophon at the end of the book.

**Citation:** Bowon Kwon (ed.), *A Library That Remembers What You Read: Building an LLM Wiki — A Self-Study Guide for Lawyers*, edition 2.1-en (November 7, 2026), https://github.com/BowonKwon/AI-Assisted-Handbooks

**License:** To the extent the editor holds rights in it, the text is licensed under [CC BY-NC 4.0](../LICENSE). Quotations and tables taken from original works are not covered by this license and remain subject to the rights of their authors. The fonts in `en/fonts/` are modified (instanced, subset and renamed) versions of Source Serif 4, Source Sans 3, Source Code Pro and Noto Sans KR, licensed under the SIL Open Font License 1.1 (license files in the same folder).
