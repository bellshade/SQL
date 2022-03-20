## CREATE OBjECT

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

[<< Materi sebelumnya](https://github.com/bellshade/SQL/tree/main/Basic/02_Data_Manipulation_Language/4_Menghapus_Data) | [Materi selanjutnya >>](https://github.com/bellshade/SQL/tree/main/Basic/03_Data_Defintion_Language/2_Menampilkan_Object)