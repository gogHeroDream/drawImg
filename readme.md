### 版本区别说明
>1.0版本是一个轻量级的，根据你要生成的文本立即生成这个图片；
>2.0版本支持异步慢慢去绘制可以不断绘制并生成对应的图片;
>3.0版本对2.0版本进行优化，可以在页面中先生成对应的canvas，待最后都完成了在生成一个img 修复上两个版本的有可能少绘制一个字的问题
### 使用说明
>1.先引入资源文件
>2.根据需求传参并new一个实例
>3.拿3.0使用示范，（相同版本代，推荐使用后面的稳定的，例如1.0和2.0就有换行和显示少一位的BUG，1.1和2.1都进行了修复。1.X版本在init后是一个回调，还要继续对这个生成的img进行操作，放到指定位置 就不举例了，2和3差不多）
### new一个实例
>var abc=new Watermark(obj);
>abc.init();
其中这个obj要按照规范进行传产，如果不传就是默认值，请根据需求传产

>var obj={
   src:'./images/1.png', //素材路径
   size:{width:'750',height:'440'}, // 素材大小
   text:"dfeoijfaedjfaof0e 大额啊哒哒哒我大神", // 文本内容
   textAlign:'left', //水平对齐方式
   textBaseline:'top', //垂直对齐方式
   textPosition:{wx:'20',hx:'20',width:'200',maxWidth:"710"}, //文本位置
   colorPosition:{x0:'0',y0:'0',x1:'750',y1:'440'}, //渐变范围
   color:[["0","yellow"],["0.3","pink"],["1.0","blue"]],//渐变色值和范围规范
   font:"30px microsoft yahei",//字体格式
   initHeight:0,
   hHeight:40, 
   sync:'async',//同异步
   times:{delay:100,interval:200},//延时与否
   // img:'',
   fatherBox:dom,  //一个原生的DOM对象 要存放位置的父元素；
   };
