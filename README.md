
<img src="https://assets-global.website-files.com/6097e0eca1e87557da031fef/63739a32259566fc9428cb1d_Deneme.png" alt="alt text"  width="353"/>


 # ⚡ SQL Eğitim Patika ⚡

> #### Bu repo'da [Patika](https://academy.patika.dev/) Platformu üzerinde [Gürcan Çekiç](https://www.linkedin.com/in/gurcancekic/) Hocamızın vermiş olduğu. SQL eğitiminde yapmış olduğumuz ödevler bulunmaktadır.

<br>

- **SQL Ödev 01 | WHERE ve Karşılaştırma & Mantıksal - <a href="https://github.com/dorukhanbekdur">Tıklayın. </a>**
- **SQL Ödev 02 | BETWEEN & IN - <a href="https://github.com/dorukhanbekdur">Tıklayın.</a>**
- **SQL Ödev 03 | LIKE & ILIKE - <a href="https://github.com/dorukhanbekdur">Tıklayın.</a>**
- **SQL Ödev 04 | DISTINCT & COUNT - <a href="https://github.com/dorukhanbekdur">Tıklayın.</a>**
- **SQL Ödev 05 | ORDER BY | LIMIT & OFFSET - <a href="https://github.com/dorukhanbekdur">Tıklayın.</a>**
- **SQL Ödev 06 | Aggregate Fonksiyonlar - <a href="https://github.com/dorukhanbekdur">Tıklayın.</a>**
- **SQL Ödev 07 | GROUP BY | HAVING - <a href="https://github.com/dorukhanbekdur">Tıklayın.</a>**
- **SQL Ödev 08 | Tablo Oluşturmak | Verileri Güncellemek - <a href="https://github.com/dorukhanbekdur">Tıklayın.</a>**
 
<br>

## 📄 | SQL Ödev 01 | WHERE ve Karşılaştırma & Mantıksal Operatörler 

<br>
<br>
<br>

Q1 -) <strong> film </strong> tablosunda bulunan <strong> title</strong> ve <strong> description</strong> 
sütunlarındaki verileri sıralayınız.

```
SELECT title, description FROM film;
```

<br>
<br>
<br>

Q2-) <strong>film</strong>  tablosunda bulunan tüm sütunlardaki verileri film uzunluğu <strong>(length)</strong>  60 dan büyük <strong>VE</strong>  75 ten küçük olma koşullarıyla sıralayınız.

```
SELECT * FROM film
WHERE length > 60 AND length < 75;
```
<br>
<br>
<br>

Q3-)  <strong>film</strong> tablosunda bulunan tüm sütunlardaki verileri  <strong>rental_rate</strong> 0.99  <strong>VE</strong>  <strong>replacement_cost</strong> 12.99  <strong>VEYA</strong> 28.99 olma koşullarıyla sıralayınız.

```
SELECT * FROM film
WHERE rental_rate = 0.99 AND replacement_cost = 12.99 
OR replacement_cost = 28.99;
```
<br>
<br>
<br>

Q4-) <strong>customer</strong> tablosunda bulunan <strong>first_name</strong> sütunundaki değeri 'Mary' olan müşterinin <strong>last_name</strong> sütunundaki değeri nedir?

```
SELECT last_name FROM customer
WHERE first_name = 'Mary';
```

<br>
<br>
<br>

Q5-) <strong>film</strong>  tablosundaki <strong>uzunluğu(length)</strong>  50 ten büyük OLMAYIP aynı zamanda <strong>rental_rate</strong>  değeri 2.99 <strong>veya</strong>  4.99 OLMAYAN verileri sıralayınız.

```
SELECT * FROM film
WHERE length <= 50 
AND NOT (rental_rate = 2.99 OR rental_rate = 4.99);
```
<br>
<br>

## 📄 | SQL Ödev 02 | BETWEEN & IN

<br>
<br>    
<br>

Q1-) <strong>film</strong> tablosunda bulunan tüm sütunlardaki verileri <strong>replacement cost</strong> değeri 12.99 dan büyük eşit ve 16.99 küçük olma koşuluyla sıralayınız ( BETWEEN - AND yapısını kullanınız.)

```
SELECT * FROM film 
WHERE replacement_cost BETWEEN 12.99 AND 16.99;
```

