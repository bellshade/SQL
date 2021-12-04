## **Operator Aritmatika**

> Merupakan Operator yang digunakan untuk melakukan operasi matematika dasar seperti menambahkan, mengurangi, perkalian dan pembagian suatu nilai untuk mendapatkan nilai yang diinginkan ketika mengambil data di database, operasi pada operator memiliki bentuk umum berupa 2 operand lalu dibandingkan dengan 1 operator, seperti contoh berikut

### **1. Bentuk Umum**

`SELECT` + Operand + Operator + Operand ..... dst
     
Note : 
> Dalam SQL penulisan Operasi operator harus diawali dengan key `SELECT` agar hasil dari operasi tersebut bisa ditampilkan
> Operand adalah value yang akan dibandingkan / di operasikan untuk menemukan hasil nilai baru


### **2. Operator Aritmatika**


| Operator | Nama     |
| ----     | -------- |
| +        | Penjumlahan     |
| -        | Pengurangan      |
| *        | Perkalian |
| /        | Pembagian    |
| ^        | Pangkat   |
| % atau MOD  | Sisa Bagi / Modulus    |
     
### **3. Contoh**

  - Penjumlahan : 
    
    SQL Query : `SELECT 4 + 6 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | 10    |
    
  - Pengurangan : 
    
    SQL Query : `SELECT 7 - 3 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | 4    |
    
  - Perkalian : 
    
    SQL Query : `SELECT 4 * 5 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | 20   |
    
  - Pembagian : 
    
    SQL Query : `SELECT 20 / 4 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | 5    |
    
- Pangkat : 
    
    SQL Query : `SELECT 2 ^ 3 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | 8   |
    
 - Sisa bagi / Modulus : 
    
    SQL Query : `SELECT 10 % 3 as HASIL`
    
    Output : 
    
    | HASIL |
    | ----  |
    | 1    |
