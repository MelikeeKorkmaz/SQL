# Odev 8
1. Test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.   
2. Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.  
3. Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.  
4. Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

## CEVAPLAR
- 1  

CREATE TABLE employee (  
id INTEGER,  
name VARCHAR(50),  
birthday DATE,  
email VARCHAR(100)  
);

- 2  

Ödev8 klasörü altındaki görsellerde işlemler mevcuttur.

- 3  

UPDATE employee
SET name = 'XXX',
birthday = '1999-05-19',
email = 'XXX'
WHERE id = 4;

UPDATE employee
SET name = 'XXX',
birthday = '1999-07-13',
email = 'XXX'
WHERE name LIKE 'B%z';

UPDATE employee
SET name = 'XXX',
birthday = '1999-07-13',
email = 'XXX'
WHERE birthday = '2024-11-25';

UPDATE employee
SET name = 'XXX',
birthday = '1999-07-13',
email = 'XXX'
WHERE email = 'jshillum0@arstechnica.com';

UPDATE employee
SET name = 'test',
birthday = '1999-07-13',
email = 'XXX'
WHERE id = 15
RETURNING *;

- 4  

DELETE FROM employee
WHERE name = 'XXX'
RETURNING *;

DELETE FROM employee
WHERE birthday = '2024-09-20';

DELETE FROM employee
WHERE email ILIKE 'l%'
RETURNING *;

DELETE FROM employee
WHERE id = 47;

DELETE FROM employee
WHERE name = 'Ethelda Seiler';