## parseInt

["1", "2", "3"].map(parseInt)

[1, NaN, NaN] 

解析：parseInt (val, radix) ：兩個參數，val值，radix基數（就是多少進位轉換） 
`map` 能傳進回調函數 3參數 (element, index, array) 而題目中, map只傳入了回調函數--`parseInt`

```js
parseInt('1', 0); //0代表10進位 
parseInt('2', 1); //沒有1進位，不合法 
parseInt('3', 2); //2進位根本不會有3 

["1", "1", "11","5"].map(parseInt) //[1, NaN, 3, NaN]
```

> 在沒有指定基數，或者基數為 0 的情況下，JavaScript 作如下處理：
> * 如果字符串 string 以"0x"或者"0X"開頭, 則基數是16 (16進制).  
> * 如果字符串 string 以"0"開頭, 基數是8（八進制）或者10（十進制），那麼具體是哪個基數由實現環境決- 定。ECMAScript 5 規定使用10，但是並不是所有的瀏覽器都遵循這個規定。因此，永遠都要明確給出radix參數的值。  
> *  如果字符串 string 以其它任何值開頭，則基數是10 (十進制)。  
