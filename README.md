### 🐧 Linux - это операционная система с открытым исходным кодом, основанная на ядре Linux

# Основные моменты, связанные с Linux:
|История | *Linux был создан Линусом Торвальдсом в 1991 году как проект хобби. С течением времени он стал популярным и развился в операционную систему с открытым исходным кодом, привлекая множество разработчиков и сообществ* |
| :---: | :---: |
| **Дистрибутивы** | *Linux доступен в различных дистрибутивах, таких как Ubuntu, Fedora, Debian и многих других. Дистрибутивы предлагают различные комбинации программного обеспечения и инструментов, чтобы удовлетворить потребности различных пользователей* |
| **Открытый исходный код** | *Одна из ключевых особенностей Linux - это его открытый исходный код. Это означает, что любой может просматривать, изменять и распространять код операционной системы. Это способствует инновациям, сотрудничеству и быстрому исправлению ошибок* |
| **Утилиты и программное обеспечение** | *Linux поставляется с множеством утилит и программного обеспечения, которые расширяют его функциональность. Это включает текстовые редакторы, компиляторы, интерпретаторы языков программирования, графические интерфейсы, серверы, базы данных и многое другое. Большинство из них также являются программами с открытым исходным кодом* |
| **Ядро Linux** | *Ядро Linux является основой операционной системы. Оно управляет ресурсами компьютера, обеспечивает взаимодействие с аппаратным обеспечением и поддерживает различные функции, такие как управление памятью, планирование задач, файловая система и сетевые возможности* |
| **Многозадачность и многопользовательская поддержка** | *Linux поддерживает многозадачность, что означает, что он может выполнять несколько задач одновременно. Он также поддерживает многопользовательскую среду, позволяя нескольким пользователям работать на одной системе одновременно* |
| **Командная строка** | *Linux предоставляет мощную командную строку, которая позволяет пользователям выполнять различные задачи и управлять системой. Командная строка предлагает широкий спектр команд и утилит для управления файлами, процессами, сетью и другими аспектами операционной системы* |
| **Безопасность** | *Linux известен своей высокой степенью безопасности. Открытый исходный код позволяет быстро обнаруживать и исправлять уязвимости, а также предоставляет возможность настройки системы безопасности в соответствии с потребностями пользователя* |
| **Файловая система** | *Linux поддерживает различные файловые системы, такие как ext4, XFS, Btrfs и другие. Файловая система отвечает за организацию и управление файлами и папками на диске, а также за обеспечение доступа к данным* |
| **Сетевые возможности** | *Linux обладает мощными сетевыми возможностями, которые позволяют подключаться к сети, обмениваться данными и предоставлять сетевые услуги. Он поддерживает протоколы TCP/IP, имеет встроенные сетевые утилиты и может работать как клиент и сервер* |

<div>
  <img src="https://github.com/devicons/devicon/blob/master/icons/linux/linux-original.svg" title="Linux" alt="Linux" width="100" height="100"/>&nbsp;
</div>
	
