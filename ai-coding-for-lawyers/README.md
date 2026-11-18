# 법률가를 위한 인공지능 코딩 자습서

권보원 엮음 · 1.0.1판(2026. 11. 18.) · 영어판 1.0-en(2026. 11. 18.) · 실행 환경 기준일 2026. 9. 6.

- [화면본(HTML)](https://bowonkwon.github.io/AI-Assisted-Handbooks/ai-coding-for-lawyers/)
- [인쇄본(PDF, 260쪽)](ai-coding-for-lawyers-v1.0.1.pdf)
- 영어판(English edition): [화면본](https://bowonkwon.github.io/AI-Assisted-Handbooks/ai-coding-for-lawyers/en/) · [인쇄본(PDF, 306쪽)](en/ai-coding-for-lawyers-v1.0-en.pdf)
- [실습 저장소](https://github.com/BowonKwon/AI-Coding-for-Lawyers) — 실습 코드와 장별 Colab 노트북 59개

GitHub에서 `index.html` 을 누르면 책 대신 코드가 보이거나 파일이 커서 표시되지 않습니다. 책은 위 화면본 링크로 여십시오.

코딩 경험이 없는 법률가가 혼자 읽고 따라 하면서 개발환경에서 출발해 딥러닝 모델을 직접 구현하는 데까지 가도록 쓴 자습서입니다. 제1부는 개발환경·파이썬·디버거·AI 코딩 보조 도구·Git을, 제2부는 PyTorch로 학습 파이프라인·CNN·Transformer·언어 모델을 직접 구현하는 과정을 다룹니다. 절마다 [입문]·[중급]·[심화] 표식이 있어 읽는 길 셋(A 처음부터, B 파이썬 경험자, C 딥러닝 경험자) 가운데 하나를 골라 읽을 수 있습니다. 책의 코드는 실제로 실행해 출력을 옮겼습니다(Colab에서만 도는 셀 몇 개는 실행하지 못해 「미실행」으로 표시했습니다). 실습 저장소에 따라 하기·주석 달기·다시 만들기 노트북 59개가 있습니다(22개 장. 5·6·7장은 노트북이 없고, 2·8·9·10장은 일부 단계만 있습니다).

예제의 사건은 모두 지어낸 것입니다. 사건번호의 연도는 2099, 법원 이름은 「가상지방법원」으로 적었습니다. 텍스트 실습의 데이터는 법령 조문입니다.

## 차례

| 부 | 장 | 다루는 것 |
|---|---|---|
| 0부 | 이 책을 읽는 법 | 읽는 길 셋, 자가진단, 실습 노트북 쓰는 법 |
| 제1부 AI와 함께 코딩하기 | 2~9장 | 개발환경 구축, 파이썬 기초 I·II, 디버거로 코드 읽기, AI 코딩 보조 도구, Git과 GitHub, 코드 읽기 훈련, 로컬 VS Code에서 Colab GPU 쓰기 |
| 제2부 딥러닝 직접 구현하기 | 10~26장 | 딥러닝이 배우는 방식, PyTorch 첫걸음, 학습 파이프라인 한 바퀴(MNIST와 MLP), 저장·추론·하이퍼파라미터, 코드 구조화, 데이터셋과 DataLoader, CNN과 LeNet, VGG와 ResNet, 전이학습, 텍스트 데이터, RNN·LSTM·GRU, seq2seq와 어텐션, Transformer 직접 구현, 생성모델과 언어모델, 실험 기록과 재현성, 공개 언어모델 다루기, 만든 모델 보여주기 |
| 부록 | A~E | 오류 메시지 사전, 용어집, 설치 문제 해결, 참고 자료, 최소한의 수학 |
| 간기 | 만든 이 | 일러두기, 만든 방식, 판 이력 |

## 인용

권보원(Bowon Kwon) 엮음, 『법률가를 위한 인공지능 코딩 자습서』, 1.0.1판(2026. 11. 18.), https://github.com/BowonKwon/AI-Assisted-Handbooks

Bowon Kwon (ed.), *AI Coding for Lawyers: A Self-Study Guide*, edition 1.0-en (November 18, 2026), https://github.com/BowonKwon/AI-Assisted-Handbooks

## 이용 허락

엮은이에게 권리가 있는 글은 [CC BY-NC 4.0](../LICENSE)입니다. 실습 코드는 [실습 저장소](https://github.com/BowonKwon/AI-Coding-for-Lawyers)에 있고 PolyForm Noncommercial 1.0.0입니다. 원문에서 옮긴 인용·표와 다른 사람의 코드(8장의 PyTorch 예제 등)는 이 라이선스의 대상이 아니며 각 원저작자의 권리를 따릅니다. 화면본·인쇄본에 동봉한 글꼴은 SIL OFL 1.1입니다.

## 만든 방식

엮은이가 생성형 AI(Claude)와 함께 엮었습니다. 책의 코드는 실행해 출력을 옮겼고, 게시 전에 다른 AI 모델(OpenAI Codex)이 원고와 실습 저장소를 받아 외부 사실과 수치를 다시 대조했습니다. 지적은 원문으로 다시 확인해 반영했습니다. 그래도 틀린 서술이 남아 있을 수 있습니다. 도구의 요금·무료 한도는 자주 바뀌므로 공식 문서로 다시 확인해 주시고, 원문과 다른 곳을 찾으면 [Issues](https://github.com/BowonKwon/AI-Assisted-Handbooks/issues)로 알려 주십시오.

이 책은 엮은이가 개인적으로 공부하며 엮은 것입니다. 엮은이가 속한 기관의 견해나 업무와는 관계가 없습니다.

## 판 이력

| 판 | 날짜 | 내용 |
|---|---|---|
| 1.0 | 2026. 11. 17. | 첫 공개판 |
| 1.0.1 | 2026. 11. 18. | 12장 12.4절의 `zero_grad` 빠뜨림 실험에 「값이 실행 환경에 따라 달라진다」는 설명을 더함. 휴대폰 화면에서 순서도를 줄이지 않고 가로로 밀어 보게 함. 본문의 오기와 앞뒤가 어긋난 수치·가리킴 마흔 곳 남짓을 바로잡음(8장 예제 파일의 줄 수, 본문에 적은 실행 시간, 형사소송법 제354조 인용 문언 등) |
| 1.0-en | 2026. 11. 18. | 영어판 첫 판(한국어 1.0.1판을 옮김) |

## English

*AI Coding for Lawyers: A Self-Study Guide* · edited by Bowon Kwon · edition 1.0-en (November 18, 2026), translated from Korean edition 1.0.1

- [Read online](https://bowonkwon.github.io/AI-Assisted-Handbooks/ai-coding-for-lawyers/en/)
- [PDF (306 pages)](en/ai-coding-for-lawyers-v1.0-en.pdf)
- [Practice repository](https://github.com/BowonKwon/AI-Coding-for-Lawyers): the practice code and 59 Colab notebooks

A self-study guide that takes lawyers with no coding experience from setting up a development environment to implementing deep learning models themselves. Part 1 covers the environment, Python, the debugger, AI coding assistants, and Git; Part 2 covers training pipelines, CNNs, Transformers, and language models. The code listings were run and their output copied into the book (a few cells that run only on Colab could not be run and are marked "not run"). All cases in the examples are invented.

In the English edition the code listings, commands, and program output are printed exactly as in the Korean edition, so comments and output labels in them are in Korean; a line beginning "In English:" under a listing gives their meaning. The explanatory text in the practice notebooks is in Korean, and their code is the same Korean-commented code as the listings in the book (the Add comments and Rebuild notebooks leave out comments or function bodies for you to fill in).

These are personal study materials and do not represent the views or work of any institution the editor belongs to. Not legal advice.
