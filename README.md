# Bookmate Downloader
Downloads books from https://bookmate.ru and saves them as epub format files.

# You need to be subscribed to bookmate.com premium OR download books that are available for free !!!
Works on Mac OS X, Linux.
For Windows 10 you'll need to install WSL (Windows subsystem for linux) aka Windows Ubuntu.

Steps:
1. Buy the subscription at bookmate.ru
2. Authorize at bookmate.com with your chrome browser
3. install python3
4. Copy the bookid (open the book at bookmate.com and check the url)
5. `python3 bookmate_downloader.py --bookid BookIdHere`
6. The epub will be downloaded to "out"

## Installation details:
```bash
sudo apt update
sudo apt install -y python3-pip
git clone https://github.com/ilyakharlamov/bookmate_downloader
cd bookmate_downloader
pip3 install -r src/python3/requirements.txt
python3 src/python3/bookmate_downloader.py --bookid KFHDG3bp
```
## Docker Usage (Alternative "installation")
```bash
git clone https://github.com/ilyakharlamov/bookmate_downloader.git .
docker build -t bookmate_dl .
docker run -it --mount type=bind,source=$(pwd),target=/mnt/data bookmate_dl --bookid KFHDG3bp --log DEBUG --outdir /mnt/data
```

## From Windows:
1. Install Python
2. Install git
3. Open cmd in directory any directroy
4. ```git clone https://www.github.com/ilyakharlamov/bookmate_downloader```
5. ```cd bookmate_downloader```
6. ```sudo apt-get update```
7. ```sudo apt install -y python3-pip```
8. ```pip3 install -r src/python3/requirements.txt```
9. ```python3 src/python3/bookmate_downloader.py --bookid KFHDG3bp```
10. After completion, you will find your book at your home folder at bookmate_downloader/out


You will be asked for 'BMS cookie', in order to get it:
1. Go to your browser
2. log in to bookmate.com
3. Open developer'console (F12)
4. Click Application
5. Click 'Cookies' on the left
6. Find bms on the right 
7. Copy the value

## Для российских пользователей:
после 24.02.2022 букмейт ушёл из РФ

Русский букмейт и мировой букмейт разделились, теперь русский сайт делает команда яндекса, не связанная с предыдущей, на другом движке, поэтому **скрипт работать с яндексовским букмейтом не работает**.

Скрипт продолжает работать только с обычным, не-яндексовским bookmate.com.
Можно поставить VPN и качать с мирового.
