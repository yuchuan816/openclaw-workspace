# Session: 2026-04-05 11:30:40 UTC

- **Session Key**: agent:main:main
- **Session ID**: ab779bdf-3293-436b-9648-a46198e8967d
- **Source**: gateway:sessions.reset

## Conversation Summary

user: Sender (untrusted metadata):
```json
{
  "label": "openclaw-control-ui",
  "id": "openclaw-control-ui"
}
```

[Sun 2026-04-05 19:17 GMT+8] 如何管理你的的插件？
assistant: OpenClaw 的插件管理主要通过配置文件完成。让我先查一下文档。


assistant: OpenClaw 的插件管理主要通过 **配置文件** 和 **CLI 命令** 两种方式，下面是要点：

## 🔧 查看当前插件

```bash
openclaw plugins list          # 列出所有插件及状态
openclaw plugins info <id>     # 查看某个插件详情
openclaw plugins doctor        # 诊断插件加载问题
```

## 📦 安装插件

```bash
openclaw plugins install @openclaw/voice-call     # 从 npm 安装
openclaw plugins install ./my-plugin              # 从本地目录安装
openclaw plugins install -l ./my-plugin           # 链接模式（开发用，不复制）
openclaw plugins install @openclaw/voice-call --pin  # 固定版本
```

## ✅ 启用/禁用

```bash
openclaw plugins enable <id>
openclaw plugins disable <id>
```

## ⬆️ 更新插件

```bash
openclaw plugins update <id>     # 更新单个
openclaw plugins update --all    # 全部更新
```

## ⚙️ 配置方式

在 `openclaw.json` 中配置：

```json5
{
  "plugins": {
    "enabled": true,                // 总开关
    "allow": ["voice-call"],        // 白名单（可选）
    "deny": ["untrusted-plugin"],   // 黑名单
    "load": {
      "paths": ["~/Projects/my-extension"]  // 额外加载路径
    },
    "slots": {
      "memory": "memory-core"       // 独占插槽选择
    },
    "entries": {
      "voice-call": {
        "enabled": true,
        "config": { "provider": "twilio" }
      }
    }
  }
}
```

> ⚠️ 配置更改后需要 **重启 Gateway** 才能生效：
> ```bash
> openclaw gateway restart
> ```

## 🔑 关键概念

- **插件类型**：原生 OpenClaw 插件（进程内运行 TypeScript）或兼容 bundle（Codex/Claude/Cursor 格式）
- **安全**：插件与 Gateway 同一进程运行，**只装你信任的**；工作区插件默认禁用
- **插件目录**：`~/.openclaw/extensions/`
- **配置验证不会执行插件代码**，使用的是 manifest 中的 JSON Schema

有具体想安装或配置的插件吗？
user: Sender (untrusted metadata):
```json
{
  "label": "openclaw-control-ui",
  "id": "openclaw-control-ui"
}
```

[Sun 2026-04-05 19:21 GMT+8] 好的，谢谢
assistant: 不客气！有其他问题随时问我。
