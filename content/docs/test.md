---
title: "如何设计&&管理一个高大上Github"
date: 2023-05-29T08:41:12+08:00
draft: false
---


# 如何设计&&管理一个高大上Github

- `xxxxx.github.io`
  - 首页:用来做为`博客`和`工具`导航
- `github.com/xxxxx`
  - 内页:用来做分类`部署教程` `研究报告`等
    - LangChain
    - Web3
    - Seo


## 搜索关键词 github hugo 

> 视频链接:
- `https://www.youtube.com/watch?v=_QSr2_pxIJs`
- [Deploy Hugo Blog to Github Pages via Github Actions Custom Domain](https://www.youtube.com/watch?v=_QSr2_pxIJs)
- 通过Github操作将Hugo博客部署到Github Pages绑定域名


---
> 播放节点:

  - [0:00](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=0s) Intro
    - 介绍
  - [0:33](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=33s) Install Hugo, create a new site & a page
    - 安装Hugo创建新站
  - [1:48](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=108s) Install the PaperMod theme & add the theme in config.yml
    - 安装PaperMod模版并配置
  - [3:03](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=183s) Add minimal content in docs/test.md and run locally
    - 增加内容并本地部署
  - [3:52](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=232s) Create a git repository
    - 创建git仓库
  - [4:52](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=292s) Create a gh-pages branch in the repo important
    - 创建页面分支
  - [5:20](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=320s) Set read & write permissions for workflow important
    - 阅读并撰写git工作流脚本
  - [5:33](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=333s) Create the github actions deploy file
    - 创建github actions部署
  - [6:21](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=381s) Edit the baseurl in config.yml to https://<username>.github.io/<repo_name>/
    - 修改网站配置信息
  - [7:16](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=436s) Explain the steps in Github Actions workflow
    - 解释Github Actions工作流程
  - [10:53](https://www.youtube.com/watch?v=_QSr2_pxIJs&t=653s) Link custom domain to Github Pages
    - 绑定域名

---
> 博客链接:

- `https://theplaybook.dev/docs/deploy-hugo-to-github-pages/`
- [Hugo to Github Pages](https://theplaybook.dev/docs/deploy-hugo-to-github-pages/)

---

> 实操 && 截图

```bash
brew install hugo
hugo new site ./ -f yml
vim config.yml

baseURL: https://davidpythonseo.github.io/
languageCode: en-us
title: Github Pages Hugo site

hugo new docs/test.md

git init
git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod


