# Субъекты с муниципальными образованиями России в формате JSON

Наборы данных появилась при поддержке желания облегчить разработку. Иногда сталкиваешься с необходимостью создавать список субъектов России, но найти таковой, не заключенный в таблицу, без ссылок и другого "мусора" достаточно сложно. А список муниципалитетов - тем более.

В данном файле собраны все субъекты с муниципальными образованиями России.

Всего 85 субъектов, 2345 муниципальных образований.

Данные взяты из Википедии: [Список муниципальных районов и городских округов России](https://ru.wikipedia.org/wiki/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%D0%BC%D1%83%D0%BD%D0%B8%D1%86%D0%B8%D0%BF%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D1%85_%D1%80%D0%B0%D0%B9%D0%BE%D0%BD%D0%BE%D0%B2_%D0%B8_%D0%B3%D0%BE%D1%80%D0%BE%D0%B4%D1%81%D0%BA%D0%B8%D1%85_%D0%BE%D0%BA%D1%80%D1%83%D0%B3%D0%BE%D0%B2_%D0%A0%D0%BE%D1%81%D1%81%D0%B8%D0%B8).

## Федеральные округа, субъекты и муниципальные образования

Субъекты РФ сгруппированы по 8-ми федеральным округам, представляет собой наиболее полную административно-территориальную базу. Все хранится в файле **rf_fo_subjects_municipals.json**.

Схема файла несколько иная, дабы можно было одной функцией производить поиск в текущем элементе массива:
```
{
    "name": string,   // Название федерального округа
    "items": array [  // Массив субъектов РФ данного округа
        {
            "name": string, // Название субъекта РФ
            "items": array  // Массив с названиями муниципальных образований
        }
    ]
}
```


## Субъекты и муниципальные образования

Субъекты и муниципальные образования содержатся в файле **rf_subjects_municipals.json**.

Схема файла:

```
{
    "subject": string,   // Название субъекта РФ
    "municipals": array  // Массив с названиями муниципальных образований
}
```


## Субъекты РФ

Только субъекты РФ содержатся в файле **rf_subjects.json**. Это простой массив, каждый элемент которого - простая строка, содержащая наименование субъекта.
