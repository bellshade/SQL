# Memberi Privileges

> GRANT merupakan perintah untuk memberikan Hak Istimewa (Privileges) kepada User yang ada di MySQL agar dapat mengakses objek yang ada di database.

Secara default yang dapat memberi Hak Istimewa (_Privileges_) kepada user lain adalah user `root` (Super User) karena secara default user `root` memiliki semua _Privileges_.

_Privileges_ yang bisa diberikan adalah :

| _Privileges_ | Diskripsi                                              |
| ------------ | ------------------------------------------------------ |
| SELECT       | Hak untuk Menampilkan data yang sudah ada              |
| INSERT       | Hak untuk memasukan data                               |
| UPDATE       | Hak untuk mengubah data yang sudah ada                 |
| DELETE       | Hak untuk menghapus data yang sudah ada                |
| INDEX        | Hak untuk membuat atau menghapus Index                 |
| CREATE       | Hak untuk membuat tabel baru                           |
| ALTER        | Hak untuk mengubah tabel yang sudah ada                |
| DROP         | Hak untuk menghapus tabel yang sudah ada               |
| GRANT OPTION | Hak untuk memberi atau mencabut akses kepada User lain |
| ALL          | Semua Hak _Privileges_                                 |

## Sintak

```sql
GRANT hak_akses ON nama_objek TO user;
```

Selalu simpan perubahan yang dilakukan dengan sintak :

```sql
FLUSH Privileges;
```

## Query

Untuk contoh di materi ini, saya menggunakan :

- User : `bell_user`
- Database : `Sekolah`
- tabel : `Siswa`

### Membuat User Baru

```sql
CREATE USER 'bell_user'@'localhost' IDENTIFIED BY 'password';
```

**User** baru yang baru dibuat tidak memiliki _Privileges_ sama sekali.

Sehingga jika menjalankan `SELECT * FROM Siswa` akan mengeluarkan error

> SELECT command denied to user 'bell_user'@'localhost' for table 'Siswa'

### Memberi satu Privileges saja

Memberikan satu _Privileges_ (`SELECT` dan `INSERT`) ke User `bell_user` terhadap semua objek didalam database `Sekolah`

```sql
GRANT SELECT ON Sekolah.* TO 'bell_user'@'localhost';

GRANT INSERT ON Sekolah.* TO 'bell_user'@'localhost';
```

### Memberi dua atau lebih Privileges

Memberikan 2 atau lebih _Privileges_ ke User `bell_user` terhadap semua objek didalam database `Sekolah`.

```sql
GRANT SELECT,INSERT,CREATE ON Sekolah.* TO 'bell_user'@'localhost';
```

### Memberi Privileges terhadap 1 Kolom

_Privileges_ juga bisa diatur untuk hanya bisa mengakses beberapa kolom (`id`,`name`) dari tabel `Siswa` yang ada didalam database `Sekolah`

Untuk Query nya, nama kolom ditulis di sebelah _Privileges_ dan didalam kurung `()`

```sql
GRANT SELECT(id,name) ON Sekolah.Siswa TO 'bell_user'@'localhost';
```

### Memberikan Semua Privileges terhadap 1 Tabel

Memberikan semua _Privileges_ ke tabel `Siswa` di dalam database `Sekolah`

```sql
GRANT ALL ON Sekolah.Siswa TO 'bell_user'@'localhost';
```

### Memberikan Semua Privileges terhadap 1 database

Memberikan semua _Privileges_ ke database `Sekolah`

```sql
GRANT ALL ON Sekolah TO 'bell_user'@'localhost';
```

### Membuat Super User

Membuat user baru yang memiliki semua _Privileges_ seperti user `root`.

```sql
GRANT ALL ON * . * TO 'bell_user'@'localhost';
```
