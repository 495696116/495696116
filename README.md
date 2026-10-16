# Qiaoran · 乔冉

**AI agent systems · Runtime infrastructure · LLM interoperability**

I build reliable AI agent systems, with a focus on execution boundaries, recovery, and model/tool protocols. My work combines ongoing engineering on **Agnes Harness** with focused contributions to upstream open-source projects.

## Building: Agnes Harness

[**Agnes Harness**](https://github.com/AgnesAI-Labs/agnes-harness) is a pluggable agent harness for Forward Deployed Engineering. My contributions focus on the runtime and the services that make agent execution dependable.

Selected engineering work, merged into the **runtime-pluginization integration branch**:

- **MCP session isolation and recovery** — manage session ownership across runtime generations and avoid replaying calls with unknown outcomes after a crash. [PR #144](https://github.com/AgnesAI-Labs/agnes-harness/pull/144)
- **Credential-handle verification** — check that a handle is genuine and valid without reading or consuming the secret; re-verify when the credential is used. [PR #412](https://github.com/AgnesAI-Labs/agnes-harness/pull/412)
- **Runtime composition** — install the agent loop, tools, and context on the new run path. [PR #312](https://github.com/AgnesAI-Labs/agnes-harness/pull/312)

These links document integration work, not a claim that every feature is released.

## Selected upstream contributions

### Goose — a usable provider selector

Fixed the CLI provider picker so long provider lists stay within a ten-row view, with a search fallback. Incorporated maintainer feedback by replacing sentinel strings with a type-safe Rust enum, with regression tests and formatting, build, and Clippy checks.

**Merged by the maintainer:** [aaif-goose/goose #10420](https://github.com/aaif-goose/goose/pull/10420).

### new-api — valid tool calls in Responses history

Fixed conversion of unnamed function calls into Responses output. The streaming path holds arguments until a valid name arrives and omits calls that never receive one, preserving output-index continuity and usage data.

**Integrated upstream:** my [PR #7219](https://github.com/QuantumNous/new-api/pull/7219) was superseded by the maintainer's merged [PR #7636](https://github.com/QuantumNous/new-api/pull/7636). The merged change retains my contribution and [co-author attribution](https://github.com/QuantumNous/new-api/commit/1a4166d8e8ba9802d2ca56fe8ecf0ed5404e80d5), and [issue #7094](https://github.com/QuantumNous/new-api/issues/7094) is closed as completed.

## Engineering interests

Agent runtimes and recovery · MCP and tool protocols · Credential boundaries · Regression testing · Developer tooling

<details>
<summary>中文介绍</summary>

我叫乔冉，关注 AI Agent 系统、运行时基础设施，以及模型与工具协议的兼容性。

在 Agnes Harness 中持续参与运行时、MCP 会话恢复和凭证隔离相关工程；同时向外部开源项目贡献可复现、有回归验证的修复。Goose 的 CLI 修复已由维护者合并，new-api 的工具调用转换修复已被上游整合并保留共同作者署名。上面的链接对应具体实现、协作过程和采纳结果。

</details>
