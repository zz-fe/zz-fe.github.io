# 九个Console命令，让js调试更简单

## 一、显示信息的命令
```
   console.log('hello world')
   console.info('信息')
   console.error('错误信息')
   console.warn('警告')
  
  以上这四个是比较常见的的 
```

## 二、占位符(不常用,知道就好)

#####  console上述的集中度支持printf的占位符格式，支持的占位符有：字符（%s）、整数（%d或%i）、浮点数（%f）、和对象（%o）和css样式(%c):

```
   1: <script type="text/javascript">
   2:         console.log("%d年%d月%d日",2014,6,26);
   3: </script>

```
控制台效果

```
   2014年6月26日
``` 


```
   1: <script type="text/javascript">
   2:        console.log("%cHello world,欢迎您！","color: red; font-size: 24px");   
   3: </script>

```
控制台效果

```
   //输出红色字体 24px大小的字符串
   Hello world,欢迎您  
```
总结 

其实有的时候大家在看百度或者阿里的控制台的时候，可能会输入一些字符画，其实就是可以通过以下工具来生成  

1.<a href='http://www.degraeve.com/img2txt.php'>mg2txt</a>

2.<a href='http://www.network-science.de/ascii/'>Ascii generator</a>

有兴趣的可以玩玩 

## 三、信息分组 
```
 9:   console.group("第一组信息");
10:
11:     console.log("第一组第一条");
12:
13:     console.log("第一组第二条)");
14:
15:   console.groupEnd();
```

输出效果 

```
第一组信息
	 第一组第一条
	 第一组第二条
```

## 四、查看对象的信息 

```
   var data = {
       name :  'hello',
       age : 20
   }
   console.dir(data)
```

输入效果

```
   Object 
      age: 20
      name: 'hello' 
      _proto_:Object

``` 

## 五、显示某个节点的内容

console.dirxml()用来显示网页的某个节点（node）所包含的html/xml代码。


```
<div id='info'>
   <p>hello world</p>
</div>
<script>
   var info = document.getElementById('info');
   console.dirxml(info);
</script>
//jq 
<script>
     var info = $('#info')[0];
     console.dirxml(info);
</script>

```
控制台效果

```
<div id='info'>
   <p>hello world</p>
</div>

```

## 六、判断变量是否是真 

console.assert()用来判断一个表达式或变量是否为真。如果结果为否，则在控制台输出一条相应信息，并且抛出一个异常。


```
<script>
     var info = '我帅吗？';
     console.assert(info == '我不帅');
</script>

```

输入效果 

```
  error 

```

## 七、追踪函数的调用轨迹（框架中应用）

```
/*函数是如何被调用的，在其中加入console.trace()方法就可以了*/
　　function add(a,b){
     console.trace();
　　　　return a+b;
　　}
　　var x = add3(1,1);
　　function add3(a,b){return add2(a,b);}
　　function add2(a,b){return add1(a,b);}
　　function add1(a,b){return add(a,b);}

```

控制台输出

```
console.trace
add @ index.html:11
add1 @ index.html:17
add2 @ index.html:16
add3 @ index.html:15
(anonymous) @ index.html:14
 

``` 

## 八、计时功能 (性能测试)

```
   1: <script type="text/javascript">
   2: 　　console.time("控制台计时器一");
   3: 　　for(var i=0;i<1000;i++){
   4: 　　　　for(var j=0;j<1000;j++){}
   5: 　　}
   6: 　　console.timeEnd("控制台计时器一");
   7: </script>
``` 

控制台输出结果 


```
运行时间是38.84ms

```

## 性能分析（Profiler）

console.profile()的性能分析，就是分析程序各个部分的运行时间，找出瓶颈所在，使用的方法是console.profile()。 

```
<script type="text/javascript">
 　　function All(){
         alert(11);
　　　　     for(var i=0;i<10;i++){
             funcA(1000);
          }
　　　　    funcB(10000);
　　    }

　　function funcA(count){
　　　　for(var i=0;i<count;i++){}
　　}

　　function funcB(count){
　　　　for(var i=0;i<count;i++){}
　　}

　　console.profile('性能分析器');
　　All();
　　console.profileEnd();
</script>


```

```
可以查看javaScript Profilter

```

