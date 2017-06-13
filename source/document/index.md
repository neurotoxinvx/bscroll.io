---
title: 文档
---

​	  

## Install 安装

------

### 通过npm引入

安装better-scroll

```javascript
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

## Options 参数

------

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

#### **滚动列表参数：**

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

#### **slider组件参数：**

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

#### **picker组件参数：**

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


  ​

## Method 实例方法

------

我们还提供了一些实例方法，以对BScroll实例进行特定操作，比如，让列表混动到某个位置或某个元素。

​	

#### **实例方法列表：**

------

**scroll.scrollTo(x, y, time, easing)**

- 参数：
  - `{number} x` : X轴坐标
  - `{number} y` : Y轴坐标
  - `{number} time` : 动画时间
  - `{Function} easing` : 缓动函数


- 用法：

  滚动BScroll实例到指定元素。


- 示例：

  ```javascript
  let scroll = new BScroll(document.getElementById('wrapper'))
  scroll.scrollTo(0, 500)
  ```

  ​

**scroll.scrollToElement(el, time, offsetX, offsetY, easing)**

- 参数：
  - `{Object} el` : 某个DOM元素，必填
  - `{number} time` : 动画时间
  - `{number} offsetX` : X轴坐标偏移量
  - `{number} offsetX` : Y轴坐标偏移量
  - `{Function} easing` : 缓动函数


- 用法：

  滚动BScroll实例到指定位置。


- 示例：

  ```javascript
  let scroll = new BScroll(document.getElementById('wrapper'))
  let el = document.getElementById('elId')
  scroll.scrollToElement(el)
  ```

  ​

**scroll.getCurrentPage()**

- 返回值：`{Object}` 

  ```javascript
  // 对象结构
  {
  	x: 0,	// 滚动横向的位置
  	y: 0,	// 滚动纵向的位置
  	pageX: 0,	// 横向的页面索引
  	pageY: 0	// 纵向的页面索引
  }
  ```

- 用法：

  当 snap 为 true 时，获取滚动的当前页。
  ​

**scroll.goToPage(x, y, time, easing)**

- 参数：
  - `{number} x` : 横向页面索引
  - `{number} y` : 纵向页面索引
  - `{number} time` : 动画时间
  - `{Function} easing` : 缓动函数


- 用法：

  当 snap 为 true，滚动到指定的页面。
  ​

**scroll.refresh()**

- 用法：

  强制BScroll实例重新计算，当 better-scroll 中的元素发生变化的时候调用此方法。
  ​

**scroll.enable()**

- 用法：

  启用 better-scroll，默认开启。
  ​

**scroll.disable()**

- 用法：

  禁用 better-scroll。
  ​

**scroll.destroy()**

- 用法：

  销毁 better-scroll，解绑事件。


  ​

## Events 事件

------

在创建BScroll对象之后，我们还提供了多类事件，如scrollStart、scroll、scrollCancel等，大家可根据需要，绑定自定义事件handle。

用法示例:

```javascript
let scroll = new BScroll(document.getElementById('wrapper'),{
   probeType: 3
})

scroll.on('scroll', (pos) => {
  console.log(pos.x + '~' + posx.y)
  ...
})
```

​		

#### Events **列表：**

------

- beforeScrollStart - 滚动开始之前触发
- scrollStart - 滚动开始时触发
- scroll - 滚动时触发
- scrollCancel - 取消滚动时触发
- scrollEnd - 滚动结束时触发
- flick - 触发了 fastclick 时的回调函数
- refresh - 当 better-scroll 刷新时触发
- destroy - 销毁 better-scroll 实例时触发
  ​
  ​