+++
date = "2017-05-10T09:32:59+08:00"
draft = false
title = "Angular: 從做中學 - 2"

+++

### Component, Component and Component!

<!--more-->

##### 瞧瞧 `ng-todo` 的目錄結構
```
tree -I 'node_modules'
......
|-- src
|   |-- app
|   |   |-- app.component.css
|   |   |-- app.component.html
|   |   |-- app.component.spec.ts
|   |   |-- app.component.ts
|   |   `-- app.module.ts
......
```

`src/app` 底下的幾個檔案是我們現在要關心的。

###### app.component.ts:
```
......
@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
......
```

- `selector`: 告訴 Angular，只要在 html 裡面看到 `<app-root>`，就用 templateUrl 裡面的內容替換掉
- `templateUrl`: HTML template 的位置
- `styleUrls`: CSS 檔案的位置

###### app.module.ts
```
......
@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    FormsModule,
    HttpModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

在 `app.module.ts` 中

- `declarations`: 告訴 Angular，我會用到哪些 Components
- `bootstrap`: 告訴 Angular，哪一個 Component 是根組件。Angular 會從 `index.html` 找到 `AppComponent` 對應的`<app-root>` 的標籤並初始化

###### Angular application 大概的執行流程
1. Angular 找到 `bootstrap` 定義的根組件(這裡是 `AppComponent`)
2. 把 index.html 裡對應的 `<app-root>` 替換成 `AppComponent` 的內容，如果 `AppComponent` 裡面有其他組件，就重複這個取代的流程。

> 更詳細且精確的定義可以參考 [Angular Docs]


#### 所以說 Angular application 是由各種 Component(組件)組合而成
##### 舉例來說
- APP
    - Component1
        - Component2
        - Component3
            - Component4
    - Component5

#### 而 Component 是由 HTML template，CSS template，和其他 Component 所組成
- Component
    - HTML Template
    - CSS Template
    - Child Component

[Angular Docs]: https://angular.io/docs/ts/latest/

