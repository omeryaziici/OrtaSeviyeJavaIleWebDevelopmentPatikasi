# Orta Seviye Java ile Web Development Patikasi
Orta Seviye Java ile Web Development Patikası -> SQL -> Ödev 8

# ÖDEV 8
Merhabalar,

1. test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
2. Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
3. Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
4. Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
Kolay Gelsin.

# CEVAPLAR
1. CREATE table employee (
	id SERIAL PRIMARY KEY,
	name VARCHAR(50) Not NULL,
	birthday Date,
	email VARCHAR(100)
);
2. insert into employee (name, birthday, email) values ('Ömer', '07/02/1994', 'yaziiciomer@gmail.com'); .....
3. UPDATE employee SET name = 'OMER' WHERE id = 1;
4. DELETE FROM employee WHERE id=1 RETURNING *
