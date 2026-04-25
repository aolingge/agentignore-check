<p align="center">
  <img src="assets/readme-banner.svg" alt="Agentignore Check banner" width="100%">
</p>

<h1 align="center">Agentignore Check</h1>

<p align="center">检查仓库是否有 .agentignore 风格规则，避免 AI Agent 读取密钥和噪声文件。</p>

<p align="center"><a href="README.md">English</a> · <a href="#快速开始">快速开始</a> · <a href="#检查项">检查项</a></p>

<p align="center">
  <img alt="Node.js" src="https://img.shields.io/badge/node-%3E%3D18-0EA5E9">
  <img alt="dependencies" src="https://img.shields.io/badge/dependencies-0-111827">
  <img alt="license" src="https://img.shields.io/badge/license-MIT-2563EB">
</p>

## 为什么做这个

AI Agent 工具链正在快速增长，但很多仓库缺少能直接放进 CI 或本地预检的小工具。这个项目保持零依赖、命令短、输出清楚，适合被收藏、fork、二次改造。

## 快速开始

```bash
npx github:aolingge/agentignore-check --path .agentignore
```

Generate Markdown:

```bash
npx github:aolingge/agentignore-check --path .agentignore --markdown > report.md
```

Use a score gate:

```bash
npx github:aolingge/agentignore-check --path .agentignore --min-score 80
```

## 检查项

| Check | What it looks for |
| --- | --- |
| env | Ignores env and secret files. |
| logs | Ignores logs. |
| build | Ignores generated dependencies and builds. |
| private | Ignores private data. |

## Output

```text
Agentignore Check score: 100/100
PASS  example-check  Useful signal found
FAIL  missing-check  Add the missing guidance
```

## 参与贡献

Good first PRs: add checks, add fixtures, improve docs, or add GitHub Actions examples.

## License

MIT
