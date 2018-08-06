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

## HTMLCollection元素对象（接口）
- 元素的动态集合，提供用来从该集合中选择元素的方法和属性。当其所包含的文档结构发生改变时，它会自动更新，不是真正的数组，是伪数组。
- 常用属性 (`HTMLCollection.length`)
- 常用方法 （`HTMLCollection.item()`, `HTMLCollection.namedItem()`, Array.prototype.slice.call(c)）

## NodeList对象节点集合
- NodeList对象是一个节点的集合, 伪数组
- 常用属性 （`length`）
- 常用方法 （`NodeList.item()`, Array.prototype.slice.call(c)）

- 注意
   - 不要用`for in`进行循环，因为会把length和item也被访问到，所以最好用索引进行循环遍历
   - `querySelectorAll` 返回的NodeList是一个固定的集合，不会随着变化而变
   - Node节点的childNodes属性是实时动态的更新
   
## 事件
- 事件绑定事件（DOM0）
   - 第一种: 直接在HTML中给标签添加事件属性
   - 通过JS代码给元素添加事件属性 （兼容性好，但一个标签只能绑定一次事件响应方法）
   - 事件三要素： 事件源，事件类型，事件响应方法
- 事件流
   - 事件分为捕获阶段和冒泡阶段。捕获阶段就是事件信息从顶层向下层传递的过程，而冒泡是事件反应从底层向上层反馈的过程。
   - Js可以通过`addEventListener`来实现捕获阶段或者冒泡阶段的事件响应方法注册
   - 直接对DOM对象上设置事件属性和标签中直接编写标签属性的方式都是在冒泡阶段执行。
- 事件绑定事件（DOM2）
   - addEventListener(type, listen,useCapture)
   - removeEventListener(type,listen,useCapture);
 - IE浏览器绑定和解绑事件attachEvent (IE8以前)
   - attachEvent(on + 事件类型字符，函数/匿名函数)
   - detachEvent(跟上面一样)
   - 只能在冒泡阶段触发
 DOM0：只能绑定一个事件，只能在冒泡阶段触发，兼容性好
 DOM2: 可以多绑定事件，可以选择在捕获或者冒泡阶段触发，兼容性不好
- 事件响应方法的执行顺序
   - 设置标签的事件属性或者直接给元素设置事件属性的最优先执行（带有确定）
   - addEventListener的事件响应方法执行顺序跟注册顺序一致
   - attachEvent注册的事件响应方法的执行顺序不确定，执行过程不能依赖它的注册顺序
## 事件对象
- DOM事件触发时，会产生一个事件对象Event，封装事件相关信息：事件源对象，事件类型，事件处理方法
- 常用属性
   - Event.target 事件源对象， IE6-IE8 Event.srcElement
   - Event.type 事件类型
   - Event.cancelBubble 取消事件冒泡（IE以下）
   - Event.returnValue 布尔类型，false阻止默认行为
- 常用方法
   - 阻止默认行为 Event.stopDefault(), IE不能用， 事件响应方法returnValue = false
   - 阻止事件冒泡 Event.stopPropagation(), IE不能用， 用cancleBubble = true;
   
## 鼠标事件对象（接口） MouseEvent
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

## Node接口
- Node接口是对节点的封装，继承字EventTarget
- 常用属性：（`nodeType`, `nodeName`, `nodeValue`）
- 节点关系：（`Node.childNotes`, `Node.firstChild`, `Node.lastChild`, `Node.nextSibling`, `Node.previousSibling`, 
`Node.parentNode`,`Node.parentElement`）
- 常用方法： （`Node.appendChild`, `Node.insertBefore`, `Node.removeChild`, `Node.hasChildNodes`,`Node.cloneNode(deep)` ）
   - deep：两个值：true 或者 false， true完全复制，false部分复制
- 创建节点：（`document.createElement`,`document.createAttribute`, `document.createComment`, `document.createTextNode`）

## 元素样式操作（61）
- 内联样式 （`Element.style` ,  `Element.style.cssText`, `Element.className`, `Element.setAttribute`）
- 样式表操作 （动态添加样式表）
