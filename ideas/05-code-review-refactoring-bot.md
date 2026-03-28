# Idea 5: AI Code Review & Refactoring Bot

## Overview
Integrate OpenClaw into your development workflow as an always-on code review assistant. It watches pull requests, runs static analysis, summarizes diffs, suggests improvements, and can even apply simple refactors automatically — all without sending your proprietary code to external services.

## Problem It Solves
Code reviews are time-consuming and inconsistent. External AI review tools (Copilot, CodeRabbit) send code to the cloud. OpenClaw can provide the same capability locally, making it suitable for teams handling sensitive or proprietary source code.

## Core Features
- **PR Watcher**: OpenClaw polls GitHub/GitLab for new PRs and automatically runs a review when one is opened.
- **Diff Summarizer**: Generates a concise English summary of what changed and why it matters.
- **Issue Detector**: Spots common bugs, security issues (e.g., SQL injection, hardcoded secrets), and style violations.
- **Refactoring Suggestions**: Recommends specific, line-level changes with explanations.
- **Auto-Fix Mode**: For low-risk issues (formatting, trivial renaming), applies fixes and opens a follow-up commit.
- **Chat Interface**: Developers can ask "Explain the changes in PR #42" via Slack/Discord.

## Tech Stack
- OpenClaw skill with GitHub/GitLab webhook listener
- Local LLM via Ollama (DeepSeek Coder, CodeLlama, or Qwen2.5-Coder)
- Tree-sitter or ast-grep for code parsing
- Slack or Discord integration for notifications

## Stretch Goals
- Test generation: automatically write unit tests for new functions
- Dependency vulnerability scanning as part of the review
- Historical pattern learning: track which types of issues are most common per team/repo

## Why It's Great for a Hackathon
Developer-audience-friendly, immediately relatable, and has clear before/after impact. A live demo reviewing an actual PR is very convincing.
