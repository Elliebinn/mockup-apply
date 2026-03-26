# mockup-apply

> HTML 목업을 기존 웹 페이지에 적용하는 Claude Code 스킬

## 한국어

### 설명

HTML 목업 파일을 분석하여 기존 코드와 비교하고, 변경사항을 ADD/CHANGE/KEEP으로 분류합니다. 기존 기능(다크모드, 번역, API 등)을 100% 보존하면서 새 디자인/기능만 구현합니다.

- **ADD**: 목업에 있고 코드에 없는 것 → 구현
- **CHANGE**: 양쪽 다 있지만 다른 것 → 수정
- **KEEP**: 코드에 있고 목업에 없는 것 → 절대 제거하지 않음

### 설치

```bash
git clone https://github.com/Elliebinn/mockup-apply.git ~/.claude/skills/mockup-apply
```

### 사용법

```
/mockup-apply path/to/mockup.html
/mockup-apply path/to/mockup.html --page dashboard
/mockup-apply path/to/mockup.html --analyze-only
```

### 워크플로우

1. **분석** — 목업 vs 현재 코드 비교, 체크리스트 생성, 사용자 승인
2. **디자인 동기화** — DESIGN.md 업데이트, 공통 CSS 클래스 확인
3. **구현** — 체크리스트 순서대로 적용, 기존 기능 보존
4. **검증** — 콘솔 에러 체크, 스크린샷, 사용자 확인

### 요구사항

- [Claude Code](https://claude.com/claude-code)
- Playwright MCP (검증 스크린샷용)

---

## English

### Description

Analyzes HTML mockup files, compares them with existing code, and classifies changes as ADD/CHANGE/KEEP. Implements only new designs/features while preserving 100% of existing functionality (dark mode, translations, APIs, etc.).

- **ADD**: In mockup, not in code → Implement
- **CHANGE**: In both, but different → Modify
- **KEEP**: In code, not in mockup → Never remove

### Install

```bash
git clone https://github.com/Elliebinn/mockup-apply.git ~/.claude/skills/mockup-apply
```

### Usage

```
/mockup-apply path/to/mockup.html
/mockup-apply path/to/mockup.html --page dashboard
/mockup-apply path/to/mockup.html --analyze-only
```

### Workflow

1. **Analyze** — Compare mockup vs current code, generate checklist, user approval
2. **Design Sync** — Update DESIGN.md, check common CSS classes
3. **Implement** — Apply changes per checklist, preserve existing features
4. **Verify** — Console error check, screenshot, user confirmation

### Requirements

- [Claude Code](https://claude.com/claude-code)
- Playwright MCP (for verification screenshots)

---

## 中文

### 说明

分析HTML原型文件，与现有代码进行比较，将变更分类为ADD/CHANGE/KEEP。在100%保留现有功能（暗黑模式、翻译、API等）的同时，仅实现新设计/功能。

- **ADD**: 原型中有，代码中没有 → 实现
- **CHANGE**: 两边都有但不同 → 修改
- **KEEP**: 代码中有，原型中没有 → 绝不删除

### 安装

```bash
git clone https://github.com/Elliebinn/mockup-apply.git ~/.claude/skills/mockup-apply
```

### 使用方法

```
/mockup-apply path/to/mockup.html
/mockup-apply path/to/mockup.html --page dashboard
/mockup-apply path/to/mockup.html --analyze-only
```

### 工作流程

1. **分析** — 比较原型与现有代码，生成检查清单，等待用户批准
2. **设计同步** — 更新DESIGN.md，检查公共CSS类
3. **实现** — 按检查清单顺序应用变更，保留现有功能
4. **验证** — 控制台错误检查、截图、用户确认

### 要求

- [Claude Code](https://claude.com/claude-code)
- Playwright MCP（用于验证截图）

---

## License

MIT
