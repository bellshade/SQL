## **Aliasing**

> Mengubah nama tabel atau kolom secara sementara, agar tabel atau kolom mudah dibaca dan dipahami saat menampilkan data.

### **1. Bentuk Umum**

`SELECT nama_kolom AS nama_kolom_alias`

`SELECT * FROM nama_tabel AS nama_tabel_alias`

### **2. Contoh**

  - Nama kolom : 
    
    SQL Query : `SELECT 5 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | 5   |
    | 5   |
    
    Penjelasan : 
    Menampilkan kolom bernilai 5 dengan nama **HASIL** disemua baris.
    
  - Nama kolom dari Tabel : 
    
    SQL Query : `SELECT gaji_karyawan as gaji FROM karyawan`
    
    Output :
    
    | gaji |
    | ----  |
    | 8000000   |
    | 9000000   |
    | 8500000   |
    
    Penjelasan : 
    Menampilkan kolom **gaji_karyawan** dengan nama **gaji** saat ditampilkan.

  - Nama Kolom dari hasil aritmatika :
    
    SQL Query : `SELECT gaji_karyawan_per_jam * waktu_kerja as total_gaji FROM karyawan`
    
    Output : 
    
    | total_gaji |
    | ---- |
    | 8000000   |
    | 9000000   |
    | 8500000   |
    
    Penjelasan : 
    Menampilkan hasil perhitungan kolom **gaji_karyawan_per_jam** dan **waktu_kerja** dengan nama **total_gaji** saat ditampilkan.
   
    - Nama tabel :
        
      SQL Query : `SELECT * FROM tabel_absen_mahasiswa AS tbl_mhs`
            
      Penjelasan : 
      menyingkat nama tabel **tabel_absen_mahasiswa** menjadi **tbl_mhs**
