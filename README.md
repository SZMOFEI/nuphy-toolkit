# NuPhy PRD Clarifier

把模糊的运营需求，通过逐步提问澄清为可直接进入飞书需求池的结构化需求与轻量 PRD。

这个插件适合 NuPhy 运营、内容、电商、活动、网站和数据分析需求。它只负责需求澄清和 PRD 草稿，不会修改代码、写入飞书、联系研发或自动上线。

## 能做什么

- 对模糊需求进行逐步访谈，每次优先询问最影响范围和验收的问题。
- 检查已有需求缺少哪些关键信息。
- 在用户要求时跳过访谈，直接生成带缺口和假设的草稿。
- 输出飞书需求池条目和轻量 PRD。
- 区分已知事实、待补充信息和待确认假设。
- 默认使用中文，也可以按要求输出英文。

## 从 GitHub 安装

需要已安装支持 Plugins 的 ChatGPT 桌面版或 Codex CLI。

### 方式一：直接添加 GitHub Marketplace

```bash
codex plugin marketplace add SZMOFEI/nuphy-prd-clarifier
codex plugin add nuphy-prd-clarifier@nuphy-open-plugins
```

安装后请新建一个聊天，让新 Skill 生效。

### 方式二：下载 ZIP 后安装

1. 在 GitHub 仓库中选择 **Code → Download ZIP**，然后解压。
2. 在终端执行：

```bash
codex plugin marketplace add /absolute/path/to/nuphy-prd-clarifier
codex plugin add nuphy-prd-clarifier@nuphy-open-plugins
```

请把 `/absolute/path/to/nuphy-prd-clarifier` 换成解压后的仓库绝对路径。

### 检查与更新

```bash
codex plugin marketplace list
codex plugin marketplace upgrade nuphy-open-plugins
```

更新后重新安装插件并新建聊天：

```bash
codex plugin add nuphy-prd-clarifier@nuphy-open-plugins
```

## 使用示例

- `帮我把这条模糊需求澄清成可提交的需求卡。`
- `一步步补齐这段运营需求，并生成 PRD 草稿。`
- `检查这条需求还缺什么，输出飞书可粘贴版本。`
- `先不要继续提问，直接基于现有信息生成草稿。`

## 输出内容

1. 飞书需求池条目
2. 轻量 PRD 草稿
3. 待补充信息
4. 待确认假设

## 隐私与权限

- 不需要 NuPhy、飞书或其他第三方账号。
- 不包含 MCP 服务，不向 NuPhy 服务器发送对话数据。
- 不读取本地文件，除非用户主动在当前对话中提供。
- 不应输入密码、API Key、支付信息、客户个人信息或其他秘密。

## 仓库结构

```text
.agents/plugins/marketplace.json
plugins/nuphy-prd-clarifier/
├── plugin.json
├── .codex-plugin/plugin.json
├── assets/
├── skills/
├── submission/
└── tests/
```

## 开发与验证

插件主体位于 `plugins/nuphy-prd-clarifier`。提交更改前，应运行 OpenAI `skill-creator` 和 `plugin-creator` 提供的验证器，并确认 `tests/test-cases.json` 中的场景仍符合预期。

## License

MIT

---

## English summary

NuPhy PRD Clarifier turns vague operations requests into a Feishu-ready requirement entry and lightweight PRD through focused questions. Install it from this GitHub marketplace, start a new chat, and ask it to clarify a requirement. It has no external service, authentication, or automatic write capability.
