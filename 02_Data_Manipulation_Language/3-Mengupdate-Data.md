# SQL UPDATE

Bahasa Query dari `UPDATE` digunakan untuk mengubah data yang sudah ada di sebuah table dari database yang kita miliki.<br>

**UPDATE** sintak

```sql
UPDATE nama_tabel
SET nama_kolom = nilai_baru, nama_kolom_2 = nilai_baru_2
WHERE kondisi --optional
```

Contoh :

`SELECT * FROM SISWA` --> referensi tabel [2-Menginput-Data](https://github.com/fairusatoir/SQL/blob/main/02_Data_Manipulation_Language/2-Menginput-Data.md)

| nish | nama     |
| ---- | -------- |
| 1    | Budi     |
| 3    | Ani      |
| 4    | Poseidon |
| 5    | Hades    |

Diatas disediakan tabel **nish** dan **nama** dari tabel **SISWA**

### -> Ubah kolom **nama** `Budi` saja menjadi `Alice`

```SQL
-- cara 1
UPDATE SISWA
SET nama = 'Alice'
WHERE nama = 'Budi' -- Menggunakan kondisi di kolom `nama`

-- cara 2
UPDATE SISWA
SET nama = 'Alice'
WHERE nish = 1 -- Menggunakan kondisi di kolom `nish`
```

Hasil :
| nish | nama |
|------|----------|
| 1 | Alice |
| 3 | Ani |
| 4 | Poseidon |
| 5 | Hades |

### -> Ubah semua yang ada di kolom **nama** menjadi `Bob`

```SQL
UPDATE SISWA
SET nama = 'Bob'
```

Hasil :
| nish | nama |
|------|----------|
| 1 | Bob |
| 3 | Bob |
| 4 | Bob |
| 5 | Bob |

---

### Compatibility Query

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server                     | :heavy_check_mark: |
| MariaDB                        | :heavy_check_mark: |
| . .                            |                    |
