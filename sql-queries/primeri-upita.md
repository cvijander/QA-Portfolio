# Primeri SQL Upita

Ovaj fajl sadrži kolekciju SQL upita napisanih za rešavanje različitih zadataka na zamišljenoj bazi podataka sa likovima. Svaki zadatak je praćen odgovarajućim SQL rešenjem.

---

### 1. Ispišite ime, prezime, patronus svih likova koji imaju patronusa i on je poznat.
```sql
select fname, lname, patronus from characters where patronus is not null;
```

### 2. Ispišite prezime likova čije prezime završava slovom 'e'.
```sql
select lname from characters where lname like '%e';
```

### 3. Izračunajte ukupne godine svih likova i ispišite to na ekran.
```sql
select sum(age) as total_years from characters;
```

### 4. Ispišite ime, prezime i godine likova po opadajućem redosledu njihovih godina.
```sql
select fname, lname, age from characters order by age desc;
```

### 5. Ispišite ime likova i godine onih čije godine su u rasponu od 50 do 100 godina.
```sql
select fname, age from characters where age between 50 and 100;
```

### 6. Ispišite godine svih likova tako da među njima nema onih sa istim godinama.
```sql
select distinct age from characters;
```

### 7. Ispišite sve informacije o likovima čiji je fakultet 'Gryffindor' i čije su godine preko 30.
```sql
select * from characters where faculty = 'Gryffindor' and age > 30;
```

### 8. Ispišite imena prva tri fakulteta iz tabele tako da se fakulteti ne ponavljaju.
```sql
select distinct faculty from characters limit 3;
```

### 9. Ispišite imena likova čije ime počinje sa 'N' i ima 5 slova, ili čije ime počinje sa 'L'.
```sql
select fname from characters where fname like 'N____' or fname like 'L%';
```

### 10. Izračunajte prosečne godine svih likova.
```sql
select avg(age) as average_age from characters;
```

### 11. Obrišite lika sa ID = 11.
```sql
delete from characters where char_id = 11;
```

### 12. Ispišite prezime svih likova koja sadrže slovo 'a'.
```sql
select lname from characters where lname like '%a%';
```

### 13. Koristite pseudonim da privremeno zamenite naziv kolone fname u Half-Blood Prince.
*Napomena: Ispravna sintaksa za pseudonime sa razmakom koristi duple navodnike.*
```sql
select fname as "Half-Blood Prince" from characters where fname = 'Severus';
```

### 14. Ispišite id i imena svih patronusa po abecednom redu, pod uslovom da su poznati.
```sql
select char_id, fname, patronus from characters where patronus is not null order by patronus asc;
```

### 15. Koristite operator IN, ispišite ime i prezime likova čije je prezime Crabbe, Granger ili Diggory.
```sql
select fname, lname from characters where lname in ('Crabbe', 'Granger', 'Diggory');
```

### 16. Ispišite minimalne godine likova.
```sql
select min(age) as minimalne_godine from characters;
```

### 17. Koristite operator UNION, ispišite imena iz tabele characters i naslove knjiga iz tabele library.
```sql
select fname as name from characters
union
select book_name as name from library;
```

### 18. Koristite operator HAVING, izračunajte broj likova po svakom fakultetu, ostavljajući samo one fakultete gde je broj studenata veći od 1.
```sql
select faculty, count(*) as broj_studenata
from characters
group by faculty
having count(*) > 1;
```
