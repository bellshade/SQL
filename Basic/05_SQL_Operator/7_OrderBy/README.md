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

## 3. Contoh Query

- Tabel Latihan

  > Keterangan: Tabel berikut merupakan tabel **mahasiswa** yang berisi data **nama**, **kota**, dan **umur**.

      | nama    | kota         | umur |
      | ------- | ------------ | ---- |
      | Adi     | Jambi        | 18   |
      | Budi    | Manado       | 19   |
      | Celine  | Kuala Lumpur | 19   |
      | Dhike   | Jakarta      | 18   |
      | Frieska | Jakarta      | 19   |
      | Ghaida  | Manado       | 18   |

- ASCENDING :

  1. SQL Query : `SELECT` nama, kota, umur `FROM` mahasiswa **`ORDER BY`** nama **`ASC`**

     Output :

     | nama    | kota         | umur |
     | ------- | ------------ | ---- |
     | Adi     | Jambi        | 18   |
     | Budi    | Manado       | 19   |
     | Celine  | Kuala Lumpur | 19   |
     | Dhike   | Jakarta      | 18   |
     | Frieska | Jakarta      | 19   |
     | Ghaida  | Manado       | 18   |

  > Penjelasan : Menampilkan data nama, kota, dan umur dari tabel mahasiswa yang tersusun secara ascending/meningkat (a-z) berdasarkan kolom nama.

  2. SQL Query : `SELECT` nama, kota, umur `FROM` mahasiswa **`ORDER BY`** umur **`ASC`**

     Output :

     | nama    | kota         | umur |
     | ------- | ------------ | ---- |
     | Adi     | Jambi        | 18   |
     | Dhike   | Jakarta      | 18   |
     | Ghaida  | Manado       | 18   |
     | Budi    | Manado       | 19   |
     | Celine  | Kuala Lumpur | 19   |
     | Frieska | Jakarta      | 19   |

  > Penjelasan : Menampilkan data nama, kota, dan umur dari tabel mahasiswa yang tersusun secara ascending/meningkat (0-9) berdasarkan kolom umur.

- DESCENDING :

  1. SQL Query : `SELECT` nama, kota, umur `FROM` mahasiswa **`ORDER BY`** nama **`DESC`**

     Output :

     | nama    | kota         | umur |
     | ------- | ------------ | ---- |
     | Ghaida  | Manado       | 18   |
     | Frieska | Jakarta      | 19   |
     | Dhike   | Jakarta      | 18   |
     | Celine  | Kuala Lumpur | 19   |
     | Budi    | Manado       | 19   |
     | Adi     | Jambi        | 18   |

  > Penjelasan : Menampilkan data nama, kota, dan umur dari tabel mahasiswa yang tersusun secara descending/menurun (z-a) berdasarkan kolom nama.

  2. SQL Query : `SELECT` nama, kota, umur `FROM` mahasiswa **`ORDER BY`** umur **`DESC`**

     Output :

     | nama    | kota         | umur |
     | ------- | ------------ | ---- |
     | Budi    | Manado       | 19   |
     | Celine  | Kuala Lumpur | 19   |
     | Frieska | Jakarta      | 19   |
     | Adi     | Jambi        | 18   |
     | Dhike   | Jakarta      | 18   |
     | Ghaida  | Manado       | 18   |

  > Penjelasan : Menampilkan data nama, kota, dan umur dari tabel mahasiswa yang tersusun secara descending/menurun (9-0) berdasarkan kolom umur.

- Multiple Column Ordering

  1. SQL Query : `SELECT` nama, kota, umur `FROM` mahasiswa **`ORDER BY`** kota **`ASC`**, umur **`DESC`**

     Output :

     | nama    | kota         | umur |
     | ------- | ------------ | ---- |
     | Frieska | Jakarta      | 19   |
     | Dhike   | Jakarta      | 18   |
     | Adi     | Jambi        | 18   |
     | Celine  | Kuala Lumpur | 19   |
     | Budi    | Manado       | 19   |
     | Ghaida  | Manado       | 18   |

  > Penjelasan : Menampilkan data nama, kota, dan umur dari tabel mahasiswa yang tersusun secara ascending berdasarkan kolom kota diikuti tersusun secara descending berdasarkan kolom umur.

  2. SQL Query : `SELECT` nama, kota, umur `FROM` mahasiswa **`ORDER BY`** kota, umur

     Output :

     | nama    | kota         | umur |
     | ------- | ------------ | ---- |
     | Dhike   | Jakarta      | 18   |
     | Frieska | Jakarta      | 19   |
     | Adi     | Jambi        | 18   |
     | Celine  | Kuala Lumpur | 19   |
     | Ghaida  | Manado       | 18   |
     | Budi    | Manado       | 19   |

  > Penjelasan : Menampilkan data nama, kota, dan umur dari tabel mahasiswa yang tersusun berdasarkan kolom kota, lalu diikuti kolom umur secara default, nilai default dari order by adalah **`ASC`**
