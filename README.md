Скрипт полуавтоматически преобразует закодированные файлы Bitrix в читабельный формат.

# Инструкция

1. Открываем файл и копируем закодированную часть.
2. Приводим к правильному виду через https://www.cleancss.com/php-beautify/ (можно стандартными средствами IDE) и копируем в файл decode_file.php
3. В подготовленом файле сверху находятся один или 2 массива и функция. Вырезаем их и вставляем в файл variables.php. Начинаться они будут примерно так: 
  * Массив: `$GLOBALS['____153126584'] = array(base64_deco...`
  * Функция: `if (!function_exists(__NAMESPACE__.'\\___1076931394')) { function ___1076931394($_367941623) {...`
4. Названиея массива копируем в 'GLOBAL_VARIABLES' в index.php а на звания функций в 'GLOBAL_FUNCTIONS' они обозначены тремя нижними подчеркиваниями.
5. Запускаем скрипт из консоли `php index.php`
6. Появится файл encode_file.php в нем будет читабельный код. Injoy :)

### Пример строки

Было:
`$_236203417 = $GLOBALS[___1076931394(0)]->Query(___1076931394(1), true);`

Стало:
`$_236203417 = $GLOBALS['DB']->Query('SELECT VALUE FROM b_option WHERE NAME='~PARAM_MAX_USERS' AND MODULE_ID='main' AND SITE_ID IS NULL', true);`