# Общие команды Linux:
```bash
uname -a                     # Показать всю информацию об операционной системе
whoami                       # Под каким логином находимся
pwd                          # Где сейчас находимся
uptime                       # Посмотреть сколько по времени включена тачка
lscpu                        # Посмотреть информацию о процессоре
clear                        # Очистить экран консоли
ls -ali                      # Посмотреть подробную информацию о файлах в директории
echo hello linux             # Вывести текст
echo $PATH                   # Посмотреть директории в которых linux будет запускать команды
whereis snap                 # Посмотреть путь, где находится файл/ПО
locate snap                  # Посмотреть путь, где находится файл/ПО
find /home -name "file.txt"  # Поиск файлов везде
sudo reboot -f               # Перезагрузка в фоновом режиме
sudo shutdown                # Выключить машину
top                          # Диспечер задач ([Shift]+[P] фильтр по cpu, [Shift]+[M] фильтр по RAM, [V] отобразить процессы в виде древа, [Z] подсветить чуть покрасивее, [Shift]+[E] показать в КБ/МБ/ГБ)
htop                         # Диспечер задач с красивым отображением в % загрузки
atop                         # Диспечер задач с красивым отображением в % загрузки
free -h                      # Показать RAM общую и нагруженную
dmesg                        # Лог ядра Linux
sudo apt update              # Проверка обновлений
sudo apt install {program}   # Установка ПО
sudo apt upgrade             # Установка обновлений
sudo su / sudo -s            # Вход под рутом и остаться в нём
neofetch                     # Как свойства компьютера в Windows
lsscsi                       # Диспетчер устройств (dec/sd*)
type {command}               # Узнать тип команды
history                      # Показать историю всех команд пользователя
export variable              # Даёт возможность наследования выбранной переменной в дочерний процесс
man {command}                # Мануал по команде
info {command}               # Аналог man
crontab -e                   # Редактировать запуск по расписанию в системе
set                          # Показать все переменные
ls | nl                      # (nl) Проставить нумерацию строк
date                         # Вывести информацию о времени
sleep                        # Задать таймер выключения системы
yes                          # Автозаполнение поля согласия на выполнение команды
watch -n 60 {command}        # Выполнять любую команду каждые 60 секунд
```

> Установка и удаление программ:
```bash
sudo apt-get {program}        # Скачать и установить ПО с APT (убунту репозитория)
sudo apt-get remove {program} # Удалить ПО
wget https://program.ru/file  # Скачать что либо с интернета. Пример -> wget https://raw.githubusercontent.com/DragonDamage/Vagrant/main/Vagrantfile
sudo dpkg -i {program}        # Установить ПО скаченное с интернета
sudo dpkg -r {program}        # Удалить ПО скаченное с интернета
sudo apt remove {program}     # Удалить ПО, но оставить конфигурационные файлы
sudo apt purge {program}      # Удалить ПО полностью
sudo apt autoremove           # Удалить ненужные зависимости
sudo apt autoclean            # Удалить старые архивы
sudo apt install -f           # Починить зависимости, если где-то возникли проблемы
```

> Работа с пользователями, группами и правами:
```bash
su {user_name}                           # Зайти под другим пользователем
exit                                     # Выйти из под пользователя
who                                      # Кто сейчас ещё онлайн из пользователей
w                                        # Показывает подключенных пользаков и что они делают
cat /etc/passwd                          # Все пользователи
cat /etc/group                           # Все группы и кто в них входит
cat /etc/shadow                          # Пароли пользаков
cat /etc/sudoers                         # Пользователи с правами на команды
sudo chage {user_name}                   # Настроить пароль пользаку
id                                       # Кем мы сейчас работаем
id {user_name}                           # Посмотреть права пользователя
newgrb adm                               # Активная группа
sudo ls -al /home/user_name              # Показать файлы юзера
sudo adduser {user_name}                 # Создать побыстрому юзера и дать пароль
sudo userdel -r {user_name}              # Удалить юзера и (-r все его файлы)
sudo deluser {user_name} {group_name}    # Удалить пользователя из группы
sudo passwd {user_name}                  # Поменять пароль юзеру
sudo usermod -aG sudo                    # Добавить пользака в группу sudo
sudo usermod -aG adm {user_name}         # Добавить в список дополнительных групп адм пользователя
sudo groupadd {group_name}               # Создать группу
sudo groupdel {group_name}               # Удалить группу
passwd                                   # Сменить самому себе пароль
sudo chown -R andrey:www-data file_name  # Изменить владельца директории
sudo chgrp -R adm file_name              # Изменить владельца только группы adm
sudo chmod u=rwx,g=rw,o=r {file_name}    # Для владельца полные права (чтение, запись, исполнение), для группы (чтение,запись), для остальных (чтение) в name_file
sudo chmod +x {file_name}                # Дать права на исполнение для всех
sudo chmod 777 {file_name}               # Дать права на всё для всех
sudo chmod -R 777 /directory             # Дать права рекурсивно на все подпапки и файлы внутри директории
last                                     # Посмотреть кто заходил в систему из пользователей за последнее время
finger                                   # Показать пользователей в сети
sudo useradd -s /bin/bash -m -d /home/user_name user_name  # Создать пользователя
```

