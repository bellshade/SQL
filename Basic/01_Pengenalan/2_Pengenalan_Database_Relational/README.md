# SQL INTRO RELATIONAL DATABASE

## Apa itu Relational Database

> Yaitu Adalah Model Database dengan tabel-tabel yang saling berhubungan satu dengan yang lain, Secara praktis kita dapat memahami bahwa antar satu tabel memiliki kaitan dengan tabel lain.
> Simple nya adalah tabel - tabel pada database akan saling berelasi satu sama lain

Database Relasional Memiliki Terminologi nya yaitu :
1. Relasi : Tabel dengan Kolom dan Baris
2. Atribut : Nama Kolom Dari Relasi
3. Domain : Sekumpulan Nilai yang diijinkan untuk satu atau lebih atribut
4. Tuple dan Record : kumpulan isi elemen data dari suatu relasi yang saling berhubungan

Properti dari suatu relasi tabel:
1. Nama Tabel harus berbeda dari semua nama tabel lain dalam satu database
2. Setiap Sel dari tabel berisi tepat satu nilai atomik (tunggal)
3. Setiap Kolom Memiliki Nama yang Berbeda
4. Nilai dari semua kolom dari domain yang sama
5. Setiap Record Berbeda, tidak ada record duplikat
6. Urutan Kolom tidak bermasalah
7. Urutan Record secara teoritis tidak memiliki makna

Hubungan antar data dalam database relasional di identifikasi kan menggunakan sebuah Relational Key.
berikut ini jenis-jenis dari relational key:

1. Primary Key
> Satu Kolom yang bisa dijadikan sebuah key yang hanya mengidentifikasikan setiap kejadian dengan sebuah value secara unik dan spesifik, dimana setiap record harus mempunyai primary key yang berbeda-beda yang tidak mungkin sama 

2. Foreign Key
> Sebuah Atribut dengan domain yang sama yang menjadi kunci utama pada sebuah relasi pada tabel lain tetapi pada relasi lain atribut tersebut hanya atribut biasa

3. Super Key
> Satu Atribut / Kumpulan Atribut yang secara unik mengidentifikasikan sebuah tuple didalam relasi

4. Candidate Key
> Suatu Atribut atau Satu set minimal atribut yang mengidentifikasikan secara unik kejadian spesifik dari entitas

5. Alternatif Key
> Sebuah Candidate Key yang tidak dipakai atau tidak dipilih sebagai primary key

[<< Materi sebelumnya](https://github.com/bellshade/SQL/tree/main/Basic/01_Pengenalan/1_Pengenalan_Database) | [Materi selanjutnya >>](https://github.com/bellshade/SQL/tree/main/Basic/01_Pengenalan/3_Pengenalan_Query_Database)