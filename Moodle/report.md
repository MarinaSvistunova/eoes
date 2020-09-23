## Тема 2.
### Спроектируйте и осуществите развёртывание LMS Moodle на базе виртуального хостинга и системы управления контейнерами docker-compose

#### Для этого:
  - Проанализируйте техническую документацию по docker-compose (https://docs.docker.com/compose/);
  - Сверьтесь с инструкцией: https://kodaktor.ru/moodle-dump-compose.pdf
___

## Вариант 1

#### Создание сервера на vscale:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/1.png" width="30%">

#### Установка nginx, проверка текущей версии:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/2-crop.png" width="40%">

#### Проверка статуса nginx:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/3-crop.png" width="80%">

#### Сервер подключен к домену m.marinasv.ru. По этому адресу выдается заглушка nginx сразу после его установки:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/4.png" width="60%">

#### Установка php7.2-fpm (fpm - серверный вариант реализации интерпретатора, который соединяется с веб-сервером,  в данном случае - nginx), проверка статуса :

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/5-crop.png" width="100%">

#### Для связи php сценария и веб-сервера необходимо изменить файл настроек nginx:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/6-edit.png" width="60%">

#### Изменить файл настроек php, после перезапустить nginx и php:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/7-edit.png" width="60%">

#### Добавить index.php как один из вариантов индексной станицы (настройки nginx):

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/8-edit.png" width="60%">

#### Добавление репозитория базы данных:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/9-crop.png" width="60%">

#### Настройки базы данных:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/10.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/11.png" width="60%">

#### Поиск пакета mysql:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/12-crop.png" width="60%">

#### Установка пароля пользователя root:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/13.png" width="60%">

#### Конфигурация безопасных настроек mysql:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/14.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/15.png" width="60%">

#### Создание базы данных moodle:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/16-crop.png" width="60%">

#### Получение сертификата ssl:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/17.png" width="60%">

#### Изменение файла настроек nginx. Добавление имени сервера, порта 443 и пути к сертификату и ключу:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/18-edit.png" width="60%">

#### Очистка папки сайта и скачивание zip-архива с moodle:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/19-crop.png" width="60%">

#### Изменение настроек nginx, добавление регулярных выражений для описания того, каким образом происходит передача данных:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/20-edit.png" width="60%">

#### Начало установки moodle при переходе на страницу m.marinasv.ru/install.php (на скриншоте видно, что соединение защищено):

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/22-edit.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/23.png" width="60%">

#### Ошибка установки:
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/24.png" width="60%">

#### Для устранения ошибки, указанной выше, необходимо в папке сайта вручную создать папку, поменять владельца и добавить право записи в эту папку:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/25-crop.png" width="60%">

#### Продолжение установки:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/26.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/27.png" width="60%">

#### Создать config.php в /var/www/html/moodle (текст файла будет сгенерирован moodle):

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/28.png" width="60%">

#### Продолжение установки:
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/29.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/30.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/31.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/32.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/33.png" width="60%">

#### Moodle развернут. Завершение регистрации:
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/34.png" width="60%">

#### Создание нового пользователя:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/35.png" width="60%">

#### Созданы 2 пользователя (администратор и преподаватель). Moodle работает:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/36.png" width="60%">


## Вариант 2

#### Создание сервера на vscale:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/37.png" width="60%">

#### Проверка версии docker-compose.Создание папки сайта и скачивание в нее файла docker-compose.yml:
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/38-crop.png" width="60%">

#### Файл docker-compose.yml:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/39.png" width="60%">

#### Скачивание дамба базы данных moodle:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/40-crop.png" width="60%">

#### Сборка командой "docker-compose up":

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/41.png" width="60%">

#### По адресу c.marinasv.ru доступна заглушка Apache2 Ubuntu. Есть ssl сертификат:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/42.png" width="60%">

#### Для установки moodle необходимо перейти по адресу c.marinasv.ru/moodle. Возникает следующая ошибка:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/43.png" width="80%">

#### Попытка подключиться к контейнеру, который отвечает за nginx:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/44-crop.png" width="100%">

#### В файле config.php внести директиву, которая включает проксирование https трафика:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/45-edit.png" width="80%">

#### После внесения директивы ошибка исчезает:
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/46.png" width="60%">

#### Установка аналогичная предыдущему варианту:
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/47.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/48.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/49.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/50.png" width="60%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/51.png" width="60%">

#### Создание категории для курсов:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/52.png" width="60%">

#### Создание курса:
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/53.png" width="60%">

#### Курс создан. Moodle работает:
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/54.png" width="60%">