> [CHMOD] комбинации разрешений для команды:
```bash
r (read)     # Позволяет просматривать содержимое файла/каталога
w (write)    # Позволяет изменять содержимое файла/каталога
x (execute)  # Позволяет выполнять файл как программу или скрипт

Вид разрешения                   | Символьный код  |  Числовой код  |
Нет допуска	                 |       —         |       0        |
Чтение	                         |       r-	   |       4        |
Изменение	                 |      -w-        |       2        |
Запуск	                         |      -x	   |       1        |
Запуск + Изменение	         |      -wx	   |       3        |
Чтение + Запуск	                 |      r-x        |       5        |
Чтение + Изменение	         |      rw-        |       6        |
Запуск + Изменение + Запуск	 |      rwx        |       7        |
```

> Работа с директориями:
```bash
cd <name_directory>                # Перейти в директорию
ls -d */                           # Показать только директории
mkdir <name_directory>             # Создать директорию
mkdir dir{1..3}                    # Одной командой создать несколько директорий - создать dir1, dir2, dir3
cp -R <directory> <new_directory>  # Скопировать директорию (с вложенными в неё файлами) в другую директорию
rm -R <name_directory>             # Удалить директорию
du -hs <./name_directory>          # Посмотреть обьём директории
tree                               # Показать директории и файлы в виде дерева (очень полезная команда)
ncdu <./name_directory>            # Посмотреть свободное и занятое место в директориях
find /* -type d -name "dir_name"   # Поиск папки по названию
ls -d [!t]*/                       # Поиск папок с исключением
```

> Работа с файлами:
```bash
cat file.txt                  # Показать что в файле
nano -l file.txt              # Редактировать файл -l добавляет отображение строк (Ctrl+O сохранить изменения, Ctrl+X закрыть редактирование)
more file.txt                 # Показать что в файле (q для выхода из режима чтения)
less file.txt                 # Просмотр содержимого файла (/ для поиска, как ctrl+f в windows), (q для выхода)
touch file.txt                # Создать файл
cp file.txt ~/var/            # Скопировать файл в другую директорию
rm file.txt                   # Удалить файл
mv file.txt .new_file_name    # Переименовать файл (. сделать его скрытым)
mv file.txt ~/Desktop/        # Перенести файл в директорию (рабочий стол)
wc file.txt                   # Показать сколько: строк, слов, символов
wc -l file.txt                # Показать только количество строк
wc -w file.txt                # Показать только количество слов
wc -m file.txt                # Показать только количество символов
sort file.txt                 # cat + сортировка по алфавиту
sort -n file.txt              # cat + сортировка по цифрам
sort du file.txt              # cat + сортировка по размеру
sort -u file.txt              # cat + сортировка с удалением дубликатов
cut -d ">" -f 3 file.txt      # cat + делиметр, какое поле
cat file.txt > new_file.txt   # Сохранить результат команды в файл
cat file.txt >> new_file.txt  # Сохранить и добавить результат команды в файл с уже существующим текстом
ln file.txt file_dupl.txt     # Дублировать файл (жесткая ссылка)
echo file.txt                 # Вывести файл на консоль
echo ????                     # Вывести файлы с 4 символами
echo ????*                    # Вывести файлы 4 и больше символов
touch file.txt{01..10}        # Создать несколько файлов от 01 до 10
diff file1.txt file2.txt      # Сравнить содержимое файлов (c - изменённые строки, d - удалённые строки, а - новые строки)
file file.txt                 # Узнать точный формать файла
tac file.txt                  # cat в обратном порядке
uniq file.txt                 # cat без дублей
cut -c1-10 file.txt           # cat файла с первого символа по десятый
find /* -name file.txt        # Поиск файла file.txt по всем директориям
cat *.yml | grep -r "text"    # Найти и вывести файлы и их наименование, в которых есть text
find /* -type f или d или l -size + 40k      # Поиск по f-файлу, d-директории или l-ссылке, и по размеру файла в килобайтах
ln -s /home/andrey/name_directory name_link  # Создать символическую ссылку
lsof                                         # Показать список всех открытых файлов для всех процессов
ll | tee file.txt                            # tee сохраняет вывод команды в файл
cat file.txt | xclip -selection clipboard    # Копирование содержимого файла в буфер обмена
xsel --output > output.txt                   # Вставить содержимое буфера обмена в файл
ls -l | xclip -selection clipboard           # Копирование вывода команды в буфер обмена
```

