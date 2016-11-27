
# React 基础知识

## React的HelloWorld

```javascript

<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>React Demo1</title>

	<!-- React 核心库 -->
	<script type="text/javascript" src="libs/react.js"></script> 

	<!-- React DOM适配库 -->
	<script type="text/javascript" src="libs/react-dom.js"></script>

	<!-- Babel 是将JSX语法转换为Javascript语法的库 -->
	<script type="text/javascript" src="libs/babel.min.js"></script>
	
</head>
<body>
	<div id="container"></div>
	<script type="text/babel">
		/* 使用了JSX语法的React */
		/* 使用ReactDOM.render(element,container,[callback])
			https://facebook.github.io/react/docs/react-dom.html#render
		*/
		ReactDOM.render(
			<span>Hello React!</span>,
			document.getElementById('container')
		);
	</script>
</body>
</html>

```

### 解析语法
*. ReactDOM.render(element,container,[callback])
  element: 插入的元素
  container: 装载element的容器，必须使用js原生的getElementById获取
  callback：回调函数
  语法说明：https://facebook.github.io/react/docs/react-dom.html#render

### 参考文档
https://facebook.github.io/react/docs/

