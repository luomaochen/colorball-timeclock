# colorball-timeclock

运用html 的canv做的一个动态时钟效果；能够产生色彩小球并输出，实现酷炫效果，效果如下：

![Alt text](https://github.com/luomaochen/colorball-timeclock/raw/master/Screenshots/1.png)




原先的代码实现如果长时间失焦  会导致小球冗杂  加了一下代码实现失焦情况停止计时器计时，就不会冗杂了。

var intervalId = setInterval(    //每秒执行30次
  	 function(){
       render( context );
       update();
   		}
  	 ,
  	 30
	);
 
	//获得焦点
	window.onfocus = function(){
  	 intervalId = setInterval(    //每秒执行30次
       function(){
           render( context );
           update();
       }
       ,
       30);
     };
 
 
 
	//失去焦点
	    window.onblur = function(){
  		 clearInterval(intervalId);
		}

