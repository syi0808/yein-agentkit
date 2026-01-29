# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## MANDATORY WORKFLOW

**Every task must follow this pattern:**

```
1. START  →  work-context-finder (check previous work)
2. WORK   →  implement the task
3. FINISH →  /log-work (document automatically)
4. IF SPECS CHANGED → planning-manager
```

### Before Starting Any Task

Run `work-context-finder` agent first (skip if continuing within same session):
```
Use Task tool with subagent_type="work-context-finder"
```

### After Completing Any Task

Execute `/log-work` skill automatically (do NOT ask for permission):
```
Use Skill tool with skill="work-logger"
```

If specifications changed, run `planning-manager` agent.

---

{{custom}}