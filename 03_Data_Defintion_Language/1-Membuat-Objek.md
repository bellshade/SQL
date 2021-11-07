## **Membuat sebuah objek atau objek lainnya yang belum ada.**

  `CREATE`

  Bentuk Umum : `CREATE` + Objek + Nama Object + `;`
  
  - Membuat Database : 
    > `CREATE DATABASE`+ Nama Database + `;`
    
  - Membuat Table : 
    > `CREATE TABLE `+ Nama tabel + `(` + Nama Kolom +` ` + Tipe Data Kolom +`(` + Panjang Data +`) `+ Key + ` AUTO INCREMENT NOT NULL); `
   
  Contoh : 
  
  Note 
  > Jika terdapat lebih dari 1 kata maka gunakan tanda ``_`` sebagai pengganti spasi.

  - Membuat Database : 
    > `CREATE DATABASE Mahasiswa;`

  - Membuat Table : 
    >`CREATE TABLE NILAI (ID INT PRIMARY KEY AUTO INCREMENT);`
    
    >`CREATE TABLE NILAI (ID INT PRIMARY KEY, Nama_Mahasiswa VARCHAR(255) NOT NULL, Nilai INT , Mata_Kuliah VARCHAR(255), Tanggal_Input DateTime);`
   
    >`CREATE TABLE NILAI (ID INT PRIMARY KEY AUTO INCREMENT NOT NULL, ID_Mahasiswa INT NOT NULL, Nama_Mahasiswa VARCHAR(255) NOT NULL, Nilai INT , Mata_Kuliah VARCHAR(255), Tanggal_Input DateTime);`
