# EdgePLC 文档仓库

EdgePLC 系列控制器产品的中英双语 MkDocs 文档网站仓库。

本仓库沿用 EdgeIO 仓库的目录结构与构建方式：基于 MkDocs Material 主题，集成静态国际化和 GitHub Pages 自动部署。

## What to edit

- `mkdocs.yml`
- `docs/index.md` for Chinese content
- `docs/en/index.md` for English content
- `docs/` for Chinese pages
- `docs/en/` for English pages with matching paths
- `docs/assets/图片材料/` for shared site images
- `docs/EdgePLC说明书/` 存放各型号说明书 Markdown 源文件及其图片目录

## Local development

```bash
pip install -r requirements.txt
mkdocs serve
```

## Internationalization

- Chinese is the default language.
- English pages live under `docs/en/`.
- English pages should mirror the relative path of their Chinese counterpart.
- Untranslated pages fall back to the Chinese source page.

## Deploy

推送到 `main` 分支后，GitHub Actions 会自动构建并发布到 GitHub Pages。