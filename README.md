# axios-analysis

## axios.js

> 创建 Axios 实例，而且对实例使用 `bind` 函数包裹，返回一个函数。
>
> 同时将 `Axios.prototype` 和 `Axios` 上的方法和属性 `extend` 到函数上。使得函数既可以 `axios({})` 也可以 `axios.request/get` 调用。
>
> 同时对函数添加创建 Axios 实例的工厂方法 `create`，使得可以使用 `axios.create`。

## utils.js

> 工具函数集合

## Axios.js

> Axios 构造函数的具体实现。
> > request: 合并 config、执行拦截器、调用发出请求函数
> > > 请求拦截器
> > > > 异步请求拦截器(默认方案)
> > > >
> > > > 同步请求拦截器(需要自己开启)
> > > >
> > > > 因为默认是异步请求拦截器。等待主线程执行完后，才会执行微任务去发送 ajax 请求。
> > >
> > > 响应拦截器
>
> > getUri，根据配置计算出请求的完整 uri
>
> > 绑定 delete、get、head、options、post、put、patch 等方法
> >
> > 同时还有 postForm、putForm、patchForm 等方法

## InterceptorManager.js

> 拦截器构造函数实现
>
> 采用数组的存储 拦截器，同时对请求拦截器支持 runWhen 和 synchronous 参数
> use 添加拦截器
>
> eject 清除一个拦截器
>
> clear 清空所有拦截器
>
> forEach 遍历拦截器
