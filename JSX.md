## jSX

### jsx 的本质是什么

jsx 是 javascript 的一种语法扩展，他和模板语言很接近，但是它充分具备了 javascript 的能力。

### 为什么要用 jsx

jsx 允许我们使用熟悉的 html 标签语法来创建虚拟 DOM，在降低学习成本的同时，也提升了开发效率和开发体验

### jsx 背后的功能模块是什么

jsx 会被babel编译成 React.createElement 的格式，用来创建 ReactElement 也就是虚拟DOM。

### React.createElement 做了什么事情

入口：React.createElement =》 二次处理 key、ref、self、source =》遍历 config，筛选出可以提取进 props 的属性=》提取子元素推入 childArray 数组 =》 初始化 defaultProps =》 结合以上数据作为入参，发起 ReactElement 调用

### ReactDom.render 方法

虚拟DOM（ReactElement）会和目标容器一起作为参数传递给 ReactDOM.render 方法，用于创建真实DOM

```
   ReactDom.render({
    // 需要渲染的函数（ReactElement）
     element,
    // 元素挂载的目标容器（一个真实的DOM）
     container,
    // 回调函数 可选参数 可以用来处理渲染结束后的逻辑
     [callback]
   })

   // example
   const rootElement = document.getElementById('root')
   ReactDOM.render(<APP />,rootElement)
```
