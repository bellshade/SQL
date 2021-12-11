# GRANT USER

> GRANT merupakan perintah untuk memberikan izin Hak Istimewa (Privileges) kepada User yang ada di MySQL agar dapat mengakses objek yang ada di database.

Secara default yang dapat memberi Hak Istimewa (_Privileges_) kepada user lain adalah user `root` (Super User) karena secara default user `root` memiliki semua _Privileges_.

_Privileges_ yang bisa diberikan adalah :

| _Privileges_     | Diskripsi                                    |
| ---------------- | -------------------------------------------- |
| SELECT           | Hak untuk Menampilkan data yang sudah ada    |
| INSERT           | Hak untuk memasukan data                     |
| UPDATE           | Hak untuk mengubah data yang sudah ada       |
| DELETE           | Hak untuk menghapus data yang sudah ada      |
| INDEX            | Hak untuk membuat atau menghapus Index       |
| CREATE           | Hak untuk membuat tabel baru                 |
| ALTER            | Hak untuk mengubah tabel yang sudah ada      |
| DROP             | Hak untuk menghapus tabel yang sudah ada     |
| GRANT OPTION     | Hak untuk memberi akses kepada User lain     |
| ALL _Privileges_ | Memberikan semua _Privileges_ yang sudah ada |

## Sintak

```sql
GRANT hak_akses ON nama_objek TO user;
```

Selalu simpan perubahan yang dilakukan dengan sintak :

```sql
FLUSH Privileges;
```

## Sintak Query

Untuk contoh di materi ini, saya menggunakan :

- User : `bell_user`
- Database : `Sekolah`
- tabel : `Siswa`

### Membuat User Baru

**User** baru yang baru dibuat tidak memiliki _Privileges_ sama sekali kesemua objek.

```sql
CREATE USER 'bell_user'@'localhost' IDENTIFIED BY 'password';
```

### Memberi satu Privileges saja

Memberikan satu _Privileges_ ke User `bell_user` terhadap semua objek didalam database `Sekolah`

```sql
-- Memberikan Privileges SELECT
GRANT SELECT ON Sekolah.* TO 'bell_user'@'localhost';

-- Memberikan Privileges INSERT
GRANT INSERT ON Sekolah.* TO 'bell_user'@'localhost';
```

### Memberi dua atau lebih Privileges

Memberikan 2 atau lebih _Privileges_ ke User `bell_user` ke terhadap semua objek didalam database `Sekolah`.

```sql
GRANT SELECT,INSERT,CREATE ON Sekolah.* TO 'bell_user'@'localhost';
```

### Memberi Privileges terhadap Tabel

_Privileges_ juga bisa diatur untuk hanya bisa mengakses beberapa tabel yang ada didalam database `Sekolah`

```sql
-- Memberikan Privileges SELECT dan INSERT terhadap tabel Siswa
GRANT SELECT,INSERT ON Sekolah.Siswa TO 'bell_user'@'localhost';
```

### Memberi Privileges terhadap Kolom

_Privileges_ juga bisa diatur untuk hanya bisa mengakses beberapa kolom tabel yang ada didalam database `Sekolah`

Untuk Query nya, nama kolom ditulis di sebelah _Privileges_ dan didalam kurung `()`

```sql
-- Memberikan Privileges SELECT hanya di kolom id dan name didalam tabel Siswa
GRANT SELECT(id,name) ON Sekolah.Siswa TO 'bell_user'@'localhost';
```

### Memberikan semua Privileges terhadap 1 database

Memberikan semua _Privileges_ ke database `Sekolah`

```sql
GRANT ALL ON Sekolah TO 'bell_user'@'localhost';
```

### Memberikan semua Privileges terhadap 1 Tabel

Memberikan semua _Privileges_ ke tabel `Siswa` di dalam database `Sekolah`

```sql
GRANT ALL ON Sekolah.Siswa TO 'bell_user'@'localhost';
```

### Membuat Super User

Membuat user baru yang memiliki semua _Privileges_ seperti user `root`.

```sql
GRANT ALL ON * . * TO 'bell_user'@'localhost';
```
