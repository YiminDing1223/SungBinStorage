# SungBinStorage

基于 Quarto 的文章网站：首页、作品目录、作品简介与分章阅读。

## 在电脑上预览

安装 Quarto 后，在本文件夹运行：

```bash
quarto preview
```

生成网站文件：

```bash
quarto render
```

生成的网站位于 `_site/`。

## 添加作品

1. 复制 `works/sample/`，改成新作品的英文文件夹名。
2. 修改作品的 `index.qmd`，按 `01.qmd`、`02.qmd` 增加章节。
3. 在 `works/index.qmd` 添加作品入口。
4. 在 `_quarto.yml` 的 `sidebar` 添加对应章节链接。
5. 运行 `quarto preview` 检查页面，再运行 `quarto render`。

## 上传与发布

在 GitHub 新建名为 `SungBinStorage` 的仓库，把整个项目上传并推送到 `main`。如果使用 Vercel：导入该 GitHub 仓库，Framework Preset 选 Other，Build Command 留空，Output Directory 填 `_site`。本地运行 `quarto render` 后再提交 `_site`。如果选择 Cloudflare Pages，输出目录同样填写 `_site`。
