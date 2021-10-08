# SQL

Tutorial dari _structure query language_ (sql)

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