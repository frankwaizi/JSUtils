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
