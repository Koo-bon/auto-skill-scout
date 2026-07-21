# 🔔 auto-skill-scout

매일 정해진 시간에 당신의 **Claude Code 대화를 자동으로 분석**해서,
당신의 **작업 현황을 브리프로 정리**하고 **딱 맞는 검증된 스킬 2~3개**를 추천해주는 **개인 비서 스킬**입니다.

## 🚀 1분 설정

```bash
git clone https://github.com/Koo-bon/auto-skill-scout.git
cp -r auto-skill-scout ~/.claude/skills/auto-skill-scout
```

Claude Code에서:
```bash
/schedule "auto-skill-scout" --daily 09:00
```

**완료!** 매일 09:00에 Claude에 알림이 옵니다. ✅

## ✨ 뭘 하나?

```
매일 09:00
  ↓
당신의 대화 자동 분석 (지난 7일)
  ↓
"요즘 당신은 이런 일을 하고 있어요" 브리프 작성
  ↓
필요한 스킬 2~3개 추천 (GitHub 링크 포함)
  ↓
Claude에 알림
  ↓
_scout-recommendations.md에 자동 저장
```

## 📊 추천 예시

```
📊 당신의 작업 현황

요즘 당신은:
• 이미지 처리 (오전 10-11시)
• 팀 협업 (증가 추세)
• 문서 작성 (주 3회)

🎯 오늘 추천

1️⃣ oh-my-claudecode
   팀 협업 + 문서 자동화
   🔗 github.com/Koo-bon/oh-my-claudecode

2️⃣ jezweb image-processing
   배치 이미지 처리
   🔗 github.com/jezweb/image-processing

3️⃣ claude-code-workflow
   반복 작업 자동화
   🔗 github.com/anthropics/skills/workflow
```

## ⚙️ 시간 설정

```bash
# 오전 8시
/schedule "auto-skill-scout" --daily 08:00

# 오후 2시
/schedule "auto-skill-scout" --daily 14:00

# 매주 월요일만
/schedule "auto-skill-scout" --weekly mon 09:00
```

## 📁 데이터

- 📝 **`_scout-recommendations.md`** — 매일의 추천 기록 자동 저장
- 🔔 **Claude 알림** — 추가 설정 필요 없음

## 🎯 특징

- ✅ **완전 자동** — `/schedule` 한 줄로 설정 완료
- ✅ **관리자 무관** — 별도의 승인이나 설정 필요 없음
- ✅ **간결함** — 2~3개만 추천 (많이 안 뿌림)
- ✅ **검증됨** — Reddit/GitHub 인기도 기반
- ✅ **저장됨** — 모든 추천이 파일에 기록

## ❓ FAQ

**시간 바꾸고 싶으면?**
```bash
/schedule "auto-skill-scout" --daily 14:00
```

**지난 추천 봐요?**
프로젝트 폴더의 `_scout-recommendations.md` 파일에 저장됩니다.

**스케줄 확인?**
```bash
/schedule list
```

---

**GitHub**: https://github.com/Koo-bon/auto-skill-scout  
**License**: MIT

Made with ❤️ by Koo-bon
