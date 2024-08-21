SQL запити для зв'язаних таблиць
 - Wine
 - Customers
 - Sales
 - Purchases

Таблиця Wine (Вино):
WineID (INT, PRIMARY KEY): Унікальний ідентифікатор вина.
Name (NVARCHAR(255), NOT NULL): Назва вина.
Description (NVARCHAR(MAX)): Опис вина.
Type (NVARCHAR(50)): Тип вина (червоне, біле, і т. д.).
Country (NVARCHAR(50)): Країна виробництва вина.
Price (DECIMAL(10, 2)): Ціна за пляшку вина.

Таблиця Customers (Клієнти):
CustomerID (INT, PRIMARY KEY): Унікальний ідентифікатор клієнта.
FirstName (NVARCHAR(50)): Ім'я клієнта.
LastName (NVARCHAR(50)): Прізвище клієнта.
Email (NVARCHAR(100)): Адреса електронної пошти клієнта.
Phone (NVARCHAR(15)): Номер телефону клієнта.
Address (NVARCHAR(MAX)): Адреса клієнта.

Таблиця Sales (Продажі):
SaleID (INT, PRIMARY KEY): Унікальний ідентифікатор продажу.
WineID (INT, FOREIGN KEY): Посилання на відповідне вино в таблиці Wine.
SaleDate (DATE): Дата продажу.
QuantitySold (INT): Кількість проданих пляшок.
TotalAmount (DECIMAL(10, 2)): Загальна сума продажу.
CustomerID (INT, FOREIGN KEY): Посилання на клієнта в таблиці Customers.


Таблиця Purchases (Закупки):
PurchaseID (INT, PRIMARY KEY): Унікальний ідентифікатор закупки.
WineID (INT, FOREIGN KEY): Посилання на відповідне вино в таблиці Wine.
PurchaseDate (DATE): Дата закупки.
QuantityPurchased (INT): Кількість закуплених пляшок.
Cost (DECIMAL(10, 2)): Вартість закупки.

Ці поля та їх типи дозволять створити структуру бази даних для винного магазину та внести та відстежувати всю необхідну інформацію про вина, продажі, закупки та клієнтів.
