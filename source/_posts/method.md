---
title: Method 实例方法
date: 1
---

我们还提供了一些实例方法，以对BScroll实例进行特定操作，比如，让列表混动到某个位置或某个元素。

​	

### **实例方法列表**

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