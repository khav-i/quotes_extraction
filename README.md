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

> [
    {
        "text": "“The world as we have created it is a process of our thinking. It cannot be changed without changing our thinking.”",
        "author": "Albert Einstein",
        "author_info": {
            "birth_date": "March 14, 1879",
            "birth_place": "in Ulm, Germany",
            "description": "In 1879, Albert Einstein was born in Ulm, Germany. He completed his Ph.D. at the University of Zurich by 1909. His 1905 paper explaining the photoelectric effect, the basis of electronics, earned him the Nobel Prize in 1921. His first paper on Special Relativity Theory, also published in 1905, changed the world. After the rise of the Nazi party, Einstein made Princeton his permanent home, becoming a U.S. citizen in 1940. Einstein, a pacifist during World War I, stayed a firm proponent of social justice and responsibility. He chaired the Emergency Committee of Atomic Scientists, which organized to alert the public to the dangers of atomic warfare.At a symposium, he advised: \"In their struggle for the ethical good, teachers of religion must have the stature to give up the doctrine of a personal God, that is, give up that source of fear and hope which in the past placed such vast power in the hands of priests. In their labors they will have to avail themselves of those forces which are capable of cultivating the Good, the True, and the Beautiful in humanity itself. This is, to be sure a more difficult but an incomparably more worthy task . . . \" (\"Science, Philosophy and Religion, A Symposium,\" published by the Conference on Science, Philosophy and Religion in their Relation to the Democratic Way of Life, Inc., New York, 1941). In a letter to philosopher Eric Gutkind, dated Jan. 3, 1954, Einstein stated: \"The word god is for me nothing more than the expression and product of human weaknesses, the Bible a collection of honorable, but still primitive legends which are nevertheless pretty childish. No interpretation no matter how subtle can (for me) change this,\" (The Guardian, \"Childish superstition: Einstein's letter makes view of religion relatively clear,\" by James Randerson, May 13, 2008). D. 1955.While best known for his mass–energy equivalence formula E = mc2 (which has been dubbed \"the world's most famous equation\"), he received the 1921 Nobel Prize in Physics \"for his services to theoretical physics, and especially for his discovery of the law of the photoelectric effect\". The latter was pivotal in establishing quantum theory.Einstein thought that Newtonion mechanics was no longer enough to reconcile the laws of classical mechanics with the laws of the electromagnetic field. This led to the development of his special theory of relativity. He realized, however, that the principle of relativity could also be extended to gravitational fields, and with his subsequent theory of gravitation in 1916, he published a paper on the general theory of relativity. He continued to deal with problems of statistical mechanics and quantum theory, which led to his explanations of particle theory and the motion of molecules. He also investigated the thermal properties of light which laid the foundation of the photon theory of light.He was visiting the United States when Adolf Hitler came to power in 1933 and did not go back to Germany. On the eve of World War II, he endorsed a letter to President Franklin D. Roosevelt alerting him to the potential development of \"extremely powerful bombs of a new type\" and recommending that the U.S. begin similar research. This eventually led to what would become the Manhattan Project. Einstein supported defending the Allied forces, but largely denounced the idea of using the newly discovered nuclear fission as a weapon. Later, with Bertrand Russell, Einstein signed the Russell–Einstein Manifesto, which highlighted the danger of nuclear weapons. Einstein was affiliated with the Institute for Advanced Study in Princeton, New Jersey, until his death in 1955.His great intellectual achievements and originality have made the word \"Einstein\" synonymous with genius.More: http://en.wikipedia.org/wiki/Albert_E...http://www.nobelprize.org/nobel_prize..."
        }
    }, ...
]
