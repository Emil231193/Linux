1. Написать скрипт очистки директорий. На вход принимает путь к директории. Если директория существует, то удаляет в ней все файлы с расширениями .bak, .tmp, .backup. Если директории нет, то выводит ошибку.
#!/bin/bash
if [ -d $1 ]
then
echo "Got it!"
for file in $1/*
do
if [[ $file == *.bak ]] || [[ $file == *.tmp ]] || [[ $file == *.backup ]]
then
rm $file
fi
done
echo "Done"
else
echo "Directory does not exist"
fi
