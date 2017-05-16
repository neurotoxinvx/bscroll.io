---
title: 起步
---

------



### HTML **引入**

直接下载 [**开发版本**](https://github.com/ustbhuangyi/better-scroll/blob/master/build/bscroll.js) 或 [**生产版本**](https://github.com/ustbhuangyi/better-scroll/blob/master/build/bscroll.min.js) ，并在HTML文件中使用`<script>`标签引入。

```html
<body>
  <div id="wrapper">
    <ul>
       <li>...</li>
       <li>...</li>
       ...
    </ul>
  </div>
  <script type="text/javascript" src="bscroll.min.js"></script>
  <script type="text/javascript">
    new BScroll(document.getElementById('wrapper'));
  </script>
</body>
```
​	

### NPM **引入**

安装better-scroll

```shell
npm install better-scroll --save-dev
```

引入better-scroll

```javascript
import BScroll from 'better-scroll'
```

如果不支持import, 请使用

```javascript
var BScroll = require('better-scroll')
```

​	



