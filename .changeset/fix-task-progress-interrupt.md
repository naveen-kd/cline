---
"cline": patch
---

fix: filter task_progress messages to prevent interrupting cline asks

Fixes a bug where task_progress updates would interrupt cline asks like plan_mode_respond. The webview now filters out task_progress messages when determining the last message and cline ask state, ensuring the UI remains in the correct waiting-for-input state.