<br> 
<br>
<br>

Q2-) <strong>actor</strong> tablosunda bulunan <strong>first_name</strong> ve <strong>last_name</strong> sütunlardaki verileri <strong>first_name</strong> 'Penelope' veya 'Nick' veya 'Ed' değerleri olması koşuluyla sıralayınız. ( IN operatörünü kullanınız.)

```
SELECT first_name, last_name FROM actor 
WHERE first_name IN ('Penelope', 'Nick', 'Ed');
```
<br>
<br>
<br>

Q3-) <strong>film</strong> tablosunda bulunan tüm sütunlardaki verileri <strong>rental_rate</strong> 0.99, 2.99, 4.99 VE <strong>replacement_cost</strong> 12.99, 15.99, 28.99 olma koşullarıyla sıralayınız. ( IN operatörünü kullanınız.)

```
SELECT first_name, last_name FROM actor 
WHERE first_name IN ('Penelope', 'Nick', 'Ed');
```
<br>

## 📄 | SQL Ödev 03 | LIKE ve ILIKE

<br>
<br>
<br>

Q1-)  <strong>country</strong> tablosunda bulunan  <strong>country</strong> sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.

```

SELECT country FROM country
WHERE country LIKE 'A%a' 

```



<br>
<br>
<br>

Q2-) <strong>country</strong> tablosunda bulunan <strong>country</strong> sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.

```

SELECT country FROM country 
WHERE country LIKE '_____%n' 

```


<br>
<br>
<br>

Q3-) <strong>film</strong> tablosunda bulunan <strong>title</strong> sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin <strong>'T'</strong> karakteri içeren film isimlerini sıralayınız.

```

SELECT title FROM film 
WHERE title ILIKE '%T%T%T%T%'

```


<br>
<br>
<br>

Q4-) <strong>film</strong> tablosunda bulunan tüm sütunlardaki verilerden <strong>title</strong> 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve <strong>rental_rate</strong> 2.99 olan verileri sıralayınız.

```

SELECT * FROM film 
WHERE title LIKE 'C%' AND length > 90 AND rental_rate = 2.99; 

```

<br>

## 📄 | SQL Ödev 04 | DISTINCT ve COUNT

<br>
<br>
<br>

Q1-)  <strong>film</strong> tablosunda bulunan  <strong>replacement_cost</strong> sütununda bulunan birbirinden farklı değerleri sıralayınız.

```

SELECT DISTINCT replacement_cost FROM film

```


<br>
<br>
<br>

Q2-) <strong>film</strong> tablosunda bulunan <Strong>replacement_cost</strong> sütununda birbirinden farklı kaç tane veri vardır?

```

SELECT COUNT (DISTINCT replacement_cost) FROM film;

```


<br>
<br>
<br>

Q3-) <strong>film</strong> tablosunda bulunan film isimlerinde  <strong>(title)</strong> kaç tanesini T karakteri ile başlar ve aynı zamanda  <strong>rating</strong> 'G' ye eşittir?

```

SELECT COUNT(*) FROM film 
WHERE title LIKE 'T%' AND rating = 'G';

```

<br>
<br>
<br>



Q4-) <strong>country</strong> tablosunda bulunan ülke isimlerinden (country) kaç tanesi <strong>5</strong> karakterden oluşmaktadır?


```

SELECT COUNT(DISTINCT country) FROM country 
where country like '_____';

```

<br>
<br>
<br>

Q5-) city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?

```

SELECT COUNT(city) FROM city 
WHERE city ILIKE 'R%';

```

<br>

## 📄 | SQL Ödev 05 | ORDER BY | LIMIT ve OFFSET

<br>
<br>
<br>

Q1-) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.

```

SELECT title, length FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;

```



<br>
<br>
<br>

Q2-) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.


```

SELECT title, length FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
LIMIT 5 OFFSET 5;

```



<br>
<br>
<br>

Q3-) customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.


```
SELECT * FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
LIMIT 4;
```



<br>


## 📄 | SQL Ödev 06 | AGGREGATE FONKSİYONLAR

<br>
<br>
<br>

Q1-) film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?


```
SELECT ROUND(AVG(rental_rate),2) FROM film ;
```



<br>
<br>
<br>

Q2-) film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

```
SELECT COUNT(*) FROM film
WHERE title LIKE 'C%';
```

