# 스냅샷 데이터

기준일 **2026-10-25** (한국 시각). 실제 접근은 UTC 2026-10-24 18:15~18:20 사이에 했다. 이 폴더의 값은 구조 변수(블록 헤더, 난이도, 해시율 추정, 출력 유형별 수량)만 담는다. 암호자산 가격, 시가총액, 수익률 자료는 넣지 않는다. 전력 단가나 해시 임대 단가 같은 경제 변수는 위젯 사용자가 직접 입력한다.

## 파일

| 파일 | 내용 | 출처 1 | 출처 2 | 접근 시각(UTC) | 산식·확인 |
|---|---|---|---|---|---|
| `genesis_block.hex` | 비트코인 제네시스 블록 전체 직렬화(285바이트), 소문자 16진수 | https://blockstream.info/api/block/000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f/raw | https://mempool.space/api/block/000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f/raw | 2026-10-24T18:15:22Z / 18:15:24Z | 두 응답이 바이트 단위로 같다(파일 SHA-256 `5299fac9…5f9e99`) |
| `genesis_header.hex` | 위 블록의 앞 80바이트(블록 헤더) | 같음 | 같음 | 같음 | SHA256(SHA256(헤더))를 바이트 역순으로 읽으면 블록 해시 `000000000019d668…8ce26f` |
| `genesis_block.meta.json` | 위 두 파일의 출처, 해독한 필드, 대조 결과 | Bitcoin Core v31.1 `src/kernel/chainparams.cpp` L70, L134–L137 (커밋 `9be056a`) | btcd `chaincfg/genesis.go` L78–L88 (커밋 `dd169fe`) | — | nTime 1231006505, nNonce 2083236893, nBits 0x1d00ffff, nVersion 1, 머클 루트 `4a5e1e4b…eda33b` 모두 일치 |
| `hashrate_2026-10-25.json` | 기준일 난이도와 추정 해시율 | Blockstream Esplora API(블록 JSON·헤더) | mempool.space API(블록 JSON·헤더) | 2026-10-24T18:17:18Z~18:17:34Z | D = target(0x1d00ffff)/target(nBits), H = D × 2^32 / 600 |
| `exposed_output_types_2026-10-25.json` | 공개키(또는 지불 스크립트)가 이미 체인에 드러난 출력의 유형별 BTC 수량 | Project Eleven Bitcoin Risq List 집계(https://bitcoin-risq-list.projecteleven.com/api/btc-at-risk/metrics), 공개 SQL https://github.com/p-11/bitcoin-risq-list-query/blob/bb3177f89de8a5d826132658ffc7ca0f08dc4688/btc_at_quantum_risk_query.sql | mempool research UTXO Set Report(https://research.mempool.space/utxo-set-report/), 블록 892385 | 2026-10-24T18:19:27Z / 18:18:22Z | 2차 집계. 단위는 **BTC 수량**(비교 출처는 UTXO 개수와 BTC 수량 둘 다) |

## 소스 코드 고정 링크

- Bitcoin Core v31.1 태그 커밋 `9be056a8a72b624dae9623b2f7bded92c2a21c91`
  - 제네시스: https://github.com/bitcoin/bitcoin/blob/9be056a8a72b624dae9623b2f7bded92c2a21c91/src/kernel/chainparams.cpp#L134-L137
  - 코인베이스 문구 상수: https://github.com/bitcoin/bitcoin/blob/9be056a8a72b624dae9623b2f7bded92c2a21c91/src/kernel/chainparams.cpp#L70
- btcd 커밋 `dd169fe0c32a56087d28b92fff3b8cf4fb43477a`: https://github.com/btcsuite/btcd/blob/dd169fe0c32a56087d28b92fff3b8cf4fb43477a/chaincfg/genesis.go#L78-L88

## 제네시스 블록 확인 결과

데이터에서 직접 계산한 값이다(파이썬 `hashlib`·`struct`).

```
blockstream bytes: 285  mempool bytes: 285  byte-identical: True
nVersion: 1
hashPrevBlock: 0000000000000000000000000000000000000000000000000000000000000000
hashMerkleRoot: 4a5e1e4baab89f3a32518a88c31bc87f618f76673e2cc77ab2127b7afdeda33b
nTime: 1231006505  nBits: 0x1d00ffff (486604799)  nNonce: 2083236893
double-SHA256(header) as displayed (byte-reversed): 000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f
txid = double-SHA256(tx): 4a5e1e4baab89f3a32518a88c31bc87f618f76673e2cc77ab2127b7afdeda33b  == merkle root: True
push2 decoded ASCII: 'The Times 03/Jan/2009 Chancellor on brink of second bailout for banks'
output value (sat): 5000000000  scriptPubKey len: 67  last byte 0xac
```

코인베이스 입력 스크립트는 세 개의 푸시로 되어 있다. `ffff001d`(리틀엔디언 486604799, nBits와 같은 수), `04`, 그리고 69바이트 ASCII 문구다. 출력은 65바이트 비압축 공개키 뒤에 OP_CHECKSIG(0xac)가 붙은 P2PK다.

## 해시율 추정

| 항목 | 값 |
|---|---|
| 관측 시점 체인 끝 높이 | 972958 |
| 직전 난이도 조정 블록 | 971712 (= 482 × 2016) |
| nBits | 0x17020093 (두 블록 같음) |
| 난이도 D | 140,577,680,051,919.625 |
| 추정 해시율 D × 2^32 / 600 | 1.006294 × 10^21 H/s (약 1,006 EH/s) |
| 비교값: mempool.space `currentHashrate` | 1.077240 × 10^21 H/s |

두 탐색기의 헤더 원시 바이트가 같았고, 헤더의 이중 SHA-256이 블록 해시와 같으며 목표값 이하임을 확인했다. **가정:** 블록이 평균 600초마다 하나씩 발견된다. 2^32는 난이도 1에서 블록 하나에 필요한 해시 수의 기댓값이다. 실제 블록 간격이 600초와 다르면 실제 해시율도 그만큼 다르다. mempool.space가 같은 시각에 보고한 최근 평균 블록 간격은 571.1초였다. 비교값은 다른 방법(최근 블록 간격 반영)으로 낸 추정치이며, 어느 쪽도 참값이라고 하지 않는다.

## 노출 출력 유형

1차 데이터를 먼저 찾았다. 공개 노드에서 유형별 UTXO 집계를 직접 돌린 재현 결과는 이번 회차에 만들지 못했다. 대신 방법과 코드를 공개한 2차 집계 둘을 옮겼다.

- **주 출처(블록 972132, 2026-10-19 생성):** 공개키 노출 BTC 합계 7,121,995.44 BTC. 스크립트 유형 자체로 노출(P2PK 1,715,077 · P2TR 217,063 · 맨 P2MS 417)이 1,932,557 BTC, 이미 지출한 적 있는 주소·스크립트에 남은 잔고(P2WPKH 2,098,570 · P2SH 1,199,815 · P2PKH 1,185,672 · P2WSH 705,381)가 5,189,439 BTC다.
- **분모:** 스냅샷 높이까지 일정대로 발행된 보조금 합계 20,100,415.625 BTC. 실제 UTXO 총액보다 약간 큰 상한이다(쓸 수 없는 제네시스 출력과 채굴자가 받지 않은 보조금 포함). 이 분모로 계산한 노출 비율은 35.4%다.
- **비교 출처(블록 892385, 2025-04-14):** 스크립트 유형만 본 집계. P2PK는 UTXO 개수로 0.03%, 금액으로 8.70%(1,720,270 BTC)이고, P2TR은 개수로 34.22%, 금액으로 0.75%(147,912 BTC)다.

**한계.** 두 출처 모두 제3자 집계이며 이번에 노드에서 다시 계산하지 않았다. 두 출처는 시점과 방법이 달라 겹치는 범주(P2PK, P2TR)에서 크기 수준만 맞는다. P2SH·P2WSH 재사용 범주는 드러난 스크립트에 키가 없어도 노출로 센다. 서명 메시지나 확장 공개키 공유 같은 체인 밖 노출, 멤풀 체류 중 노출은 세지 않는다. 주 출처 응답에 있던 환율 필드는 옮기지 않았다.
