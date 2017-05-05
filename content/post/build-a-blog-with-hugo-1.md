+++
date = "2017-05-05T13:54:40+08:00"
draft = false
title = "用 Hugo 建立你的部落格 - 1"

+++

### 詳細可參考: [Hugo Quickstart Guide]

<!--more-->

#### 開始建立 Blog

1. 在 GitHub 上建立 `blog` Repository
2. 初始化 Hugo Blog

    ```bash
    hugo new site blog
    cd blog
    git init
    git remote add origin git@github.com:[YOUR_USERNAME]/blog.git
    ```

#### 選擇主題
- [Hugo Theme Showcase]
- [Hugo Theme Repository]

挑一個你喜歡的主題，這邊選了 hugo-theme-bootstrap4-blog 當例子

```bash
git submodule add https://github.com/alanorth/hugo-theme-bootstrap4-blog themes/hugo-theme-bootstrap4-blog
```

#### 建立文章

```bash
hugo new post/hello-hugo.md
```

#### config.toml
- 可參考 [hugo-theme-bootstrap4-blog config.toml]
- [languageCode]

#### 本地執行
```bash
hugo server --buildDrafts --theme=hugo-theme-bootstrap4-blog
```






[Hugo Quickstart Guide]: https://gohugo.io/overview/quickstart/
[Hugo Theme Showcase]: http://themes.gohugo.io/
[Hugo Theme Repository]: https://github.com/spf13/hugoThemes
[hugo-theme-bootstrap4-blog config.toml]: https://github.com/alanorth/hugo-theme-bootstrap4-blog/blob/master/exampleSite/config.toml
[languageCode]: https://github.com/spf13/hugo/issues/349