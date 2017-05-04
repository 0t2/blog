+++
date = "2017-05-04T11:08:14+08:00"
draft = false
title = "使用 Hugo 前的準備工作"

+++

### 環境 

> [Bash on ubuntu on Windows]

<!--more-->

- [Connecting to GitHub with SSH]
- Hugo

    ```
    mkdir hugo
    wget https://github.com/spf13/hugo/releases/download/v0.20.6/hugo_0.20.6_Linux-64bit.tar.gz -P hugo
    tar zxf hugo/hugo_0.20.6_Linux-64bit.tar.gz -C hugo
    sudo cp hugo/hugo /usr/local/bin/
    rm -rf hugo
    ```

### [Visual Studio Code]

- [修改語言]
- [修改 VSCode 預設終端機為 Bash]
- [修改 Bash 語言] - 因為中文會造成終端機跑版

### 參考連結

- [Hugo]
- [Markdown Cheatsheet]
- [顏文字]


[Bash on ubuntu on Windows]: https://msdn.microsoft.com/zh-tw/commandline/wsl/about
[Visual Studio Code]: https://code.visualstudio.com/
[Connecting to GitHub with SSH]: https://help.github.com/articles/connecting-to-github-with-ssh/
[修改語言]: https://code.visualstudio.com/docs/getstarted/locales
[修改 VSCode 預設終端機為 Bash]: https://code.visualstudio.com/docs/editor/integrated-terminal
[修改 Bash 語言]: https://superuser.com/questions/1108090/how-do-i-change-the-language-of-the-linux-subsystem-in-windows-10-wsl#answer-1124983
[主題]: https://themes.gohugo.io/hugo-theme-bootstrap4-blog/
[Markdown Cheatsheet]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#emphasis
[顏文字]: http://facemood.grtimed.com/
[Hugo]: https://gohugo.io/