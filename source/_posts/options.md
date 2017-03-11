---
title: Options
date: 3
---

Example:

```javascript
let scroll = new BScroll(document.getElementById('wrapper'), {
  startX: 0,
  startY: 0
})
```

Options List:

- startX: `0` 开始的X轴位置
- startY: `0` 开始的Y轴位置
- scrollY: `true` 滚动方向
- click: `true` 是否启用click事件
- directionLockThreshold: `5`
- momentum: `true` 是否开启拖动惯性
- bounce: `true` 是否启用弹力动画效果，关掉可以加速
- selectedIndex: `0` 
- rotate: `25` 
- wheel: `false` 该属性是给 picker 组件使用的，普通的列表滚动不需要配置
- snap: `false` 是否开启捕捉元素，当为 true 时，捕捉的元素会根据可滚动的位置和滚动区域计算得到可滑动几页。
- snapLoop: `false` 是否创建当前滚动元素子集的拷贝
- snapThreshold: `0.1` 滑动的长度限制，只有大于这个距离才会触发事件
- swipeTime: `2500` swipe 持续时间
- bounceTime: `700` 弹力动画持续的毫秒数
- adjustTime: `400`
- swipeBounceTime: `1200`
- deceleration: `0.001` 滚动动量减速越大越快，建议不大于0.01
- momentumLimitTime: `300` 惯性拖动的回弹时间
- momentumLimitDistance: `15` 惯性拖动的回弹距离
- resizePolling: `60` 重新调整窗口大小时，重新计算better-scroll的时间间隔
- probeType: `1` 监听事件的触发时间，1为即时触发，3为延迟到事件完毕后触发
- preventDefault: `true` 是否阻止默认事件
- preventDefaultException: `{ tagName: /^(INPUT|TEXTAREA|BUTTON|SELECT)$/ }` 阻止默认事件
- HWCompositing: `true` 是否启用硬件加速
- useTransition: `true` 是否使用CSS3的Transition属性，否则使用-requestAnimationFram代替
- useTransform: `true` 是否使用CSS3的Transform属性
- probeType: `1` 滚动的时候会派发scroll事件，会截流。`2`滚动的时候实时派发scroll事件，不会截流。 `3`除了实时派发scroll事件，在swipe的情况下仍然能实时派发scroll事件

