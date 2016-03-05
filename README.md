# JSUtils
JS 实用小脚本汇总

### 1、JSON 转 queryString
```javascript
let query = options.query || {};
let queryString = '?';
for(let i in query) {
  queryString = queryString + i +'='+ query[i] +'&';
}

queryString = queryString.slice(0, -1);
```

### 2、金额格式化
```javascript
let sign = (num == ( num = Math.abs(num)));
num = Math.floor(num * 100 + 0.50000000001);
let cents = num % 100;
num = Math.floor(num / 100).toString();
if(cents < 10)
  cents = "0" + cents;
for(var i = 0; i < Math.floor((num.length - (1 + i)) / 3); i++)
  num = num.substring(0,num.length - (4 * i + 3)) + ',' + num.substring(num.length - (4 * i + 3));
if(point){
  return (((sign)?'':'-') + num);
}else{
  if(cents == "00"){
    return (((sign)?'':'-') + num);
  }else{
    return (((sign)?'':'-') + num + '.' + cents);
  }
}
```
