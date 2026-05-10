# Paper Reading 13 Questions

> 논문을 깊고 빠르게 읽는 13가지 질문.

AI+Robotics 논문을 배경, 문제, 방법, 검증, 결과, 한계, 공개 자원까지 구조적으로 읽고 비교하기 위한 single-page prompt framework입니다.

Live site: <https://gisbi-kim.github.io/paper-reading-13-questions/>

## Why

논문 요약은 쉽게 피상적으로 흐릅니다.  
이 페이지는 논문을 단순히 소개하는 대신, 다음 질문에 답하도록 강제합니다.

- 왜 이 논문이 나왔는가?
- 기존 방법의 어떤 빈칸을 메우는가?
- 핵심 아이디어는 무엇이고 어떻게 구현되는가?
- 어떤 데이터셋, 실험, baseline으로 검증했는가?
- 결과를 어디까지 믿을 수 있고, 어디서 깨지는가?
- 코드, 데이터셋, benchmark 같은 공개 자원은 실제로 확인되는가?

## The 13 Questions

각 논문은 아래 13개 항목으로 정리합니다.

| No. | Question | Purpose |
| --- | --- | --- |
| 01 | 배경 | 연구가 놓인 큰 분야와 임무 맥락을 잡습니다. |
| 02 | 문제 | 논문이 풀려는 구체적 과제를 명확히 합니다. |
| 03 | 기존 한계 | 기존 방법, 도구, 가정의 부족한 지점을 찾습니다. |
| 04 | 목표 | 논문이 명시적으로 달성하려는 목표를 확인합니다. |
| 05 | 방법 | 제안 알고리즘, 시스템, 모델, 절차를 요약합니다. |
| 06 | 핵심 아이디어 | 방법을 차별화하는 기술적 메커니즘을 뽑습니다. |
| 07 | 검증 | 데이터셋, 시뮬레이션, 하드웨어 실험, 시나리오를 봅니다. |
| 08 | 결과 | 성능, 정량 결과, 검증 성공 여부를 확인합니다. |
| 09 | 비교 | baseline, benchmark, 기존 연구와의 차이를 정리합니다. |
| 10 | 의의 | 결과가 가능하게 하는 활용과 연구적 의미를 봅니다. |
| 11 | 한계 | 남아 있는 제약, 실패 사례, 취약점을 분리합니다. |
| 12 | 향후 과제 | 다음 연구 단계나 후속 방향을 구체화합니다. |
| 13 | 자원 공개 | 코드, 데이터셋, 툴킷, benchmark 공개 여부를 확인합니다. |

## Source Discipline

프롬프트는 요약 전에 가능한 한 원문 근거를 확인하도록 설계되어 있습니다.

- Abstract만 보지 않고 PDF 본문, figure, table, appendix까지 최대한 확인합니다.
- arXiv, IEEE, conference proceeding, project page, GitHub, dataset page 같은 1차 출처를 우선합니다.
- 논문 본문과 project page, GitHub가 다르게 말하면 차이를 명시합니다.
- 확인 불가능한 내용은 `확인되지 않음`, `논문 내 명시 없음`, `공개 링크 확인 안 됨`처럼 표시합니다.
- 한계와 향후 과제는 논문이 직접 말한 것과 논문 근거로 도출한 것을 구분합니다.

## Design

The page is intentionally lightweight and static.

- Apple-style bright interface
- Large typography and generous spacing
- Thin borders, soft shadows, and white/translucent cards
- One-column vertical layout for the 13 summary rows
- Rainbow accents for the 13 rows
- Rainbow color is used as information structure, not decoration
- Copy-ready prompt block
- Fully self-contained `index.html`

## ORB-SLAM Example

The live page includes an expandable ORB-SLAM example.

Click `ORB-SLAM 예시 보기` to see how the 13-question framework turns a real SLAM paper into a structured summary.

Example paper:

- ORB-SLAM: a Versatile and Accurate Monocular SLAM System
- IEEE Transactions on Robotics, 2015
- arXiv: <https://arxiv.org/abs/1502.00956>
- Code: <https://github.com/raulmur/ORB_SLAM>

## How To Use

1. Open the live site.
2. Go to `복사용 전체 프롬프트`.
3. Copy the full prompt.
4. Replace the `[논문 리스트]` section with paper titles and URLs.
5. Ask the model to generate `paper_summaries_apple_style.html`.

## Local Preview

Open `index.html` directly in a browser, or serve the folder locally:

```powershell
python -m http.server 8001 --bind 127.0.0.1
```

Then open:

```text
http://127.0.0.1:8001/index.html
```

## Project Structure

```text
.
├── index.html
├── README.md
└── .gitignore
```

## Intended Scope

This framework is especially useful for AI+Robotics papers, including:

- SLAM
- robot navigation
- 3D perception
- VLM/VLA
- embodied AI
- robot learning
- human-robot interaction

It can also be adapted to broader technical paper reading when source-grounded, structured comparison matters.
