# Task_1_ot_01_10_2026
Bitrix: курс контент-менеджера https://dev.1c-bitrix.ru/learning/course/index.php?COURSE_ID=34

## Сдать тесты в кусе контент-менеджера
![Финальный тест](./docs/Final_test_result.png)

- Установить битрикс и начать разбираться в админке

Битрикс развернут в Docker Desktop.

При установке возникла проблема: ошибка при скачивании архива. 
Которая была решена следующим образом.

6. Скачайте установщик bitrixsetup.php (доплненный)

```cmd
   # войдите внутрь контейнера под пользователем bitrix
   docker compose exec --user=bitrix php sh
   
   # перейдите в папку сайта
   cd /opt/www/
   
   # скачайте файл для установки продукта
   wget https://www.1c-bitrix.ru/download/scripts/bitrixsetup.php
   
   # скачать архив
   wget https://www.1c-bitrix.ru/download/business_encode.tar.gz
```

7. Запустите установку демоверсии
Откройте браузер и перейдите по адресу:
```
   http://localhost:8588/bitrixsetup.php?test=1
```

Благодаря параметру test скрипт обнаружит, что архив уже скачан и предложет распаковать его.

## Сделать шаблон компонента news.list

