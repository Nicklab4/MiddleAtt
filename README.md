# Итоговая контрольная работа
## Информация о проекте
Необходимо организовать систему учета для питомника в котором живут
домашние и вьючные животные.
## Как сдавать проект
Для сдачи проекта необходимо создать отдельный общедоступный
репозиторий(Github, gitlub, или Bitbucket). Разработку вести в этом
репозитории, использовать пул реквесты на изменения. Программа должна
запускаться и работать, ошибок при выполнении программы быть не должно.
Программа, может использоваться в различных системах, поэтому необходимо
разработать класс в виде конструктора
## Задание 1.

1. Используя команду cat в терминале операционной системы Linux, создать
два файла Домашние животные (заполнив файл собаками, кошками,
хомяками) и Вьючные животными заполнив файл Лошадьми, верблюдами и
ослы), а затем объединить их. Просмотреть содержимое созданного файла.
Переименовать файл, дав ему новое имя (Друзья человека).

### Решение:
Создание файлов - Домашние животные (DomesticAnimals) и Вьючные животные (PackAnimals)

(комбинация клавиш Ctrl + d, оканчивает ввод текста)
```
cat >> DomesticAnimals
собаки
кошки
хомяки
```

```
cat >> PackAnimals
лошади
верблюды
ослы
```

Объединение файлов DomesticAnimals и PackAnimals в файл NewText
```
cat DomesticAnimals PackAnimals > NewText
```

Переименование файла NewText в файл HumanFriends
```
mv NewText HumanFriends
```

Просмотр файла HumanFriends
```
cat HumanFriends
```

## Задание 2.
2. Создать директорию, переместить файл туда.

### Решение:
Создать директорию animal

```
mkdir animal
```

Переместить файл Animals в директорию animal
```
mv Animals animal/Animals
```

## Задание 3.
3. Подключить дополнительный репозиторий MySQL. Установить любой пакет
из этого репозитория.
### Решение:

Скачивание deb пакета с официального сайта разработчиков MySQL
```
wget https://dev.mysql.com/get/mysql-apt-config_0.8.33-1_all.deb
```
Установка пакета mysql-apt-config_0.8.33-1_all.deb
```
sudo dpkg -i mysql-apt-config*
```
Обновление списка пакетов в репозиториях
```
sudo apt update
```
Установка клиента и сервера MySQL
```
sudo apt install mysql-server mysql-client
```

4. Установить и удалить deb-пакет с помощью dpkg.

6. Выложить историю команд в терминале ubuntu

7. Нарисовать диаграмму, в которой есть класс родительский класс, домашние
животные и вьючные животные, в составы которых в случае домашних
животных войдут классы: собаки, кошки, хомяки, а в класс вьючные животные
войдут: Лошади, верблюды и ослы).

8. В подключенном MySQL репозитории создать базу данных “Друзья
человека”

9. Создать таблицы с иерархией из диаграммы в БД

10. Заполнить низкоуровневые таблицы именами(животных), командами
которые они выполняют и датами рождения

11. Удалив из таблицы верблюдов, т.к. верблюдов решили перевезти в другой
питомник на зимовку. Объединить таблицы лошади, и ослы в одну таблицу.

12. Создать новую таблицу “молодые животные” в которую попадут все
животные старше 1 года, но младше 3 лет и в отдельном столбце с точностью
до месяца подсчитать возраст животных в новой таблице

13. Объединить все таблицы в одну, при этом сохраняя поля, указывающие на
прошлую принадлежность к старым таблицам.

14. Создать класс с инкапсуляцией методов и наследованием по диаграмме.

15. Написать программу, имитирующую работу реестра домашних животных.
В программе должен быть реализован следующий функционал:

    - Завести новое животное

    - Определять животное в правильный класс

    - Увидеть список команд, которое выполняет животное

    - Обучить животное новым командам

    - Реализовать навигацию по меню

16. Создайте класс Счетчик, у которого есть метод add(), увеличивающий̆
значение внутренней̆int переменной̆на 1 при нажатие “Завести новое
животное” Сделайте так, чтобы с объектом такого типа можно было работать в
блоке try-with-resources. Нужно бросить исключение, если работа с объектом
типа счетчик была не в ресурсном try и/или ресурс остался открыт. Значение
считать в ресурсе try, если при заведения животного заполнены все поля.
