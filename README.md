Скрипт полуавтоматически преобразует закодированные файлы Bitrix в читабельный формат.

# Инструкция

1. Открываем файл и копируем закодированную часть.
2. Приводим к правильному виду через https://www.cleancss.com/php-beautify/ (можно стандартными средствами IDE) и копируем в файл decode_file.php
3. В подготовленом файле сверху выделены один или 2 массива и функция. Начинаться они будут примерно так: 
  3. Массив:
  ```
  $GLOBALS['____153126584'] = array(base64_deco...
  ```
  3. Функция:
  ```
  if (!function_exists(__NAMESPACE__.'\\___1076931394')) { function ___1076931394($_367941623) {...
  ```

