+++
date = "2017-05-21T11:41:28+08:00"
draft = false
title = "Angular: 從做中學 - 4"

+++

### 事件綁定

<!--more-->

#### 透過 button 刪除 Todo
首先在 `AppComponent` 中加上一個 `deleteTodo` 的方法。  

```
deleteTodo(index: number) {
    this.todos.splice(index, 1);
}
```

`deleteTodo`做的事情很單純

1. 收到一個 index
2. 將 todos 陣列對應的 todo 刪除

那該如何將這個方法綁定到 button 呢?  
修改 `app.component.html`

```
<ul>
  <li *ngFor="let todo of todos; let i = index">
    <button (click)="deleteTodo(i)">x</button> {{ todo }}
  </li>
</ul>
```

首先透過 `*ngFor` 提供的 index 取得目前位置  
button 裡的 `(click)="deleteTodo(i)` 代表將 `點擊事件` 與 `deleteTodo` 做綁定

另外在 `app.component.css` 加上以下 css 來移除 li 前面的點
```
li {
    list-style-type: none;
}
```

打開網頁看看目前的結果吧

- [Github]
- [Commit for this post]

[NgFor]: https://angular.io/docs/ts/latest/api/common/index/NgFor-directive.html
[Github]: https://github.com/0t2/ng-todo
[Commit for this post]: https://github.com/0t2/ng-todo/commit/396ce9aa06fd4f6a926cf93a52ca0dd7ba4fb034
