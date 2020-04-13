＃ 创建
```
var promise = new Promise(function(resolve, reject){ 
  if(/*一步操作成功*/){
    resolve(value);
  }else{
    reject(error);
  }
 })
//resolve和reject是由JavaScript引擎提供的两个函数，不用自己部署
//resolve的作用是将promise的状态由pending变为resolved，并且将value作为参数传递出去
//reject的作用是将promise的状态由pending变为rejected，并且将error作为参数传递出去
promise.then(function(value),function(error))
//当promise状态改为resolved是执行第一个函数，改为reject则执行第二个函数    
```