<br>
<br>
<br>

Q3-) film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

```
SELECT MAX(length) FROM film 
WHERE rental_rate = 0.99;
```

<br>
<br>
<br>

Q4-) ffilm tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

```
SELECT COUNT(DISTINCT replacement_cost) FROM film 
WHERE length > 150;
```
<br>

## 📄 | SQL Ödev 07 | GROUP BY | HAVING

<br>
<br>
<br>

Q1-) film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.


```

SELECT rating, COUNT(*) FROM film
GROUP BY rating;

```


<br>
<br>
<br>

Q2-) film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.

```
SELECT replacement_cost, COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
```

<br>
<br>
<br>

Q3-) customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?

```
SELECT store_id, COUNT(*) 
FROM customer
GROUP BY store_id;
```

<br>
<br>
<br>

 Q4-) city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.

 ```
SELECT country_id, COUNT(*) 
FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;
```

<br>

## 📄 | SQL Ödev 08 | TABLO OLUŞTURMAK | VERİLERİ GÜNCELLEMEK

<br>
<br>
<br>

1-) test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.


```

CREATE TABLE employee (
  id INTEGER,
  name VARCHAR(50) NOT NULL,
  birthday DATE,
  email VARCHAR(100)
);

```


<br>
<br>
<br>

2-) Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

