# Лабораторная работа №1: Командная строка Windows

Цель работы: Развитие профессиональных навыков работы в командной строке Windows.  
Вариант: 1 (строка приглашения — системная дата).

---

## Задачи

| № | Задача |
|---|--------|
| 1 | Создать дерево каталогов в Temp |
| 2 | В каталоге A2 создать B4, B5, удалить B2 |
| 3 | В Personal создать Name.txt, Date.txt, School.txt |
| 4 | В University создать Name.txt (вуз, специальность) и Mark.txt (оценки, сумма) |
| 5 | В Hobby создать hobby.txt |
| 6 | Скопировать hobby.txt в A2 → переименовать в Lab_1.txt |
| 7 | В A2 скопировать Lab_1.txt и удалить копию |
| 8 | Очистить экран (cls) |
| 9 | Вывести содержимое всех файлов из Personal |
| 10 | Отсортировать файлы в Personal по имени |
| 11 | Объединить файлы Personal в all.txt и вывести |
| 12 | Добавить год рождения в all.txt и вывести |
| 13 | Скопировать all.txt в A1 |
| 14 | Удалить все каталоги с буквой А или цифрой 2 |
| 15 | Изменить строку приглашения по варианту 1 (системная дата) |

---

## Ход работы

### 1. Создание дерева каталогов

cd %TEMP%
md Personal\A1
md Personal\A2\B1
md Personal\A2\B2
md Personal\A2\B3
md Personal\University
md Personal\Hobby

### 2. Создание B4, B5 и удаление B2

md Personal\A2\B4
md Personal\A2\B5
rd Personal\A2\B2

### 3. Создание файлов в Personal

cd Personal
copy con Name.txt

Ввести ФИО

copy con Date.txt

Дата рождения 

copy con School.txt

Образовательное учреждение

### 4. Создание файлов в University

cd University
copy con Name.txt

Вуз и специальность

copy con Mark.txt

Оценки и суммы баллов

### 5. Создание файлов в Hobby

cd ..\Hobby
copy con hobby.txt

Увлечения

6. Копирование hobby.txt в A2 и переименование


copy hobby.txt ..\A2
cd ..\A2
ren hobby.txt Lab_1.txt
7. Создание копии и её удаление

copy Lab_1.txt copy_Lab_1.txt
del copy_Lab_1.txt
8. Очистка экрана

cls
9. Вывод содержимого файлов Personal

cd ..
type Name.txt
type Date.txt
type School.txt
10. Сортировка файлов по имени

dir /on
11. Объединение файлов в all.txt

copy Name.txt+Date.txt+School.txt all.txt
type all.txt
12. Добавление года рождения

echo 2008 >> all.txt
type all.txt
13. Копирование all.txt в A1

copy all.txt A1
14. Удаление каталогов с буквой А или цифрой 2

cd ..
rd /s /q A1 A2
15. Изменение строки приглашения (Вариант 1)

prompt $D
Результат: строка приглашения принимает вид системной даты.


