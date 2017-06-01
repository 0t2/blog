+++
date = "2017-06-01T14:48:01+08:00"
draft = false
title = "透過 Angular CLI 建立 Routing 專案"

+++

`ng new $PROJECT_NAME --routing`

<!--more-->


Angular CLI 會自動建立 `app-routing.module.ts`

```
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';

const routes: Routes = [
  {
    path: '',
    children: []
  }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

並且將 `AppRoutingModule` 加入 `app.module.ts`