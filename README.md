### Выполнение базовых команд Bash
---

### Задание 1

| Задача                                                                 | Команда                           |
| -----------------------------------------------------------------------| :-------------------------------: |
| Зайти в домашнюю директорию через терминал                             | cd ~                              |
| Создать папку test 3                                                   | pwd                               |
| Создать внутри этой папки каталог с именем test1                       | mkdir test1                       |
| Перейти в папку test1                                                  | cd test1                          |
| Создать файл 1,2 и 3 внутри каталога test1                             | touch 1.txt 2.txt 3.txt           |
| Проверить содержимое каталога test1                                    | ls                                |
| Перейти в домашнюю директорию                                          | cd ~                              |
| Создать папку test2 внутри домашней директории                         | mkdir test2                       |
| Удалить папку test2                                                    | rmdir test2                       |
| Удалить файл 2 из папки test1                                          | rm test1/2.txt                    |
| Создать папку в домашней директории test3 и <br/> добавить в нее два файла   | mkdir test3 <br/> touch test3/one.txt test3/two.txt <br/> cd ..         |       
| Удалить папку test3                                                    | rm -r test3                       |
| Создать папку test4 в домашней директории                              | mkdir test4                       |
| Переместить файлы 1 и 3 из папки test1 в папку test4                   | mv test1/1.txt test1/3.txt test4  |
| Добавить в файл 1 три строки со словами line                           | echo "line" > test4/1.txt <br/> echo "line" >> test4/1.txt <br/> echo "line" >> test4/1.txt       |
| Посмотреть содержимое файла 1                                          | cat test4/1.txt                   |
| Добавьте в файл 3 три строки со словами line                           | echo "line" > test4/3.txt <br/> echo "line" > test4/3.txt <br/> echo "line" > test4/3.txt        |
| Просмотрите содержимое двух файлов (1 и 3) сразу                       | cat test4/1.txt test4/3.txt       |
| Используя один из редакторов замените все строки в файле 1             | nano test4/1.txt <br/> Ctrl + \ для Replace <br/> Search (to replace): "line" <br/> Replace with: "string"    |

### Задание 2

| Задача                                                                 | Команда                           |
| -----------------------------------------------------------------------| :-------------------------------: |
| Зайти в домашнюю директорию через терминал                             | cd ~                              |
| Создать папку test 3                                                   |   mkdir test_3                    |
| Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых </br> должно быть по 4 строки row1, row2, row3, row4 | touch test_3/4.txt test_3/5.txt test_3/6.txt </br> echo -e "row1\nrow2\nrow3\nrow4 " > test_3/4.txt </br> echo -e "row1\nrow2\nrow3\nrow4 " > test_3/5.txt </br> echo -e "row1\nrow2\nrow3\nrow4 " > test_3/6.txt      |
| Найдите строку row2 в файле 5                                              | grep "row2" test_3/5.txt     |
| Найдите строку row в папке test3                                      | grep "row" test_3/*.txt      |
| Посчитайте сколько строк с содержимым row в файле 6                                      | grep -c "row" test_3/6.txt      |
| Найдите файл 5 внутри папки test3                                       | find test_3 -name "5.txt       |
| Используя команду find, удалите файл 5                                      | find . -name "5.txt" -delete "5.txt"       |
| Используя команду echo, добавьте слово test в файл 4                                      | echo "test" >> test_3/4.txt      |
| Замените слово test в файле 4 на fail                                      | sed -i 's/test/fail/g' test_3/4.txt       |
| Добавьте в файл 4 слово test так, чтобы сохранилось содержимое                                      | echo "test" >> test_3/4.txt    |
| Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе                                      | ps -W       |
| Убейте любой неважный процесс в консоли                                                    | kill 69988       |
| Узнайте доступность ресурса rusau.net, используя ping                                      | ping rusau.net     |
| Отправьте 5 пакетов на сайт rusau.net                                      | ping -c 5 rusau.net  |
| Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/       | curl https://petstore.swagger.io/v2/pet/findByStatus?status=available      |
| Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/                                      | curl -X POST 'https://petstore.swagger.io/v2/user' <br/> -H 'accept: application/json' <br/> -H 'Content-Type: application/json' <br/> -d '{ <br/> "id": 0, <br/> "username": "AvocadoKing1", <br/> "firstName": "Avic", <br/> "lastName": "Kingovich", <br/> "email": "avocadok@mail.ru", <br/> "password": "avK1234567", <br/> "phone": "string", <br/> "userStatus": 0 <br/> }'       |
