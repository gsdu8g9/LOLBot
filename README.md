LOLBOT
========

Чат-бот для ВКонтакте

**ВНИМАНИЕ:**

Бот был написан с целью поближе изучить python, код местами может быть ужасающим

Разработкой бота я больше не занимаюсь, но с радостью приму ваши pull-request'ы и новые плагины

Работоспособность проверена исключительно на ОС семейства Linux, на Windows/Mac работоспособность не гарантируется (но не исключается)

Начальная настройка
========

1. Установить модуль vk_api: `pip install vk_api`
2. В файле `lolbot.py` заменить на 22 строке `login` и `password` на логин и пароль соответственно
3. Запустить: `python lolbot.py`

Смена префиксов
========

По умолчанию бот отзывается на пять префиксов: `lolbot`, `лолбот`, `лб`, `чб`, `кб`

Сменить их можно в `lolbot.py` на строке 75

Плагины
========

* Приветствие
* Список плагинов
* Музыка
* Случайное число
* Случайные сиськи :3 (берутся из первого попавшегося паблика по соответствующему запросу в вк)

Создание плагинов
========

В папке plugins лежит пример плагина под именем example.py, отвечающий строкой на команду `лб примерплагина`

Каждый плагин обязательно должен иметь три метода:

1. Конструктор (ему передается экземпляр vk_api)
2. `getkeys`, возвращающий слова-триггеры для вызова плагина
3. `call`, вызываемый по слову-триггеру из getkeys

Плагины размещаются в папке `plugins`. В случае наличия одинакового триггера в двух плагинах, будет использоваться последний загруженный

Плагины могут работать со всеми методами API вконтакте

Лицензия
========

Код распространяется под лицензией [WTFPL](https://ru.wikipedia.org/wiki/WTFPL) (Do What The Fuck You Want To Public License) версии 2
