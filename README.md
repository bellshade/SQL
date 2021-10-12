# SQL

## Pengertian dari _Structure Query Language (SQL)_

_Structure Query Language (SQL)_ adalah sebuah bahasa yang biasa digunakan untuk mengakses atau memanipulasi data pada _Relational Database Management System (RDBMS)_. Contoh RDBMS yang populer saat ini, yaitu _MySQL_, _PostgreSQL_, _Microsoft SQL Server, dan Oracle_.

SQL syntax tidak bersifat _case sensitive_. Jadi antara ```insert``` sama saja dengan ```INSERT```. Tetapi beberapa programmer suka menggunakan ```UPPERCASE``` dalam menulis SQL syntax.

## Insert

Digunakan untuk menambahkan data.

```sql
insert into table (nama, kelas) values ('Anggora', 3)
```

## Select

Digunakan untuk mengambil data.

### Ambil Data dari Semua Field

```sql
select * from table
```

### Ambil Data dari Sebagian Field

```sql
select field1, field2, field3 from table
```

## Update

Memodifikasi data.

```sql
update table set nama = 'kucing' where id = 1
```

## Delete

Menghapus data.

```sql
delete from table where id = 3
```