# AntDesign_Training
一个AntDesign的入门学习，包含AntDesign、react、babel等


## 依赖项目

### React !()[./dependence/react/README.md]





# 待整理内容


## React官网学习笔记
 http://react-china.org/t/react/191
 
Origin
1、React并不会通过String类型的Html片段生成DOM
2、在componentWillReceiveProps中调用setState()不会触发re-render
3、componentWillUpdate中不能调用this.setState()
4、在通过Ajax获取到数据，调用this.setState()之前，应该通过this.isMounted()确定当前的component已经处在渲染完成的阶段
5、父组件到子组件通过props传递数据，子组件向父组件传递数据通过global event方式来处理，即在root element上接受所有子组件的事件处理
6、移动设备的touch事件需手动开启：React.initializeTouchEvents(true)
7、setState(data, callback)中的callback是在re-render完成之后调用的

FLUX
1、Dispatcher分发来自页面事件行为的事件名称和数据到全局的Store中
2、Dispather中要注册各种事件及其对应的行为(更新Store)
3、通过使用类似于MicroEvent.js这样的类库，为Store提供对象的事件行为，监听它的数据变化
4、在componentDidMount中注册Store的行为，在componentWillUnmount中解绑Store的行为

JSX
1、组件的变量名必须大写，用于区分原生的Html标签和自定义组件
2、用大括号包裹的js表达式来表示组件的属性，替代原生写法的双引号
3、如果想给最终装换成的HTML元素添加自定义的属性，必须用前缀"data-“
4、props应该作为不可变常量使用，不能component.props.foo = x 这样使用
5、<Component {…someObj} /> 可以将someObj中的所有属性写进Component的props中
6、<Component {…someObj} attr=“higherLevel" /> 中的attr属性会复写someObj中的同名属性
7、JSX封装了React的原生接口为类XML协议的语法，使之更加易于编写
8、获取父级的属性用this.props，获取内嵌的子元素用this.props.children
9、为防止XSS攻击，提供安全性，在插入原生的HTML时需使用

<span dangerouslySetInnerHTML={{__html: rawHtml}}>
10、css的内嵌写法style，必须接受一个对象，其key是css属性名，多单词属性采用小驼峰写法，如果需要添加浏览器厂商前缀，则该前缀的首字母必须大写
11、除指定的某些元素(http://facebook.github.io/react/tips/style-props-value-px.html
)外，style中的属性值如果是纯数字会添加’px’后缀，如{height: 10} 编译成 height: 10px
12、通过this.transferPropsTo( subComponent ) 将当前组件的所有props传递给它的某个子组件，也可以通过{...this.props}的方式传递