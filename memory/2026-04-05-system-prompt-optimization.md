# Session: 2026-04-05 10:22:51 UTC

- **Session Key**: agent:main:main
- **Session ID**: 8ba91bce-f03e-427b-98d5-8fa0ca0bb58e
- **Source**: gateway:sessions.reset

## Conversation Summary

user: Sender (untrusted metadata):
```json
{
  "label": "openclaw-control-ui",
  "id": "openclaw-control-ui"
}
```

[Sun 2026-04-05 18:19 GMT+8] 我现在都开启了哪些插件？怎么关闭他们
assistant: 你现在开启了 **43 个插件**（总共 85 个可用）。以下是已启用（loaded）的插件列表：

## 已启用的插件

**AI 模型提供商**：
- amazon-bedrock, anthropic, anthropic-vertex, byteplus, chutes, cloudflare-ai-gateway, copilot-proxy, deepseek, fal, github-copilot, google, huggingface, kilocode, kimi, litellm, microsoft-foundry, minimax, mistral, modelstudio, moonshot, nvidia, ollama, openai, opencode, opencode-go, openrouter, qianfan, sglang, synthetic, together, venice, vercel-ai-gateway, vllm, volcengine, xai, xiaomi, zai

**工具/功能**：
- browser（浏览器工具）
- device-pair（设备配对）
- duckduckgo（DuckDuckGo 搜索）
- memory-core（核心记忆搜索）
- phone-control（手机控制）
- talk-voice（语音选择）

**已禁用的插件**（22 个）包括：acpx, bluebubbles, brave, deepgram, diagnostics-otel, diffs, discord, elevenlabs, exa, feishu, firecrawl, googlechat, groq, imessage, irc, line, lancedb, microsoft-speech, msteams, nextcloud-talk, nostr, open-prose, openshell, perplexity, qqbot, searxng, signal, slack, synology-chat, tavily, telegram, thread-ownership, tlon, twitch, voice-call, whatsapp, zalo, zalouser 等。

---

## 如何关闭插件

关闭插件的命令格式：
```bash
openclaw plugins disable <插件 ID>
```

例如：
```bash
openclaw plugins disable browser
openclaw plugins disable duckduckgo
```

如果你想批量关闭不需要的插件，可以一次性执行多条命令。需要我帮你关闭某些特定的插件吗？
user: Sender (untrusted metadata):
```json
{
  "label": "openclaw-control-ui",
  "id": "openclaw-control-ui"
}
```

[Sun 2026-04-05 18:21 GMT+8] 你现在的系统提示词太臃肿了，每次对话至少消耗我1万的token，请问该怎么优化一下
