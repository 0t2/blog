+++
date = "2017-05-23T13:48:36+08:00"
draft = false
title = "在 Angular 中使用 amCharts"

+++

### 畫畫圖

<!--more-->

建立 `test-amcharts` 專案，並安裝 [amcharts3-angular2]
```
ng new test-amcharts
yarn add @amcharts/amcharts3-angular 
```

#### 1. `index.html`
在 head 加上
```
<link rel="stylesheet" href="https://www.amcharts.com/lib/3/plugins/export/export.css" type="text/css" media="all" />
```

`body` 加上
```
<script src="https://www.amcharts.com/lib/3/amcharts.js"></script>
<script src="https://www.amcharts.com/lib/3/serial.js"></script>
<script src="https://www.amcharts.com/lib/3/themes/light.js"></script>
<script src="https://www.amcharts.com/lib/3/plugins/export/export.min.js"></script>
```

#### 2. `app.module.ts`

開頭加上

```
import { AmChartsModule } from "@amcharts/amcharts3-angular";
```
imports 陣列加上 `AmChartsModule`

#### 3. `app.component.html`

```
<div id="chartdiv" [style.width.%]="100" [style.height.px]="500"></div>
```

#### 4. `app.component.ts`

開頭加上
```
import { AmChartsService } from "@amcharts/amcharts3-angular";
```

在 AppComponent 中
```
  private chart: any;

  constructor(private AmCharts: AmChartsService) { }

  ngOnInit() {
    this.chart = this.AmCharts.makeChart("chartdiv", {
        ...... // 圖表設定值
    });
  }

  ngOnDestroy() {
    this.AmCharts.destroyChart(this.chart);
  }
```

打開 amCharts 的範例: [Date Based Data]，將圖表設定值複製過來

打開網頁檢查結果  
`ng serve`

- [Source Code - Github]

[amcharts3-angular2]: https://github.com/amcharts/amcharts3-angular2
[Date Based Data]: https://www.amcharts.com/demos/date-based-data/
[Source Code - Github]: https://github.com/0t2/test-amcharts