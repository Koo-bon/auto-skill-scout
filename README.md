# 🔔 auto-skill-scout

매일 정해진 시간에 당신의 **Claude Code 대화를 자동으로 분석**해서,
당신에게 딱 맞는 **검증된 스킬 2~3개만** 추천해주는 **자동 알람 스킬**입니다.

> **핵심:** 매일 09:00에 알람처럼 스킬이 도착하고, 피드백을 주면 계속 똑똑해집니다.

## 🎯 뭘 하나?

```
매일 09:00
  ↓
당신의 대화 자동 분석 (지난 7일)
  ↓
"요즘 이런 거 하시죠?" 객관식 확인
  ↓
Reddit/GitHub에서 실제 검색
  ↓
제일 검증된 2~3개만 추천
  ↓
Slack/Discord로 알림
  ↓
피드백 수집
  ↓
다음 추천에 자동 반영
```

## ✨ 특징

- ✅ **매일 자동 알람** — 설정만 하면 매일 스킬 도착
- ✅ **당신 맞춤형** — 대화 기반 분석 + 피드백 학습
- ✅ **검증된 것만** — Reddit/GitHub 인기도 + 커뮤니티 반응
- ✅ **적게, 정확하게** — 많이 뿌리지 않고 최고 2~3개만
- ✅ **자동 저장** — 모든 추천과 피드백 기록
- ✅ **주간 리뷰** — 매주 효과 분석 및 개선

## 🚀 설치

### 1단계: 클론
```bash
git clone https://github.com/Koo-bon/auto-skill-scout.git
cp -r auto-skill-scout ~/.claude/skills/auto-skill-scout
```

### 2단계: 스케줄 설정
Claude Code에서:
```bash
/schedule "auto-skill-scout" --daily 09:00
```

끝! 이제 매일 09:00에 스킬 추천이 옵니다.

## 📖 사용법

### 매일 자동 실행
- 매일 09:00에 자동으로 실행 (시간 변경 가능)
- Claude 앱에 추천 결과 도착
- Slack/Discord로도 알림 (설정했으면)

### 피드백 제공
추천을 받은 후:
```
/feedback "이 스킬 좋았나요?"
```
- ⭐⭐⭐⭐⭐ 완벽해요
- ⭐⭐⭐⭐ 좋아요
- ⭐⭐⭐ 그럭저럭
- ⭐⭐ 별로예요
- ⭐ 안 맞아요

### 시간 변경
```bash
# 오전 8시
/schedule "auto-skill-scout" --daily 08:00

# 오후 2시
/schedule "auto-skill-scout" --daily 14:00

# 매주 월요일만
/schedule "auto-skill-scout" --weekly mon 09:00
```

## 📊 데이터 저장

모든 추천과 피드백은 당신의 프로젝트 폴더에 저장됩니다:

### `_scout-recommendations.md`
매일의 추천 기록:
```
## 2026-07-21 (월) 09:00

🔭 지난주: 이미지 처리 + 문서 작성

### 1️⃣ oh-my-claudecode ⭐⭐⭐⭐⭐
팀 협업 + 문서 자동화

### 2️⃣ jezweb image-processing ⭐⭐⭐⭐⭐
배치 이미지 처리

**피드백**: ⏳ 대기 중
```

### `learnings.md`
매주 학습 내용:
```
## Week 30

✅ 효과 있던 추천
- image-processing (만족도 5/5)
- oh-my-claudecode (만족도 4.7/5)

⚠️ 개선 필요
- workflow-orchestration (만족도 3/5)

📊 통계
- 총 추천: 5건
- 설치율: 80%
- 평균 만족도: 4.2/5
```

## 🧠 어떻게 학습하나?

1. **첫 실행** — 당신 대화 분석 후 "요즘 이런 거 하시죠?" 객관식
2. **피드백 수집** — 매 추천 후 만족도 자동 수집
3. **패턴 학습** — 어떤 스킬이 잘 맞는지 학습
4. **자동 최적화** — 다음부턴 학습된 선호도로 자동 선택
5. **주간 리뷰** — 매주 효과 분석 및 다음주 전략 업데이트

## ❓ FAQ

**Q: 추천이 안 와요**
A: 1) `/schedule list` 로 확인 2) Claude Code 재시작 3) 설정 시간 재확인

**Q: 추천이 원하는 거 아니면?**
A: `/feedback` 으로 반응 남겨주세요. 피드백이 다음 추천에 반영됩니다.

**Q: 자동 선택이 아니라 매번 선택하고 싶으면?**
A: `_scout-preferences.json` 에서 `"autoSelect": false` 로 설정하세요.

**Q: 지난 추천들 봐요?**
A: `_scout-recommendations.md` 에 모두 저장됩니다.

**Q: 학습 내용은?**
A: `learnings.md` 에서 매주 통계와 인사이트를 확인할 수 있습니다.

## 🔧 알림 설정

### Slack 활성화
```
/setup-notification slack
```

### Discord 활성화
```
/setup-notification discord
```

## 🎯 예상 효과

```
📅 1주차: 기본 추천 (패턴 파악)
📅 2주차: 학습 시작 (피드백 반영)
📅 3주차: 최적화 (점점 정확)
📅 4주차: 완전 자동화 (선택 필요 없음)
```

## 📈 주간 통계 예시

```
Week 30 (2026-07-14 ~ 2026-07-20)

추천 5건
설치 4건 (80%)
평균 만족도 4.2/5 ⭐

효과 있던:
✓ image-processing (5/5)
✓ oh-my-claudecode (4.7/5)

개선 필요:
✗ workflow-orchestration (3/5) - 설정 복잡함
```

## 🐛 버그 & 피드백

[GitHub Issues](https://github.com/Koo-bon/auto-skill-scout/issues)에서:
- 추천 정확도 피드백
- 새 기능 제안
- 버그 리포트

## 📝 라이선스

MIT — 자유롭게 사용, 수정, 배포 가능

## 🙌 감사

- skill-scout 기반 개발
- Anthropic Claude Code 팀
- 스폰지클럽 커뮤니티

---

**Made with ❤️ by Koo-bon**

**더 알아보기**: [GitHub](https://github.com/Koo-bon/auto-skill-scout)
