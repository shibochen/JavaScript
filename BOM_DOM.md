# DOM
## document对象
- 常用属性： `URL`， `title`
- 时钟补充： `setTimeout`, `setInterval`, `clearInterval()`, `clearTimeout()`;

## 访问节点
- `getElementById(id)`: 返回Element对象
- `getElementsByTagName(tagName)`: 返回HTMLCollection对象
- `getElementsByName(name)`: 返回NodeList对象
- `querySelector(selectors)`: 返回Element对象
- `querySelectorAll(selectors)`: 返回NodeList对象

接口：有自己规定的方法，属性，但必须有子类给他实现
类型：可以直接创建实例

 鼠标事件对象（接口） MouseEvent
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


## 键盘和文本事件（49）
- keydown, keypress, keyup
- 事件触发顺序： keydown -> keypress - keyup
- keydown和keyup都是通过事件对象的keyCode获取按下键的字符编码. keypress是通过事件对象的charCode来获取按下键的字符码
（ie8 可以通过keyCode获取）
- 键盘事件的对象也包括shiftKey, ctrlKey, altKey和metaKey 属性
- 键盘分为：可以打印的字符串和不可打印的功能键
- change事件 （当失去焦点后触发）

## 事件高级 （52 ！important）
- 事件绑定封装
- 事件对象封装
- 文档加载完成封装
- 事件委托（？）

## 元素样式操作（61）
- 内联样式 （`Element.style` ,  `Element.style.cssText`, `Element.className`, `Element.setAttribute`）
- 样式表操作 （动态添加样式表）
