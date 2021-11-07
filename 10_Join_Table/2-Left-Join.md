# LEFT JOIN
![LEFT JOIN](https://user-images.githubusercontent.com/93637835/140651291-d56eaa9f-d258-4d23-8036-c7bbc0823536.png)

> `LEFT JOIN` memiliki fungsi untuk mengambil seluruh data dari tabel kiri (_Table 1_) dan mengambil data pada tabel kanan (_Table 2_) yang cocok dengan _Table 1_.
> 
> `LEFT JOIN` tidak akan mengambil data dari _Table 2_ yang tidak sesuai dengan _Table 1_.

## Syntax
```
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```
