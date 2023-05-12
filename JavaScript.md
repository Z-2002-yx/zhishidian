# JavaScript知识点

### 事件

##### 1、阻止事件冒泡

event.stopPropagation()

##### 2、阻止标签默认行为

event.preventDefault()



##### 3、滚轮事件

onwheel   监听到的元素对象中存在deltaY 表示整数时为向下滚动，表示负数时为向上滚动



### BOM

*浏览器对象模型*

##### 获取浏览器窗口尺寸

- window方法
  - window.innerHeight 获取浏览器高度
  - window.innerWidth 获取浏览器宽度
- document方法
  - document.body.clientHeight
  - document.body.clientWidth



##### Scroll元素节点的实际高宽，操纵顶部左侧

- scrollWidth 获取元素节点的宽度
- scrollHeight 获取元素节点的高度
- scrollTop  定位当前元素的顶部位置
- scrollLeft 定位当前元素的左侧位置

