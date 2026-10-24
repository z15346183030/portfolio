# 赵旭 — 个人简历网站

单文件、零依赖的个人简历站。左侧固定信息栏 + 右侧 Bento 项目网格，浅色为默认，支持深色切换与打印导出。

线上地址：https://z15346183030.github.io/resume-site/

## 设计参考

| 模板 / 风格 | 借鉴点 |
|---|---|
| Brittany Chiang v4 | 左侧固定栏 + 右侧滚动内容、等宽字体小标签 |
| Magic Portfolio (Once UI) | 极简、排版驱动、大量留白 |
| 2026 Bento Grid | 大小错落的模块化卡片承载项目 |
| Neo-Minimalism | 超大标题、克制用色、战略级负空间 |

## 特点

- **单文件**：一个 `index.html`，无构建、无依赖、无框架
- **双主题**：浅色默认 + 深色模式，跟随系统并记忆选择（快捷键 `T`）
- **Bento 网格**：项目卡片按重要性排布，点开是完整的产品思考（判断 / 取舍 / 结果）
- **发邮件菜单**：QQ / 163 / 126 / Gmail / Outlook / 系统默认 / 复制地址
- **可打印**：`Ctrl/Cmd + P` 自动切换为单栏简历版式，可直接存 PDF
- **可访问**：键盘可操作、focus 可见、`prefers-reduced-motion` 降级
- **SEO**：Open Graph + JSON-LD `Person` 结构化数据

## 部署

### GitHub Pages
1. 推送到 GitHub 仓库 `main` 分支
2. Settings → Pages → Source 选 `main` / root
3. 访问 `https://z15346183030.github.io/resume-site/`

### 本地预览
直接双击打开 `index.html` 即可，无需服务器。

## 修改内容

所有文案都在 `index.html` 里：

- 左侧信息栏：搜索 `LEFT RAIL`
- 关于 / 数据：搜索 `id="about"`
- 经历时间线：搜索 `id="exp"`，每段是一个 `<div class="tl-item">`
- 项目卡片：搜索 `id="work"`，每张卡片是一个 `<article class="card">`
- 项目详情：脚本里的 `var P = { ... }`，key 与卡片的 `data-project` 对应
- 配色：`<style>` 顶部的 `:root` 与 `html[data-theme="dark"]` 变量
