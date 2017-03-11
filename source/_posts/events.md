---
title: Events 事件
date: 3
---

Example:

```javascript
let scroll = new BScroll(document.getElementById('wrapper'),{
   probeType: 3
})

scroll.on('scroll', (pos) => {
  console.log(pos.x + '~' + posx.y)
  ...
})
```

Events 列表

- beforeScrollStart - 滚动开始之前触发
- scrollStart - 滚动开始时触发
- scroll - 滚动时触发
- scrollCancel - 取消滚动时触发
- scrollEnd - 滚动结束时触发
- flick - 触发了 fastclick 时的回调函数
- refresh - 当 better-scroll 刷新时触发
- destroy - 销毁 better-scroll 实例时触发