> Сочетание клавиш + полезные команды:
```bash
*             # Означает все
?             # Означает воспринять один любой символ
-v            # verbose - показывать процесс выполнения команды
|             # Пайп - выполнить одну команду за другой
.             # Текущая директория
..            # Предыдущая директория
&&            # Выполнить команды следом друг за другом
.Directory    # Значит конфигурационные директории
[TAB]         # Показывает варианты автозавершения команды
[CTRL] + [R]  # Поиск введённых команд по истории
[CTRL] + [C]  # Завершить исполнение процесса или выполнения команды
[CTRL] + [Z]  # Продолжить выполнять процесс в фоновом режиме
%             # Возобновить процесс из фонового режима
[Ctrl] + [A]  # Для быстрого перехода в начало строки
[Ctrl] + [E]  # Для быстрого перехода в конец строки
sudo visudo или nano /etc/sudoers  # Добавить строчку в самый низ: andrey ALL=(ALL:ALL) NOPASSWD: ALL  # теперь пользователь может выполнять sudo без пароля
cd /var/log $ head syslog          # Перейти в папку и показать первые 10 строчек лога
cd /var/log $ tail -n 20 syslog    # Перейти в папку и показать последние  (-n 20) 20 строк
nano /etc/ssh/sshd_config          # Настройка ssh - отключить вход под root → (PermitRootLogin yes меняем на no); изменить порт по умолчанию → (Port 22 меняем на 2222)
nano ~/.bashrc                     # Для отображения веток GIT - В последнюю строку вставляем: PS1='\[\033[0;32m\]\[\033[0m\033[0;32m\]\u\[\033[0;36m\] @ \[\033[0;36m\]\h \w\[\033[0;32m\] \$\[\033[0m\033[0;32m\] ▶\[\033[0m\] '
```

> Нужные папки:
```bash
cat /etc/passwd            # Все пользователи
cat /etc/shadow            # Пароли пользаков
cat /etc/sudoers           # Пользователи с правами на команды (например sudo)
cat /etc/apt/sources.list  # Репозиторий ubuntu
cd /var/log/               # Хранение логов в данной папке
cat /etc/hosts             # Файл с параметрами DNS
cat /etc/fstab             # Файловые системы
cat /etc/hostname          # Имя ПК
cat /etc/hosts             # Посмотреть имя и ip локалхоста и нашей тачки
cat /etc/rsyslog.conf      # Файл с настройками логирования
cat /etc/crontab           # Файл crontab
cat /var/log/kern.log      # Логи ядра
cat /etc/netplan/00-installer-config.yaml  # Файл с конфигами сети
```

