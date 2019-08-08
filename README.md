# 简易 Bootstrap

## 项目介绍

实现 Bootstrap 的核心：栅格系统。

## 思路

- 用法：通过 class 去控制栅格占比
- 通过媒体查询实现不同屏幕下的占比也不同
- 使用媒体查询时，多个 class 会覆盖，从而实现自适应

## 代码如下
HTML
```
<div class="container">
  <div class="row">
    <div class="col-xs-4 col-sm-6 col-md-4 col-lg-2">1</div>
    <div class="col-xs-6 col-sm-6 col-md-4 col-lg-2">2</div>
    <div class="col-xs-2 col-sm-12 col-md-4 col-lg-2">3</div>
  </div>
</div>
<div class="container header">
  <p>header</p>
</div>
```
CSS
```
* {
  box-sizing: border-box;
}

.header {
  background: #ccc;
}

.container {
  padding-right: 15px;
  padding-left: 15px;
  margin-right: auto;
  margin-left: auto;
}

@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}

@media (min-width: 992px) {
  .container {
    width: 970px;
  }
}

@media (min-width: 1200px) {
  .container {
    width: 1170px;
  }
}

.row {
  margin-left: -15px;
  margin-right: -15px;
}

.row::after {
  content: '';
  display: block;
  clear: both;
}

.row > div {
  border: 1px solid red;
  margin-top: 10px;
}

.col-xs-1,
.col-xs-2,
.col-xs-3,
.col-xs-4,
.col-xs-5,
.col-xs-6,
.col-xs-7,
.col-xs-8,
.col-xs-9,
.col-xs-10,
.col-xs-11,
.col-xs-12 {
  float: left;
}

.col-xs-1 {
  width: 8.333333333333333%;
}
.col-xs-2 {
  width: 16.666666666666666%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-4 {
  width: 33.333333333333336%;
}
.col-xs-5 {
  width: 41.66666666666667%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-7 {
  width: 58.333333333333336%;
}
.col-xs-8 {
  width: 66.66666666666667%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-10 {
  width: 83.33333333333333%;
}
.col-xs-11 {
  width: 91.66666666666667%;
}
.col-xs-12 {
  width: 100%;
}


@media (min-width: 768px) {
  .col-sm-1,
  .col-sm-2,
  .col-sm-3,
  .col-sm-4,
  .col-sm-5,
  .col-sm-6,
  .col-sm-7,
  .col-sm-8,
  .col-sm-9,
  .col-sm-10,
  .col-sm-11,
  .col-sm-12 {
    float: left;
  }

  .col-sm-1 {
    width: 8.333333333333333%;
  }
  .col-sm-2 {
    width: 16.666666666666666%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-4 {
    width: 33.333333333333336%;
  }
  .col-sm-5 {
    width: 41.66666666666667%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-7 {
    width: 58.333333333333336%;
  }
  .col-sm-8 {
    width: 66.66666666666667%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-10 {
    width: 83.33333333333333%;
  }
  .col-sm-11 {
    width: 91.66666666666667%;
  }
  .col-sm-12 {
    width: 100%;
  }
}


@media (min-width: 992px) {
  .col-md-1,
  .col-md-2,
  .col-md-3,
  .col-md-4,
  .col-md-5,
  .col-md-6,
  .col-md-7,
  .col-md-8,
  .col-md-9,
  .col-md-10,
  .col-md-11,
  .col-md-12 {
    float: left;
  }

  .col-md-1 {
    width: 8.333333333333333%;
  }
  .col-md-2 {
    width: 16.666666666666666%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-4 {
    width: 33.333333333333336%;
  }
  .col-md-5 {
    width: 41.66666666666667%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-7 {
    width: 58.333333333333336%;
  }
  .col-md-8 {
    width: 66.66666666666667%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-10 {
    width: 83.33333333333333%;
  }
  .col-md-11 {
    width: 91.66666666666667%;
  }
  .col-md-12 {
    width: 100%;
  }
}

@media (min-width: 1200px) {
  .col-lg-1,
  .col-lg-2,
  .col-lg-3,
  .col-lg-4,
  .col-lg-5,
  .col-lg-6,
  .col-lg-7,
  .col-lg-8,
  .col-lg-9,
  .col-lg-10,
  .col-lg-11,
  .col-lg-12 {
    float: left;
  }

  .col-lg-1 {
    width: 8.333333333333333%;
  }
  .col-lg-2 {
    width: 16.666666666666666%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-4 {
    width: 33.333333333333336%;
  }
  .col-lg-5 {
    width: 41.66666666666667%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-7 {
    width: 58.333333333333336%;
  }
  .col-lg-8 {
    width: 66.66666666666667%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-10 {
    width: 83.33333333333333%;
  }
  .col-lg-11 {
    width: 91.66666666666667%;
  }
  .col-lg-12 {
    width: 100%;
  }
}
```


