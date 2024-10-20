Команда **chmod** используется для изменения прав доступа в к файлам и каталогам. Эти права определяют, кто может читать, записывать и выполнять файлы. Права можно задавать для трёх категорий пользователей:
1. Владелец (User, **u**) - владелец файла
2. Группа (Group, **g**) - группа пользователей, к которой принаджежит владелец
3. Остальные (Others, **o**) - все остальные пользователи системы.

Каждая категория пользователей может иметь три типа прав:
1. Чтение (Read, **r**) - возможность просматривать содержимое файла или список файлов в директории
2. Запись (Write, **w**) - возможность изменять файл или содержимое директории.
3. Исполнение (Execute, **x**) - возможность запускать файл как программу или перемещаться по директории.

Права можно задавать в двух форматах: Символьный (**r**, **w**, **x**) и Цифровой (с помощью восьмеричных чисел).

Операции:

- `+` — добавить права.
- `-` — убрать права.
- `=` — назначить точные права, убрав предыдущие.

Примеры символьного формата:

- `chmod u+x file` — добавить право на исполнение для владельца.
- `chmod g-w file` — убрать право на запись для группы.
- `chmod o=r file` — установить право только на чтение для остальных пользователей.

Цифровой формат:
Восьмеричная система используется для задания прав числовыми значениями. Каждое право имеет своё числовое представление:

- **r** (чтение) = `4`
- **w** (запись) = `2`
- **x** (исполнение) = `1`

Число прав для каждой категории пользователей складывается. Например:

- **7** = `rwx` (чтение, запись и исполнение).
- **6** = `rw-` (чтение и запись).
- **5** = `r-x` (чтение и исполнение).
- **4** = `r--` (только чтение).

Формат записи состоит из трёх цифр:

1. Права владельца.
2. Права группы.
3. Права остальных.

Пример:

- `chmod 755 file` — владелец может читать, писать и выполнять (7 = `rwx`), группа и остальные могут только читать и выполнять (5 = `r-x`).