＃ 区别：  
var 定义的是全局域或者函数域  
let  定义的是块级域变量  
例子：  
```
<html>
<head></head>
<body><body>
<script>
var a = [];
var b = [];
for(var i=0;i<10;i++){
	a[i] = function(){
		console.log(i);
	}
	console.log(i); // 0 1 3 4 5 6 7 8 9
}
 
a[1](); // 10
console.log(i); // 10
for(let j=0;j<10;j++){
	b[j] = function(){
		console.log(j);
	}
	console.log(j); // 0 1 3 4 5 6 7 8 9
}
b[1](); // 1
console.log(j); // j is not defined
</script>
</html>
```
对于let j ， for 的每一次循环都会新建一个只属于该次循环且属于循环块内的j，且j的值会继承上一次循坏，所以在for循环块外部的j是 not definded的