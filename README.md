# fixproblem
前端开发常遇到的问题  
1.css问题  
1）清除所有固定样式的margin,padding,这样做就可定位精准。*{margin:0;padding:0}  
2)margin-top和margin-bottom不能正常显示，清除塌陷 可以使用clearfix类：  
或者是父盒子中的子盒子使用margin-top不管用，需要在子盒子中加入{height:0;overflow:hidden;}  
3)父盒子没有高度，子盒子使用了浮动，不能撑开父盒子问题，需要清除浮动。  
使用样式在父元素中加入如下样式：  
.clearfix:before,.clearfix:after{  
    content:"";  
    display:table;  
}  
.clearfix:after{  
    clear:both;  
}  
.clearfix{  
    zoom:1;           //兼容ie  
}   
4）几个隐藏的占位问题  
overflow:hidden:元素隐藏，超出部分不占原来位置;可以隐藏元素的滚动条。  
还可单独使用overflow-x,overflow-y:hidden 隐藏元素水平方向或者垂直方向的滚动条。  
overflow:auto:超出父元素部分，可用滚动条滚动观看。  
display:none:元素隐藏，但元素占原来位置。  
visibility:hidden;元素隐藏，但元素占原来位置;  
visibility:visible;  
5)opacity设置半透明效果  
opacity:0.5;  
filter:alpha(opacity=50); //兼容ie  
5)类名中的效果不能实现，要考虑：是否权重问题，是否类名写重复了。  
6）设置字体用font连写性能更好：font:bold 15px/30px "Microsoft Yahei";  
7）图片和表格可用定位：vertical-align:baseline/top/middle/bottom;  
8)只有定位元素才能设置z-index;  
  
2.html问题  
1）设置超链接：  
href:目标url地址;  
target:_self和_blank(新窗口中打开);  
2）ul标签type值：disc(黑点)，square(方黑点)，circle(空心圆点)  
3）ol标签type值：type=a英文字母编号，type=1数字编号，type=I罗马数字编号  
4）如果a标签不闭合,会多出很多a标签。  

3.DOM    
1)node.style.cssText="width:200px;" 会覆盖掉之前设置的属性相同的样式。







