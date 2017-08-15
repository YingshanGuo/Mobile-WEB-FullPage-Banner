# 移动web-全屏滚动页面(jQuery)

## 依赖

依赖于jQuery、slip.js

## 主要实现代码

- 不回滚到第一页

```
var container = document.getElementById('container');
var pages = document.querySelectorAll('.page');
var slip = Slip(container, 'y').webapp(pages);
```

- 回滚到第一页

```
 Slip(document.getElementById('container'), 'y').webapp().end(function () {
    if (this.page === 4) location.reload();
});
```