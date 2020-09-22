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

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/6-edit.png" width="40%">

#### Изменить файл настроек php, после перезапустить nginx и php:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/7-edit.png" width="40%">

#### Добавить index.php как один из вариантов индексной станицы (настройки nginx):

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/8-edit.png" width="40%">

#### Добавление репозитория базы данных:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/9-crop.png" width="40%">

#### Настройки базы данных:

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/10.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/11.png" width="40%">

<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/12-crop.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/13.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/14.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/15.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/16-crop.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/17.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/18-edit.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/19-crop.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/20-edit.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/22-edit.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/23.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/24.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/25-crop.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/26.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/27.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/28.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/29.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/30.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/31.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/32.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/33.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/34.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/35.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/36.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/37.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/38-crop.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/39.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/40-crop.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/41.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/42.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/43.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/44-crop.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/45-edit.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/46.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/47.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/48.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/49.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/50.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/51.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/52.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/53.png" width="40%">
<img src="https://github.com/MarinaSvistunova/eoes/blob/master/images/Moodle/54.png" width="40%">
