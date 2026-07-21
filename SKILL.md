---
name: auto-skill-scout
description: 매일 정해진 시간에 당신의 Claude Code 대화를 자동으로 분석해서 딱 맞는 스킬 2~3개를 추천해주고, 피드백을 받아서 계속 개선하는 자동 알람 스킬
---

# 🔔 auto-skill-scout

당신의 대화를 매일 자동으로 분석해서 **딱 맞는 검증된 스킬 2~3개만** 추천해주는 알람 스킬입니다.
**대화 기반 추론 → 객관식 자동 선택 → 실제 검색 → 최고 검증된 것만 → 자동 저장 → 피드백 학습 → 다음 추천에 반영**

## 🎯 핵심 기능

### 1️⃣ 매일 자동 알람
- ⏰ 매일 정해진 시간에 자동 실행
- 📊 지난 7일 대화 자동 분석
- 🔔 Slack/Discord로 알림

### 2️⃣ 스마트 추천
- 🧠 당신의 반복 작업 패턴 학습
- 🎯 최고로 검증된 2~3개만 (많이 안 뿌림)
- 📈 Reddit/GitHub 실제 인기도 기반

### 3️⃣ 피드백 + 학습
- ⭐ 추천 만족도 자동 수집
- 📝 어떤 스킬이 잘 맞는지 학습
- 🚀 다음 추천에 자동 반영

### 4️⃣ 추천 히스토리
- 💾 매일의 추천 결과 자동 저장
- 📅 추천 경향 추적
- 📊 주간 리뷰 자동 생성

## 🚀 설치

### 방법 1: 수동 설치
```bash
git clone https://github.com/Koo-bon/auto-skill-scout.git
cp -r auto-skill-scout ~/.claude/skills/auto-skill-scout
```

### 방법 2: Claude Code
```bash
/schedule "auto-skill-scout" --daily 09:00
```

## 📝 사용 방법

### 1️⃣ 첫 설정 (한 번만)
```
/schedule "auto-skill-scout" --daily 09:00
```
(원하는 시간으로 변경 가능)

### 2️⃣ 매일 자동 실행
- 매일 09:00에 자동으로 실행
- 당신의 Claude 앱에 추천 도착
- Slack/Discord로도 알림 (설정했으면)

### 3️⃣ 피드백 제공 (선택)
추천을 받은 후:
```
/feedback "이 스킬 좋았나요?"
```

### 4️⃣ 학습 리뷰 (매주 자동)
매주 월요일 자동으로:
- 지난주 추천 성공률 분석
- 피드백 기반 학습 기록
- 다음주 전략 업데이트

## 동작 흐름

```
매일 09:00 (설정 시간)
    ↓
당신의 대화 자동 분석 (지난 7일)
    ↓
반복 작업·관심 도메인 추론
    ↓
객관식 자동 선택
(첫 실행: 물어봄 → 이후 학습된 선호도로 자동 선택)
    ↓
Reddit/GitHub 실제 검색 (2~3개)
    ↓
최고 검증된 것만 필터링
    ↓
추천 결과 저장 (_scout-recommendations.md)
    ↓
Slack/Discord 알림
    ↓
피드백 수집 (/feedback)
    ↓
learnings.md에 학습 기록
    ↓
다음 추천에 반영
```

## 📁 자동 생성 파일

### `_scout-recommendations.md`
매일의 추천 결과를 저장합니다.
```
## 2026-07-21 (월) 09:00
🔭 지난주 패턴: 이미지 처리 + 문서 작성

### 1️⃣ oh-my-claudecode ⭐⭐⭐⭐⭐
이미지 + 문서 처리 자동화 / 팀 협업

### 2️⃣ jezweb image-processing ⭐⭐⭐⭐⭐
배치 이미지 변환

### 3️⃣ claude-code-workflow-orchestration ⭐⭐⭐⭐
반복 작업 자동화

**피드백**: ⏳ 대기 중
```

### `learnings.md`
매주 자동으로 학습 내용을 정리합니다.
```
## Week 30 (2026-07-14 ~ 2026-07-20)

### ✅ 효과 있었던 추천
- image-processing: 설치율 80%, 만족도 5/5
- oh-my-claudecode: 설치율 100%, 만족도 4.7/5

### ⚠️ 개선 필요
- workflow-orchestration: 만족도 3/5 ("설정 복잡함")

### 📊 통계
- 총 추천: 5건
- 평균 만족도: 4.2/5

### 다음주 전략
- 이미지 처리 스킬 우선순위 높이기
- 설정 간단한 스킬 우선
```

## ⚙️ 시간 변경

원하는 시간으로 변경:
```bash
# 오전 8시
/schedule "auto-skill-scout" --daily 08:00

# 오후 2시
/schedule "auto-skill-scout" --daily 14:00

# 저녁 6시
/schedule "auto-skill-scout" --daily 18:00

# 매주 월요일 9시
/schedule "auto-skill-scout" --weekly mon 09:00
```

## 🔧 알림 설정

### Slack 활성화
```
/setup-notification slack
```

### Discord 활성화
```
/setup-notification discord
```

### 이메일 활성화
```
/setup-notification email
```

## 🎓 어떻게 학습하나?

1. **첫 추천** — 당신의 대화 분석 후 객관식으로 "요즘 이런 거 하시죠?" 물어봄
2. **반응 수집** — 추천 후 `/feedback` 으로 만족도 수집
3. **패턴 학습** — 어떤 카테고리가 잘 맞는지 자동 학습
4. **자동 최적화** — 다음부턴 학습된 선호도로 객관식 자동 선택
5. **주간 리뷰** — 매주 "이번주 뭐가 효과 있었나" 정리

## ❓ FAQ

**Q: 추천이 안 와요**
A: `/schedule list` 로 스케줄이 설정되었는지 확인하세요. 설정 시간을 지났는데도 안 오면 Claude Code를 재시작해보세요.

**Q: 추천이 원하는 거랑 다르면?**
A: `/feedback` 으로 반응을 남겨주세요. 피드백이 많을수록 다음 추천이 더 정확해집니다.

**Q: 매일 안 하고 주 1회만 받고 싶으면?**
A: `/schedule "auto-skill-scout" --weekly mon 09:00`

**Q: 지난 추천들은 어디서 봐요?**
A: `_scout-recommendations.md` 파일에 모두 저장됩니다. 편집기로 열어보세요.

**Q: 학습 내용은?**
A: `learnings.md` 에서 매주 업데이트된 통계와 다음주 전략을 확인할 수 있습니다.

## 📈 예상 효과

```
📅 1주차: 기본 추천 (당신 패턴 파악)
📅 2주차: 피드백 반영 (선호도 학습 시작)
📅 3주차: 패턴 최적화 (점점 정확해짐)
📅 4주차: 완전 자동화 (객관식 선택 없이 바로 추천)
```

## 🐛 문제 리포트

버그나 피드백은 [GitHub Issues](https://github.com/Koo-bon/auto-skill-scout/issues)에서:
- 추천 정확도 피드백
- 새 기능 제안
- 버그 리포트

## 📝 라이선스

MIT License — 자유롭게 사용, 수정, 배포 가능

---

**Made with ❤️ by Koo-bon**
