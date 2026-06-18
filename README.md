# Valdis

**Valdis** is a native local-first AI companion for **macOS**, **iOS**, and **iPadOS**.

It connects to local or user-controlled LLM runtimes, supports voice conversations, and is designed around privacy-first usage without collecting user data by default.

This public repository is used for **issue tracking, roadmap discussions, release notes, and support**.

The native Swift codebase is currently private. It may be opened later.

**Supported OS:** macOS 15+ and iOS/iPadOS 18+.

## Quick links

- **Website / Download:** https://valdis.app
- **Report a bug / request a feature:** https://github.com/shura-v/valdis/issues/new/choose
- **Browse existing issues:** https://github.com/shura-v/valdis/issues
- **FAQ / Support:** https://valdis.app/faq
- **Privacy:** https://valdis.app/privacy

## What Valdis focuses on

- Native Apple-platform experience built with Swift and SwiftUI
- Local-first AI workflows with Ollama, LM Studio, and user-controlled runtimes
- Voice conversations with on-device speech-to-text via WhisperKit
- 3D avatar experience powered by RealityKit and Reality Composer Pro
- Privacy-first design: no telemetry or data collection by default
- macOS-hosted local AI with iPhone/iPad companion usage

## How to open an issue

1. Sign in to GitHub.
2. Open the new issue chooser: https://github.com/shura-v/valdis/issues/new/choose
3. Pick **Bug report** or **Feature request**, fill out the template, and submit.

## Before you file an issue

1. Search existing issues first.
2. If it’s a **crash / bug**, include:
   - Device + OS version (macOS/iOS/iPadOS + version)
   - Diagnostics (includes Valdis version/build + system info)
      - **macOS:** menu bar → **Valdis → About Valdis** → **Copy diagnostics**
      - **iOS/iPadOS:** Valdis → **Settings → About** → **Copy diagnostics**
   - Steps to reproduce
   - Expected vs actual behavior
   - Screenshots / screen recording, if helpful
   - Logs **only if you’re comfortable sharing them**

Valdis is privacy-first. Logs do not include chat content, prompt text, context, messages, tokens, or secrets.

## Debug logging

Valdis includes an optional Debug logging mode. When enabled, you can copy recent app logs to include in bug reports.

- **macOS:** menu bar → **Valdis → About Valdis** → **Debug logging**
- **iOS/iPadOS:** Valdis → **Settings → About** → **Debug logging**
- Restart the app after changing the setting.
- After restart, use **Copy logs** to copy recent logs.
- Logs exclude sensitive content: prompts, context, message text, tokens, and secrets.

### Screenshots

| macOS: Enable                                                                         | iOS/iPadOS: Enable                                                                  |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <img src="images/mac-debug-mode.png" alt="macOS Debug logging toggle" height="400" /> | <img src="images/ios-debug-mode.png" alt="iOS/iPadOS Debug logging toggle" height="400" /> |

| macOS: Copy logs                                                                        | iOS/iPadOS: Copy logs                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <img src="images/mac-logs-copy-button.png" alt="macOS Copy logs button" height="400" /> | <img src="images/ios-logs-copy-button.png" alt="iOS/iPadOS Copy logs button" height="400" /> |

## Reset flags (macOS)

If Valdis behaves strangely after an update, or when asked by a maintainer, you can start from a clean state using command-line reset flags.

⚠️ **These actions are destructive and cannot be undone.** Only use them if you understand what will be deleted.

- `--reset-settings` — resets app settings
- `--reset-data` — resets app data: provider instances, model selections, cached state
- `--reset-history` — clears chat history

### Run with Launch Services

```bash
open -a Valdis --args --reset-data --reset-settings --reset-history
```

### Run the app binary directly

```bash
/Applications/Valdis.app/Contents/MacOS/Valdis --reset-data --reset-settings --reset-history
```

## What to report here

✅ Bugs, crashes, UX issues, and performance problems  
✅ Feature requests and product ideas  
✅ Docs, website, and release-note issues

## What not to post

❌ Tokens, API keys, or passwords  
❌ Private conversation content  
❌ Personal data or sensitive logs

## Security

If you believe you found a security issue, **do not** open a public issue.

Email: security@valdis.app

## Thanks ❤️

Valdis builds on great work from the local AI and Apple developer ecosystem:

- **[Ollama](https://github.com/ollama/ollama)** — local LLM runtime
- **[LM Studio](https://lmstudio.ai/)** — local AI on your computer
- **[WhisperKit](https://github.com/argmaxinc/WhisperKit)** by **Argmax** — on-device speech-to-text
- **[Vapor](https://github.com/vapor/vapor)** — WebSocket server backend on macOS
- **[textual](https://github.com/gonzalezreal/textual)** — Markdown rendering
