# Panduan Berkontribusi

## Kontributor

Kami sangat senang anda telah ikut berkontribusi dalam implementasi algoritma, struktur data atau memperbaiki error.
Semua boleh ikut berkontribusi walaupun hal kecil dengan pengecualian sebagai berikut :

- Hasil pekerjaan kamu adalah buatan kamu sendiri dan tidak ada hak cipta dari orang lain.
  - Jika kami menemukan kesamaan maka kami tidak `merged`.
- Hasil kerja kamu akan berlisensi [MIT](LICENSE) ketika permintaan pull kamu sudah di merged.
- Hasil kerja kamu wajib mengikuti standar dan style koding dari kami.
- Beri penjelasan yang mudah dipahami, minimum ` 150 ` karakter, dan untuk maksimumnya sebanyak yang diinginkan para kontributor.
- Permateri harus ada minimal 1 contoh query SQL , 1 Penjelasan, 1 Bentuk umum Query, lebih bagus lagi jika mencantumkan contoh lebih dari 1.
- Masukkan referensi bila diperlukan, dan jika copy paste materi dari tempat lain, harap untuk dimodifikasi kata-katanya terlebih dahulu.

**Note**:
- File README.md yang ada pada setiap folder materi SQL, tinggal diubah saja isinya, dan tidak perlu diubah nama file markdown-nya.


# *Pull Request*

### ***Pull request* yang baik**

Informasi: Gunakan [*issues*](https://github.com/bellshade/SQL/issues) apabila ingin menambahkan kode atau memperbaiki kode, dll (*basic*) agar tidak ada konflik dengan *pull request* lainnya.

- Lakukan penjelasan deskripsi perubahan yang anda lakukan pada repositori kami dengan membuat penjelasan di [*issues*](https://github.com/bellshade/SQL/issues).
- Setelah menjelaskan perubahan anda di [*issues*](https://github.com/bellshade/SQL/issues) kemudian lakukan *fork* pada repositori kami.
- Setelah melakukan *fork*, anda dibebaskan untuk mengubah atau menambah kode.
- Untuk *pull request* merubah atau memperbaiki, diusahakan kamu menerapkan kode yang lebih baik dan lebih mudah serta memeberikan penjelasan lebih detail alasan dari perubahaan tersebut lebih baik dari sebelumnya.
- Diusahakan untuk membuat branch baru setelah fork. Untuk membuat branch baru lihat tulisan kode dibawah ini :
  ```bash
  git checkout -b <branch_name>
  git add . # atau git add nama_perubahan_kamu
  git commit -m "feat: menambahkan materi SQL yaitu ..."
  ```
- Lakukan *push* ke *branch* kamu dan kemudian *open pull request*.

**Saran pesan commit**

- `feat:` untuk menambah algoritma, atau tambahan lainnya;
- `fix:` untuk mengubah algoritma yang sudah ada, atau memperbaiki;
- `docs:` untuk mengubah atau membuat dokumentasi;
- `add:` untuk menambah algoritma, atau tambahan lainnya (opsional); 

Catatan: Pesan commit harus menjelaskan perubahan secara singkat.

Contoh: 
- &#9746; feat: menambahkan materi SQL
- &#9745; feat: menambahkan materi SQL yaitu .....
- &#9745; docs: menambah penjelasan pada materi ......
- &#9745; fix: mengubah atau memperbaiki code SQL pada materi ......

Lebih lengkapnya bisa dilihat di:
- [EN](https://www.conventionalcommits.org/en/v1.0.0/)
- [ID](https://www.conventionalcommits.org/id/v1.0.0/)

Pull request akan di-*merge* jika:

- Mengikuti standar dan arahan dari `CONTRIBUTING.md`;
- Lulus test, dan cek dari beberapa tes (commit check) yang sudah kami siapkan.

**Tambahan**:

- Jika ada kendala atau masalah dalam *pull request*, kamu bisa laporkan masalahnya dalam [issues](https://github.com/bellshade/SQL/issues).
- Jika ada tes yang tidak lewat atau gagal, kami akan cek kembali perubahan anda.

Untuk *pull request*, disarankan untuk menjelaskan secara detail yang kamu ubah atau tambahkan, dan bersikap sopan serta selalu berterima kasih. Itu salah satu bentuk tata krama yang baik terhadap sesama *contributor* dan *programmer* lainnya.
