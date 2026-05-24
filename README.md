<div align="center">

# 🖥️ Лабораторная работа №1

## Командная строка Windows

Вариант 1 | Дата: май 2026

</div>

---

## 📍 Цель работы

> Развитие профессиональных навыков работы в командной строке Windows

---

## 📋 Список задач

| № | Задача | Статус |
|:-:|--------|:------:|
| 1 | Создать дерево каталогов в Temp | ✅ |
| 2 | В A2 создать B4, B5, удалить B2 | ✅ |
| 3 | В Personal создать Name.txt, Date.txt, School.txt | ✅ |
| 4 | В University создать Name.txt и Mark.txt | ✅ |
| 5 | В Hobby создать hobby.txt | ✅ |
| 6 | Скопировать hobby.txt в A2 → переименовать в Lab_1.txt | ✅ |
| 7 | Создать копию файла и удалить её | ✅ |
| 8 | Очистить экран (cls) | ✅ |
| 9 | Вывести содержимое всех файлов из Personal | ✅ |
| 10 | Отсортировать файлы в Personal по имени | ✅ |
| 11 | Объединить файлы в all.txt и вывести | ✅ |
| 12 | Добавить год рождения в all.txt | ✅ |
| 13 | Скопировать all.txt в A1 | ✅ |
| 14 | Удалить каталоги с буквой А или цифрой 2 | ✅ |
| 15 | Изменить строку приглашения на системную дату | ✅ |

---

## 🚀 Ход выполнения

### 1️⃣ Создание дерева каталогов

`bash
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

### 6. Копирование hobby.txt в A2 и переименование


copy hobby.txt ..\A2
cd ..\A2
ren hobby.txt Lab_1.txt
### 7. Создание копии и её удаление

copy Lab_1.txt copy_Lab_1.txt
del copy_Lab_1.txt
8. Очистка экрана

cls
### 9. Вывод содержимого файлов Personal

cd ..
type Name.txt
type Date.txt
type School.txt
### 10. Сортировка файлов по имени

dir /on
### 11. Объединение файлов в all.txt

copy Name.txt+Date.txt+School.txt all.txt
type all.txt
### 12. Добавление года рождения

echo 2008 >> all.txt
type all.txt
### 13. Копирование all.txt в A1

copy all.txt A1
### 14. Удаление каталогов с буквой А или цифрой 2

cd ..
rd /s /q A1 A2
### 15. Изменение строки приглашения (Вариант 1)


prompt $D
Результат: строка приглашения принимает вид системной даты.

Скриншоты: <img width="1920" height="1080" alt="2026-05-24_19-53-11" src="https://github.com/user-attachments/assets/6eaeccc8-600a-4cc6-99d6-01c372044db5" />
<img width="1920" height="1080" alt="2026-05-24_19-53-19" src="https://github.com/user-attachments/assets/2220780f-7b17-42d9-bd60-c7e3e3f5dd18" />




