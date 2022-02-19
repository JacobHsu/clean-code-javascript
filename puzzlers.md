## parseInt

["1", "2", "3"].map(parseInt)

[1, NaN, NaN] 

解析：parseInt (val, radix) ：兩個參數，val值，radix基數（就是多少進位轉換） 
`map` 能傳進回調函數 3參數 (element, index, array) 

```js
parseInt('1', 0); //0代表10進位 
parseInt('2', 1); //沒有1進位，不合法 
parseInt('3', 2); //2進位根本不會有3 

["1", "1", "11","5"].map(parseInt) //[1, NaN, 3, NaN]
```
