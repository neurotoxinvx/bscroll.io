---
title: Trigger 派发事件
date: 1
---

## 派发滚动

- scrollTo(x, y, time, easing) 滚动到某个位置，x,y 代表坐标，time 表示动画时间，easing 表示缓动函数

Example:

```javascript
let scroll = new BScroll(document.getElementById('wrapper'))
scroll.scrollTo(0, 500)
...
```
- scrollToElement(el, time, offsetX, offsetY, easing) 滚动到
  某个元素，el（必填）表示 dom 元素，time 表示动画，offsetX 和 offsetY 表示坐标偏移量，easing 表示缓动函数

