---
name: auto-skill-scout
description: 매일 정해진 시간에 당신의 Claude Code 대화를 자동으로 분석해서 당신의 작업 현황을 브리프로 정리하고 딱 맞는 검증된 스킬 2~3개를 Claude 알림으로 추천해주는 개인 비서 스킬
---

# 🔔 auto-skill-scout

당신의 대화를 매일 분석해서 **사용 현황 브리프 + 맞춤 스킬 추천**을 Claude 알림으로 보내주는 스킬입니다.
마치 개인 보고서처럼 당신의 작업을 판단하고, 필요한 스킬을 자동으로 추천합니다.

## 🎯 핵심 기능

- ⏰ **매일 자동 실행** — 정해진 시간에 자동으로 분석 & 추천
- 📊 **사용 현황 브리프** — 당신의 지난 7일 작업 패턴 정리
- 🎯 **맞춤 스킬 추천** — 2~3개만 (깔끔하고 선택하기 쉬움)
- 🔗 **GitHub 링크 포함** — 각 스킬의 저장소 바로 가기
- 💾 **자동 저장** — `_scout-recommendations.md`에 매일 기록
- 🔔 **Claude 알림** — 따로 설정 필요 없음

## 📖 사용 방법

### 1단계: 설치
```bash
git clone https://github.com/Koo-bon/auto-skill-scout.git
cp -r auto-skill-scout ~/.claude/skills/auto-skill-scout
```

### 2단계: 스케줄 설정
Claude Code에서:
```bash
/schedule "auto-skill-scout" --daily 09:00
```

**시간 변경:**
```bash
/schedule "auto-skill-scout" --daily 08:00    # 오전 8시
/schedule "auto-skill-scout" --daily 14:00    # 오후 2시
/schedule "auto-skill-scout" --weekly mon 09:00  # 매주 월요일
```

### 완료! 🎉
- 매일 정해진 시간에 Claude에서 알림
- 추천 스킬 + GitHub 링크 제공
- `_scout-recommendations.md`에 자동 저장

## 💬 추천 메시지 예시

```
📊 당신의 작업 현황 (지난 7일)
━━━━━━━━━━━━━━━━━━━━━━━
요즘 당신은:
• 이미지 처리 → 오전 10-11시 (지난 3일 5회)
• 팀 협업 활동 → 증가 추세
• 문서 작성 → 주 3회

🎯 오늘 추천 (최고 검증된 2~3개)
━━━━━━━━━━━━━━━━━━━━━━━

1️⃣ oh-my-claudecode
   팀 협업 + 문서 작성 자동화
   ⭐ 4.8/5 | GitHub 2.3k⭐
   🔗 https://github.com/Koo-bon/oh-my-claudecode

2️⃣ jezweb image-processing
   배치 이미지 변환 & 자동 최적화
   ⭐ 4.9/5 | GitHub 1.8k⭐
   🔗 https://github.com/jezweb/image-processing

3️⃣ claude-code-workflow-orchestration
   복잡한 반복 작업 자동화
   ⭐ 4.1/5 | GitHub 1.5k⭐
   🔗 https://github.com/anthropics/skills/workflow
```

## 📁 자동 생성 파일

### `_scout-recommendations.md`
매일의 추천 기록이 자동으로 저장됩니다.
시간이 지나면서 당신의 추천 히스토리를 확인할 수 있습니다.

## 🔄 작동 흐름

```
설정된 시간 (예: 매일 09:00)
    ↓
당신의 대화 자동 분석 (지난 7일)
    ↓
작업 패턴 추출 + 브리프 작성
    ↓
Reddit/GitHub에서 맞춤 스킬 검색
    ↓
최고 검증된 2~3개 선별
    ↓
Claude 알림으로 전송
    ↓
파일에 자동 저장
```

## ✨ 특징

| 항목 | 설명 |
|------|------|
| **설정** | `/schedule` 한 줄로 완료 |
| **알림** | Claude Code 자체 알림 (추가 설정 없음) |
| **추천** | 2~3개만 (간결하고 선택 쉬움) |
| **검증** | Reddit/GitHub 인기도 기반 |
| **저장** | 자동으로 md 파일에 기록 |
| **관리자** | 필요 없음 (개인 사용) |

## ❓ FAQ

**Q: 알림이 안 와요**
A: `/schedule list` 로 스케줄 확인 후, 설정 시간이 지났는지 확인하세요.

**Q: 시간을 바꾸고 싶으면?**
A: `/schedule "auto-skill-scout" --daily 14:00` 등으로 재설정하세요.

**Q: 지난 추천들은?**
A: `_scout-recommendations.md` 파일에 모두 저장되어 있습니다.

---

**GitHub**: https://github.com/Koo-bon/auto-skill-scout
**License**: MIT
