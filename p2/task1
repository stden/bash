#!/bin/bash
# Создайте и однократно выполните скрипт 
# (в этом скрипте нельзя использовать условный оператор и операторы проверки свойств и значений), 
# который будет пытаться создать директорию test в домашней директории.
# Если создание директории пройдет успешно, скрипт выведет в файл ~/report сообщение вида "catalog test was created successfully" 
# и создаст в директории test файл с именем Дата_Время_Запуска_Скрипта.
# Затем независимо от результатов предыдущего шага скрипт должен опросить 
# с помощью команды ping хост www.net_nikogo.ru и, если этот хост недоступен, дописать сообщение об ошибке в файл ~/report.

newdir=~/test # Имя каталога для создания
testfile="./"$newdir"/"$(date +"%F_%R") 
report="~/report.txt"
host="www.net_nikogo.ru"
M_CREATEFILE_SUCCESS="catalog test was created successfully"
M_PING_PROBLEM="ping failed"

echo Создаём каталог $newdir
mkdir $newdir && { echo "$M_CREATEFILE_SUCCESS"; echo "$M_CREATEFILE_SUCCESS" > "$report"; touch "$testfile"; } || ping -q -c 1 -w 1 "google.com" | grep -qo "rtt" && echo $M_PING_PROBLEM;

exit 1