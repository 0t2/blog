+++
date = "2017-05-20T14:36:18+08:00"
draft = false
title = "更新 Angular CLI"

+++

### 分成`全域`和`專案`套件

<!--more-->

1. 全域套件(Global package):

    ```
    npm uninstall -g @angular/cli
    npm cache clean
    npm install -g @angular/cli@latest
    ```
2. 專案套件(Local project package):

    ```
    rm -rf node_modules dist
    yarn add @angular/cli@latest --dev
    ```