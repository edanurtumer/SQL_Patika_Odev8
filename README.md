# SQL_Patika_Odev8
pgadmin4_Odev8

### 1- test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
CREATE TABLE employee  (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  birthday DATE,
  email VARCHAR(50) NOT NULL
); 

### 2- Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
  

### 3- Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
  #### 1- id değeri 1 olan kişinin emailini değiştir.
  UPDATE Employee
  SET email = 'test@test.com'
  #### 2- İsmi 'A' ile başlayan çalışanların doğum gününü bugün olarak güncelle.
  UPDATE employee
  SET birthday = CURRENT_DATE
  WHERE name ILIKE 'A%'
  #### 3- id değeri 7 olan kişinin ismini Halid olarak güncelle.
  UPDATE Musteriler
  SET name = ‘Halid’
  WHERE id = 7;
  #### 4-ID değeri çift olan çalışanların isimlerini büyük yap.
  UPDATE employee
  SET name=upper(name)
  WHERE id % 2 = 0
  #### 5-Name alanı "e" ile biten çalışanların doğum günün bugün yap.
  UPDATE employee
  SET birthday = CURRENT_DATE
  WHERE name ILIKE '%e'

### 4- Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
  #### 1-İsmi 'a' ile biten çalışanları sil.
  DELETE FROM employee
  WHERE name LIKE '%a'
  #### 2-İsminin 'an' geçen kişileri sil.
  DELETE FROM employee
  WHERE name ILIKE '%an%'
  #### 3- id'si 3 olanı sil.
  DELETE FROM Employees
  WHERE ID = 3;
  #### 4- id 15 olanı sil.
  DELETE FROM employee 
  WHERE  id=15
  #### 5- isim Ali olan kişileri sil.
  DELETE FROM Employee 
  WHERE name=’Ali’;
