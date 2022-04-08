# Orta Seviye Java ile Web Development Patikasi
Orta Seviye Java ile Web Development Patikası -> SQL -> Ödev 12

# ÖDEV 12
Merhabalar,

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

1. film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
2. film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
3. film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.
4. payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.

Kolay Gelsin.

# CEVAPLAR
1. SELECT COUNT(*) FROM film WHERE length > (SELECT AVG(length) FROM film)
2. SELECT COUNT(*) FROM film WHERE rental_rate =  (SELECT MAX(rental_rate) FROM film)
3. SELECT title FROM film WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) AND replacement_cost = (SELECT MIN(replacement_cost) FROM film) ORDER BY title
4. SELECT customer.first_name, customer.last_name FROM customer INNER JOIN payment ON customer.customer_id = payment.customer_id WHERE payment.amount = (SELECT MAX(amount) FROM payment) ORDER BY payment DESC
