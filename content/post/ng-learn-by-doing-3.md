+++
date = "2017-05-12T10:21:58+08:00"
draft = false
title = "Angular: 從做中學 - 3"

+++

### 數據顯示

<!--more-->

> 在 `ng-todo` 資料夾中先啟動 Angular CLI 的開發伺服器:  
> `ng serve`

#### Interpolation (插值表達式)

首先看到 `app.component.ts` 裡面有
```
title = 'app works!';
```
Angular 會找到 AppComponent 對應的 template: `app.component.html`  
接著把值替換上去，就變成你在網頁上看到的內容。
```
<h1>
  {{title}}
</h1>
```
現在，試著修改 `app.component.ts`
```
title = 'Angular Todo'
```
存檔後，你會發現 Angular 自動幫你編譯並重新整理網頁，延長你的 <kbd>F5</kbd> 壽命。

#### 顯示陣列資料 - *ngFor

假設我們將 Todo 的資料都放在陣列裡，修改 `app.component.ts`
```
title = 'Angular Todo';
todos = ['整理房間', '聚餐', '繳卡費', '運動'];
```
接著修改 `app.component.html`
```
<h1>
  {{title}}
</h1>
<ul>
  <li *ngFor="let todo of todos">
    {{ todo }}
  </li>
</ul>
```

1. `*ngFor` 會從 todos 陣列把每一個 item 拿出來，塞到 todo 這個變數中。  
2. 每拿出一個 item，都會產生一個內容為 todo 值的 li。

打開網頁看看目前的結果吧

- [Github]
- [Commit for this post]

[VSCode Angular TypeScript & Html Snippets]: https://marketplace.visualstudio.com/items?itemName=Mikael.Angular-BeastCode
[Github]: https://github.com/0t2/ng-todo
[Commit for this post]: https://github.com/0t2/ng-todo/commit/118e81bcd3fcf176fcb570551193aac0167da636