> Работа с архивами:
```bash
wget https://....tar.gz              # Скачать архив в директорию
tar cvf <name.tar> /name_directory   # Создать архив директории с названием name.tar
tar tf <name.tar>                    # Посмотреть что находится внутри архива
tar xvf <name.tar>                   # Разархивировать архив (или tar -xvpf file.tar)
gzip <name.tar>                      # Запаковать/скомпрессировать файл
gungzip <name.tar.gz>                # Распаковать файл
xz <name.tar>                        # Средне запаковать/скомпрессировать файл
unxz <name.tar.xz>                   # Распаковать файл
bzip2 <name.tar>                     # Сильно запаковать/скомпрессировать файл
bunzip2 <name.tar.bz2>               # Распаковать файл
tar cvzf <name.gz> /name_directory   # Создать архив директории и запаковать его с помощью gzip
tar xvf <name.gz>                    # Распаковать файл gz
tar cvJf <name.xz> /name_directory   # Создать архив директории и запаковать его с помощью xz
tar xvf <name.xz>                    # Распаковать файл xz
tar cvjf <name.bz2> /name_directory  # Создать архив директории и запаковать его с помощью bzip
tar xvf <name.bz2>                   # Распаковать файл bz2
zip -r <name.zip> /name_directory    # Создать архив zip директории с названием name.zip
unzip <name.zip>                     # Распаковать файл zip
```

> [ps] Работа с процессами:
```bash
ps                       # Посмотреть запущенные процессы
ps -u                    # Посмотреть запущенные процессы под пользаком
ps -afx или ps -aux      # Показать все запущенные процессы всех пользователей
ps auf | grep ssh        # Показать пользователей подключенных по ssh
kill -9 "id ps -afx"     # Убить процесс (KILL)
kill -15 "id ps -afx"    # Корректно завершить процесс (TERM)
ps -T -p [№процесса]     # Показать потоки процесса
ps -efl                  # Посмотреть список процессов с PID
jobs                     # Посмотреть есть ли приостановленные процессы
nice -n 3 bash           # Запустить bash с приоритетом процесса 3
ps I                     # Показать процессы по приоритетам
time wget https://ya.ru  # Секундомер позволяющий подсчитать время исполнения процесса (real - время исполнения, user - сколько времени пользователь занял у CPU, sys - сколько времени CPU было потрачено системой)
```

> [systemctl] Работа с сервисами:
```bash
systemctl list-units --type=service --state=running     # Просмотр всех активных сервисов
systemctl list-units --type=service --all               # Просмотр всех сервисов (включая неактивные)
systemctl list-units --state=failed --type=service      # Посмотреть все неудачно загруженные сервисы
systemctl list-unit-files --state=failed --type=service # Посмотреть все неудачно загруженные сервисы
systemctl list-units --type=service --state=running --no-pager --no-legend | awk '{print $1}' | xargs -I {} systemctl status {} --no-pager --no-legend  # Просмотр всех активных серисов с выводом времени запуска
systemctl list-units --type=service --state=running --no-pager --no-legend | awk '{print $1}' | xargs -I {} sh -c "echo {}; systemctl status {} --no-pager --no-legend | grep 'Active:' | awk '{print \$2, \$3, \$4, \$5, \$6}'"  # То же самое, только вывести ещё дату
systemctl show service_name.service      # Посмотреть настройки сервиса
systemctl --type=service | grep failed   # Проверка сервисов на ошибки 
---
systemctl status name_service.service     # Показать статус сервиса
systemctl status -l name_service.service  # Показать более подробный статус сервиса
systemctl start name_service.service      # Запустить сервис
systemctl stop name_service.service       # Остановить сервис
systemctl restart name_service.service    # Рестарт сервиса
systemctl enable name_service.service     # Всегда запускать сервис при включении ПК
```

