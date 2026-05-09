# 설치 가이드 / Installation Guide

> CYS Vision Coaching Skills를 Claude Code에 설치하는 방법
> How to install CYS Vision Coaching Skills in Claude Code

---

## 📋 사전 요구사항 / Prerequisites

### 한국어
1. **Claude Code 설치**: [claude.com/claude-code](https://claude.com/claude-code) 에서 다운로드
2. **Git**: 명령줄에서 `git --version` 으로 설치 확인
3. **터미널 접근**: macOS 터미널, Linux Bash, Windows WSL/Git Bash

### English
1. **Claude Code installed**: Download from [claude.com/claude-code](https://claude.com/claude-code)
2. **Git**: Verify with `git --version`
3. **Terminal access**: macOS Terminal, Linux Bash, or Windows WSL/Git Bash

---

## 🚀 빠른 설치 / Quick Install

### Step 1: 저장소 복제 / Clone Repository

```bash
# 원하는 위치로 이동 (예: 홈 폴더)
cd ~

# 저장소 복제
git clone https://github.com/ysfuture/cys-claude-vision-coaching-skills.git

cd cys-claude-vision-coaching-skills
```

### Step 2: 25개 스킬 자동 등록 / Auto-Register 25 Skills

#### macOS / Linux

```bash
# Claude Code 스킬 디렉토리 확인 (없으면 생성)
mkdir -p ~/.claude/skills

# 25개 스킬 모두 심볼릭 링크로 등록
for d in skills/*/; do
 name=$(basename "$d")
 ln -sf "$(pwd)/$d" ~/.claude/skills/$name
done

# 등록 확인
ls -la ~/.claude/skills/ | grep vision-
```

성공 시 25개 스킬이 모두 표시됩니다.

#### Windows (WSL 또는 Git Bash)

```bash
# WSL은 위 macOS/Linux 명령 그대로
# Git Bash는 다음 사용:

mkdir -p ~/.claude/skills

for d in skills/*/; do
 name=$(basename "$d")
 cp -r "$(pwd)/$d" ~/.claude/skills/$name
done

ls -la ~/.claude/skills/ | grep vision-
```

(Windows는 심볼릭 링크 권한이 까다로워서 *복사*가 안전합니다. 단, 업데이트 시 다시 복사 필요.)

### Step 3: Claude Code 재시작 / Restart Claude Code

Claude Code를 *완전히 종료*하고 다시 실행하여 새 스킬을 인식시킵니다.

---

## ✅ 설치 검증 / Verify Installation

Claude Code에서 다음 명령 실행:

```
/vision-five-stages
```

박사님 비전 5단계 스킬이 작동하면 설치 성공입니다.

또는:

```
/vision-cys-competence-visioncoding
```

CYS 비전 역량 진단 스킬이 작동하면 정상.

---

## 🔄 업데이트 / Updates

저장소 업데이트가 있을 때:

```bash
cd ~/cys-claude-vision-coaching-skills
git pull origin main

# Symlink 사용자는 자동 반영
# Copy 사용자는 다시 복사 필요:
for d in skills/*/; do
 name=$(basename "$d")
 cp -rf "$(pwd)/$d" ~/.claude/skills/$name
done
```

---

## 🗑 제거 / Uninstall

```bash
# 모든 vision-* 스킬 제거
ls ~/.claude/skills/ | grep "^vision-" | xargs -I {} rm -rf ~/.claude/skills/{}

# 저장소 제거
rm -rf ~/cys-claude-vision-coaching-skills
```

---

## 🛠 부분 설치 / Partial Install

전체 25개가 아닌 *일부 스킬*만 설치하려면:

```bash
# 예시: 진단 7종만 설치
SKILLS=(
 vision-cys-competence-visioncoding
 vision-mbti-visioncoding
 vision-enneagram-visioncoding
 vision-strong-visioncoding
 vision-multipleintel-visioncoding
 vision-values-visioncoding
 vision-readiness-visioncoding
)

for s in "${SKILLS[@]}"; do
 ln -sf "$(pwd)/skills/$s" ~/.claude/skills/$s
done
```

또는 *박사님 책 토대 척추 5종*:

```bash
SKILLS=(
 vision-five-stages
 vision-mission-frame
 vision-statement-writer
 vision-smart-five-competence
 vision-eight-training-areas
)

for s in "${SKILLS[@]}"; do
 ln -sf "$(pwd)/skills/$s" ~/.claude/skills/$s
done
```

자세한 *사용자 유형별 추천 패키지*는 [SKILL_CATALOG.md](SKILL_CATALOG.md) 참조.

---

## 🐛 문제 해결 / Troubleshooting

### 문제: 스킬이 Claude Code에서 인식되지 않음

**해결**:
1. Claude Code *완전 종료* 후 재시작
2. `~/.claude/skills/` 안에 `vision-*` 폴더가 있는지 확인
3. 각 폴더 안에 `SKILL.md` 파일이 있는지 확인:
 ```bash
 ls ~/.claude/skills/vision-five-stages/SKILL.md
 ```
4. 권한 확인:
 ```bash
 ls -la ~/.claude/skills/ | head
 ```

### 문제: 심볼릭 링크가 깨짐 (broken symlink)

**해결**:
```bash
# 깨진 링크 모두 제거
find ~/.claude/skills/ -maxdepth 1 -type l ! -exec test -e {} \; -delete

# 다시 등록
cd ~/cys-claude-vision-coaching-skills
for d in skills/*/; do
 name=$(basename "$d")
 ln -sf "$(pwd)/$d" ~/.claude/skills/$name
done
```

### 문제: macOS Gatekeeper / Windows Defender 경고

**해결**: 본 패키지는 *Markdown 텍스트 파일만* 포함하며 실행 코드 없음. 안전 표시 후 진행.

---

## 📚 다른 박사님 시리즈와의 연계 / Integration with Other Dr. Choi Series

### foresight-* 시리즈 (미래 예측)
박사님이 별도 운영하는 미래 예측 스킬 시리즈와 연계 가능.
- `foresight-futures-wheel` — 박사님 책 미래 자극 단계 핵심 도구

### sermon-* 시리즈 (설교)
박사님 담임목사 활용 설교 도구 시리즈와 별도이나 함께 사용 가능.

---

## 💡 다음 단계 / Next Steps

설치 완료 후:

1. **[PHILOSOPHY.md](PHILOSOPHY.md)** — 박사님 비전 철학 학습
2. **[SKILL_CATALOG.md](SKILL_CATALOG.md)** — 25개 스킬 카탈로그 탐색
3. **박사님 원서 구입** — 『미래준비학교』(지식노마드, 2016)
4. **첫 스킬 실행**:
 ```
 /vision-five-stages
 ```

---

## 📞 도움말 / Help

- **이슈 제기**: GitHub Issues
- **이메일**: ysfuture@gmail.com
- **박사님 소속**: 아시아미래인재연구소 / 소망과사랑의교회

---

*비전, 그 깊은 데로 가라. 비전, 그 행복으로 가라.*
*— 박사님 책*
