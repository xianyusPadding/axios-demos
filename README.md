### axios-demos这是关于axios的一般使用
> demo的相关依赖 bootstrap.css（为了美观）、vue.min.js和axios.min.js

![](https://github.com/xianyusPadding/axios-demos/blob/master/about/style.jpg)
<br>
#### axios的相关使用：
* axios.get(url[, config]).then(res).catch(error)
* axios.post(url[, data[, config]]).then(res).catch(error)
* axios({url,data/params,config}).then(res).catch(error)
![](https://github.com/xianyusPadding/axios-demos/blob/master/about/http.jpg)
<br>

#### 具体使用可参考源码（也比较简单）

#### axios的全局拦截器（可以进行一些loading处理）：
```javascript
axios.interceptors.request.use( config => {
  console.log('request init.')
  //loading...
  return config
})
axios.interceptors.response.use( response => {
  console.log('response init.')
  //loading...
  return response
})
```

#### 遇到的问题：
在iis服务器上post请求会发出405 (Method Not Allowed)，待解决