> [journalctl] Работа с логами сервисов:
```bash
journalctl -e name_service.service   # Смотрим самые свежие логи
journalctl -eu name_service.service  # -eu Фильтр по определенному юниту
journalctl --all --since "5 minutes ago" --no-tail --no-pager -p 7 -f                # Смотрим логи за последние 5 минут
journalctl --all --since "5 minutes ago" --no-tail --no-pager -p 7 -f | grep 'ERROR' # Смотрим логи за последние 5 минут с 'ERROR'
journalctl --all --since "2024-07-09 12:00:00" --until "2024-07-09 21:00:00" --no-tail --no-pager -p 7 -u name_service.service > logs_name_service.txt  # Самый ТОП по логам
journalctl -eu name_service.service --since today          # Лог за сегодня
journalctl -eu name_service.service --since "2 hours ago"  # Лог за последние 2 часа
journalctl -a --since today | grep <text> > logs.txt       # Логи по grep по логам всех сервисов
```

> [ip] [ss] [netstat] Работа с сетью и портами:
```bash
ifconfig           # Вся информация по сети
ip addr show       # Показать адаптеры и ip
ip -c a            # Инфа по сети
ip -c a | grep mtu # Посмотреть MTU
traceroute         # Куда пересылаются пакеты с промежуточными маршрутизаторами
route              # Куда пересылаются пакеты
ping 8.8.8.8       # Достучаться по сети до ip
host -t a ya.ru    # Показать ip сайта
dig ya.ru          # Показать ip сайта (подробнее)
mtr -b google.com  # Показать полную маршрутизацию и ip адрес хоста
netstat            # Показать открытые порты
lsof               # Показать открытые порты
sudo ufw allow 22  # Открыть порт
ip -c r            # Показать проведеные ip
ss -nutlp          # Показать какие сокеты открыты
ss -tulpan         # Полностью все открытые подключения
resolvectl         # Посмотреть параметры DNS
dig 8.8.8.8        # Посмотреть параметры DNS
dig -t mx ya.ru    # Посмотреть почтовую запись
curl -Lv ya.ru     # Отправить HTTP запрос на сервер
netstat -tuln | grep 9200        # Проверить свободный ли порт
cat /etc/services | grep -i 9200 # Проверить свободный ли порт
curl -v telnet://127.0.0.1:22    # Проверить доступность удаленного порта
```

> CURL [Client URL]:
```bash
curl https://link.ru           # Get запрос на чтение HTML страницы
curl -X GET https://link.ru    # Get запрос на чтение HTML страницы
curl -I -X GET https://link.ru # Get запрос на статус и сервер
curl -Lv 127.0.0.1             # Отправить HTTP запрос на сервер
```

> SSH [Secure Shell Protocol]:
```bash
sudo apt-get install openssh-server       # Ставим ssh-сервер на тачку
sudo systemctl status ssh                 # Проверить работает ли сервис ssh
sudo systemctl start ssh                  # Включить сервис ssh
ssh <you_ip>                              # Обычный способ подключиться по ssh к тачке
ssh -p 22 user_name@you_ip                # Подключиться по ssh к тачке с портом, user_name и айпишником
ssh -i C:\Users\user_name\key.pem         # Подключение по ssh с помощью ключа .pem
exit                                      # Выйти из сессии
ssh -L 9000:localhost:8000 {Server_NAME}  # Пробросить порт 8000 с сервера localhost на нашу тачку с портом 9000 (теперь приложение, которое было на 8000 порту мы пожем глянуть на нашей тачке по порту 9000)
```

