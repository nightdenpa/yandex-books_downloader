# [Русский readme здесь](ru_README.md)

# Yandex Books Downloader
Downloads books from https://books.yandex.ru and saves them as epub format files.

# You need to be subscribed to Yandex Plus subscription OR download books that are available for free !!!
Works on Mac OS X, Linux, Windows.

Steps:
1. Buy Yandex Plus subscription on plus.yandex.ru(or books.yandex.ru)
2. Authorize at books.yandex.ru with your chrome browser
3. install python3
4. Copy the bookid (open the book at books.yandex.ru and check the url)
5. `python3 yandex-books_downloader.py --bookid BookIdHere`
6. The epub will be downloaded to "out"

## Installation details:
```bash
sudo apt update
sudo apt install -y python3-pip
git clone https://github.com/nightdenpa/yandex-books_downloader
cd yandex-books_downloader
pip3 install -r src/python3/requirements.txt
python3 src/python3/yandex-books_downloader.py --bookid KFHDG3bp
```
## Docker Usage (Alternative "installation")
```bash
git clone https://github.com/nightdenpa/yandex-books_downloader .
docker build -t ya-books_dl .
docker run -it --mount type=bind,source=$(pwd),target=/mnt/data ya-books_dl --bookid KFHDG3bp --log DEBUG --outdir /mnt/data
```

## From Windows:
1. Install Python
2. Install git
3. Open cmd in any directory
4. ```git clone https://github.com/nightdenpa/yandex-books_downloader```
5. ```cd yandex-books_downloader```
6. ```pip3 install -r src/python3/requirements.txt```
7. ```python3 src/python3/yandex-books_downloader.py --bookid KFHDG3bp```
8. After completion, you will find your book at your home folder at yandex-books_downloader/out


You will be asked for 'Session id', in order to get it:
1. Go to your browser
2. log in to books.yandex.ru
3. Open developer'console (F12)
4. Click Application
5. Click 'Cookies' on the left
6. Find Session_id on the right 
7. Copy the value
