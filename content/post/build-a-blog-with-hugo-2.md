+++
date = "2017-05-06T15:05:24+08:00"
draft = false
title = "用 Hugo 建立你的部落格 - 2"

+++

### 使用 [GitHub Pages]

<!--more-->

[GitHub Pages] 提供了直接使用 `/docs` 作為網頁來源的服務。  
這邊偷懶一點，直接將 Hugo 的輸出資料夾指向 `docs`，就不用再切換 branch 或者開兩個 Repository。

```bash
hugo -d docs
git add -A
git commit -m "My first blog post!"
git push -u origin master
```

#### GitHub 設定

1. 打開 GitHub blog repository 的設定頁面
2. 找到 `GitHub Pages` 的設定欄
3. Source 選擇 `master branch/docs folder` 後按下 `Save`

連上網頁檢查 `https://[YOUR_USERNAME].github.io/blog/`

#### Custom domain & SSL

自訂域名有點小複雜，每個人的需求都不盡相同。這邊就提供幾個我設定時有參考到的資料給大家。  
另外，記得將 `config.toml` 裡的 `baseURL` 修改成你的自訂域名。

- [域名掃盲]
- [Using a custom domain with GitHub Pages]
- [Using HTTPs with Custom Domain Name on GitHub Pages]

[GitHub Pages]: https://pages.github.com/
[Using a custom domain with GitHub Pages]: https://help.github.com/articles/using-a-custom-domain-with-github-pages/
[域名掃盲]: (http://www.pchou.info/ssgithubPage/2013-01-05-build-github-blog-page-03.html)
[Using HTTPs with Custom Domain Name on GitHub Pages]: https://www.jonathan-petitcolas.com/2017/01/13/using-https-with-custom-domain-name-on-github-pages.html