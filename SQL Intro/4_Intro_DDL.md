# PENGENALAN DDL (DATA DEFINITION LANGUAGE)

### Data Definition Language (DDL)

>Kumpulan perintah dalam SQL yang digunakan untuk mendefinisikan, membuat, memodifikasi ataupun menghapus struktur suatu object apapun bisa berupa database, table, schema ataupun view.

Berikut contoh dari DDL : 

### 1. **Membuat sebuah objek atau objek lainnya yang belum ada.**

  `CREATE`

  Bentuk Umum : `CREATE` + Objek + Nama Object + `;`
  
  - Membuat Database : 
    > `CREATE DATABASE`+ Nama Database + `;`
    
  - Membuat Table : 
    > `CREATE TABLE `+ Nama tabel + `(` + Nama Kolom +` ` + Tipe Data Kolom +`(` + Panjang Data +`) `+ Key + ` AUTO INCREMENT NOT NULL); `
   
  Contoh : 
  - Membuat Database : 
    > `CREATE DATABASE Mahasiswa;`

  - Membuat Table : 
    >`CREATE TABLE NILAI (ID INT PRIMARY KEY AUTO INCREMENT);`
    
    >`CREATE TABLE NILAI (ID INT PRIMARY KEY, Nama_Mahasiswa VARCHAR(255) NOT NULL, Nilai INT , Mata_Kuliah VARCHAR(255), Tanggal_Input DateTime);`
   
    >`CREATE TABLE NILAI (ID INT PRIMARY KEY AUTO INCREMENT NOT NULL, ID_Mahasiswa INT NOT NULL, Nama_Mahasiswa VARCHAR(255) NOT NULL, Nilai INT , Mata_Kuliah VARCHAR(255), Tanggal_Input DateTime);`

           
### 2. **Menampilkan dan Menggunakan sebuah objek beserta struktur nya**

  `SHOW` dan `USE`
  
  Bentuk Umum : `SHOW ` + Objek + `s ;`
                `USE ` + Nama Objek + `;`
  Contoh : 
  - Menampilkan List Database yang dimiliki 
    > `USE DATABASES;`
  - Menggunakan Database yang ingin diakses
    > `USE Mahasiswa;`
  - Menampilkan List Table didalam database Mahasiswa
    > `SHOW TABLES;`
   
### 3. **Menghapus sebuah objek**

  `DROP`

  Bentuk Umum : `DROP` + Objek + Nama Objek + `;`
  - Mengubah Database
    > `DROP` + Objek + Nama Objek + `;`
  Contoh : 
  
  - Menghapus Database
    > `DROP DATABASE Perkuliahan;`
  - Menghapus Sebuah Tabel Mahasiswa
    > `DROP TABLES Mahasiswa;`

### 4. **Menghapus semua Record atau Data didalam sebuah tabel**

  `TRUNCATE`

  Bentuk Umum : `TRUNCATE TABLE ` + Nama Objek + `;`
   
  Contoh : 
  - `TRUNCATE TABLE Mahasiswa;`

### 5. **Mengubah Struktur Objek**

  `ALTER`

  Bentuk Umum : `ALTER` + Objek + Nama Objek + `;`
  
  - Mengubah Database
   > 
  Contoh : 
  

