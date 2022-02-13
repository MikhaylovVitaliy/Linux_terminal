## __Linux_terminal Group_27 08.02.2022 Terminal_1__

### __1. Посмотреть где я__
```
$ pwd
/c/users/vit/QA_Vadim
```

### __2. Создать папку__
```
$ mkdir 001
```

### __3. Зайти в папку__
```
$ cd 001
```

### __4. Создать 3 папки__
```
$ mkdir folder_1 folder_2 folder_3
```

### __5. Зайти в любоую папку__
```
$ cd folder_1
```

### __6. Создать 5 файлов (3 txt, 2 json)__
```
$ touch file_1.txt file_2.txt file_3.txt file_1.json file_2.json
```

### __7. Создать 3 папки__
```
$ mkdir folder_1 folder_2 folder_3
```

### __8. Вывести список содержимого папки__
```
$ ls
file_1.json  file_1.txt  file_2.json  file_2.txt  file_3.txt  folder_1/  folder_2/  folder_3/
```

### __9. + Открыть любой txt файл__
### __10. + написать туда что-нибудь, любой текст__
### __11. + сохранить и выйти__
```
$ vim vim.txt

$ cat vim.txt
1. Posmotret' gde ya
2. Sozdat' papku
3. Zaiti v papku
4. Sozdat' 3 papki
5. Zaiti v lubuyu papku
6. Sozdat' 5 failov
7. Sozdat' 3 papki
8. Hvatit :)))))
```

### __12. Выйти из папки на уровень выше__
```
$ cd ..
```

___


### __13. переместить любые 2 файла, которые вы создали, в любую другую папку__
```
$ mv file_1.txt file_1.json /c/users/vit/QA_Vadim/001/folder_2/
```

### __14. скопировать любые 2 файла, которые вы создали, в любую другую папку__
```
$ cp file_2.txt file_2.json folder_3/
```

### __15. Найти файл по имени__
```
$ find . -name "vi*"
./vim.txt
```

### __16. просмотреть содержимое в реальном времени (команда grep) изучите как она работает__
```
$ tail -f vim.txt | grep -C1 "lubuyu" vim.txt
4. Sozdat' 3 papki
5. Zaiti v lubuyu papku
6. Sozdat' 5 failov
```

tail -f vim.txt - _выводит файл в реальном времени_ 
grep -C1 _"lubuyu" - ищет в нем "lubuyu" и выводит по одной строке до и после_

### __17. вывести несколько первых строк из текстового файла__
```
$ head -4 vim.txt
1. Posmotret' gde ya
2. Sozdat' papku
3. Zaiti v papku
4. Sozdat' 3 papki
```

### __18. вывести несколько последних строк из текстового файла__
```
$ tail -n 4 vim.txt
5. Zaiti v lubuyu papku
6. Sozdat' 5 failov
7. Sozdat' 3 papki
8. Hvatit :)))))
```

### __19. просмотреть содержимое длинного файла (команда less) изучите как она работает__
```
$ less file_4.log
```

### __20. вывести дату и время__
```
$ date
Thu Feb 10 20:26:25     2022
```

___
___

### __1. Отправить http запрос на сервер__
```
$ curl http://162.55.220.72:5005/terminal-hw-request
$ curl "http://162.55.220.72:5005/get_method?name="Vit"&age="44""
```

### __2. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13__
```sh
#!/usr/bin/bash
cd /c/users/vit/QA_Vadim/001
mkdir Script_1 Script_2 Script_3
cd Script_2
touch script_1.txt script_2.txt script_3.txt script_1.json script_2.json
mkdir 01 02 03
ls
mv script_1.txt script_2.json /c/users/vit/qa_vadim/001/Script_2/02/
```

