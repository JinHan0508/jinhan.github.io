# HAN Jin (韩瑾) — Academic website

Quarto 学术主页，使用 GitHub Pages 发布。页面使用英文，维护说明使用中文。

## 页面内容

- `index.qmd`：个人介绍、所属大学、公开邮箱。
- `research.qmd`：已确认的三个研究方向。
- `teaching.qmd`：教学资料页面，待提供资料后补充。
- `cv.qmd`：已确认的在读身份和研究方向。
- `styles.css`：白底、深蓝链接、衬线字体和移动端布局。
- `theme.scss`：使用系统字体，关闭主题默认的外部字体加载。
- `_quarto.yml`：导航、网站标题和输出设置。

当前公开内容仅使用已确认信息：姓名 HAN Jin (韩瑾)、香港中文大学经济学博士研究生、邮箱 jinhan@link.cuhk.edu.hk，以及 Law and Economics、Judicial Transparency、Economic Development 三个研究方向。没有添加未经确认的论文、教学经历、入学年份、个人照片或其他学历。

## 本地预览

从 [Quarto 官方网站](https://quarto.org/docs/get-started/) 安装 Quarto 后，在此目录运行：

```text
quarto preview
```

生成静态网站：

```text
quarto render
```

生成文件位于 `_site/`，不需要安装 R 或 Python。

## GitHub Pages

当前仓库：[JinHan0508/jinhan.github.io](https://github.com/JinHan0508/jinhan.github.io)。

此仓库按项目网站发布，配置的网址是 <https://jinhan0508.github.io/jinhan.github.io/>。GitHub Pages 的一级域名由账户名决定；把仓库命名为 `jinhan.github.io` 并不会把账户名 `JinHan0508` 改为 `jinhan`。

1. 首先确认 GitHub 账号和仓库管理权限；如已有主页仓库，先检查其内容。
2. 当前采用用户指定的公开仓库 `jinhan.github.io`。如果未来迁移到新账户，用户主页仓库需要命名为 `<github-username>.github.io`，并同步更新 `_quarto.yml` 中的 `site-url`。不要覆盖已有网站。
3. 将本目录源文件提交到 `main`，包括 `.github/workflows/pages.yml`。不提交 `_site/` 或 `.quarto/`。
4. 仓库 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**。
5. 在 **Actions** 中检查 `Publish academic website`，必要时点击 **Run workflow**。
6. 以 Pages 设置或部署任务返回的实际公开 URL 为准，并检查 Home、Research、Teaching、CV 四个页面。

工作流使用 Quarto 1.10.19 构建，再通过 GitHub Pages 官方部署操作发布。此项目不包含 GitHub 密钥或访问令牌。

## 后续维护

修改 `.qmd` 并推送到 `main` 后会自动重新发布。上传正式简历 PDF 后，可把文件放入 `files/cv.pdf`，再在 `cv.qmd` 中加入 `[Download CV (PDF)](files/cv.pdf)`。论文和教学经历应在内容确认后再添加。

官方参考：[Quarto GitHub Pages](https://quarto.org/docs/publishing/github-pages.html) · [GitHub Pages 自定义工作流](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)
