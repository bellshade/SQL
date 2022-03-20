## **Operator Perbandingan**

> Merupakan Operator yang digunakan untuk melakukan perbandingan antara 2 nilai untuk mendapatkan salah satu atau hasil dari perbandingan nilai yang diinginkan ketika mengambil data di database, operasi pada operator memiliki bentuk umum berupa 2 operand lalu dibandingkan dengan 1 operator, seperti contoh berikut

### **1. Bentuk Umum**

`SELECT` + Operand + Operator + Operand ..... dst
     
Note : 
> Dalam SQL penulisan Operasi operator harus diawali dengan key `SELECT` agar hasil dari operasi tersebut bisa ditampilkan
> Operand adalah value yang akan dibandingkan / di operasikan untuk menemukan hasil nilai baru

### **2. Operator Perbandingan**

| Operator | Nama     | Penjelasan |
| ----     | -------- | ----------- |
| <        | Kecil Dari     | Nilai 1 yang lebih kecil dari nilai ke 2 |
| >        | Besar Dari      | Nilai 1 yang lebih besar dari nilai ke 2 |
| <=        | Kecil dari Sama Dengan |  Nilai 1 yang lebih kecil dan bisa sama dengan nilai ke 2 |
| >=       | Besar Dari Sama Dengan    |  Nilai 1 yang lebih besar dan bisa sama dengan nilai ke 2 |
| ==        | Sama Dengan   |  Nilai 1 harus sama dengan nilai ke 2 |
| !=  | Tidak Sama Dengan   | Nilai 1 tidak boleh sama dengan nilai ke 2 |
| LIKE  | Operator yang mengandung nilai didalam nya   | Mencari apakah nilai ke 2 mengandung nilai 1 didalam nya |
     
### **3. Contoh**

  - Kecil Dari : 
    
    SQL Query : `SELECT 5 < 9 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | true    |
    
    Penjelasan : 
    hasilnya true karena secara logika benar 5 lebih kecil dari 9
    
  - Besar Dari : 
    
    SQL Query : `SELECT 9 > 12 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | false    |
    
    Penjelasan : 
    hasilnya adalah false karena secara logika 9 bukan lebih kecil dari 12
    
  - Lebih Kecil Sama Dengan : 
    
    SQL Query : `SELECT 9 <= 9 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | true   |
    
    Penjelasan : 
    hasilnya bisa dikatakan true karena secara logika nilai 1 bisa lebih kecil atau bisa sama dengan nilai 2
    
  - Lebih besar sama dengan  : 
    
     SQL Query : `SELECT 15 >= 11 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | true    |
    
    Penjelasan : 
    hasilnya bisa dikatakan true karena secara logika nilai 1 lebih besar atau bisa sama dengan nilai 2
    
- Sama Dengan : 
    
    SQL Query : `SELECT 2 == 3 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | false   |
    
    Penjelasan : 
    hasilnya dikatakan false karena nilai 1 tidak sama dengan nilai 2
    
- Sama Dengan : 
    
    SQL Query : `SELECT 2 != 3 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | true   |
    
    Penjelasan : 
    hasilnya dikatakan false karena benar nilai 1 tidak sama dengan nilai 2

[<< Materi sebelumnya](https://github.com/bellshade/SQL/tree/main/Basic/05_SQL_Operator/1_Operator_Aritmatika) | [Materi selanjutnya >>](https://github.com/bellshade/SQL/tree/main/Basic/05_SQL_Operator/3_Operator_Logika)