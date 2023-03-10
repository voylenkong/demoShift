Программа сортировки слиянием нескольких файлов.
Входные файлы содержат данные одного из двух видов: целые числа или строки. Данные записаны
в столбик (каждая строка файла – новый элемент). Строки могут содержать любые не пробельные
символы, строки с пробелами считаются ошибочными.

Результатом работы программы должен являться новый файл с объединенным содержимым
входных файлов, отсортированным по возрастанию или убыванию путем сортировки слиянием.

Уточнения запуска программы:
1. Имя выходного файла должно идти первым, затем имена входных файлов. out.txt идет раньше in.txt.
   Например: java -jar demoShift.jar -i -a out.txt in.txt
2. Можно не делать перечисление входных файлов, а указать каталог.
   Например: java -jar demoShift.jar -i -a tmp\
   В случае если во входном наборе файлов первым идет каталог остальные входные файлы отбрасываются (in2.txt in3.txt)
3. Имеются допоплнительные ключи -f и -b.
   Ключ -f указывает максимальный размер файла (в байтах). Максимальный размер файла - это размер, до размера которого не будет происходить его фрагментация.
   Ключ -b указывает максимальный размер буфера (в строках). Максимальный размер буфера - это размер фрагмента при фрагментации.
   Например: пришли на вход два файла объемом 10Gb. Объем оперативной памяти не позволит провести его сортировку.
   Опцией -f укажем размер файла до которого не будем проводить фрагментацию (-f 1073741824).
   Опцией -b укажем размер фрагмента файла (-b 50000000).
   Таким образом наш входной файл разобъем на фрагменты.


Информация по технологиям:
1. Java 11
2. Maven 3.8.1
3. Project Lombok
   https://mvnrepository.com/artifact/org.projectlombok/lombok/1.18.24
4. Apache Commons CLI
   https://mvnrepository.com/artifact/commons-cli/commons-cli/1.5.0
5. Apache Commons IO
   https://mvnrepository.com/artifact/commons-io/commons-io/2.11.0