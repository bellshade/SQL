# ORDER BY

## Pengertian ORDER BY

> ORDER BY merupakan perintah untuk mengurutkan data yang ditampilkan berdasarkan kolom, dan jenis pengurutan yang dipilih. ORDER BY memiliki beberapa jenis pengurutan seperti ASC, dan DESC.

## 1. Bentuk Umum

`SELECT` nama_kolom `FROM` nama_tabel **`ORDER BY`** nama_kolom **`ASC`**

`SELECT` nama_kolom `FROM` nama_tabel **`ORDER BY`** nama_kolom **`DESC`**

## 2. Jenis pengurutan ORDER BY

| Jenis      | Deskripsi                                            | Query |
| ---------- | ---------------------------------------------------- | ----- |
| ASCENDING  | Pengurutan dari nilai terkecil menuju nilai terbesar | ASC   |
| DESCENDING | Pengurutan dari nilai terbesar menuju nilai terkecil | DESC  |

## Contoh Query

### **3. Contoh**

- ASCENDING :

  SQL Query : `SELECT` nama `FROM` mahasiswa **`ORDER BY`** nama **`ASC`**

  Output :

  | nama   |
  | ------ |
  | Adi    |
  | Budi   |
  | Celine |

  Penjelasan : Menampilkan daftar nama dari tabel mahasiswa yang tersusun secara ascending/meningkat (a-z) berdasarkan kolom nama.

  SQL Query : `SELECT` nim, nama `FROM` mahasiswa **`ORDER BY`** nim **`ASC`**

  Output :

  | nim  | nama   |
  | ---- | ------ |
  | 0901 | Budi   |
  | 0905 | Adi    |
  | 0909 | Celine |

  Penjelasan : Menampilkan daftar nim, dan nama dari tabel mahasiswa yang tersusun secara ascending/meningkat (0-9) berdasarkan kolom nim.

- DESCENDING :

  SQL Query : `SELECT` nama `FROM` mahasiswa **`ORDER BY`** nama **`DESC`**

  Output :

  | nama   |
  | ------ |
  | Celine |
  | Budi   |
  | Adi    |

  Penjelasan : Menampilkan daftar nama dari tabel mahasiswa yang tersusun secara descending/menurun (z-a) berdasarkan kolom nama.

  SQL Query : `SELECT` nim, nama `FROM` mahasiswa **`ORDER BY`** nim **`DESC`**

  Output :

  | nim  | nama   |
  | ---- | ------ |
  | 0909 | Celine |
  | 0905 | Adi    |
  | 0901 | Budi   |

  Penjelasan : Menampilkan daftar nim, dan nama dari tabel mahasiswa yang tersusun secara descending/menurun (9-0) berdasarkan kolom nim.
