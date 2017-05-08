+++
date = "2017-05-08T10:37:44+08:00"
draft = false
title = "Angular: 從做中學 - 1"

+++

#### 寫點東西當筆記
網路上有很多 Angular 的教學文章和影片，照著做都懂，但自己要動手卻又好像少了點什麼。

<!--more-->

#### 開始前的準備
[Angular 4 環境準備]

#### 初探 Angular
首先透過 [Angular CLI] 建立專案
```
ng new ng-todo
```
[Angular CLI] 會自動建立 `ng-todo` 資料夾，並且將環境初始化(需要花一點時間)  

接著進入 `ng-todo`
```
cd ng-todo
```
啟動 [Angular CLI] 的開發伺服器
```
ng serve
```
檢查 `http://localhost:4200/` 是否有成功顯示
```
app works!
```

[Angular 4 環境準備]: ../../../../2017/05/angular-4-環境準備/
[Angular 2 Tutorial: Create a CRUD App with Angular CLI]: https://www.sitepoint.com/angular-2-tutorial/
[Angular CLI]: https://cli.angular.io/