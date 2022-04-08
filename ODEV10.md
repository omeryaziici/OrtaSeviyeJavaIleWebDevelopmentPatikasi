# Orta Seviye Java ile Web Development Patikasi
Orta Seviye Java ile Web Development Patikası -> SQL -> Ödev 10

# ÖDEV 10
Merhabalar,

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1. city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.
2. customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.
3. customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.

Kolay Gelsin.

# CEVAPLAR
1. SELECT city.city, country.country FROM city LEFT JOIN country ON city.country_id = country.country_id
2. SELECT first_name,last_name FROM customer RIGHT JOIN payment ON customer.customer_id = payment.customer_id
3. SELECT first_name,last_name FROM customer FULL JOIN rental ON customer.customer_id = rental.customer_id
