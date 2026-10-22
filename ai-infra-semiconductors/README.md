# AI 인프라와 반도체

**통계·전산·AI 배경 학습자를 위한 일곱 회차 자습서** · 일요일은 AI · 반도체 스터디 · 권보원 엮음 · 2.0.1판(2026. 10. 22.)

- [화면본(HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/ai-infra-semiconductors/)
- [인쇄본(PDF, 206쪽)](ai-infra-semiconductors-v2.0.1.pdf)
GitHub에서 `index.html` 을 누르면 책 대신 코드가 보이거나 파일이 커서 표시되지 않습니다. 책은 위 화면본 링크로 여십시오. 인터랙티브 그림 12종은 화면본 본문에 들어 있고, 그림 하나씩 따로 여는 단독 페이지는 `widgets/` 폴더에 있습니다(예: [루프라인](https://bowonkwon.github.io/AI-Assisted-Handbooks/ai-infra-semiconductors/widgets/roofline.html)).

「일요일은 AI」 스터디의 반도체 회차를 위해 엮은 자습서입니다. 반도체를 전공하지 않았지만 통계·전산·AI 배경이 있는 독자를 위해 썼고, 용어를 외우는 대신 몇 개의 식을 세워 숫자를 직접 넣어 보게 합니다. 회차마다 정량 실습과 전체 풀이(32문항)가 붙어 있습니다. 화면본에서는 식 가까이에 놓인 인터랙티브 그림에서 값을 바꿔 볼 수 있고, 인쇄본에는 같은 자리에 처음 상태의 그림이 실려 있습니다. 이용할 때 유의할 점과 만든 방식은 책 앞의 「이 책의 사용법」과 끝의 간기에 있습니다.

## 차례

| | 주제 | 세우는 도구 |
|---|---|---|
| 사용법 | 8주 진행표, 수치에 관한 일러두기 | |
| 1회차 | AI 반도체 산업 지형 | 정의를 먼저 묻는 습관 |
| 2회차 | AI 칩 — 연산 반도체(GPU·NPU·TPU·ASIC) | 루프라인 모델 |
| 3회차 | AI 메모리 — DRAM · HBM · HBF | 대역폭과 용량의 분리 |
| 4회차 | 팹리스 · 파운드리와 밸류체인 | 수율 식 |
| 5회차 | 전공정(노광·식각·증착·계측) | 레일리 판정식 |
| 6회차 | 후공정과 첨단 패키징 | 칩렛 손익, 열저항 사슬 |
| 7회차 | AI 데이터센터(전력·냉각) | 종합 |
| 부록 | 공식 요약과 실습 색인, 용어 색인(114개), 인터랙티브 그림 목록 | |

## 인용

권보원(Bowon Kwon) 엮음, 『AI 인프라와 반도체』, 2.0.1판(2026. 10. 22.), https://github.com/BowonKwon/AI-Assisted-Handbooks

## 이용 허락

글은 [CC BY-NC 4.0](../LICENSE), 인터랙티브 그림의 코드(HTML·CSS·자바스크립트)는 [PolyForm Noncommercial 1.0.0](widgets/LICENSE.md)입니다(엮은이에게 권리가 있는 범위에서). 코드를 상업적으로 이용하시려면 미리 [Issues](https://github.com/BowonKwon/AI-Assisted-Handbooks/issues)로 연락해 주십시오. 원문에서 옮기거나 다시 그린 표·인용·그림은 이 라이선스들의 대상이 아니며 각 원저작자의 권리를 따릅니다.

## 판 이력

2026년 8월 스터디 교재에서 출발해 스터디 내부 배포본(1판, 공개하지 않았다)을 거쳤습니다.

| 판 | 날짜 | 내용 |
|---|---|---|
| 2.0 | 2026. 10. 8. | 첫 공개판. 1판을 바탕으로 스터디 발표·토론에서 나온 내용을 1차 출처로 확인해 더하고, 인터랙티브 그림 12종과 원자료 링크를 넣었다. 시점이 지난 수치를 다시 확인하고, 다른 AI 모델의 전권 통독으로 계산·서술 오류와 지나친 단정을 고쳤다 |
| 2.0 정정 | 2026. 10. 13. | 이용 허락 문구를 고치고, 인터랙티브 그림의 코드를 PolyForm Noncommercial 1.0.0으로 바꿨다(상업적 이용은 별도 협의). 그 전에 받은 사본에는 종전 조건(CC BY-NC 4.0)이 그대로 적용된다. 화면본이 휴대전화에서 가로로 넘치던 것도 고쳤다. 본문 내용은 같다 |
| 2.0.1 | 2026. 10. 22. | TSMC A16 공정의 양산 시기를 바로잡았다. 2024년 발표 때의 「2026년 생산 계획」만 적었던 것을, 2026년 4월 기술 심포지엄에서 보도된 TSMC 임원 발언에 따른 「양산 2027년 시작 예상」으로 고쳤다(4회차 4절 표, 5회차 3절). 영문판을 번역하고 원자료와 대조하는 과정에서 확인된 사실·서지 오류도 함께 바로잡았고(인터랙티브 그림 중 노광 그림의 설명 포함), 회사 이름은 각 회사의 현재 표기(Sandisk·Arm·ZEISS)로 맞췄다 |

## English edition

*AI Infrastructure and Semiconductors: A Self-Study Guide* · Sunday AI semiconductor sessions · edited by Bowon Kwon · edition 2.0.1-en (October 22, 2026), translated from the Korean edition 2.0.1

- [Read online (HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/ai-infra-semiconductors/en/)
- [Print edition (PDF, 234 pages)](en/ai-infra-semiconductors-v2.0.1-en.pdf)

The twelve interactive figures are embedded in the online edition; stand-alone pages for each figure are in the `en/widgets/` folder (for example, [roofline](https://bowonkwon.github.io/AI-Assisted-Handbooks/ai-infra-semiconductors/en/widgets/roofline.html)). The print edition shows each figure in its initial state.

The editor translated the book working with Claude Code. Quotations that were originally in English were restored from the original sources rather than translated back from Korean, and numbers were carried over unchanged. A few boxes headed "Comparable cases elsewhere" add examples that are not in the Korean edition. Before publication, OpenAI Codex, given the Korean and English texts and the sources they cite, compared the two editions sentence by sentence; each finding was rechecked against the originals. Details are in the colophon at the end of the book.

**Citation:** Bowon Kwon (ed.), *AI Infrastructure and Semiconductors: A Self-Study Guide*, edition 2.0.1-en (October 22, 2026), https://github.com/BowonKwon/AI-Assisted-Handbooks

**License:** To the extent the editor holds rights in them, the text is licensed under [CC BY-NC 4.0](../LICENSE) and the code of the interactive figures (HTML/CSS/JavaScript) under the [PolyForm Noncommercial License 1.0.0](en/widgets/LICENSE.md). For commercial use of the code, please open an [issue](https://github.com/BowonKwon/AI-Assisted-Handbooks/issues) first. Tables, quotations, and figures reproduced or redrawn from original works are not covered by these licenses and remain subject to the rights of their authors.
