---
title: Options 参数
date: 3
---

在创建BScroll对象时，我们提供了多项参数的灵活配置。

用法示例：

```javascript
let scroll = new BScroll(document.getElementById('wrapper'), {
  startX: 0,
  startY: 0
})
```

这些参数项，大部分是用于普通滚动列表的，也有小部分是仅用于轮播图slider或picker组件。

​	

### **滚动列表参数**

------

**scrollY**

- 类型：`boolean`
- 默认值：`true`
- 配置：是否以Y轴为滚动方向

**scrollX**

- 类型：`boolean`
- 默认值：`false`
- 配置：是否以X轴为滚动方向

**startY**

- 类型：`number`
- 默认值： `0` 
- 配置：滚动列表的初始X轴位置为startY

**startX**

- 类型：`number`
- 默认值： `0` 
- 配置：滚动列表的初始X轴位置为startX

**click**

- 类型：`boolean`
- 默认值：`true`
- 配置：是否启用click事件

**directionLockThreshold**

- 类型：`number`
- 默认值：`5`
- 配置：如果Y（或X）轴的偏移量减去X（或X）轴的偏移量大于directionLockThreshold，则方向锁定为Y（或X）轴

**momentum**

- 类型：`boolean`
- 默认值：`true`
- 配置：是否开启拖动惯性

**bounce**

- 类型：`boolean`
- 默认值：`true`
- 配置：是否启用弹力动画效果，关掉可以加速

**swipeTime**

- 类型：`number`
- 默认值：`2500`
- 配置：swipe 持续时间

**bounceTime**

- 类型：`number`
- 默认值：`700`
- 配置：弹力动画持续的毫秒数

**swipeBounceTime**

- 类型：`number`
- 默认值：`1200`
- 配置：swipe 回弹时间

**deceleration**

- 类型：`number`
- 默认值：`0.001`
- 配置：滚动动量减速。越大越快，建议不大于0.01

**momentumLimitTime**

- 类型：`number`
- 默认值：`300`
- 配置：符合惯性拖动的最大时间

**momentumLimitDistance**

- 类型：`number`
- 默认值：`15`
- 配置：符合惯性拖动的最小拖动距离

**resizePolling**

- 类型：`number`
- 默认值：`60`
- 配置：重新调整窗口大小时，重新计算better-scroll的时间间隔

**preventDefault**

- 类型：`boolean`
- 默认值：`true`
- 配置：是否阻止默认事件

**preventDefaultException**

- 类型：`object`
- 默认值：`{ tagName: /^(INPUT|TEXTAREA|BUTTON|SELECT)$/ }`
- 配置：阻止默认事件

**HWCompositing**

- 类型：`boolean`
- 默认值：`true`
- 配置：是否启用硬件加速

**useTransition**

- 类型：`boolean`
- 默认值：`true`
- 配置：是否使用CSS3的Transition属性

**useTransform**

- 类型：`boolean`
- 默认值：`true`
- 配置：是否使用CSS3的Transform属性

**probeType**

- 类型：`number`
- 默认值：无
- 配置： `1` 滚动的时候会派发scroll事件，会截流；`2`滚动的时候实时派发scroll事件，不会截流； `3`除了实时派发scroll事件，在swipe的情况下仍然能实时派发scroll事件
  ​

### **slider组件参数**

------

**snap**

- 类型：`boolean`
- 默认值：`false`
- 配置：是否使用slider组件

**snapLoop**

- 类型：`boolean`
- 默认值：`false`
- 配置：是否可以无缝循环轮播

**snapThreshold**

- 类型：`number`
- 默认值：`0.1`
- 配置：用手指滑动页面切换的阈值，大于这个阈值时，将滑动到下一页

**snapSpeed**

- 类型：`number`
- 默认值：`400`
- 配置：轮播图切换的动画时间
  ​

### **picker组件参数**

------

**wheel**

- 类型：`boolean`
- 默认值：`false`
- 配置：是否使用picker组件

**selectedIndex**

- 类型：`number`
- 默认值：`0`
- 配置：仅当wheel 为 true 时有效，配置被选中的 wheel 索引

**rotate**

- 类型：`number`
- 默认值：`25`
- 配置：仅当wheel 为 true 时有效，配置被选中的 wheel 每一层的旋转角度

**adjustTime**

- 类型：`number`
- 默认值：`400`
- 配置：仅当wheel 为 true 有用，调整停留位置的时间

