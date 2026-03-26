# mockup-apply

> 디자이너가 만든 목업, 개발자가 만든 코드 — 그 사이를 연결합니다.

"이 목업대로 만들어줘"라고 했을 때, 기존에 잘 돌아가던 기능이 날아가버린 적 있으신가요?
이 스킬은 **새 디자인은 적용하되, 기존 기능은 한 줄도 잃지 않는 것**을 약속합니다.

---

## 한국어

### 이런 상황에서 쓰세요

- 디자이너(또는 AI)가 HTML 목업을 만들었는데, 실제 코드에 적용해야 할 때
- 디자인은 바꾸고 싶지만, 이미 동작하는 기능(API, 다크모드, 번역 등)은 건들고 싶지 않을 때
- "뭘 추가하고 뭘 건들지 말아야 하는지" 정리가 필요할 때

### 핵심 아이디어

```
ADD:    목업에 있고 코드에 없는 것 → 새로 만든다
CHANGE: 둘 다 있지만 다르게 생긴 것 → 목업에 맞춘다
KEEP:   코드에만 있는 것 → 절대 건들지 않는다
```

목업에 다크모드 버튼이 없다고 삭제하면 안 되잖아요. 그런 실수를 방지합니다.

### 설치

```bash
git clone https://github.com/Elliebinn/mockup-apply.git ~/.claude/skills/mockup-apply
```

### 사용법

```bash
/mockup-apply docs/mockups/dashboard.html              # 기본
/mockup-apply docs/mockups/detail.html --page backtest  # 페이지 지정
/mockup-apply docs/mockups/overview.html --analyze-only # 분석만
```

### 어떻게 동작하나요?

1. **분석** — 목업과 현재 코드를 나란히 읽고, ADD/CHANGE/KEEP 체크리스트를 만들어 보여드립니다. "이거 맞아?" 확인받고 나서야 시작합니다.
2. **디자인 동기화** — DESIGN.md에 새 디자인 토큰을 추가하고, 공통 CSS 클래스를 정리합니다. 톤앤매너가 흐트러지지 않도록.
3. **구현** — 체크리스트를 하나씩 처리합니다. 한꺼번에 다 바꾸지 않고, 하나 하고 확인하고 다음으로.
4. **검증** — 콘솔 에러가 없는지, 기존 기능이 다 살아있는지 확인합니다.

---

## English

### When to use

- You have an HTML mockup (from a designer or AI) and need to apply it to real code
- You want to update the design but keep all working features (APIs, dark mode, i18n, etc.)
- You need a clear plan of what to add, what to change, and what to leave alone

### Core idea

```
ADD:    In mockup, not in code → Build it
CHANGE: In both, but different → Match the mockup
KEEP:   In code, not in mockup → Don't touch it
```

Just because the mockup doesn't show a dark mode toggle doesn't mean you should delete it. This skill prevents that.

### Install

```bash
git clone https://github.com/Elliebinn/mockup-apply.git ~/.claude/skills/mockup-apply
```

### Usage

```bash
/mockup-apply docs/mockups/dashboard.html              # basic
/mockup-apply docs/mockups/detail.html --page backtest  # specify page
/mockup-apply docs/mockups/overview.html --analyze-only # analysis only
```

### How it works

1. **Analyze** — Reads the mockup and current code side by side. Generates an ADD/CHANGE/KEEP checklist and waits for your approval before touching anything.
2. **Design Sync** — Updates DESIGN.md with new tokens, ensures common CSS classes are used consistently.
3. **Implement** — Works through the checklist one item at a time. No big-bang rewrites.
4. **Verify** — Checks for console errors and confirms all existing features still work.

---

## 中文

### 使用场景

- 设计师（或AI）制作了HTML原型，需要应用到实际代码中
- 想更新设计，但不想影响已有功能（API、暗黑模式、国际化等）
- 需要清晰地整理哪些该添加、哪些该修改、哪些不能动

### 核心理念

```
ADD:    原型中有，代码中没有 → 新建
CHANGE: 两边都有，但样式不同 → 按原型改
KEEP:   只在代码中有 → 绝对不动
```

原型里没有暗黑模式按钮，不代表应该删掉它。这个技能就是为了防止这种事情发生。

### 安装

```bash
git clone https://github.com/Elliebinn/mockup-apply.git ~/.claude/skills/mockup-apply
```

### 使用方法

```bash
/mockup-apply docs/mockups/dashboard.html              # 基本用法
/mockup-apply docs/mockups/detail.html --page backtest  # 指定页面
/mockup-apply docs/mockups/overview.html --analyze-only # 仅分析
```

### 工作流程

1. **分析** — 并排阅读原型和现有代码，生成ADD/CHANGE/KEEP检查清单，等待你确认后才开始动手。
2. **设计同步** — 更新DESIGN.md中的设计令牌，确保公共CSS类的一致性。
3. **实现** — 按检查清单逐项处理，不会一次性大改。
4. **验证** — 检查控制台错误，确认所有现有功能仍然正常工作。

---

## Requirements

- [Claude Code](https://claude.com/claude-code)
- Playwright MCP (optional, for verification screenshots)

## License

MIT
