# 법률가를 위한 블록체인

**기술과 경제학으로 읽기** · 권보원 엮음 · 1.0판(2026. 11. 14.) · 수치 기준일 2026. 10. 25.

- [화면본(HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/blockchain-for-lawyers/)
- [인쇄본(PDF, 464쪽)](blockchain-for-lawyers-v1.0.pdf)
- [노트북 21권](notebooks/README.md) · [동봉 데이터](data/README.md)

GitHub에서 `index.html` 을 누르면 책 대신 코드가 보이거나 파일이 커서 표시되지 않습니다. 책은 위 화면본 링크로 여십시오. 인터랙티브 그림 12종은 화면본 본문에 들어 있고, 그림 하나씩 따로 여는 단독 페이지는 `widgets/` 폴더에 있습니다(예: [이중지불 확률](https://bowonkwon.github.io/AI-Assisted-Handbooks/blockchain-for-lawyers/widgets/double-spend.html)).

법학자가 고교 수학만으로 끝까지 읽을 수 있게 쓴 블록체인 자습서입니다. 해시와 서명에서 수수료 시장과 스테이블코인까지 기술과 경제학의 말로 풀고, 법의 질문이 생기는 자리를 「법률가의 질문」 상자로 표시했습니다. 문단마다 [입문]·[중급]·[심화] 표식이 있어 [입문]만 따라 읽어도 끝까지 갈 수 있습니다. 본문 그림 77개와 인터랙티브 그림 12종이 있고, 본문의 파이썬 코드는 장별 노트북 21권으로 다시 돌려 볼 수 있습니다. 인용은 원문을 각주에 그대로 실었습니다.

이 책은 학술 자습서이며 투자 권유나 법률 자문이 아닙니다. 특정 암호자산·토큰·금융상품을 사거나 팔거나 보유하라고 권하지 않고, 가격 전망을 하지 않습니다. 코드는 모두 원리를 보이기 위한 공부용이며 실제 자산·개인키·거래에 쓰면 안 됩니다. 고지 전문은 책 끝의 판권면(부록 F.4)에 있습니다.

## 차례

| 부 | 장 | 다루는 것 |
|---|---|---|
| 0부 지도 | 1~3장 | 블록체인이 푸는 문제, 30년 전사(전자현금에서 백서까지), 이 책을 읽는 법 |
| 1부 기술 기초 | 4~12장 | 해시 함수, 공개키 서명, 머클 트리, 블록과 체인, 작업증명, 최종성의 확률적 성격, 지분증명, UTXO와 계정, 제네시스 블록 해부 |
| 2부 스마트계약과 응용 | 13~18장 | 이더리움 가상머신과 가스, 토큰 표준, 탈중앙 거래소와 AMM, 오라클 문제, MEV와 거래 순서, 확장성 |
| 3부 경제학 | 19~25장 | 화폐의 기능론, 보안 예산, 수수료 시장, 토큰 설계의 경제학, 게임이론, 스테이블코인, 버블의 계량검정 |
| 4부 사건으로 읽기 | 26장 | Mt.Gox · The DAO · Terra-Luna · FTX |
| 5부 법제도 | 27~28장 | 기술과 법의 다리: 학설 구도, 법역별 서베이, 쟁점별 개관 |
| 6부 열린 문제 | 29~30장 | 양자 전환, 명명 문제(가상자산·crypto-asset·digital asset·暗号資産·cryptoasset) |
| 부록 | A~F | 동향 노트, 흔한 오해 판정표, 기술 용어 ↔ 법령 용어 대역표, 연표, 수학 보충, 용어집·목록·판권 |

## 인용

권보원(Bowon Kwon) 엮음, 『법률가를 위한 블록체인 — 기술과 경제학으로 읽기』, 1.0판(2026. 11. 14.), https://github.com/BowonKwon/AI-Assisted-Handbooks

## 이용 허락

글과 인터랙티브 그림(코드와 설명 글)은 [CC BY-NC 4.0](../LICENSE)입니다(엮은이에게 권리가 있는 범위에서, 그림 쪽 고지는 [`widgets/LICENSE.md`](widgets/LICENSE.md)). 각주에 인용한 원문과 원문에서 옮기거나 다시 그린 표·그림은 이 라이선스의 대상이 아니며 각 원저작자의 권리를 따릅니다. 동봉 데이터의 출처·기준일·산식은 [`data/README.md`](data/README.md)에 있습니다. 화면본·인쇄본에 쓴 글꼴(`fonts/`)은 Source Serif 4·Source Sans 3·Source Code Pro·Noto Serif KR·Noto Sans KR 을 줄이고 이름을 바꾼 수정본으로, SIL Open Font License 1.1 을 따릅니다(같은 폴더의 라이선스 파일).

## 만든 방식

엮은이가 생성형 AI(Claude)와 함께 엮었습니다. 장마다 원문과 대조하는 검증을 여러 차례 거쳤고, 게시 전에 다른 AI 모델(OpenAI Codex)이 원고와 원자료만 받아 사실·인용·수치를 다시 대조했습니다. 지적은 하나씩 원문을 다시 열어 확인한 뒤 반영했습니다. 그래도 틀린 서술이 남아 있을 수 있습니다. 수치와 인용은 원문으로 다시 확인해 주시고, 원문과 다른 곳을 찾으면 [Issues](https://github.com/BowonKwon/AI-Assisted-Handbooks/issues)로 알려 주십시오.

## 판 이력

| 판 | 날짜 | 내용 |
|---|---|---|
| 1.0 | 2026. 11. 14. | 첫 공개판 |

## English edition

*Blockchain for Lawyers: A Reading Through Technology and Economics* · edited by Bowon Kwon · edition 1.0-en (November 14, 2026), translated from the Korean edition 1.0 · reference date for figures 2026-10-25

- [Read online (HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/blockchain-for-lawyers/en/)
- [Print edition (PDF, 549 pages)](en/blockchain-for-lawyers-v1.0-en.pdf)
- [21 notebooks](en/notebooks/README.md)

The twelve interactive figures are embedded in the online edition; stand-alone pages for each figure are in the `en/widgets/` folder (for example, [double-spend probability](https://bowonkwon.github.io/AI-Assisted-Handbooks/blockchain-for-lawyers/en/widgets/double-spend.html)). The print edition shows each figure in its initial state.

A self-study guide to blockchains that a legal scholar can read to the end with high-school mathematics. It explains the subject, from hashes and signatures to fee markets and stablecoins, in the language of technology and economics, and marks the places where legal questions arise. The treatment of law keeps the Korean edition's scope: Korean and Japanese provisions and judgments are given in the original, followed by the editor's working gloss in English, which is not an official translation.

This book is an academic self-study guide. It is not investment advice or legal advice, it does not recommend buying, selling or holding any crypto-asset, token or financial product, and it makes no price forecasts. All the code is for study only. The full notice is in the colophon (Appendix F.4).

The editor translated the book working with a generative AI system (Claude). Quotations that were originally in English were restored from the original sources rather than translated back from Korean, and numbers were carried over unchanged. Before publication, another AI model (OpenAI Codex), given only the Korean and English texts and the sources they cite, compared the two editions and checked the quotations against the originals; each finding was rechecked against the originals before it was applied. Errors may remain; please report any discrepancy via [Issues](https://github.com/BowonKwon/AI-Assisted-Handbooks/issues).

**Citation:** Bowon Kwon (ed.), *Blockchain for Lawyers: A Reading Through Technology and Economics*, edition 1.0-en (November 14, 2026), https://github.com/BowonKwon/AI-Assisted-Handbooks

**License:** To the extent the editor holds rights in them, the text and the interactive figures (code and explanatory text) are licensed under [CC BY-NC 4.0](../LICENSE); see also [`en/widgets/LICENSE.md`](en/widgets/LICENSE.md). Originals quoted in the footnotes, and tables and figures reproduced or redrawn from original works, are not covered by this license and remain subject to the rights of their authors. The fonts in `en/fonts/` are modified (instanced, subset and renamed) versions of Source Serif 4, Source Sans 3, Source Code Pro and Noto Sans KR, licensed under the SIL Open Font License 1.1 (see the license files in that folder).
