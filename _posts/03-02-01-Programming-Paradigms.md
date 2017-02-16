---
isChild: true
anchor:  programming_paradigms
---

## 編程範式 {#programming_paradigms_title}

PHP 是一個彈性的動態語言，支援多種編程技術。這幾年一直不斷的進化，重要的里程碑包含 PHP 5.0 (2004) 增加完善的物件導向模型，PHP 5.3 (2009) 增加匿名函式與命名空間以及 PHP 5.4 (2012) 增加的特徵（traits）。

### 物件導向編程

PHP 擁有完整的物件導向編程的特性，包含支援類別、抽象類別、介面、繼承、構造函數、克隆和異常等。

* [閱讀 PHP 物件導向][oop]
* [閱讀 Traits][traits]

### 函式編程

PHP 支持第一類函式（first-class function），即函式可以被賦值給一個變數，包括使用者自定義或者是內建函式，然後動態調用它。函式可以作為參數傳遞給其他函式（稱作高階函數），也可以作為函數回傳值回傳。

PHP 支援遞迴，也就是函式可以呼叫自己，但多數 PHP 程式碼較常使用迭代。

自從 PHP 5.3 (2009) 之後開始引入支援閉包匿名函式。

PHP 5.4 支援將閉包綁定到物件的作用域中，並改善其可調用性，如此即可在大部分狀況下使用匿名函式取代一般函式。

* 學習更多 [PHP 函式編程](/pages/Functional-Programming.html)
* [閱讀匿名函式][anonymous-functions]
* [閱讀閉包類別][closure-class]
* [更多關於 Closures RFC][closures-rfc]
* [閱讀 Callables][callables]
* [閱讀動態調用函式 `call_user_func_array`][call-user-func-array]

### 元編程

PHP 通過反射 API 和魔術方法機制，支援多種方式的元編程。開發者通過魔術方法，如 `__get()`, `__set()`, `__clone()`, `__toString()`, `__invoke()`, 等等，可以改變類別的行為。Ruby 開發者經常說 PHP 沒有 `method_missing` 方法，實際上通過 `__call()` 和 `__callStatic()` 就可以完成相同的功能。

* [閱讀魔術方法][magic-methods]
* [閱讀反射][reflection]
* [Read about Overloading][overloading]


[oop]: http://php.net/language.oop5
[traits]: http://php.net/language.oop5.traits
[anonymous-functions]: http://php.net/functions.anonymous
[closure-class]: http://php.net/class.closure
[closures-rfc]: https://wiki.php.net/rfc/closures
[callables]: http://php.net/language.types.callable
[call-user-func-array]: http://php.net/function.call-user-func-array
[magic-methods]: http://php.net/language.oop5.magic
[reflection]: http://php.net/intro.reflection
[overloading]: http://php.net/language.oop5.overloading

