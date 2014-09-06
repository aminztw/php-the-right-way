---
isChild: true
anchor:  namespaces
---

## 命名空間 {#namespaces_title}

如前所述，PHP 社群裡許多開發者已經開發了大量的程式碼。這意味著一個函式庫的的 PHP 程式碼可能使用了另外一個函式庫中相同的類別名稱。如果他們使用同一個命名空間，那將會產生衝突導致異常。

_命名空間_ 解決了這個問題。如 PHP 手冊裡所描述，命名空間類似作業系統中的目錄，兩個同名的文件可以共存於不同的目錄下。同理兩個同名的 PHP 類別可以在不同的 PHP 命名空間下共存，就這麼簡單。

因此把你的程式碼放在你的命名空間下就非常重要，避免其他開發者擔心與第三方函式庫衝突。

One recommended way to use namespaces is outlined in [PSR-4][psr4], which aims to provide a standard file, class and
namespace convention to allow plug-and-play code.

2014 年 10 月，PHP-FIG 稟棄了舊的自動加載標準：[PSR-0][psr0]。目前兩個 PSR-0 和 PSR-4 都能使用，但後者要求 PHP 5.3 以上的版本，所以許多 PHP 5.2 專案都還是使用 PSR-0。

如果你在新應用程式或套件中使用自動加載標準，應優先考慮使用 PSR-4。

* [閱讀命名空間][namespaces]
* [閱讀 PSR-0][psr0]
* [閱讀 PSR-4][psr4]


[namespaces]: http://php.net/language.namespaces
[psr0]: http://www.php-fig.org/psr/psr-0/
[psr4]: http://www.php-fig.org/psr/psr-4/
