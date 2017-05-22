+++
date = "2017-05-22T10:41:30+08:00"
draft = false
title = "Angular: 從做中學 - 5"

+++

### 使用者輸入

<!--more-->

#### 透過 `input` 新增 Todo

目標:

1. 在 input 新增 todo
2. 按下 Enter 後，將 todo 加入 todos 陣列
3. 清空 input

首先在 `AppComponent` 中加上一個 `addTodo` 的方法。

```
addTodo(value: string) {
  if (value && value.trim())
    this.todos.push(value);
}
```

`addTodo` 做的事情很單純

1. 收到一個 `value`
2. 檢查 `value` 是否為空
3. 將 `value` 放進 todos 陣列


在 `app.component.html` 新增一個 `input`
```
<input #todoInput (keyup.enter)="addTodo(todoInput.value); todoInput.value = ''">
```

`#todoInput` 可以理解成給 input 一個參考的名稱，更方便的操作 input 的屬性。

跟[上一篇]提到的一樣，這邊對 input 的 `keyup.enter` 事件，與 addTodo 做綁定，
並且將 `todoInput` 的值傳給 addTodo。  
而後面的 `todoInput.value = ''` 則是在新增 todo 的同時，將 `todoInput` 給清空。

打開網頁看看目前的結果吧

- [Github]
- [Commit for this post]


簡單的教學就寫到這邊，想了解更多的可以參考 [ANGULAR DOCS] 喔!

[上一篇]: ../../../../2017/05/angular-從做中學---4/
[Github]: https://github.com/0t2/ng-todo
[Commit for this post]: https://github.com/0t2/ng-todo/commit/d40d1c522bf467cf544718ed0324d10193849bac
[ANGULAR DOCS]: https://angular.io/docs/ts/latest/
