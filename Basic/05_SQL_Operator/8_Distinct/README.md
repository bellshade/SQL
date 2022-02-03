# DISTINCT

## Pengertian DISTINCT

> DISTINCT merupakan perintah untuk menampilkan data yang memiliki nilai yang berbeda (tidak duplikat) dari kolom yang dipilih. Sehingga data yang ditampilkan tidak ada yang memiliki nilai yang sama.

## 1. Bentuk Umum

    `SELECT` `DISTINCT` nama_kolom `FROM` nama_tabel

## 2. Contoh Query

- Tabel Latihan

  > Keterangan: Tabel berikut merupakan tabel **mahasiswa** yang berisi data **nama**, **kota**, dan **umur**.

  | nama    | kota         | umur |
  | ------- | ------------ | ---- |
  | Adi     | Jambi        | 18   |
  | Budi    | Manado       | 19   |
  | Celine  | Kuala Lumpur | 19   |
  | Dhike   | Jakarta      | 19   |
  | Frieska | Jakarta      | 19   |
  | Ghaida  | Manado       | 19   |

- SQL Query : `SELECT` `DISTINCT` **kota** `FROM` **mahasiswa**

  Output :

  | kota         |
  | ------------ |
  | Jambi        |
  | Manado       |
  | Kuala Lumpur |
  | Jakarta      |

  Penjelasan :

  > Menampilkan data kota dari mahasiswa dengan record data manado, dan jakarta hanya ditampilkan 1 kali (tanpa duplikasi).

- SQL Query : `SELECT` `DISTINCT` **umur** `FROM` **mahasiswa**

  Output :

  | kota |
  | ---- |
  | 18   |
  | 19   |

  Penjelasan :

  > Menampilkan data umur dari mahasiswa dengan record data 19 tahun hanya ditampilkan 1 kali (tanpa duplikasi).
