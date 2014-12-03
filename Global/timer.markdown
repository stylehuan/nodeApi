# 'timer'对象

---

`setTimeout`和`setInterval`定时器函数均返回一个对象。下面列举出该对象的方法。



## unref()

当定时器函数指定多少ms后执行某个回调函数时。可以使用这个定时器函数返回的对象的unref方法取消该回调。

	var _timer = setTimeout(function(msg){
		console.log(msg);
	},1000, "我是msg");

	//取消该定时器
	_timer.unref();


##ref()

当使用定时器对象的unref方法取消回调函数调用后，可使用该定时器对象的ref方法恢复函数的调用。



##setImmediate(cd, ms, [arg...])

`setImmediate`是node0.91之后新的用于非I/O的异步执行方法。她的`callback`的执行实在I/O事件之后，但是是在其他定时器`setTimeout`和`setIntervar`之前。返回一个`immediateId`.`clearImmediate`通过这个ID来停止回调的触发。

##clearImmediate(immediate);

通过`immediate`停止`setImmediate`回调函数的触发.