> Генерация ключей ssh (ходим на тачку без пароля):
```bash
0. Проверяем что на серваках включена аутентификация по ключам: PubkeyAuthentication yes
cat /etc/ssh/sshd_config | grep PubkeyAuthentication

1 Вариант (автоматически)
ssh-keygen -t rsa -b 4096  # Генерим ключи на нашем АРМ
ssh-copy-id domain\\username@server_ip  # Копируем ключи с нашего АРМ на удаленный server_ip

2 Вариант (вручную)
ssh-keygen                 # Сгенерировать пару ключей RSA формата (со стороны АРМа)
ssh-keygen -t ed25519      # Сгенерировать пару ключей более нового формата (со стороны АРМа)
ssh-copy-id                # Переносим ключ паблик вручную в /.ssh в файл authorized_keys (далее нужно было перелогиниться)
mkdir .ssh                 # Если на сервере нет скрытой директории .ssh, то создаем её
nano .ssh/authorized_keys  # Вставляем public-key на сервер
chown -R {NAME:NAME} /home/user_name/.ssh  # Делаем все файлы в директории от создателя {NAME}
chmod 700 ~/.ssh           # Даём права доступа на папку
chmod 644 ~/.ssh/*         # Даём права доступа на все файлы
cd /etc/ssh → sshd_config  # Можно изменить порт (на 61022 например)
---

Если много серверов, то создаем скрипт:
1. Создаем список IP-адресов серверов:
nano servers.txt  # Вставляем списком
2. Пишем скрипт:
nano script_ssh.sh
---
#!/bin/bash
for server in $(cat servers.txt); do
    ssh-copy-id domain\\username@$server
done
---
3. Запускаем скрипт:
./script_ssh.sh
```

> [GREP] and [AWK]:
```bash
grep text ./*                             # Поиск файлов, в которых есть текст text, в текущей директории
grep -i text ./*                          # Поиск файлов, в которых есть текст text, в текущей директории (-i означает игнорировать регистр)
grep -ri text *                           # Поиск файлов, в которых есть текст text (-i означает игнорировать регистр, -r означает рекурсивный поиск)
grep -rnw '/' -e "text"                   # Поиск файла по тексту на всём ПК
grep andrey /etc/* &> all_log.txt         # Отправить все ответы в файл
grep andrey /etc/* > good.txt             # Отправить хорошие ответы в файл
grep andrey /etc/* 2> errors_file.txt     # Отправить плохие ответы в файл
grep andrey /etc/* 2> /dev/null           # Отправить в никуда
grep andrey /etc/* > good.txt 2> bad.txt  # Отправить хорошие ответы в файл good, а плохие ответы в файл bad
nano file.txt -> 1 2 3 , cat file.txt | awk '{print $2}'  # awk выбирает данные по столбцам
```

> Разбор [ls -l]:
```bash
-rwxrw-r-- 1 andrey andrey 1024 Nov 22 18:34 file.txt  # Пример
-    # Означает файл
d    # Означает директория
l    # Означает линк (ссылка)
rwx              # Права на r-чтение, w-редактирование, x-исполнение
rwx|rw-|r--      # Первые права доступа к пользователю, вторые права доступа пользователям, третьи права доступа ко всем
1 или 2 и более  # Означает количество линков
andrey           # Пользователь и группа кто создал
```

> Just_For_Fun:
```bash
sudo ls -la -R /  # Пролистать все диски 
sudo rm -R /      # Удалить все что есть на тачке (НИКОГДА НЕ ИСПОЛЬЗУЙТЕ)
```

> Работа с дисками:
```bash
fdisk -l                        # Показать информацию о разделах на жестком диске
lsblk                           # Показать жесткие диски и другие устройства хранения (свободное место на примонтируемых дисках)
smartctl -a /dev/sda            # Показать полное состояние конкретного диска
df -h / df -kh                  # Показать общий размер файловой системы, использованное и доступное место
du -skh dir/                    # Показать сколько весит папка
du -h -d 1                      # Показать размер всех файлов и директорий в текущей директории
du -h -d 1 /you/dir             # Показать размер файлов и директорий внутри определяемой директории
du -h -a | sort -h -r           # Показать размер всех файлов и всех директорий с сортировкой
du -h | awk '$1 > 1M' | sort -h # Показать файлы и папки с размером и сортировкой по возрастанию с указанием от какого размера МБ
df -i                           # Показать иноды по дискам
cfdisk /dev/sdb                 # dos, создаем партицию диска
mkfs.ntfs -f /dev/sdb1          # Форматировать диск
nano /etc/fstab                 # /dev/sdb1 /media/hdd ntfs default 0 0  # делаем автомонтирование диска
mount /media/hdd                # Монитруем диск
ln -s /media/hdd ~/Desktop/HDD  # Создаём символическую ссылку с диском на рабочем столе
parted -l                       # Посмотреть таблицу разделов системы
iostat                          # Показать загрузку дисковой подсистемы
ftp                             # Передача данных другой системе
ncdu -x                         # Покажет, что место занимает и можно походить по директория посмотреть
```

