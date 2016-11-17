# Als/Dtf

Класс, который предоставляет некоторые дополнительные возможности по оперированию с объектами типа «дата».


## Installation

```bash
$ composer require als/dtf
```


## Basic Usage

Примеры вызова (методы класса вызываются статически).

Напечатать время now в человеческом формате по русски:
```ruby
^Als/Dtf:format[%T %d %h %Y]
```

Напечатать время now в человеческом формате по английски:
```ruby
^Als/Dtf:format[%T %d %h %Y;;${Als/Dtf:ei-locale}]
```

Напечатать дату рождения из переменной `$bithday` в формате %d/%m/%Y:
```ruby
^dtf:format[%d/%m/%Y;$bithday]
```

Описаны методы:
```ruby
###################################
# @create[date]				из строки/даты конструирует объект типа date
# @format[fmt;date;locale]		выводит полученную date, используя форматную строку
# @last-day[date]			возвращает дату последнего дня заданного[текущего] месяца
# @from822[string]			создает дату из переданной строки-даты в формате RFC822
# @to822[date;timezone]			сдвигает дату из текущей TZ в указанную TZ и выводит её в виде строки в формате RFC822
# @setLocale[locale]			задает новое значение locale, возвращая старое
# @resetLocale[]			сбрасывает locale в default
###################################
```


## References

- Bugs and feature request are tracked on [GitHub](https://github.com/parser3/als.sql/issues)
