# SQL INSERT INTO
Bahasa Query dari ```INSERT INTO``` digunakan untuk memasukkan data baru ke dalam sebuah table dari database yang kita miliki.<br>

contohnya adalah
```SQL
-- Membuat Database Sekolah
CREATE DATABASE sekolah;

-- Memakai Database Sekolah
USE sekolah;

-- Membuat tabel siswa yang terdiri dari nidn dan nama
CREATE TABLE siswa (
  nidn int, -- int adalah bilangan bulat -> Integer
  nama varchar(50), -- varchar adalah karakter, 50 adalah limit maksimal panjang karakter
  primary key(nidn) -- primary key adalah unique value dari data tersebut
  );
  
-- Memasukkan data siswa baru ke dalam seluruh kolom dari tabel siswa (nidn dan nama)
INSERT INTO siswa VALUES(1,"Budi");

-- Hanya memasukkan nidn saja
INSERT INTO siswa (nidn) VALUES (2);

-- Memasukkan multiple data ke dalam tabel siswa
INSERT INTO siswa VALUES(3,"Ani"), (4,"Poseidon"), (5,"Hades");
```
