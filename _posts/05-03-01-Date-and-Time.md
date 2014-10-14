---
isChild: true
anchor: date_and_time
---

## Datum en tijd {#date_and_time_title}

PHP heeft een klasse genaamd DateTime om je te helpen met bij lezen, schrijven, vergelijken of berekenen van een datum of tijd. 
Naast DateTime zijn er nog vele andere datum en tijd gerelateerde functies in PHP. Echter biedt DateTime een nette objectgeoriënteerde
interface voor de meest gebruikelijke toepassingen zoals bv het omgaan tijdzones. Dit valt echter buiten de scope van deze beknopte introductie.

Om gebruik te maken van DateTime dien je een datum / tijd string te converteren naar een object middels `createFromFormat()` factory functie of 
maak gebruik van `new \DateTime` om de huidige datum / tijd te gebruiken. Gebruik `format()` functie om DateTime terug te converteren naar een string om te
gebruiken voor output.

{% highlight php %}
<?php
$raw = '22. 11. 1968';
$start = \DateTime::createFromFormat('d. m. Y', $raw);

echo 'Start date: ' . $start->format('m/d/Y') . "\n";
{% endhighlight %}

Berekening maken met DateTime is mogelijk met de DateInterval klasse. DateTime kent functies zoals `add()` en `sub()` die
een DateInterval als een argument accepteren. Schrijf geen code waarbij exact hetzelfde aantal seconde voor iedere dag wordt verwacht
aangezien zomertijd en tijdzone verschillen deze aanname ondermijnen. Maak daarom gebruik van DateInterval. Om het verschil
te berekenen kun je gebruik maken van de `diff()` functie. Deze retourneert een nieuwe DateInterval die je weer eenvoudig kunt weergeven. 

{% highlight php %}
<?php
// Make een kopie van $start en voeg één maand en 6 dagen toe
$end = clone $start;
$end->add(new \DateInterval('P1M6D'));

$diff = $end->diff($start);
echo 'Difference: ' . $diff->format('%m month, %d days (total: %a days)') . "\n";
// Verschil: 1 maand, 6 datgen (totaal: 37 dagen)
{% endhighlight %}

Bij DateTime objecten kun je standaard vergelijkingen toepassen:
{% highlight php %}
<?php
if ($start < $end) {
    echo "Start is before end!\n";
}
{% endhighlight %}

Ter afsluiting nog één voorbeeld om de DatePeriod klasse te demonstreren. Het kan worden gebruikt om te intereren over terugkerende
gebeurtenissen. Je kunt hierbij twee DateTime objecten met een start en eind datum gebruiken en alle tussenliggende gebeurtenissen retourneren.

{% highlight php %}
<?php
// output alle donderdagen tussen $start en $end
$periodInterval = \DateInterval::createFromDateString('first thursday');
$periodIterator = new \DatePeriod($start, $periodInterval, $end, \DatePeriod::EXCLUDE_START_DATE);
foreach ($periodIterator as $date) {
    // output iedere datum binnen deze periode
    echo $date->format('m/d/Y') . ' ';
}
{% endhighlight %}

* [Lees meer over DateTime][datetime]
* [Lees meer over datum opmaak][dateformat] (geaccepteerde datum opmaak)

[datetime]: http://www.php.net/manual/book.datetime.php
[dateformat]: http://www.php.net/manual/function.date.php
