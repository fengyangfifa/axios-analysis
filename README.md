# axios-analysis

## axios.js

> 创建 Axios 实例，而且对实例使用 `bind` 函数包裹，返回一个函数。
> 
> 同时将 `Axios.prototype` 和 `Axios` 上的方法和属性 `extend` 到函数上。使得函数既可以 `axios({})` 也可以 `axios.request/get` 调用。
>
> 同时对函数添加创建 Axios 实例的工厂方法 `create`，使得可以使用 `axios.create`。
