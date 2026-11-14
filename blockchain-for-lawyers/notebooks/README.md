# 노트북 — 『법률가를 위한 블록체인 — 기술과 경제학으로 읽기』

본문의 파이썬 코드 셀을 장별로 그대로 옮긴 노트북 21권이다(0부 NB00 · 1부 NB04~NB12 · 2부 NB13~NB17 · 3부 NB19~NB25 · 6부 NB29). 출력은 엮은이가 Python 3.13.17에서 실행한 결과이며, 본문의 「출력」 블록과 같은 실행에서 나왔다. 본문의 「NB09-2」는 NB09 노트북의 둘째 코드 셀이다.

- **외부 패키지.** NB25만 `numpy` 2.5.4 하나를 쓴다(`requirements.txt` 에 이유). 나머지는 표준 라이브러리만 쓴다. 설치 셀은 없다. 외부 API를 부르지 않는다.
- **동봉 데이터.** NB12는 `data/genesis_header.hex`·`data/genesis_block.hex` 를, NB20-3은 `data/hashrate_2026-10-25.json` 을, NB29-2는 `data/exposed_output_types_2026-10-25.json` 을 읽는다. 파일이 없으면 같은 값의 상수로 대신하므로 Colab에서 파일 없이도 돈다. NB25는 **합성 자료만** 쓴다(시드 고정, 실제 시세 자료 없음 — 25장).
- **실사용 금지.** 모든 코드는 공부용 장난감이다. 실제 자산·실제 개인키·실제 거래에 쓰지 않는다.

| 노트북 | 장 | 셀 | 내용 | 열기 |
|---|---|---|---|---|
| NB00 | 3 | 1 | 환경 점검 — 파이썬 판, `hashlib`·`secrets`·`struct`·`json`·`decimal` 동작, numpy 유무 안내 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB00.ipynb) |
| NB04 | 4 | 5 | SHA-256 지문, 눈사태, 검사합 위조 vs 해시, 생일 역설, 손으로 짠 SHA-256 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB04.ipynb) |
| NB05 | 5 | 4 | 장난감 곡선(p=97) 군 연산, 장난감 ECDSA·가변성, k 재사용 키 복원, 실제 secp256k1 매개변수 확인 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB05.ipynb) |
| NB06 | 6 | 3 | 머클 트리·증명·검증, 증명 길이 표, 비트코인식 트리와 CVE-2012-2459 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB06.ipynb) |
| NB07 | 7 | 2 | 장난감 체인 변조·재연결, 두 일관된 체인 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB07.ipynb) |
| NB08 | 8 | 4 | 손 채굴기, 시도 횟수 분포, nBits→목표값→난이도, 조정 규칙 시뮬레이션 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB08.ipynb) |
| NB09 | 9 | 5 | 백서 식·표 재현, P<0.1% 표, 정확식(음이항 유한합), 몬테카를로, 해시율 불변성 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB09.ipynb) |
| NB10 | 10 | 2 | 담보 가중 선택, 슬래싱 즉시·상관 벌금 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB10.ipynb) |
| NB11 | 11 | 2 | UTXO 상태 전이, 계정 상태 전이 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB11.ipynb) |
| NB12 | 12 | 3 | 제네시스 헤더 파싱, 이중 SHA-256 대조, 코인베이스 거래 해부 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB12.ipynb) |
| NB13 | 13 | 3 | 장난감 EVM(황서 부록 G 요금표 값), 거래 적용(유효성·선지급·되돌림·환불·기본 수수료 소각), 무한 루프와 가스 소진 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB13.ipynb) |
| NB14 | 14 | 3 | ERC-20 장부 흉내와 approve 경쟁 조건, ERC-721 장부 흉내(safeTransferFrom·운영자·가변 URI), Keccak-256 직접 구현과 ERC-165/721 식별자 재계산 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB14.ipynb) |
| NB15 | 15 | 2 | 상수곱 풀(스왑·유동성·슬리피지 표), 비영구 손실 표와 수수료 성장 표(풀 단위) | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB15.ipynb) |
| NB17 | 17 | 2 | 샌드위치 시뮬레이션(15장 풀 재사용), 피해자 슬리피지 허용치별 공격자 최적 투입 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB17.ipynb) |
| NB19 | 19 | 2 | 개럿–월리스 붕괴 확률(π별), 실링–울리히 식 (8) 가격 경로 구성과 마팅게일 확인(20,000 경로) | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB19.ipynb) |
| NB20 | 20 | 3 | 비트코인 보조금 일정(정수 시프트), 부디시 명제 3 공격 지속시간 t(A,e,k)·표 II 재현, 공격 비용 계산기(해시율 스냅샷·단위는 블록 보상) | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB20.ipynb) |
| NB21 | 21 | 3 | EIP-1559 정수 갱신식과 런던 포크 블록 검증(12,965,000→12,965,001), 1차 가격 경매 vs 1559 장난감 비교, EIP-4844 fake_exponential 블롭 수수료 경로 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB21.ipynb) |
| NB23 | 23 | 2 | 이기적 채굴 상태기계 몬테카를로(α·γ 표, CACM 식 (3) 대조), 2×2 이득표와 문턱 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB23.ipynb) |
| NB24 | 24 | 3 | 다이아몬드–딥비그 두 균형(V2(f) vs r1), 준비자산 구성×상환 요구→디페그 되먹임(유형 A·B·B′·C, 창구 폐쇄), 알고리듬형 반사 나선 | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB24.ipynb) |
| NB25 | 25 | 3 | 합성 자료 SADF·GSADF(PSY 표 1 대조), 몬테카를로 임계값 2,000회·BSADF 날짜 찍기, 시변 변동성 크기 왜곡과 와일드 부트스트랩 — `numpy` | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB25.ipynb) |
| NB29 | 29 | 3 | 쇼어 알고리듬 ECDLP 자원 일반식(Roetteler 2017)과 네 편 비교, `data/exposed_output_types_2026-10-25.json` 의 유형별 노출 수량 재계산(2차 집계 🟡), 잠금 스크립트 유형 분류기(제네시스 출력 + 가짜 바이트) | [Colab에서 열기](https://colab.research.google.com/github/BowonKwon/AI-Assisted-Handbooks/blob/main/blockchain-for-lawyers/notebooks/NB29.ipynb) |

1·2·16·18·22·26·27·28·30장과 부록에는 노트북이 없다(개념·서베이·조문 장). 13·14장의 Solidity 예시는 읽기용이며 노트북에 넣지 않았다.

이 폴더의 노트북은 책과 같은 조건(CC BY-NC 4.0)으로 배포한다. 책의 판권면(부록 F.4)을 보라.
