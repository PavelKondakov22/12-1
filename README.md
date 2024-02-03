# 12-1 Кондаков Павел "Базы данных"

### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

### **Ответ:**  
 1. Сотрудники  
:small_orange_diamond: Идентификатор, первичный ключ, serial  
:small_orange_diamond: Фамилия, varchar(50)  
:small_orange_diamond: Имя, varchar(50)  
:small_orange_diamond: Отчество, varchar(50)  
:small_orange_diamond: Оклад, float(2)  
:small_orange_diamond: Дата найма, date  
:small_orange_diamond: Идентификатор структурного подразделения, внешний ключ, integer  
:small_orange_diamond: Идентификатор должности, внешний ключ, integer  
:small_orange_diamond: Идентификатор филиала, внешний ключ, integer  
2. Проекты  
:small_orange_diamond: Идентификатор, первичный ключ, serial  
:small_orange_diamond: Название проекта, varchar(50), UNIQUE
3. Должности  
:small_orange_diamond: Идентификатор, первичный ключ, serial  
:small_orange_diamond: Название должности, varchar(50), UNIQUE 
4. Структурное подразделение  
:small_orange_diamond: Идентификатор, первичный ключ, serial  
:small_orange_diamond: Название подразделения, varchar(50), UNIQUE  
:small_orange_diamond: Индентификатор типа подразделения, внешний ключ, integer  
5. Тип подразделения  
:small_orange_diamond: Идентификатор, первичный ключ, serial  
:small_orange_diamond: Название типа подразделения, varchar(50), UNIQUE 
6. Филиал  
:small_orange_diamond: Идентификатор, первичный ключ, serial  
:small_orange_diamond: Адрес филиала, varchar(50)  
:small_orange_diamond: Город филиала, varchar(50)  
:small_orange_diamond: Регион филиала, varchar(50)  
7. Сводная таблица сотрудники-проекты  
:small_orange_diamond: Первичный составной ключ  
:small_orange_diamond: идентификатор сотрудника, внешний ключ, integer  
:small_orange_diamond: идентификатор проекта, внешний ключ, integer  
