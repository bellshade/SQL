# Mencabut Privileges

> REVOKE merupakan perintah untuk mencabut Hak Istimewa (Privileges) dari User yang ada di MySQL agar tidak dapat mengakses objek yang ada di database.

Secara default yang dapat mencabut Hak Istimewa (_Privileges_) dari user lain adalah user `root` (Super User) karena secara default user `root` memiliki semua _Privileges_.

**Sebisa mungkin jangan mencabut _Privileges_ dari user** `root`

_Privileges_ yang bisa dicabut adalah :

| _Privileges_ | Deskripsi                                              |
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

## Syntax

```sql
REVOKE hak_akses ON nama_objek FROM user;
```

Selalu simpan perubahan yang dilakukan dengan sintak :

```sql
FLUSH Privileges;
```

## Syntak Query

Untuk contoh di materi ini, saya menggunakan :

User : `bell_user`

Database : `Sekolah`

Tabel : `Siswa`

### Mencabut satu Privileges saja

Mencabut satu _Privileges_ (`SELECT` dan `INSERT`) dari User `bell_user` terhadap semua objek didalam database `Sekolah`

```sql
REVOKE SELECT ON Sekolah.* FROM 'bell_user'@'localhost';

REVOKE INSERT ON Sekolah.* FROM 'bell_user'@'localhost';
```

Setelah mencabut _Privileges_, jika menjalankan `SELECT * FROM Siswa` akan mengeluarkan error

> SELECT command denied to user 'bell_user'@'localhost' for table 'Siswa'

> INSERT command denied to user 'bell_user'@'localhost' for table 'Siswa'

### Mencabut dua atau lebih Privileges

Mencabut 2 atau lebih _Privileges_ (`SELECT` dan `INSERT`) dari User `bell_user` ke terhadap semua objek didalam database `Sekolah`.

```sql
REVOKE SELECT,INSERT ON Sekolah.* FROM 'bell_user'@'localhost';
```

### Mencabut Privileges terhadap 1 Kolom

Pencabutan _Privileges_ juga bisa diatur hanya untuk beberapa kolom (`id`) di tabel `siswa` yang ada didalam database `Sekolah`

Untuk Query nya, nama kolom ditulis di sebelah _Privileges_ dan didalam kurung `()`

```sql
REVOKE SELECT(id) ON Sekolah.Siswa FROM 'bell_user'@'localhost';
```

Sehingga saat menjalankan `SELECT * FROM Siswa` akan mengeluarkan error karena tidak memiliki _Privileges_ untuk melihat kolom `id` di kolom `Siswa`

> SELECT command denied to user 'bell_user'@'localhost' for column 'id' in table 'Siswa'

### Mencabut Semua Privileges terhadap 1 Tabel

Mencabut semua _Privileges_ dari tabel `Siswa` di dalam database `Sekolah`

```sql
REVOKE ALL ON Sekolah.Siswa FROM 'bell_user'@'localhost';
```

### Mencabut Semua Privileges terhadap 1 database

Mencabut semua _Privileges_ dari database `Sekolah`

```sql
REVOKE ALL ON Sekolah FROM 'bell_user'@'localhost';
```

### Mencabut Semua Hak Akses

Mencabut semua _Privileges_ yang dimiliki user `bell_user`.

Sebisa mungkin **jangan** melakukan **Pencabutan Semua Hak Akses** dari user `root`

```sql
REVOKE ALL ON * . * FROM 'bell_user'@'localhost';
```
