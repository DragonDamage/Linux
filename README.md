# Linux
### Linux Basics

> Command for Linux:
```bash
whoami  # под каким логином находимся
pwd  # где сейчас находимся
uptime  # посмотреть сколько по времени включена тачка
lscpu  # посмотреть информацию о процессоре
clear  # очистить экран консоли
ls -ali  # посмотреть подробную информацию о файлах в директории
echo hello linux #  вывести текст
echo $PATH  # посмотреть директории в которых linux будет запускать команды
whereis snap  # посмотреть путь, где находится файл/ПО
locate snap  # посмотреть путь, где находится файл/ПО
find /home -name "file.txt"  # поиск файлов везде
sudo reboot -f  # перезагрузка в фоновом режиме
sudo shutdown  # выключить машину
top  # диспечер задач (Shift+P фильтр по cpu, Shift+M фильтр по RAM)
htop  # диспечер задач с красивым отображением в % загрузки
free -h  # показать RAM общую и нагруженную
ps  # посмотреть запущенные процессы
ps -afx или ps -aux  # показать все запущенные процессы всех пользователей
ps auf | grep ssh  # показать пользователей подключенных по ssh
df -h  # показать сколько места на жестком диске
dmesg  # лог ядра Linux
sudo apt update  # проверка обновлений
sudo apt install programm  # установка ПО
sudo apt upgrade  # установка обновлений
sudo su  # вход под рутом и остаться в нём
neofetch  # как свойства компьютера в Windows
lsscsi  # диспетчер устройств (dec/sd*)
type  # узнать тип команды
history  # показать историю всех команд пользователя
export variable  # даёт возможность наследования выбранной переменной в дочерний процесс
man  # мануал по команде
info  # аналог man
crontab -e  # редактировать запуск по расписанию в системе
```

> Установка и удаление программ:
```bash
sudo apt-get name_programm  # скачать и установить ПО с убунту репозитория
sudo apt-get remove name_programm  # удалить ПО
wget https://name_programm.ru/file  # скачать что либо с интернета. Пример -> wget https://raw.githubusercontent.com/DragonDamage/Vagrant/main/Vagrantfile
sudo dpkg -i name_programm  # установить ПО скаченное с интернета
sudo dpkg -r name_programm  # удалить ПО скаченное с интернета
```

> Работа с пользователями, группами и правами:
```bash
su user_name  # зайти под другим пользователем
exit  # выйти из под пользователя
who  # кто сейчас ещё онлайн из пользователей
w  # показывает подключенных пользаков и что они делают
cat /etc/passwd  # все пользователи
cat /etc/group  # все группы и кто в них входит
cat /etc/shadow  # пароли пользаков
cat /etc/sudoers  # пользователи с правами на команды
sudo chage пользак  # настроить пароль пользаку
id  # кем мы сейчас работаем
id user_name  # посмотреть права пользователя
newgrb adm  # активная группа
sudo useradd -s /bin/bash -m -d /home/user_name user_name  # создать пользователя
sudo ls -al /home/user_name  # показать файлы юзера
sudo adduser user_name  # создать побыстрому юзера и дать пароль
sudo userdel -r user_name  # удалить юзера и (-r все его файлы)
sudo deluser user_name group_name  # удалить пользователя из группы
sudo passwd user_name  # поменять пароль юзеру
sudo usermod -aG sudo  # добавить пользака в группу sudo
sudo usermod -aG adm user_name  # добавить в список дополнительных групп адм пользователя
sudo groupadd group_name  # создать группу
sudo groupdel group_name  # удалить группу
passwd  # сменить сам себе пароль
sudo chown -R andrey:www-data name_file  # изменить владельца директории
sudo chgrp -R adm name_file  # изменить владельца только группы adm
sudo chmod u=rwx,g=rw,o=r name_file  # для владельца полыне права (чтение, запись, исполнение), для группы (чтение,запись), для остальных (чтение) в name_file
sudo chmod +x name_file  # для всех
sudo chmod 777 name_file  # всё для всех
last  # посмотреть кто заходил в систему из пользователей за последнее время
```

> Работа с директориями:
```bash
mkdir name_directory  # создать директорию
ls -d  # показать только директории
cp -R directory other_directory  # скопировать директорию (с вложенными в неё файлами) в другую директорию
rm -R name_directory  # удалить директорию
```

