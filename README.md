# CYS Vision Coaching Skills

> **최윤식 박사의 미래준비학교 — Claude Code Skills Package**
> *Dr. Choi Yoon-Sik's Future Preparation School — Claude Code Skills Package*

<!-- AUTO:BADGE -->
[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Skills: 26](https://img.shields.io/badge/Skills-26-blue)](docs/SKILL_CATALOG.md)
[![Korean](https://img.shields.io/badge/언어-한국어%20%2B%20English-success)](#)
<!-- /AUTO:BADGE -->

---

## 📖 소개 / Introduction

**한국어**

본 패키지는 미래학자 최윤식 박사의 저서 『미래준비학교 — 흔들림 없는 인생을 계획하는 5단계』(지식노마드, 2016)의 *모든 토대*를 Claude Code Skills로 구현한 *비전 코칭 도구 모음*입니다. 26개의 스킬이 박사님이 직접 운영하는 미래준비학교의 *비전 발견·완수 흐름* 그대로 작동하여, 누구나 *자신의 비전을 발견하고 완수하는 인생*을 살도록 돕습니다.

박사님 정의: **비전 = 가치 있는 시대적 소명**

박사님 핵심 메시지:
> *"혼자서 이룰 수 있는 꿈은 절대로 큰 꿈이 아니다!"*

본 패키지가 GitHub에 공개된 이유는 박사님 책의 **비전 재생산 — 비전에 몰입한 사람의 최고 경지**를 디지털·글로벌 차원에서 실현하기 위함입니다.

**English**

This package implements *every framework* from Dr. Choi Yoon-Sik's book 『Future Preparation School: 5 Stages of Planning an Unshakable Life』(Knomad, 2016) as a collection of Claude Code Skills. The 26 skills work as Dr. Choi's *vision discovery·fulfillment flow*, helping anyone *discover and fulfill their vision*.

Dr. Choi's definition: **Vision = A Valuable Calling of the Times**

Core message:
> *"A dream that can be achieved alone is never a big dream!"*

This package is published on GitHub to realize the **Vision Reproduction — the highest level of one fully immersed in vision** at a digital and global scale.

---

## 🎯 누구를 위한 패키지인가? / Who Is This For?

| 대상 / Target | 추천 활용 / Recommended Use |
|--------------|---------------------------|
| 🧑‍🎓 **청년·학생 (18~30)** | 진로·소명 발견 · Discover vocation·calling |
| 👨‍💼 **중년·직업 전환자 (35~55)** | 인생 후반 비전 재설계 · Re-design 2nd half of life |
| 👴 **은퇴기 (55+)** | 제2의 사역·가치 있는 봉사 · Find purpose for retirement |
| ⛪ **교회 청년부·셀모임** | 그룹 비전 코칭 · Group vision coaching |
| 🏫 **신학교·대학교** | 진로 지도 도구 · Career counseling tool |
| 👨‍🏫 **비전 코치·강사** | 강의·세미나 부속 도구 · Lecture·seminar companion |

---

## 🚀 빠른 시작 / Quick Start

### 1. 설치 / Install

자세한 설치는 [INSTALLATION.md](docs/INSTALLATION.md)를 참조하세요.
For detailed installation, see [INSTALLATION.md](docs/INSTALLATION.md).

```bash
# Clone repository
git clone https://github.com/ysfuture/cys-claude-vision-coaching-skills.git
cd cys-claude-vision-coaching-skills

# Symlink all skills to Claude Code
for d in skills/*/; do
 name=$(basename "$d")
 ln -sf "$(pwd)/$d" ~/.claude/skills/$name
done
```

### 2. 첫 사용 — 박사님 8단계 따라가기 / First Use — Following the 8 Stages

박사님 비전 발견·완수 1단계부터:
Start with Stage 1 of Dr. Choi's vision flow:

```
Claude Code에서:
> /vision-cys-competence-visioncoding
```

또는 박사님 책 척추 도식부터:
Or start with Dr. Choi's framework:

```
Claude Code에서:
> /vision-five-stages
```

---

## 🧭 박사님 비전 발견·완수 8단계 / The 8-Stage Flow

박사님이 직접 정리하신 *비전 발견·완수 8단계*. 이 순서대로 스킬을 사용합니다.
Dr. Choi's 8-stage flow for vision discovery·fulfillment. Skills follow this exact order.

```
1. Vision Coding (내 안에 있는 것 파악)
       ↓
2. 나와 연관된 미래 예측
       ↓
3. 5가지 시대적 필요 발견 (문제·욕구·결핍·위기·기회)
       ↓
4. 마음을 사로잡는 가치 명확화 + 비전의 결과·열매
       ↓
5. "가치 + 시대적 필요 + 내 안의 능력" 종합 → 비전 출발점·큰 그림
       ↓
6. 비전선언문 작성
       ↓
7. 비전 성취 구체 설계 (목표·전략·필요한 것)
       ↓
8. 미래비전 지속 셀프코칭 (자극·디자인·심층탐구·훈련·네트워킹·재생산)
```

| 단계 / Stage | 박사님 단계명 / Stage | 사용 스킬 / Skills |
|----------|-------------------|----------------|
| **1** | Vision Coding — 내 안에 있는 것 파악 | 진단 7종 (아래 카탈로그) |
| **2** | 나와 연관된 미래 예측 | `vision-personal-future-research` → `foresight-futures-wheel` → `vision-four-futures` → `vision-futures-timeline-map` (순차) |
| **3** | 5가지 시대적 필요(문제·욕구·결핍·위기·기회) 발견 | `vision-future-needs-prediction` · `vision-future-promise-five-criteria` |
| **4** | 마음을 사로잡는 가치 명확화 + 비전 열매 예상 | `vision-values-visioncoding` · `vision-three-realm-balance` |
| **5** | "가치 + 시대적 필요 + 내 능력" 종합 — 비전 출발점·큰 그림 | `vision-clarity-coaching` · `vision-mission-frame` |
| **6** | 비전선언문 작성 | `vision-statement-writer` |
| **7** | 비전 성취 구체 설계 — 목표·전략·필요한 것 | `vision-goal-reframing` · `vision-strategy-coach` · `vision-financial-3shields-3windows` · `vision-financial-coach` · `vision-career-recommendation` |
| **8** | 미래비전 지속 셀프코칭 — 자극·디자인·심층탐구·훈련·네트워킹·재생산 | `vision-five-stages` · `vision-smart-five-competence` · `vision-eight-training-areas` · `vision-follow-through-habits` · `vision-progress-review` |

> 참고: 본 8단계 표는 박사님이 명시한 *순서가 의미 있는* 표이므로 빌드 스크립트 자동 갱신 대상에서 제외됩니다. 새 스킬을 단계에 편입할 때 직접 편집하세요.

---

## 📚 26개 스킬 카탈로그 / 26 Skills Catalog

전체 카탈로그·연결도는 [SKILL_CATALOG.md](docs/SKILL_CATALOG.md)
Full catalog·diagram in [SKILL_CATALOG.md](docs/SKILL_CATALOG.md)

### Vision Coding - 진단 7종 / Diagnosis (7)
박사님 8단계 *1단계 — 내 안에 있는 것 파악*

| 스킬 / Skill | 측정 / Measures |
|------------|---------------|
| `vision-cys-competence-visioncoding` | CYS 10 비전 코드 (박사님 직접 개발) |
| `vision-mbti-visioncoding` | MBTI 16유형 |
| `vision-enneagram-visioncoding` | 에니어그램 9유형 |
| `vision-strong-visioncoding` | STRONG/RIASEC 직업 흥미 |
| `vision-multipleintel-visioncoding` | 다중지능 9지능 |
| `vision-values-visioncoding` | 가치 매핑 (3프레임워크 통합) — 4단계에서도 사용 |
| `vision-readiness-visioncoding` | 꿈 달성 4능력 |

### 박사님 책 토대 — 척추 도식 (5)
박사님 미래준비학교 *고유 프레임* — 8단계 전반에 걸쳐 활용

| 스킬 / Skill | 박사님 고유 모델 | 주 활용 단계 |
|------------|---------------|------|
| `vision-five-stages` | 비전 5단계 (스케치→디자인→훈련→재인식→재생산) | 8단계 (지속 셀프코칭) |
| `vision-mission-frame` | 비전 프레임 (영적 직관력+이성적 판단력+R) | 5단계 (큰 그림) |
| `vision-statement-writer` | 비전 선언문 양식 그대로 | 6단계 (선언문) |
| `vision-smart-five-competence` | SMART 5역량 (S·M·A·R·T) | 8단계 (훈련) |
| `vision-eight-training-areas` | 비전 훈련 8대 영역 | 8단계 (훈련) |

### 박사님 책 토대 — 살·근육 (7)
박사님 책의 *세부 도구* + 박사님 미래학 *응용 도구* — 8단계 전반에 걸쳐 활용

| 스킬 / Skill | 박사님 고유 모델 / 응용 | 주 활용 단계 |
|------------|---------------|------|
| `vision-financial-3shields-3windows` | 재정 3방패+3창 | 7단계 (구체 설계) |
| `vision-personal-future-research` | 진단 7종 → 개인 맞춤 미래 변화 매트릭스 (응용) | 2단계 (미래 예측 — *시작점*) |
| `vision-futures-timeline-map` | 미래지도 작성 4가지 고려 | 2단계 (미래 예측 — *완성*) |
| `vision-four-futures` | 4가지 미래 (Plausible/Possible/Wildcard/Normative) | 2단계 (미래 예측) |
| `vision-future-promise-five-criteria` | 미래 유망성 5기준 | 3단계 (시대적 필요) |
| `vision-three-realm-balance` | 비전 영역 3겹 (개인/가족·세상/정신적) | 4단계 (가치·열매) |
| `vision-future-needs-prediction` | 미래 필요 3축 분해 | 3단계 (시대적 필요) |

### 2단계 미래 예측 — 박사님 권장 순차 흐름

박사님이 직접 정리하신 2단계 *4스킬 순차 사용*:

```
[1단계 진단 7종 결과 입력]
     ↓
① vision-personal-future-research
   → 진단 7종 결과로 *나와 연관된* 미래 변화 매트릭스 추출
     ↓
② foresight-futures-wheel
   → 핵심 변화 1~2개로 1차→2차→3차→4차→고차 영향 추론
     ↓
③ vision-four-futures
   → Plausible/Possible/Wildcard/Normative 4가지 미래 가능성 분류
     ↓
④ vision-futures-timeline-map
   → 단기·중기·장기 시간축 미래지도 *완성*
     ↓
[3단계로 — 5가지 시대적 필요 발견]
```

### 처방·실행 (7)
일반 코칭 도구 — 7~8단계에 활용

| 스킬 / Skill | 도구 | 주 활용 단계 |
|------------|------|------|
| `vision-strategy-coach` | 일반 5단계 (비전핵심→장기→단기→행동→측정) | 7단계 (구체 설계) |
| `vision-career-recommendation` | 4유형 직업 추천 (미래·재미·봉사·고소득 각 5개) | 7단계 (구체 설계) |
| `vision-clarity-coaching` | 소크라테스 산파술 비전 명료화 | 5단계 (큰 그림) |
| `vision-goal-reframing` | SMART + Backcasting + OKR | 7단계 (구체 설계) |
| `vision-financial-coach` | Dave Ramsey + Suze Orman 재정 | 7단계 (구체 설계) |
| `vision-follow-through-habits` | BJ Fogg + James Clear + Charles Duhigg 습관 | 8단계 (지속) |
| `vision-progress-review` | 주간·월간·분기·연간 4단위 점검 | 8단계 (지속) |

---

## 🧭 박사님 비전 철학 / Dr. Choi's Vision Philosophy

박사님 비전 정의: **비전 = 가치 있는 시대적 소명**

### 비전 5대 공리
1. 당신은 *유일하고 고귀하고 특별*하다
2. 비전은 *모든 사람*이 가질 수 있다
3. 비전은 *개별적*이다, 그래서 *시대적*이다
4. 누구에게나 *비전을 이룰 역량*이 있거나 마련할 수 있다
5. 모든 비전은 *나·가족·이웃·인류*에게 가치 있는 것으로 귀결되어야 한다

### 3가지 비전 질문
1. 내가 *기뻐할 수 있는 가치*가 무엇인가?
2. 내가 *살아갈 시대 모습*은 무엇인가?
3. 내가 *기쁘게 헌신할 수 있는 구체적 일(소명)*은 무엇인가?

### 6대 행동 강령
- 서두르지 마라 (**Take a Time**)
- 멀리 보라 (**Foresee Futures**)
- 비전을 품어라 (**Make a Vision**)
- 계획을 짜라 (**Make a Plan**)
- 어떻게 일할지 훈련하고 생각하라 (**Train and Think about How To Work**)
- 작은 일을 소중하게 하라 (**Be Faithful with a Few Things**)

자세한 철학은 [PHILOSOPHY.md](docs/PHILOSOPHY.md) 참조.

---

## 🔧 새 스킬 추가 / Adding New Skills

박사님이 새 스킬을 만드시면 다음 절차를 따르세요:

```bash
# 1) 새 스킬 폴더 + SKILL.md 작성
#    frontmatter에 다음 두 줄을 권장 (자동 분류용)
#    category: diagnosis | spine | flesh | prescription
#    stage: 1   (또는 1,4 등 콤마 구분)

# 2) Claude Code에 등록
ln -sf "$(pwd)/skills/<new-name>" ~/.claude/skills/<new-name>

# 3) 카탈로그 자동 갱신
python3 _build_catalog.py

# (선택) 변경 필요 여부만 검증
python3 _build_catalog.py --check
```

빌드 스크립트가 자동 갱신하는 영역:
- `README.md` — 배지 (`Skills: NN`)
- `docs/SKILL_CATALOG.md` — 제목 카운트, 4대 카테고리 합계, 전체 스킬 인덱스 표

**자동 갱신 *대상 외*** (직접 편집):
- 8단계 매핑 표 (순서가 의미를 가짐)
- 카테고리별 상세 설명 카드
- 8단계 흐름 다이어그램·사용자 유형별 패키지

frontmatter에 `category`/`stage`가 없으면 `_build_catalog.py`의 `DEFAULT_META`에서 보충합니다. 신규 스킬을 카탈로그에 자동 분류시키려면 frontmatter에 직접 적거나 `DEFAULT_META`에 한 줄 추가하면 됩니다.

---

## 📂 폴더 구조 / Folder Structure

```
cys-claude-vision-coaching-skills/
├── README.md # 본 문서
├── LICENSE # CC BY-NC-SA 4.0
├── _build_catalog.py # 카탈로그 자동 빌드 스크립트
├── docs/
│ ├── PHILOSOPHY.md # 박사님 비전 철학
│ ├── SKILL_CATALOG.md # 26개 스킬 카탈로그 (8단계 흐름)
│ ├── INSTALLATION.md # 설치 가이드
│ ├── BOOK_MAPPING.md # 책 ↔ 스킬 매핑 (Phase 2)
│ ├── EIGHT_STAGE_GUIDE.md # 8단계 상세 가이드 (Phase 2)
│ ├── USAGE_PATHS.md # 사용자 유형별 경로 (Phase 2)
│ ├── WORKFLOWS.md # 통합 워크플로우 (Phase 2)
│ ├── GLOSSARY.md # 용어집 (Phase 3)
│ └── CONTRIBUTING.md # 기여 가이드 (Phase 3)
├── skills/ # 26개 Claude Code 스킬
│ ├── vision-cys-competence-visioncoding/
│ ├── vision-five-stages/
│ ├── vision-mission-frame/
│ ├── ... (26개)
│ └── vision-progress-review/
└── examples/ # 시나리오 예시 (Phase 3)
```

---

## 📖 박사님 원서 / Original Book

본 패키지의 모든 토대는 다음 책에 있습니다. 깊이 있는 학습을 위해 반드시 *원서를 함께* 읽으시기를 권장합니다.

This package is rooted in the following book. For deep learning, *please read the original book*.

> **최윤식·최현식, 『최윤식의 미래준비학교 — 흔들림 없는 인생을 계획하는 5단계』, 지식노마드, 2016. (ISBN 978-89-93322-97-2)**

---

## 🤝 기여 / Contributing

본 패키지는 박사님 *비전 재생산* 정신을 따라 *공동체적*으로 발전합니다. 피드백·번역·확장 모두 환영합니다.

This package grows *as a community* in the spirit of Dr. Choi's *vision reproduction*. Feedback, translations, and extensions are all welcome.

자세한 내용은 [CONTRIBUTING.md](docs/CONTRIBUTING.md) (Phase 3 작성 예정) 참조.

---

## 📜 라이선스 / License

본 패키지는 [CC BY-NC-SA 4.0](LICENSE) 라이선스로 제공됩니다 (비상업·저작자표시·동일조건변경허락).

This package is licensed under [CC BY-NC-SA 4.0](LICENSE) (NonCommercial-Attribution-ShareAlike).

상업적 활용 문의 / Commercial use inquiry: **ysfuture@gmail.com**

---

## 🙏 비전 / Vision

박사님 책 인용:
> *"그 어떤 사람들도 비전 재생산의 대상이 될 수 있다."*

이 패키지를 통해 한 사람이라도 더 *자신의 비전을 발견하고 완수하는 인생*을 산다면, 박사님의 *비전 재생산*이 디지털·글로벌 차원에서 살아 있는 것입니다.

If even one more person *discovers and fulfills their vision* through this package, Dr. Choi's *Vision Reproduction* lives on at a digital and global scale.

---

**Made with ❤️ following Dr. Choi Yoon-Sik's Future Preparation School**

*비전, 그 깊은 데로 가라. 비전, 그 행복으로 가라.*
*— 최윤식 박사, 『미래준비학교』*
