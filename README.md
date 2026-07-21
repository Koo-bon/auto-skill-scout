# 🔔 auto-skill-scout

매일 정해진 시간에 당신의 **Claude Code 대화를 자동으로 분석**해서,
**작업 현황 브리프**와 **딱 맞는 검증된 스킬 2~3개**를 추천해주는 **개인 비서 스킬**입니다.

---

## 🚀 설치 (10초, 터미널 필요 없음)

**Claude Code(데스크톱/CLI 앱)를 열고, 아래를 그대로 복사해서 붙여넣으세요:**

```
이 스킬 설치하고 매일 오전 9시에 실행되게 해줘:
https://github.com/Koo-bon/auto-skill-scout
```

Claude가 알아서 다운로드하고, `~/.claude/skills/`에 설치하고, 스케줄까지 잡아줍니다.
당신은 **"허용" 버튼만 한 번** 누르면 끝. ✅

> 💡 원하는 시간으로 바꾸려면 "오전 9시" 대신 "오후 2시"처럼 말하면 됩니다.

---

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
Claude 알림으로 전달
  ↓
_scout-recommendations.md에 자동 저장
```

---

## 📊 추천 예시

```
📋 당신이 자주 막혔던 문제 3가지
1. 문서 서식 정리에 매번 시간 낭비
2. "지난주에 뭘 했더라?" 회고가 흐릿함
3. 커밋 메시지 작성이 매번 고민

🎯 오늘 추천

1️⃣ oh-my-claudecode — 협업 + 문서 자동화
   💭 당신: "문서 서식 정리하는데 시간이 오래 걸려"
   Before: 서식 정리 20분  →  After: 1명령 2분
   🔗 github.com/Koo-bon/oh-my-claudecode

2️⃣ session-analyzer — 세션 분석 + 요약
   💭 당신: "지난주에 뭘 했더라?"
   Before: 회고 15분, 기억 의존  →  After: 30초 자동 요약
   🔗 github.com/anthropics/skills

3️⃣ git-master — 자동 커밋 메시지
   💭 당신: "커밋 메시지 뭐라고 쓸지 고민돼"
   Before: 메시지 작성 5분  →  After: 변경 스캔해서 자동 생성
   🔗 github.com/anthropics/skills
```

**핵심:** 추천이 무작위가 아니라 **당신이 실제로 한 말 + Before/After** 기반입니다.

---

## ⚙️ 시간 바꾸기 / 확인

설치 후엔 Claude에게 말로 하면 됩니다:

- 시간 변경: `"auto-skill-scout 실행 시간을 오후 2시로 바꿔줘"`
- 스케줄 확인: `/schedule list`

---

## ❓ FAQ

**Claude가 꺼져 있어도 오나요?**
스케줄은 **Claude 앱이 열려 있을 때** 실행됩니다. 예약 시간에 앱이 꺼져 있었다면, **다음에 앱을 켤 때** 실행됩니다. (알림을 놓치지 않습니다.)

**어디로 알림이 오나요?**
Claude Code 앱 자체 알림으로 옵니다. Slack·이메일 설정이 필요 없습니다.

**정말 내 패턴을 알 수 있나요?**
네. 지난 7일 대화를 분석해서 **당신이 실제로 한 말**을 그대로 인용하고, 그 문제를 푸는 검증된 스킬을 추천합니다. → [Before & After 예시](BEFORE_AFTER.md)

**지난 추천은 어디에?**
프로젝트 폴더의 `_scout-recommendations.md`에 매일 자동 저장됩니다.

---

**GitHub**: https://github.com/Koo-bon/auto-skill-scout
**License**: MIT

Made with ❤️ by Koo-bon
