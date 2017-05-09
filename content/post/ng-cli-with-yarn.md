+++
date = "2017-05-09T13:39:15+08:00"
draft = false
title = "在 Angular CLI 中使用 Yarn"

+++

#### 遠離 npm，多寫幾行 code

<!--more-->

每當用 Angular CLI 建立新專案的時候，會需要透過 `npm` 下載一堆相依套件。  
這個過程其實是可以加速的，因為 `npm` 並沒有緩存的機制，所以每次都是全部重新下載。  
將 `npm` 換成 `Yarn` 的話，第一次的下載時間還是在，但第二次就能明顯感受到 `Yarn` 的效果。

#### 安裝 Yarn

- [下載 Yarn]

因為我是用 [Bash on Windows]，所以是安裝在 `Ubuntu` 上。
```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn
```
檢查安裝是否成功: `yarn --version`

#### 修改 Angular CLI 設定

```
ng set --global packageManager=yarn
```
> 如果想要改回使用 npm `ng set --global packageManager=npm`

#### 測試
##### Round 1
```
time ng new test-yarn1
......
......
Successfully initialized git.
Installing packages for tooling via yarn.
Installed packages for tooling via yarn.
Project 'test-yarn1' successfully created.

real    4m49.727s
user    0m44.438s
sys     1m1.828s
```
建立新專案在我的電腦要跑到快五分鐘...~~(換換病發作)~~

1. 先確認 Angular CLI 已經使用 Yarn 來安裝套件。  
2. 第一次使用 Yarn 還是要下載套件，但是 Yarn 會建立緩存，讓下次的安裝更快。

##### Round 2
```
time ng new test-yarn2
......
......
Project 'test-yarn2' successfully created.

real    2m38.259s
user    0m27.578s
sys     0m39.875s
```

第二次只要約兩分半，從這裡就可以看到 `Yarn` 的效果囉。


#### 參考資料:
- [Tracking: Third party NPM replacements #3886]

[下載 Yarn]: https://yarnpkg.com/zh-Hans/
[Bash on Windows]: https://msdn.microsoft.com/zh-tw/commandline/wsl/about
[Tracking: Third party NPM replacements #3886]: https://github.com/angular/angular-cli/issues/3886