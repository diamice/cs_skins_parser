# Парсер для сайта со скинами lis-skins

Этот проект предназначен для сбора данных о скинах с сайта [lis-skins.ru](https://lis-skins.ru) с использованием Python.
В проекте используется библиотека `selenium` для получения HTML-кода страницы и `BeautifulSoup` для парсинга данных.

## Функциональность

1. **Получение HTML-кода страницы:** Скрипт использует `selenium` для загрузки страницы и получения её исходного кода.
2. **Парсинг данных:** Используя `BeautifulSoup`, извлекаются данные о скинах, такие как название, цена, разница в цене
   с Steam, информация о качестве и ссылке на товар.
3. **Сохранение данных:** Собранные данные сохраняются в формате JSON и HTML для последующего анализа.

## Установка зависимостей

### Перед установкой зависимостей рекомендуется создать виртуальное окружение:

```bash
python -m venv venv
```

### Активируйте виртуальное окружение:

На Windows:

```bash
venv\Scripts\activate
```

На Linux или MacOS:

```bash
source venv/bin/activate
```

### Установите зависимости:

```bash
pip install -r requirements.txt
```

## Установите драйвер Chrome:

Скачайте драйвер [ChromeDriver](https://developer.chrome.com/docs/chromedriver) извлеките его из zip-файла и поместите
его в корень проекта. Убедитесь, что путь к драйверу в коде соответствует его расположению на вашем компьютере.
Соответствующий код:

```bash
s = Service(executable_path='ваш_путь_до_хромдрайвера')
```

## Использование

**Запуск скрипта:**

   ```sh
   python main.py [section] [--sorted_by_hot] [--pages]
   ```

[section] - доступные секции для поиска на сайте.

[--sorted_by_hot] - сортировка по скидке от цены стима (По умолчанию включена)

[--pages] - количество страниц, с которых берутся данные

## Лицензия

This project is Licensed under [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0).
