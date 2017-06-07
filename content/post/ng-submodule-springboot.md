+++
date = "2017-06-07T08:27:46+08:00"
draft = false
title = "Git Submodule"

+++

### Angular &#10163; Spring Boot 

<!--more-->

#### Spring Boot #1
1. 到 [SPRING INITIALIZR] 建立新的 Spring Boot Project
2. 初始化 GitHub Project: submodule-demo

```
cd submodule-demo
git init
git remote add origin git@github.com:0t2/submodule-demo.git
git add -A
git commit -m "initial commit"
git push -u origin master
```

#### Angular #1
1. 在 submodule-demo 資料夾建立 ng-submodule Project
2. 初始化 GitHub Project: ng-submodule

```
ng new ng-submodule
cd ng-submodule
git init
git remote add origin git@github.com:0t2/ng-submodule.git
git add -A
git commit -m "submodule initial commit"
git push -u origin master
```

#### Spring Boot #2
1. 回到 submodule-demo 資料夾
2. 利用 `git submodule` 建立 submodule
3. Push commit

```
cd ..
git submodule add git@github.com:0t2/ng-submodule.git
git add -A
git commit -m "add submodule"
git push -u origin master
```

#### Angular #2
1. 修改 ng-submodule
2. Push commit

```
cd ng-submodule
touch test
git add -A
git commit -m "add file to submodule"
git push -u origin master
cd ..
git commit -am "update submodule status"
git push -u origin master
```

#### Clone Project With Submodule
1. `--recursive`: 在專案 Clone 完成後，將 submodule 一併 Clone 下來
2. `-j2`: 同時 Clone 的 Submodule 數量

```
git clone --recursive -j2 git@github.com:0t2/submodule-demo.git
```


[SPRING INITIALIZR]: https://start.spring.io/