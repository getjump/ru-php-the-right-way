---
title: Дата и время
isChild: true
---

## Дата и время

PHP имеет встроенный класс с названием DateTime, он поможет вам, когда вам нужно прочесть, записать, сравнить или посчитать дату или время.
Так-же в PHP много функций, связанных с датой и временем, помимо класса DateTime, но класс предоставляет хороший объектно-ориентированный интерфейс для решения большинства задач.
Он может обрабатывать временные зоны, но это за пределами этого короткого введения.

Для начала работы с DateTime, сконвертируйте "сырую" строку даты и времени в объект с помощью фабричного метода `createFromFormat()` или выполните `new \DateTime`, чтобы получить текущую дату и время. Используйте метод `format()` для конвертирования DateTime обратно в строку для вывода.
 
{% highlight php %}
<?php
$raw = '22. 11. 1968';
$start = \DateTime::createFromFormat('d. m. Y', $raw);

echo "Start date: " . $start->format('m/d/Y') . "\n";
{% endhighlight %}

Математика с DateTime возможна с использованием класса DateInterval. У класса DateTime есть методы `add()` и `sub()`, которые принимают DateInterval, как аргумент. Не пишите код, который ожидает одинаковое число секунд каждый день, перевод часов и смена часовых поясов разрушат это предположение. Вместо этого используйте интервалы дат. Для расчета разницы между датами используйте метод `diff()`. Он вернет новый объект DateInterval, который очень легко отобразить. 

{% highlight php %}
<?php
// Создаем копию $start и добавляем 1 месяц и 6 дней.
$end = clone $start;
$end->add(new \DateInterval('P1M6D'));

$diff = $end->diff($start);
echo "Difference: " . $diff->format('%m месяц, %d дней (всего: %a дней)') . "\n";
// Разница: 1 месяц, 6 дней (всего: 37 дней)
{% endhighlight %}

С объектами DateTime, вы можете использовать стандартные методы сравнения:
{% highlight php %}
<?php
if($start < $end) {
    echo "Start перед End!\n";
}
{% endhighlight %}

И последний пример, для демонстрации класса DatePeriod. Он используется для перебора повторяющихся событий. Он может принимать два объекта DateTime, начало и конец, и интервал для которого он вернет все события между ними.

{% highlight php %}
<?php
// вывод всех четвергов между $start и $end
$periodInterval = \DateInterval::createFromDateString('first thursday');
$periodIterator = new \DatePeriod($start, $periodInterval, $end, \DatePeriod::EXCLUDE_START_DATE);
foreach($periodIterator as $date)
{
    // вывод каждой даты в периоде
    echo $date->format('m/d/Y') . " ";
}
{% endhighlight %}

* [Подробнее о DateTime][datetime]
* [Подробнее о DateInterval][dateinterval]
* [Подробнее о DatePeriod][dateperiod]
* [Подробнее о форматировании даты][dateformat] (принятый вариант формата строки даты)

[datetime]: http://www.php.net/manual/class.datetime.php
[dateinterval]: http://www.php.net/manual/class.dateinterval.php
[dateperiod]: http://www.php.net/manual/class.dateperiod.php
[dateformat]: http://www.php.net/manual/function.date.php