```

insert into Employee (name, birthday, email) values ('Alexandr', '1935-03-02', 'abrook0@phoca.cz');
insert into Employee (name, birthday, email) values ('Vevay', '1939-05-14', 'vbarabisch1@posterous.com');
insert into Employee (name, birthday, email) values ('Ashlin', '1930-08-31', 'abirt2@apache.org');
insert into Employee (name, birthday, email) values ('Zorine', '1997-05-17', 'zstanislaw3@independent.co.uk');
insert into Employee (name, birthday, email) values ('Daphne', '1983-04-04', 'dburry4@adobe.com');
insert into Employee (name, birthday, email) values ('Chrysa', '2017-09-23', 'cdebenedictis5@webmd.com');
insert into Employee (name, birthday, email) values ('Leon', '1994-12-08', 'ldowbiggin6@japanpost.jp');
insert into Employee (name, birthday, email) values ('Earl', '1929-11-27', 'ebyrd7@wordpress.com');
insert into Employee (name, birthday, email) values ('Heinrik', '1993-06-15', 'hbeswetherick8@sitemeter.com');
insert into Employee (name, birthday, email) values ('Milty', '2023-05-08', 'mschneidau9@ftc.gov');
insert into Employee (name, birthday, email) values ('Peria', '1949-06-12', 'pcraxforda@slashdot.org');
insert into Employee (name, birthday, email) values ('Allan', '2002-12-13', 'apionterb@omniture.com');
insert into Employee (name, birthday, email) values ('Weider', '1935-11-09', 'wbraggec@cornell.edu');
insert into Employee (name, birthday, email) values ('Celinka', '1963-08-19', 'chamblettd@t-online.de');
insert into Employee (name, birthday, email) values ('Homere', '1919-04-25', 'hscothorne@weather.com');
insert into Employee (name, birthday, email) values ('Herold', '2013-09-15', 'hdeathf@reference.com');
insert into Employee (name, birthday, email) values ('Guilbert', '2003-02-06', 'gvanellig@home.pl');
insert into Employee (name, birthday, email) values ('Gerty', '1910-12-15', 'gcaugheyh@europa.eu');
insert into Employee (name, birthday, email) values ('Farrell', '1981-05-05', 'ffidgeoni@google.com.au');
insert into Employee (name, birthday, email) values ('Knox', '1980-08-26', 'kkoenraadj@prnewswire.com');
insert into Employee (name, birthday, email) values ('Hailey', '1942-03-19', 'hstrewthersk@liveinternet.ru');
insert into Employee (name, birthday, email) values ('Alic', '1920-03-13', 'avasiliul@bandcamp.com');
insert into Employee (name, birthday, email) values ('Lorant', '1901-06-27', 'lmeltonm@cocolog-nifty.com');
insert into Employee (name, birthday, email) values ('Penny', '1959-07-07', 'pkinforthn@soundcloud.com');
insert into Employee (name, birthday, email) values ('Marlow', '1966-12-06', 'moveringtono@google.com');
insert into Employee (name, birthday, email) values ('Zak', '1915-02-18', 'zendersp@posterous.com');
insert into Employee (name, birthday, email) values ('Chrisse', '1994-05-05', 'cmctrustieq@wufoo.com');
insert into Employee (name, birthday, email) values ('Roddy', '1957-03-08', 'rdooner@narod.ru');
insert into Employee (name, birthday, email) values ('Tatiania', '1988-11-28', 'tgladbachs@eepurl.com');
insert into Employee (name, birthday, email) values ('Edy', '1912-09-07', 'eocrevant@blogs.com');
insert into Employee (name, birthday, email) values ('Melvin', '2002-11-02', 'meallisu@cloudflare.com');
insert into Employee (name, birthday, email) values ('Darb', '1923-07-03', 'ddurantv@t.co');
insert into Employee (name, birthday, email) values ('Barthel', '1912-11-01', 'bblankmanw@bravesites.com');
insert into Employee (name, birthday, email) values ('Rheta', '1994-10-21', 'rblunsumx@nyu.edu');
insert into Employee (name, birthday, email) values ('Humfried', '1943-11-30', 'hgowersy@mlb.com');
insert into Employee (name, birthday, email) values ('Sheba', '1943-09-24', 'spoez@surveymonkey.com');
insert into Employee (name, birthday, email) values ('Elfrida', '2022-06-22', 'ehutcheon10@cnbc.com');
insert into Employee (name, birthday, email) values ('Dannie', '1977-09-16', 'ddanilchev11@cnet.com');
insert into Employee (name, birthday, email) values ('Sybila', '1997-05-01', 'sbeney12@hhs.gov');
insert into Employee (name, birthday, email) values ('Xavier', '1988-05-05', 'xgallear13@auda.org.au');
insert into Employee (name, birthday, email) values ('Quillan', '1932-02-25', 'qthew14@samsung.com');
insert into Employee (name, birthday, email) values ('Randy', '1909-09-21', 'rduplantier15@hugedomains.com');
insert into Employee (name, birthday, email) values ('Stanly', '1909-10-27', 'smccolm16@furl.net');
insert into Employee (name, birthday, email) values ('Elvira', '1949-01-05', 'ecorrison17@irs.gov');
insert into Employee (name, birthday, email) values ('Hymie', '1930-12-30', 'hmclaggan18@craigslist.org');
insert into Employee (name, birthday, email) values ('Janna', '2006-09-06', 'jspadotto19@chicagotribune.com');
insert into Employee (name, birthday, email) values ('Krissie', '1937-06-22', 'kfrankema1a@mit.edu');
insert into Employee (name, birthday, email) values ('Vera', '1959-12-03', 'vaspole1b@hugedomains.com');
insert into Employee (name, birthday, email) values ('Calla', '1959-12-08', 'cleisman1c@arizona.edu');
insert into Employee (name, birthday, email) values ('Andrus', '1981-03-28', 'ahighway1d@furl.net');

```

<br>
<br>
<br>

3-) Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.


```

// İsim (name) sütununu güncellemek:

UPDATE employee
SET name = 'Vevay'
WHERE name = 'Alex';


// Doğum günü (birthday) sütununu güncellemek:

UPDATE employee
SET birthday = '1994-12-08'
WHERE email = 'abirt2@apache.org';


// E-posta (email) sütununu güncellemek:

UPDATE employee
SET email = 'kkoenraadj@prnewswire.com'
WHERE birthday = '2017-09-23';


// İsim ve doğum günü sütunlarını güncellemek:

UPDATE employee
SET name = 'Alic',
    birthday = '2006-09-06'
WHERE id = 46;


// Tüm sütunları güncellemek:

UPDATE employee
SET name = 'Andrus',
    birthday = '1981-03-28',
    email = 'ahighway1d@furl.net'
WHERE id = 50;

```


<br>
<br>
<br>


4-) Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.



```

DELETE FROM employee
WHERE id = 32;

DELETE FROM employee
WHERE name ='Darb';

DELETE FROM employee
WHERE name = 'Edy' AND birthday = '1912-09-07';

DELETE FROM employee
WHERE email = 'eocrevant@blogs.com';

DELETE FROM employee
WHERE id > 5
RETURNING *;

```


<br>
