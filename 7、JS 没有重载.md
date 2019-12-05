1、重载的定义: 几个行参不同但是名字相同的函数构成重载  
2、js中同名的函数后面的会覆盖前面的，所以js中没有重载
若想在js中实现重载可借助arguments，如下  
```
function f(){ 
  if(arguments.length == 0){  // arguments就是存储传入参数的对象
  console.log("没有传入参数") 
}else{
console.log("有传入参数") 
}
}
```