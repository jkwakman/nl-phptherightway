---
anchor: code_style_guide
---

# Codeer stijlgids  {#code_style_guide_title}

De PHP community is een grote en zeer diverse gemeenschap, bestaande uit ontelbare libraries, frameworks en componenten. Het is
gebruikelijk voor PHP developers om een aantal van deze te kiezen en te combineren in één project. Het is hierbij belangrijk dat de PHP code
een gebruikelijke codeer stijl volgt (of zoveel mogelijk) om het voor andere developers mogelijk te maken om verschillende libraries te
kunnen combineren in hun projecten.

De [Framework Interop Group][fig] heeft een serie van codeer stijl aanbevelingen voorgesteld. Niet al deze aanbevelingen zijn
gerelateerd aan de codeer stijl maar die dat wel doen zijn [PSR-0][psr0], [PSR-1][psr1], [PSR-2][psr2] and [PSR-4][psr4].
Deze aanbevelingen zijn slechts een aantal regels waar projecten zoals Zend, Symfony, CakePHP, phpBB, AWS SDK, FuelPHP, Lithium, etc
aan willen voldoen. Je kunt deze regels ook volgen in je eigen projecten of gebruik maken van je eigen, persoonlijk stijl.

Idealiter schrijf je PHP code volgens een bekende standaard. Dit kan een combinatie zijn van PSR's of één van de codeer
standaarden van PEAR of Zend. Dit zorgt ervoor dat andere developers eenvoudig je code kunnen lezen en begrijpen. Applicaties
die gebruik maken van je code zijn op consistente wijze opgezet ook al maken ze gebruik van veel code van derde partijen.

* [Lees meer over PSR-0][psr0]
* [Lees meer over PSR-1][psr1]
* [Lees meer over PSR-2][psr2]
* [Lees meer over PSR-4][psr4]
* [Lees meer over PEAR Coding Standards][pear-cs]
* [Lees meer over Zend Coding Standards][zend-cs]
* [Lees meer over Symfony Coding Standards][symfony-cs]

Je kunt [PHP_CodeSniffer][phpcs] gebruiken om je code te valideren tegen één of meerdere aanbevelingen. Ook kun je gebruik
maken van plugins voor je tekst editor zoals [Sublime Text 2][st-cs] om realtime feedback te krijgen.

Gebruik Fabien Potencier zijn [PHP Coding Standards Fixer][phpcsfixer] om automatisch je code aan te passen zodat het conform de
regels van deze standaarden is. Dit scheelt je veel handmatige correcties.

De Engelse taal heeft de voorkeur bij benaming van alle symbolen en infrastructuur van je code. Commentaar mag worden geschreven
in elke taal die gemakkelijk te lezen is voor alle huidige en toekomstige partijen die werkzaamheden verrichten aan de code.

[fig]: http://www.php-fig.org/
[psr0]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-0.md
[psr1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[psr2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[psr4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md
[pear-cs]: http://pear.php.net/manual/en/standards.php
[zend-cs]: http://framework.zend.com/wiki/display/ZFDEV2/Coding+Standards
[symfony-cs]: http://symfony.com/doc/current/contributing/code/standards.html
[phpcs]: http://pear.php.net/package/PHP_CodeSniffer/
[st-cs]: https://github.com/benmatselby/sublime-phpcs
[phpcsfixer]: http://cs.sensiolabs.org/