> Инструкция по созданию и монтированию дисков:
```bash
sudo fdisk -l        # Посмотреть диски подключенные к системе
sudo fdisk /dev/sdb  # Создаём новые разделы
n                    # Создаём новый
[enter]              # Номер раздела 1
[enter]              # Первый сектор 2048
+1G                  # Размер раздела
w                    # Сохранить правки

sudo mkfs -t ext4 /dev/sdb1                       # Задаём файловую систему (ext4 linux),(ntfs для windows),(vfat для windows и macos), (bfs linux)
sudo mount   -t ext4 /dev/sdb1 /home/ubuntu/mnt   # Монтируем диск в том в заранее созданную папку mnt
```

> Команды [GRUB]:
```bash
grub> ls                            # Посмотреть диски
grub> set prefix=(hd0,1)/boot/grub  # Взять оба диска и загрузить boot раздел
grub> set root=(hd0,1)              # Запустить это от рута
grub> ls boot/grub                  # Посмотреть grub.cfg
grub> insmod ext2                   # Обновить grub (ext2 - файловая сисиетма)
grub> insmod normal                 # Перевести режим grub в норм режим
grub> normal                        # Запуск grub
```

> [base64]:
```bash
echo -n "Password" | base64             # Кодировать
Вывод: UXdlcnzNDU2
echo -n "UXdlcnzNDU2" | base64 --decode # Декодировать
Вывод: Password
```

> Декодирование переменных в Ansible:
```bash
sudo ansible-vault decrypt file.txt  # Расшифровать
sudo ansible-vault edit file.txt     # Редактировать
sudo ansible-vault encrypt file.txt  # Зашифровать 
```

---

# [Scripts]:
```bash
./script.sh               # Запустить скрипт
chmod 777 script_name.sh  # Дать права на запуск скрипта
bash script_name.sh       # Запуск скрипт, если нет прав X
```
```bash
Примеры скриптов:

# переменные и команды
#!/bin/bash
mycomp="HONOR"
myOS=`uname -a`
echo "This script name is $0"
echo "Q $1"
echo "Q $2"
num1=10
num2=20
summ=$((num1+num2))
echo "$num1 + $num2 = $summ"
myhost=`hostname`
mygtw="8.8.8.8"
ping -c 4 $myhost
ping -c 4 $mygtw
echo -n "This is done..."
echo "DONE"

# if/elif/else/fi /read/case/esac
#!/bin/bash

if   [ "$1" == "Andrey" ]; then
	echo "Q $1"
elif [ "$1" == "Igor" ]; then
	echo "Q $1"
else echo "NoQ $1"
fi
read -p "Enter you parameter:" x
x=$2
echo "Starting CASE selection..."
case $x in
		1) echo "This is one";;
	[2-9]) echo "Two-Nine";;
 "Andrey") echo "Q $x";;
		*) echo "NO_PARAMETER"
esac

# while/-lt меньше или равно/done/for
#!/bin/bash

COUNTER=0
while [ $COUNTER -lt 10 ]; do
		echo "Current counter is $COUNTER"
		COUNTER=$(($COUNTER+1))
done

# ls *.txt | cat *.txt
for file in `ls *.txt`; do
	  cat $file
done
# for in RANGE
for x in {1..10}; do
		echo "X = $x"
done
# for like java style 
for (( i=1; i<=10; i++ )); do
		echo "№ I = $i"
done

# Function
#!/bin/bash

Function()
{
        echo "This is text from Function"
        echo "First parameter is: $1"
        echo "Second parameter is: $2"
}

Function 7 Andrey
```
