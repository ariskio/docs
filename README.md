# Arisk 文档

Arisk 链上风险资金识别 AML 风控平台的 Mintlify 文档，提供简体中文、繁体中文和英文内容，包含 V1 与 V2 API 参考。

## 内容结构

- `docs.json`：站点配置、语言与版本导航。
- `zh/`、`zh-Hant/`、`en/`：三种语言的首页和 V2 快速开始。
- `<语言>/api-reference/v1/`、`<语言>/api-reference/v2/`：OpenAPI 文件、接口页面与 Webhook 说明。
- `<语言>/updatelog/`：产品发布记录。
- `logo/`、`favicon.svg`：站点品牌素材。
- `test/`：独立的 API 调用示例和语言转换脚本；调用脚本需要对应服务和 API Key。

## 本地预览

使用 Mintlify CLI 支持的 Node.js LTS 版本，在仓库根目录运行：

```bash
mint dev
```

检查内部链接：

```bash
mint broken-links
```

CLI 安装与版本要求见 [Mintlify 官方文档](https://www.mintlify.com/docs/cli/installation)。

## 编辑约定

- 页面使用带 YAML frontmatter 的 MDX。标题和描述使用对应语言。
- 修改公共说明时同步三种语言；保持接口路径、字段名和枚举值不翻译。
- API 示例使用 `https://api.arisk.io`，并与对应版本的 OpenAPI 定义一致。
- 在 `docs.json` 中登记需要展示的页面，内部链接使用不带扩展名的根路径。
- 提交说明使用英文类型前缀与中文正文，例如 `docs: 完善三语言快速开始`。

## 部署

推送到已连接的 `main` 分支后，由 Mintlify 自动部署。
