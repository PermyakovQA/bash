# bash
Работа с bash

cd ~                                                                                    # открыть домашнюю директорию

pwd                                                                                     # определить имя папки

mkdir test1                                                                             # создать каталог test1

cd test1                                                                                # перейти в test1

touch 1 2 3                                                                             # создать файлы 1,2,3

ls                                                                                      # проверить содержимое test1

cd ~                                                                                    # перейти в домашнюю директорию

mkdir test2                                                                             # создать test2

rmdir test2                                                                             # удалить test2

rm test1/2                                                                              # удалить файл 2 в test1

mkdir test3                                                                             # создать test3 и два файла в ней
touch test3/f1 test3/f2

rm -r test3                                                                             # удалить test3 

mkdir test4                                                                             # создать test4

mv test1/1 test1/3 test4                                                                # переместить 1 и 3 из test1 в test4

echo "line" >> test4/1                                                                  # добавить в файл 1 три строки со словом "line"
echo "line" >> test4/1
echo "line" >> test4/1

cat test4/1                                                                             # показать содержимое 1

echo "line" >> test4/3                                                                  # добавить в файл 3 три строки со словом "line"
echo "line" >> test4/3
echo "line" >> test4/3

cat test4/1 test4/3                                                                     # показать 1 и 3 сразу

sed -i 's/.*/newtext/' test4/1                                                          # заменить все строки в файле 1 (пример: заменить на текст newtext)

cd ~                                            					                              # зайти в домашнюю директорию

mkdir test3                                     					                              # создать папку test3

printf "row1\nrow2\nrow3\nrow4\n" > test3/4     					                              # создать файлы 4 5 6 с 4 строками (row1,row2,row3,row4)
printf "row1\nrow2\nrow3\nrow4\n" > test3/5
printf "row1\nrow2\nrow3\nrow4\n" > test3/6

grep "row2" test3/5                             					                              # найти строку row2 в файле 5

grep -r "row" test3                            					 	                              # найти строку row во всей папке test3

grep -c "row" test3/6                           					                              # посчитать сколько строк row в файле 6

find test3 -name 5                              					                              # найти файл 5 внутри test3

find test3 -name 5 -delete                      					                              # удалить файл 5 с помощью find

echo "test" > test3/4                           					                              # добавить слово test в 4 (без сохранения содержимого)

sed -i 's/test/fail/' test3/4                   					                              # заменить слово test в файле 4 на fail

echo "test" >> test3/4                          					                              # добавить test в файл 4 сохранив содержимое

ps aux                                                                                  # показать все процессы всех пользователей, не только в консоли

kill 666                                                                                # убить процесс 666

ping rusau.net                                                                          # проверить доступность rusau.net

ping -n 5 rusau.net                                                                     # отправить 5 пакетов на rusau.net

curl -X GET "https://petstore.swagger.io/v2/pet/findByStatus?status=delivered"          # GET — питомцы любого статуса

curl -X POST "https://petstore.swagger.io/v2/user" \                                    # POST — создать нового пользователя
  -H "Content-Type: application/json" \
  -d '{"id":89,"username":"Testuser","firstName":"Aleksey","lastName":"Nikitin","email":"valid@test.com","password":"testuser89","phone":"12345","userStatus":1}'
