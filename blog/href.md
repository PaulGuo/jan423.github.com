# href

## 锚点

* 目标元素的ID和Name都可以作为锚点，区别在于ID对于目标元素的类型是无限制的，而name则仅适用于以下元素：A, APPLET, FORM, FRAME, IFRAME, IMG, MAP.

		<a href="#target1">Go target1</a>   //使用name  
	    <a href="#target2">Go target2</a>   //使用id  
	    <a href="#target3">Go target3</a>   //div的name是无效的  
	    <a href="#target4">Go target4</a>   //div的id是OK的  
	    ....  
	    contents  
	    ....  
	    <a name="target1">Target1 here</a>  
	    <a id="target2">Target2 here</a>  
		<div name="target3">Target3 here</div>  
		<div id="target4">Target4 here</div> 

* 千万不要为难浏览器，大小写什么的，id和name不相同什么的

* 回到顶部的#，最好还是自己写标签。不要依靠浏览器的特性