> Работа с файлами:
```bash
cat file  # показать что в файле
nano -l file  # редактировать файл -l добавляет отображение строк (Ctrl+O сохранить изменения, Ctrl+X закрыть редактирование)
more file  # показать что в файле (q для выхода из режима чтения)
less file  # просмотр содержимого файла (/ для поиска, как ctrl+f в windows), (q для выхода)
touch file.txt  # создать файл
cp file.txt ~/var/  # скопировать файл в другую директорию
rm file.txt  # удалить файл
mv file.txt .new_file_name  # переименовать файл (. сделать его скрытым)
mv file.txt ~/Desktop/  # перенести файл в директорию (рабочий стол)
wc file.txt  # показать сколько: строк, слов, символов
wc -l file.txt  # показать только количество строк
wc -w file.txt  # показать только количество слов
wc -m file.txt  # показать только количество символов
sort file.txt  # cat + сортировка по алфавиту
sort -n file.txt  # cat + сортировка по цифрам
cut -d ">" -f 3 file.txt  # cat + делиметр, какое поле
cat file.txt > new_file.txt  # сохранить результат команды в файл
cat file.txt >> new_file.txt  # сохранить и добавить результат команды в файл с уже существующим текстом
ln file.txt file_dupl.txt  # дублировать файл (жесткая ссылка)
ln -s /home/andrey/name_directory name_link  # создать символическую ссылку
echo file.txt  # вывести файл на консоль
echo ????  # вывести файлы с 4 символами
echo ????*  # вывести файлы 4 и больше символов
touch file.txt{01..10}  # создать несколько файлов от 01 до 10
diff file1.txt file2.txt  # сравнить содержимое файлов
file file.txt  # узнать точный формать файла
(дописать) uniq  # удалить дубли
(дописать) -rni  # поиск по содержимому всех файлов
```

> Сочетание клавиш + полезные команды:
```bash
[Ctrl] + Z  # продолжить выполнять процесс в фоновом режиме (fg - вернуть на экран)
*  # означает все
?  # означает воспринять один любой символ
-v  # verbose - показывать процесс выполнения команды
|  # пайп - выполнить одну команду за другой
.  # текущая директория
..  # предыдущая директория
&&  # выполнить команды следом друг за другом
sudo visudo или nano /etc/sudoers  # добавить строчку в самый низ: andrey ALL=(ALL) NOPASSWD: ALL  # теперь пользователь может выполнять sudo без пароля
cd /var/log $ head syslog  # перейти в папку и показать первые 10 строчек лога
cd /var/log $ tail -n 20 syslog  # перейти в папку и показать последние  (-n 20) 20 строк
nano /etc/ssh/sshd_config -> (Port 22 меняем на 2222) (PermitRootLogin yes меняем на no)  # настроить ssh, отключить вход под root, изменить порт по умолчанию
.Directory  # значит конфигурационные директории
```

> Нужные папки:
```bash
cat /etc/passwd  # все пользователи
cat /etc/shadow  # пароли пользаков
cat /etc/sudoers  # пользователи с правами на команды (например sudo)
cat /etc/apt/sources.list  # репозиторий ubuntu
cd /var/log/  # хранение логов в данной папке
cat /etc/hosts  # файл с параметрами DNS
cat /etc/netplan/00-installer-config.yaml  # файл с конфигами сети
cat /etc/fstab  # файловые системы
cat /etc/hostname  # изменить имя ПК
cat /etc/hosts  # посмотреть имя и ip локалхоста и нашей тачки
cat /etc/rsyslog.conf  # файл с настройками логирования
cat /etc/crontab  # файл crontab
```

> Работа с архивами:
```bash
wget https://....tar.gz  # скачать архив в директорию
tar cvf name.tar name_directory  # создать архив директории с названием name.tar
tar tf name.tar  # посмотреть что находится внутри архива
tar xvf name.tar  # разархивировать архив (или tar -xvpf file.tar)
gzip name.tar  # запаковать/скомпрессировать файл
gungzip name.tar.gz  # распаковать файл
xz name.tar  # средне запаковать/скомпрессировать файл
unxz name.tar.xz  # распаковать файл
bzip2 name.tar  # сильно запаковать/скомпрессировать файл
bunzip2 name.tar.bz2  # распаковать файл
tar cvzf name.gz name_directory  # создать архив директории и запаковать его с помощью gzip
tar xvf name.gz  # распаковать файл gz
tar cvJf name.xz name_directory  # создать архив директории и запаковать его с помощью xz
tar xvf name.xz  # распаковать файл xz
tar cvjf name.bz2 name_directory  # создать архив директории и запаковать его с помощью bzip
tar xvf name.bz2  # распаковать файл bz2
zip -r name.zip name_directory  # создать архив zip директории с названием name.zip
unzip name.zip  # распаковать файл zip
```

