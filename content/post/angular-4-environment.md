+++
date = "2017-05-07T14:06:34+08:00"
draft = false
title = "Angular 4 環境準備"

+++

##### 編輯器
- [Visual Studio Code]
- [Bash on Windows]
    - [Node.js]: 建議透過 [nvm] 安裝
    - [Angular CLI]: `npm install -g @angular/cli`
<!--more-->

##### 建立專案
```
ng new my-dream-app
cd my-dream-app
ng -v // 檢查 Angular 版本資訊
```

##### 執行專案
```
ng serve
```
打開 `http://localhost:4200/` 檢查執行結果

#### 資源
- [Learn Angular 4 from Scratch]
- [TUTORIAL: TOUR OF HEROES]
- [Angular 2 給初學者的學習指南]

[Node.js]: https://nodejs.org/en/
[nvm]: https://github.com/creationix/nvm
[Visual Studio Code]: https://code.visualstudio.com/
[Learn Angular 4 from Scratch]: https://coursetro.com/courses/12/Learn-Angular-4-from-Scratch
[Bash on Windows]: https://msdn.microsoft.com/zh-tw/commandline/wsl/about
[Angular CLI]: https://cli.angular.io/

[Event reference]: https://developer.mozilla.org/en-US/docs/Web/Events
[Angular 2 給初學者的學習指南]: http://ithelp.ithome.com.tw/articles/10189032
[TUTORIAL: TOUR OF HEROES]: https://angular.io/docs/ts/latest/tutorial/