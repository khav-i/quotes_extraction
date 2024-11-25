# Извлечение цитат

> simple data parsing from a celebrity quotes site

## что было сделано

В этой простой работе демонстрируется пример парсинга данных с сайта.

## откуда данные

Данные были получены с сайта с цитатами [quotes.toscrape.com](https://quotes.toscrape.com/).

## как это было сделано

Прежде чем парсить данные, конечно, нужно посетить сайт и ознакомиться с материалом, посмотреть вручную на HTML-код страницы, где мы сможем увидеть имена информативных полей и их теги. Также полезно будет подметить ссылки на страницы с дополнительной информацией, чтобы, если это нужно, спарсить данные также оттуда (для этого, например, была написана функция get_author_info в ноутбуке).

## выбор инструмента

### requests

Эта библиотека предоставляет довольно простой нтерфейс для выполнения HTTP-запросов. Она поддерживает все основные методы HTTP (GET, POST и др.), что делает её универсальным инструментом для работы с веб-API и страницами.

### BeautifulSoup

Специально разработан для парсинга HTML и XML документов. Легко извлекает данные из HTML-структуры, поддерживает различные методы поиска элементов (по тегам, классам, атрибутам и т.д.).

## результат

```json
{
    "052f98ba-fdc3-4651-8471-61a853996aed":
        "text": "“I have not failed. I've just found 10,000 ways that won't work.”",
        "author": "Thomas A. Edison",
        "author_info":
            "birth_date": "February 11, 1847",
            "birth_place": "in Milan, Ohio, The United States",
            "description": "Thomas Alva Edison was an American inventor, scientist and businessman who developed many devices that greatly influenced life around the world, including the phonograph, the motion picture camera, and a long-lasting, practical electric light bulb. Dubbed \"The Wizard of Menlo Park\" (now Edison, New Jersey) by a newspaper reporter, he was one of the first inventors to apply the principles of mass production and large teamwork to the process of invention, and therefore is often credited with the creation of the first industrial research laboratory.Edison is considered one of the most prolific inventors in history, holding 1,093 U.S. patents in his name, as well as many patents in the United Kingdom, France and Germany. He is credited with numerous inventions that contributed to mass communication and, in particular, telecommunications. His advanced work in these fields was an outgrowth of his early career as a telegraph operator. Edison originated the concept and implementation of electric-power generation and distribution to homes, businesses, and factories – a crucial development in the modern industrialized world. His first power station was on Manhattan Island, New York."
        },
        "tags": [
            "edison",
            "failure",
            "inspirational",
            "paraphrased"
        ]
    }, ...
}
```
