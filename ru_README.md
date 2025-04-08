#[English readme is here](README.md)

# Загрузчик с Яндекс Книг
Скачивайте книги с https://books.yandex.ru в формате epub.

# Вам надо быть подписанным на Яндекс Плюс ИЛИ скачивать книги которые доступны бесплатно !!!
Работает на Mac OS X, Linux, Windows.

Использование:
1. Купите подписку Яндекс Плюс на plus.yandex.ru(или на books.yandex.ru)
2. Авторизируйтесь на books.yandex.ru через браузер chrome
3. установите python3
4. Скопируйте bookid (откройте книгу на books.yandex.ru и посмотрите на url, bookid идёт после reader или books)
5. `python3 yandex-books_downloader.py --bookid [здесь bookid без квадратных скобок]`
6. После завершения вы найдёте свою книгу в формате epub в папке "out" в yandex-books_downloader

## Установка:
```bash
sudo apt update
sudo apt install -y python3-pip
git clone https://github.com/nightdenpa/yandex-books_downloader
cd yandex-books_downloader
pip3 install -r src/python3/requirements.txt
python3 src/python3/yandex-books_downloader.py --bookid AwwHcnkj
```
## Docker (Альтернативный вариант "установки")
```bash
git clone https://github.com/nightdenpa/yandex-books_downloader .
docker build -t bookmate_dl .
docker run -it --mount type=bind,source=$(pwd),target=/mnt/data bookmate_dl --bookid AwwHcnkj --log DEBUG --outdir /mnt/data
```

## Установка из под Windows:
1. Установите Python
2. Установите git
3. Откройте командную строку в любой директории
4. ```git clone https://github.com/nightdenpa/yandex-books_downloader```
5. ```cd yandex-books_downloader```
6. ```pip3 install -r src/python3/requirements.txt```
7. ```python3 src/python3/yandex-books_downloader.py --bookid AwwHcnkj```
8. После завершения вы найдёте свою книгу в формате epub в папке "out" в yandex-books_downloader


У вас запросят 'Session id', чтобы его получить:
1. Зайдите в ваш браузер
2. Авторизуйтесь на books.yandex.ru
3. Откройте инструменты разработчика (F12)
4. Зайдите во вкладку Application
5. Нажмите 'Cookies' слева
6. Найдите Session_id справа
7. Скопируйте значение
