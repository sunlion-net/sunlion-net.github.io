# sunlion-net 组织站点（GitHub Pages）

这个仓库用于发布组织站点：`https://sunlion-net.github.io/`

## 目录结构

- `index.html`：站点首页
- `404.html`：找不到页面
- `assets/styles.css`：样式

## 发布方式（GitHub Pages）

1. 在 GitHub 仓库设置中进入 **Settings → Pages**
2. **Build and deployment**：选择 **Deploy from a branch**
3. **Branch**：选择 `main` / `root`（根目录）
4. 保存后等待部署完成

完成后访问：`https://sunlion-net.github.io/`

## 自定义域名（可选）

你有域名 `sunlion.net` 的话，并且希望以 `www.sunlion.net` 为主域名（推荐），可以按下面方式配置。

### 1) GitHub Pages 设置

1. 打开 **Settings → Pages**
2. 在 **Custom domain** 填写：`www.sunlion.net`
3. 保存后等待校验通过（可能需要几分钟到几十分钟）
4. 建议开启 **Enforce HTTPS**（校验通过后可用）

本仓库已包含根目录的 `CNAME` 文件（内容为 `www.sunlion.net`）。

### 2) DNS 记录（在你的域名解析商处配置）

主域名使用 `www.sunlion.net`：

- `www.sunlion.net` → CNAME → `sunlion-net.github.io`

裸域（apex）`sunlion.net` 建议做 301/URL 转发到 `https://www.sunlion.net/`（在你的域名解析商/托管商后台通常叫“URL 转发/显性跳转/301 跳转”）。

> 说明：
> - GitHub Pages 一般只需要一个“主”自定义域名；你选择 `www.sunlion.net` 做主域名时，最省事的做法是让 `sunlion.net` 301 跳转到 `www`。
> - 如果你强制要求裸域也直接解析并展示同一个站点，可以改为把 **Custom domain** 设为 `sunlion.net`，并使用 A/AAAA 记录；但这会改变“主域名”口径。
