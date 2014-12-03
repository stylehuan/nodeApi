#require(modName&path)

---

加载模块，实际上`require`本不是全局的，而是属于每个`module`.

##require.resolve(path&mod);

查询某个模块文件的绝对路径

	require.resolve("./test.js")// F:/xxx/test.js

##require.cache

`cache`是一个对象，用来保存已缓存的模块。我们知道每个模块只需要加载一次
	
	
	console.log(require.cache)//查看所有的已缓存的模块
	console.log(require.cache[xx]);//查看具体的模块对象
	
可使用 `delete`关键字删除某一个缓存的模块。那个这个模块下次将会重新加载。

	delete require.cache[xx.js];//删除缓存的某个模块对象



