=======
wh8766.github.com
=================

Github Blog

#md文档

##二级标题

```
//Pines Notify
//http://sciactive.github.com/pnotify/#demos-simple
(function() {
	//简单配置下
	$.pnotify.defaults.delay = 3000;

	//构建新的alert
	var _oldAlert = window.alert;
	var _newAlert = window.alert = function(msg, title, type) {
			$.pnotify({
				title: title || '提示信息',
				text: msg,
				type: type || 'info',
				history: false,
				text_escape: true,
				nonblock: true,
				nonblock_opacity: .2
			});
		};

	//注入到每个模块的页面中去
	//	$("#fmain").load(function(){
	//		window.frames["fmain"].alert = _newAlert;
	//		if (window.frames["fmain"].$){
	//			window.frames["fmain"].$.pnotify = $.pnotify;
	//		}
	//	});
})();
```