> Работа с процессами:
```bash
ps -afx или ps -aux  # показать все запущенные процессы всех пользователей
kill -9 "id ps -afx"  # убить процесс (KILL)
kill -15 "id ps -afx"  # корректно завершить процесс (TERM)
ps -T -p [№процесса]  # показать потоки процесса
ps -efl  # посмотреть список процессов с PID
jobs  # посмотреть есть ли приостановленные процессы
```

> Работа с сетью и портами:
```bash
ifconfig  # вся информация по сети
ip addr show  # показать адаптеры и ip
ip -c a  # инфа по сети (сам пользуюсь этой)
route  # куда пересылаются пакеты
ping 8.8.8.8  # достучаться по сети до ip
host -t a ya.ru  # показать ip сайта
dig ya.ru  # показать ip сайта (подробнее)
netstat  # показать открытые порты
lsof  # показать открытые порты
sudo ufw allow 22  # открыть порт
ip r  # показать проведеные ip
sudo ss -nutlp  # показать какие сокеты открыты
sudo ss -tulpan  # полностью все открытые подключения
resolvectl  # посмотреть параметры DNS
```

> SSH:
```bash
sudo apt-get install openssh-server  # ставим на сервер тачку
sudo systemctl status ssh  # проверить работает ли сервис ssh
sudo systemctl start ssh  # включить сервис ssh
ssh you_ip  # обычный способ подключиться по ssh к тачке
ssh -p 22 user_name@you_ip  # подключиться по ssh к тачке
exit  # выйти из сессии
```
> Генерация ключей ssh:
```bash
ssh-keygen  # сгенерировать пару ключей (со стороны АРМа)
ssh-copy-id  # Я перенёс ключ паблик вручную в /.ssh в файл authorized_keys (далее нужно было перелогиниться)
cd /etc/ssh → sshd_config  # можно изменить порт (на 61022 например)
```

> GREP:
```bash
grep text ./*  # поиск файлов, в которых есть текст text, в текущей директории
grep -i text ./*  # поиск файлов, в которых есть текст text, в текущей директории (-i означает игнорировать регистр)
grep andrey /etc/* &> all_log.txt  # отправить все ответы в файл
grep andrey /etc/* > good.txt  # отправить хорошие ответы в файл
grep andrey /etc/* 2> errors_file.txt  # отправить плохие ответы в файл
grep andrey /etc/* 2> /dev/null  # отправить в никуда
grep andrey /etc/* > good.txt 2> bad.txt  # отправить хорошие ответы в файл good, а плохие ответы в файл bad
```

> Разбор ls -l:
```bash
-rwxrw-r-- 1 andrey andrey 1024 Nov 22 18:34 file.txt  # пример
-  # означает файл
d  # означает директория
l  # означает линк (ссылка)
rwx  # права на r-чтение, w-редактирование, x-исполнение
rwx|rw-|r--  # первые права доступа к пользователю, вторые права доступа пользователям, третьи права доступа ко всем
1 или 2 и более  # означает количество линков
andrey  # пользователь и группа кто создал
```

> Just_For_Fun:
```bash
sudo ls -la -R /  # пролистать все диски 
sudo rm -R /  # удалить все что есть на тачке (НИКОГДА НЕ ИСПОЛЬЗУЙТЕ)
```

> Работа с дисками:
```bash
sudo fdisk -l  # показать диски
lsblk  # показать диски с партициями
df -h  # показать диски
sudo cfdisk /dev/sdb  # dos, создаем партицию диска
sudo mkfs.ntfs -f /dev/sdb1  # форматировать диск
sudo nano /etc/fstab  # /dev/sdb1 /media/hdd ntfs default 0 0  # делаем автомонтирование диска
sudo mount /media/hdd  # монитруем диск
ln -s /media/hdd ~/Desktop/HDD  # создаём символическую ссылку с диском на рабочем столе
parted -l  # посмотреть таблицу разделов системы
iostat  # показать загрузку дисковой подсистемы
```

> Команды GRUB:
```bash
grub> ls - посмотреть диски
grub> set prefix=(hd0,1)/boot/grub - взять оба диска и загрузить boot раздел
grub> set root=(hd0,1) - запустить это от рута
grub> ls boot/grub - посмотреть grub.cfg
grub> insmod ext2 - обновить grub (ext2 - файловая сисиетма)
grub> insmod normal - перевести режим grub в норм режим
grub> normal - запуск grub
```



>>> Scripts:
```bash
./script.sh  # запустить скрипт
chmod 777 script_name.sh  # дать права на запуск скрипта
bash script_name.sh  # запуск скрипт, если нет прав X
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
