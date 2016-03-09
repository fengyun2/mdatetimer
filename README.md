#### 移动端 - 通用性时间日期面板选择器
使用说明:

1. 在页面上引入 css 和 js (可以参考index.html)
```
<link rel="stylesheet" type="text/css" href="css/mdatetimer.css">
<script type="text/javascript" src="js/zepto.js"></script>
<script type="text/javascript" src="js/mdatetimer.js"></script>
```

2. 在页面上使用 `input[type="text"]` 作为输入框,此外为了防止手机上弹出软件盘,添加 `readonly` 属性
```
<input type="text" name="datetime" id="picktime" value="2016-03-09">
```

3. 日期组件初始化
```
var opts = {
	mode : 3, //时间选择器模式：1：年月日，2：年月日时分（24小时），3：年月日时分（12小时），4：年月日时分秒。默认：1
	format : 2, //时间格式化方式：1：2015年06月10日 17时30分46秒，2：2015-05-10  17:30:46。默认：2
	years : [2000, 2010, 2011, 2012, 2013, 2014, 2015, 2016, 2017], //年份数组
	nowbtn : true, //是否显示现在按钮
	onOk : function(){		//点击确定时添加额外的执行函数 默认null
		//alert('OK');
	},
	onCancel : function(){	//点击取消时添加额外的执行函数 默认null
		alert('A');
	},
};
$('#picktime').mdatetimer(opts);
```
