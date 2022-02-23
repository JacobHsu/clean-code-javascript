## Object.prototype.toString.call()

[Object.prototype.toString()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/toString)  
`toString()` 是 Object 的原型方法，調用該方法，默認返回當前對象的 [[Class]] 。這是一個內部屬性，其格式為 [object Xxx] ，其中 Xxx 就是對象的類型。

對於 Object 對象，直接調用 toString() 就能返回 `[object Object]` 。
而對於其他對象，則需要通過 call / apply 來調用才能返回正確的類型信息。

```js
Object.prototype.toString.call('') ;   // [object String]
Object.prototype.toString.call(1) ;    // [object Number]
Object.prototype.toString.call(true) ; // [object Boolean]
Object.prototype.toString.call(Symbol()); //[object Symbol]
Object.prototype.toString.call(undefined) ; // [object Undefined]
Object.prototype.toString.call(null) ; // [object Null]
Object.prototype.toString.call(new Function()) ; // [object Function]
Object.prototype.toString.call(new Date()) ; // [object Date]
Object.prototype.toString.call([]) ; // [object Array]
Object.prototype.toString.call(new RegExp()) ; // [object RegExp]
Object.prototype.toString.call(new Error()) ; // [object Error]
Object.prototype.toString.call(document) ; // [object HTMLDocument]
Object.prototype.toString.call(window) ; //[object global] window 是全局對象 global 的引用
```
