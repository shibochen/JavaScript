# DOM

## 42: 鼠标事件对象（借口） MouseEvent
- MouseEvent继承来自UIEvent， UIEvent继承自Event
- 鼠标事件对象中包括： 鼠标按键信息，键盘配合鼠标信息，鼠标的位置信息等

1. 鼠标事件对象的坐标位置
- 客户区坐标（视口内的坐标） ： clientX， clientY
- 页面坐标 ： pageX， pageY （除IE8以下）
  - pageX = event.clientX + (document.documentElement.scrollLeft || document.body.scrollLeft)
  - PageY = event.clientY + (document.documentElement.scrollTop || document.body.scrollTop)
- 屏幕坐标： screenX， screenY
- offestX 和 offsetY 是相对于事件源对象的内边距内测的距离 （不太理解）

Question： 区别以上clientX， pageX， screenX 等
