---
anchor: code_style_guide
---

# 程式碼風格指南 {#code_style_guide_title}

PHP 社群百花齊放，擁有大量的函式庫、框架和元件。PHP 開發者通常會選擇多個外部套件並將它們整合進單一專案中。因此 PHP 程式碼遵循（盡可能接近）一個共通的程式碼風格就會非常重要，這讓開發者可以輕鬆地將多個外部套件整合在自己的專案當中。

[Framework Interop Group][fig] 提出並通過了一系列的風格建議。其中有部分是關於程式碼風格的，即 [PSR-0][psr0]、[PSR-1][psr1]、[PSR-2][psr2] 和 [PSR-4][psr4]。這些建議是由一系列專案像是 Drupal, Zend, Symfony, Laravel, CakePHP, phpBB, AWS SDK,
FuelPHP, Lithium 所採用。你可以在您的專案中使用或者是繼續使用您自己的風格。

理想狀況下，你應該遵循一個已知的標準來撰寫 PHP 程式碼。可能是 PSR 的組合或者是 PEAR 或 Zend 程式碼標準的其中一個。這代表其他開發者能夠方便的閱讀與使用你的程式碼，且使用這些套件的應用程式能夠平順地與許多第三方套件一起使用。

* [閱讀 PSR-0][psr0]
* [閱讀 PSR-1][psr1]
* [閱讀 PSR-2][psr2]
* [閱讀 PSR-4][psr4]
* [閱讀 PEAR 編碼準則][pear-cs]
* [閱讀 Symfony 編碼準則][symfony-cs]

你可以使用 [PHP_CodeSniffer][phpcs] 來檢查程式碼是否符合這些準則，而文字編輯器 [Sublime Text 2][st-cs] 的套件也可以提供即時檢查。

可以使用以下的工具自動修正你的程式碼語法：

- One is the [PHP Coding Standards Fixer][phpcsfixer] which has a very well tested codebase.
- Also, the [PHP Code Beautifier and Fixer][phpcbf] tool which is included with PHP_CodeSniffer can be used to adjust your code accordingly.

And you can run phpcs manually from shell:

    phpcs -sw --standard=PSR2 file.php

It will show errors and describe how to fix them.
It can also be helpful to include this command in a git hook.
That way, branches which contain violations against the chosen standard cannot enter the repository until those
violations have been fixed.

If you have PHP_CodeSniffer, then you can fix the code layout problems reported by it, automatically, with the
[PHP Code Beautifier and Fixer][phpcbf].

    phpcbf -w --standard=PSR2 file.php

Another option is to use the [PHP Coding Standards Fixer][phpcsfixer].
It will show which kind of errors the code structure had before it fixed them.

    php-cs-fixer fix -v --level=psr2 file.php

English is preferred for all symbol names and code infrastructure. Comments may be written in any language easily
readable by all current and future parties who may be working on the codebase.


[fig]: http://www.php-fig.org/
[psr0]: http://www.php-fig.org/psr/psr-0/
[psr1]: http://www.php-fig.org/psr/psr-1/
[psr2]: http://www.php-fig.org/psr/psr-2/
[psr4]: http://www.php-fig.org/psr/psr-4/
[pear-cs]: http://pear.php.net/manual/en/standards.php
[symfony-cs]: http://symfony.com/doc/current/contributing/code/standards.html
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[phpcbf]: https://github.com/squizlabs/PHP_CodeSniffer/wiki/Fixing-Errors-Automatically
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: http://cs.sensiolabs.org/
