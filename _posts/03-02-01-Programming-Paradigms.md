---
isChild: true
anchor: programming_paradigms
---

## Programmeerparadigma's {#programming_paradigms_title}

PHP is een flexibele, dynamische taal en ondersteund een grote scala aan programmeertechnieken. Het is sterk geëvolueerd in
de jaren met ondersteuning van een solide objectgeoriënteerd model in PHP 5.0 (2004), anonieme functies en namespaces in
PHP 5.3 (2009) en traits in PHP 5.4 (2012).

### Objectgeoriënteerd programmeren

PHP heeft een uitgebreide set van objectgeoriënteerde features met ondersteuring voor klassen, abstracte klassen, interfaces,
overerving (inheritance), constructors, cloning, excepties enz.

* [Lees meer over objectgeoriënteerd programmeren in PHP][oop]
* [Lees meer traits][traits]

### Functioneel programmeren

PHP ondersteund first-class functies. Hierbij kun je een functie toekennen aan een variabele. Zowel PHP functies als
eigen functies kunnen dynamisch worden aangeroepen middels een variabele. Functies kunnen als argument worden doorgegeven
aan andere functies (ook wel Higher-order functions genoemd) en functies kunnen andere functies als resultaat geven.

Recursie (een feature waarbij een functie zichzelf kan aanroepen) wordt ook ondersteund door PHP, alhoewel er meestal gebruik
wordt gemaakt van iteratie.

De nieuwe anonieme functies (met ondersteuning van closures) zijn aanwezig sinds PHP 5.3 (2009).

PHP 5.4 introduceerde de mogelijkheid om closures aan een object zijn scope te verbinden en verbeterde ondersteuning voor
'callables' zodat deze in bijna alle gevallen in combinatie met anonieme functies gebruikt kunnen worden.

* [Lees meer over [Functioneel programmeren in PHP](/pages/Functional-Programming.html)
* [Lees meer over anonieme functies][anonymous-functions]
* [Lees meer over closure klassen][closure-class]
* [Lees meer over closure RFC][closures-rfc]
* [Lees meer over callables][callables]
* [Lees meer over het dynamisch aanroepen van functies middels `call_user_func_array`][call-user-func-array]

### Meta programmeren

PHP ondersteund verschillende vormen van meta programmeren middels mechanismen zoals de reflectie API en 'Magic Methods'. Er
zijn veel Magic Methods beschikbaar zoals `__get()`, `__set()`, `__clone()`, `__toString()`, `__invoke()` etc. Hiermee
kunnen developers inhaken op het gedrag van een klasse. Ruby developers klagen vaak omtrent het feit dat in PHP de functie
'method_missing' ontbreekt maar deze functionaliteit is wel degelijk beschikbaar middels `__call()` en `__callStatic()`.

* [Lees meer over Magic Methods][magic-methods]
* [Lees meer over relectie][reflection]

[namespaces]: http://php.net/manual/en/language.namespaces.php
[overloading]: http://php.net/manual/en/language.oop5.overloading.php
[oop]: http://www.php.net/manual/en/language.oop5.php
[anonymous-functions]: http://www.php.net/manual/en/functions.anonymous.php
[closure-class]: http://php.net/manual/en/class.closure.php
[callables]: http://php.net/manual/en/language.types.callable.php
[magic-methods]: http://php.net/manual/en/language.oop5.magic.php
[reflection]: http://www.php.net/manual/en/intro.reflection.php
[traits]: http://www.php.net/traits
[call-user-func-array]: http://php.net/manual/en/function.call-user-func-array.php
[closures-rfc]: https://wiki.php.net/rfc/closures
