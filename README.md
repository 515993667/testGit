<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title></title>
	<style type="text/css">
		/*浮动布局的基本样式*/
		ul{
			margin: 0;
			padding: 0;
		}
		li{
			margin: 0;
			padding: 0;
			list-style: none;
			float: left;
		}
		.clear:after{
			content:"";
			display: block;
			clear: both;
		}
		/*浮动布局的基本样式end*/
		.li01{
			width: 20%;
			background-color: red;
		}
		.li02{
			width: 30%;
			background-color: blue;
		}
		.li03{
			width: 50%;
			background-color: green;
		}
		
		/*居中的样式*/
		.centerBox{
			position: absolute;
			left:50%;
			top: 50%;
		}
		.center{
			display: inline-block;
			width: 50px;
			/*height: 100px;*/
			background-color: yellow;
			margin-top: -50%;
			margin-left:-50%;
			vertical-align: middle;
			/*这个写法是在你不知道这个div的宽高度的情况下使用的  用-50%*/
			
		}
		.center02{
			display: inline-block;
			width: 50px;
			height: 100px;
			background-color: red;
			position:relative;
			left:50%;
			top: 50%;
			/*这个写法是在你知道这个div的宽高度的情况下使用的  用具体px数值*/
			margin-top: -50px;
			margin-left:-25px;
			/*下面这个属性必须写 要不margin-top负值会失效  具体原理先别纠结  比较复杂  一般用上面那种*/
			vertical-align: middle;
		}
	</style>
</head>
<body>
	<h3>浮动布局</h3>
	<!-- 这样结构写的话你以后布局就只需要直接给li宽度就可以了   -->
	<ul class="clear">
		<li class="li01">第一个浮动块</li>
		<li class="li02">第二个浮动块</li>
		<li class="li03">第三个浮动块</li>
	</ul>
	<div>这是一个正常的div</div>


	<hr/>
	<h3>垂直水平居中</h3>
	<section style="width:100%;height:300px;position: relative;">
		<div class="centerBox">
			<div class="center">居中</div>
		</div>
	</section>

	<hr/>
	<h3>垂直水平居中 2</h3>
	<section style="width:100%;height:300px;">
		<div class="center02">居中</div>
	</section>
</body>
</html>
