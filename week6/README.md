# **Writing and Presentation Test Week 6**
## **DATABASE MYSQL BASIC**
### **Database Introduction**
Database adalah kumpulan informasi yang disimpan didalam komputer secara sistematik dan saling berelasi.

### **Database Management System**
DBMS adalah software yang dapat digunakan oleh user untuk berkomunikasi dengan data yang ada dalam media penyimpanan.
### **Istilah pada Database**
- **Table**
    <div align="justify">Table adalah kumpulan value yang dibangun oleh baris dan kolom, yang didalamnya berisikan atribut dari sebuah data.
    <div align="justify">contoh table :
- **Field**
    <div align="justify">Field adalah kolom dari sebuah tabel dimana masing-masing field memiliki tipe data masing-masing.
- **Record**
    <div align="justify">Record merupakan kumpulan nilai yang saling terkait. Record merupakan isi dari sebuah tabel.
- **SQL**
    <div align="justify">SQL atau Structured Query Language merupakan suatu bahasa (Language) yang digunakan untuk mengakses database.
    SQL adalah Bahasa Query yang digunakan untuk melakukan interaksi di RDMS (Relational Database Management System).
    - Membuat, Menampilkan dan menghapus data didalam database
    - Mengatur “Permission” (siapa saja yang bisa mengakses data
    - Membuat dan menghapus Database.
- **DDL (Data Definition Language)**
    <div align="justify">DDL merupakan kumpulan perintah SQL yang digunakan untuk membuat, mengubah dan menghapus struktur dan definisi metadata dari objek-objek Database.
   
    ```
    Contoh perintah membuat tabel mahasiswa
    create table mahasiswa(
        kode_mahasiswa varchar(10) auto_increment,
        nama varchar(50),
        jurusan varchar(50),
        primary key(nim)
    );
    ```
- **ALTER**
    <div align="justify">Alter digunakan untuk mengubah struktur dari tabel yang ada, seperti untuk menambahkan atau menghapus kolom/field.
    Membuat atau menghapus primary key, mengubah jenis kolom/field yang ada, juga mengubah kolom atau nama tabel.
  
    ```
    Menambah Primary Key
    ALTER TABLE nama_tabel ADD Primary key (nama field) ALTER TABLE pasien ADD PRIMARY KEY (KdPasien)
    Menambah Kolom/Field
    ALTER TABLE nama_tabel ADD Nama_Field Tipe_Data(Ukuran) ALTER TABLE table pasien ADD Alamat Pasien varchar(50)
    Mengubah struktur tabel untuk field Alamat Pasien dari Length (50) menjadi (40) ALTER TABLE pasien ALTER COLUMN Alamat Pasien varchar(40)
    ```
- **DROP**
     <div align="justify">Perintah Drop digunakan untuk menghapus Database, Table, dan View atau Index.
     
     ```
     DROP DATABASE nama-databas
     ```
### **DML (Data Manipulation Language)**
- **SELECT**
    <div align="justify">Perintah SELECT digunakan untuk menyeleksi data berdasarkan syarat yang diberikan.
    Dengan menggunakan perintah SELECT ini record didalam tabel tertentu yang berjumlah ribuan bahkan jutaan dapat ditampilkan.
  
    ```
    SELECT COLUMN_NAME FROM TABLE_NAME
    SELECT DISTINCT COLUMN_NAME FROM TABLE_NAME
    ```
- **INSERT**
    <div align="justify">INSERT	digunakan untuk memasukkan data ke kolom-kolom yang terdapat pada tabel/vie.
   
    ```
    INSERT INTO NAMA_TABLE (nama_field1, nama field2, ...nama_fieldN) VALUES (valuel, value2,...., valueN)
    ```
- **Where, And, Or, Not, Like**
    ```
    SELECT column1, colum2
    FROM table_name
    WHERE condition1 AND condition2 OR condition3 NOT condition;
    ```
- **UPDATE**
    <div align="justify">Digunakan untuk melakukan editing pada isi dari kolom (field) yang dipilih. Hal ini dilakukan untuk memperbaiki data lama / terjadi kesalahan.
  
    ```
    UPDATE table_name SET column_name ="new data" WHERE key_column = 1;
    ```
- **DELETE**
    <div align="justify">Digunakan untuk menghapus data dalam tabel yang menjadi target.
 
    ```
    DELETE FROM table_name WHERE condition;
    ```
### **Database Relationships**
Database relationship adalah relasi atau hubungan antara beberapa tabel dalam bahasa yang kita miliki.
Relasi antar tabel dihubungkan oleh Primary key dan foreign key.
- Primary key adalah atribut yang tidak hanya mengidentifikasi secara unik suatu kejadian, tapi juga mewakili setiap kejadian suatu entitas.
   
    ```
    create table mahasiswa(
        nim int primary key auto_increment,
        nama varchar(50),
        jurusan varchar(50),
    );
    nim pada tabel mahasiswa di jadikan primary key
    ```
- Foreign key adalah atribut yang melengkapi relationship dan menunjukan hubungan antara tabel induk dengan tabel anak.
  
    ```
    create table fav_movie(
        id_favMovie int primary key auto_increment,
        id_mahasiswa int,
        FOREIGN KEY (id_mahasiswa) REFERENCES mahasiswa(nim)
    );
    ```
### **Beberapa tipe database relationships:**
- One To One Relationships
- One to Many and Many to One Relationships
- Many to Many Relationships
- Self Referencing Relationships
Contoh kasus :
- One To One Relationships : 
    <div align="justify">Tabel mahasiswa dan tabel alamat yakni 1 mahasiswa hanya memiliki 1 alamat begitu pula sebaliknya 1 alamat ahnya di miliki 1 mahasiswa.
-  One to Many and Many to One Relationships :
    <div align="justify"> tabel Customers dan tabel order barang. yakni 1 customer dapat memiliki banyak order barang.
- Many to Many Relationships :
    tabel order dan tabel item yakni 1 order dapat memiliki banyak item begitu sebaliknya 1 item memiliki banyak order.
## **DATABASE MYSQL LANJUTAN**
### **SQL Table Join**
Join, adalah penggabungan tabel yang dilakukan melalui kolom/key tertentu yang memiliki nilai terkait untuk mendapatkan satu set data dengan informasi lengkap.
<br>
- Inner Join : menampilkan data hanya yang sesuai di kedua tabel.
   
    ```
    SELECT * FROM karyawan INNER JOIN gaji ON karyawan.karyawan_id = gaji.karyawan_id;
    ```
- Left Join : menampilkan semua data sebelah kiri dari tabel yang di joinkan dan menampilkan data sebelah kanan yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis
   
    ```
    SELECT * FROM karyawan LEFT JOIN gaji ON karyawan.karyawan_id = gaji.karyawan_id;
    ```
- Right Join : menampilkan semua data sebelah kanan dari tabel yang di joinkan dan menampilkan data sebelah kiri yang cocok dengan kondisi join. Jika tidak ditemukan kecocokan, maka akan di set NULL secara otomatis.
  
    ```
    SELECT * FROM gaji RIGHT JOIN karyawan ON gaji.karyawan_id = karyawan.karyawan_id;
    ```
### **NoSQL**
Database NoSQL adalah database yang tidak memiliki perintah SQL.
Konsep penyimpanannya semi struktural atau tidak struktural, dan tidak harus memiliki relasi layaknya tabel-tabel MySQL.

### **Kelebihan NoSQL di banding Relasional Database.**
- NoSQL bisa menampung data yang terstruktur, semi terstruktur dan tidak terstruktur.
- Menggunakan OOP dalam pengaksesan/manipulasi data.
- NoSQL tidak mengenal schema tabel yang kaku.
### **Document Database**
Document adalah salah satu dari beberapa model database NoSQL.
Mendefinisikan database sebagai dokumen artinya penyimpan data dan proses manipulasinya dalam bentuk Objek dokumen.
- Contoh objek dokumen yang sering diterapkan dalam pemrograman adalah format JSON.
### **Database Normalization**
- **Pengertian Database Normalization**
    <div align="justify">Merupakan teknik analisis data yang mengorganisasikan atribut-atribut data dengan cara mengelompokkan sehingga terbentuk entitas yang non-redundant, stabil, dan fleksible.
- **Tujuan Database Normalization**
    <div align="justify">Menghilangkan redundan data pada database.
    Memudahkan juka ada perubahan struktur table database.
    Memperkecil pengaruh jika ada perubahan dari struktur table database.
- **Efek Jika Tidak Melakukan Database Normalization**
    - INSERT Anomali : Situasi dimana tidak memungkinkan memasukkan beberapa jenis data secara langsung di database.
    - DELETE Anomali : Penghapusan data yang tidak sesuai dengan yang diharapkan, artinya data yang harusnya tidak terhapus mungkin ikut terhapus.
    - UPDATE Anomali : Situasi dimana nilai yang diubah menyebabkan inkonsistensi database, dalam artian data yang diubah tidak sesuai dengan yang diperintahkan atau yang diinginkan.
 

  ## Bentuk Database Normalization ##
 
-  **First Normal Form (1NF)**
    - Menghilangkan multiple value pada sebuah kolom table database
    - Sebuah table memenuhi kaidah 1NF jika :
        - Setiap kolom bernilai tunggal (single value)
        - Setiap kolom memiliki nama yang unik
        - Urutan penyimpanan data tidak menjadi masalah
- **Second Normal Form (2NF)**
    - Harus sudah dalam bentuk 1NF untuk mendapatkan 2NF
    - Menghapus beberapa subset data yang ada pada tabel dan menempatkan mereka pada tabel terpisah.
- **Third Normal Form (3NF)**
    - Menghilangkan seluruh atribut atau field yang tidak berhubungan dengan primary key. Dengan demikian tidak ada ketergantungan transitif pada setiap kandidat key.

### **Join Multiple Tables**
- **INNER JOIN**
    - Semua baris akan diambil dari kedua table yang akan di JOIN, selama columns cocok dengan kondisi yang sudah di tentukan.
    - Memungkinkan baris dari salah satu tabel muncul di hasil jika dan hanya jika kedua tabel memenuhi kondisi yang ditentukan dalam klausa ON.
- **LEFT JOIN**
    - Pada JOIN ini, semua records dari table di sisi kiri JOIN statement akan di pilih.
    - Jika record yang di pilih dari table kiri tidak memiliki record yang cocok pada table JOIN yang kanan, maka record tersebut masih dipilih, dan kolom pada table yang kanan akan bernilai NULL.
- **RIGHT JOIN**
    - Pada JOIN ini, semua records dari table di sisi kiri JOIN statement akan di pilih, bahkan jika table di sebelah kiri tidak memiliki record yang cocok.

## **EXPRESS JS MIDDLEWARE AUTHENTICATION & AUTHORIZATION**
### **Authentication**
Merupakan metode terhadap seorang pengguna mengkonfirmasi sebagai pengguna valid yang dapat mengakses sebuah akun atau informasi tertentu
### **Authorization**
Merupakan proses penentuan terhadap pengguna yang terautentikasi tersebut diizinkan atau ditolak untuk melakukan satu atau lebih akses terhadap sistem.
### **Encryption**
Merupakan proses pengubahan data menjadi format yang tidak bisa dibaca terkecuali apabila ada seseorang yang memiliki kunci untuk mengubah kembali data yang terenkripsi
### **Jenis Autentikasi**
- **Single Factor Authentication**
    <div align="justify">Autentikasi yang sangat sederhana dan banyak digunakan di masa sekarang. Autentikasi ini berupa memasukan sebuah identitas seperti password dan username.
- **Two Factor Authentication**
    <div align="justify">Autentikasi ini dibuat setelah Single Factor Authentication dipakai yaitu adanya tambahan autentikasi seperti OTP dan sidik jari atau wajah.
- **Multi Factor Authentication**
    <div align="justify">Autentikasi yang mewajibkan pengguna untuk memverifikasi 3 jenis identitas seperti ID pengguna (password dan username), sidik jari, dan beberapa pertanyaan yang berhubungan dengan pengguna.
### **Membuat Authentication dan Authorization**
Untuk penerapanya bisa menggunakan Express JS dengan bantuan module jsonwebtoken.
```javascript
const express = require('express');
const router = express.Router();
const jwt = require('jsonwebtoken')
const users = [
    {id : 1, email :"dhea@gmail.com", password: "123"},
    {id : 2, email :"ihza@gmail.com", password: "123"},
];
const KEY = "asdfjsdaklf234234";
router.post("/Login", (req, res) =>{
    const {email, password } = req.body;
    const userData = users.find((item) => 
    email === item.email && password === item.password);
    const token = jwt.sign(
        {
          id: userData.id,
        },
        KEY
      );
    if (userData) {
        return res.json({
            message : "secces login",
            token 
        });
    }
    else{
        res.statusCode = 401;
        res.json({
            message : "email or password are incorratct",
        });
    }
});
module.exports = router;
```
## **BUILD WEB SERVICE and RESTFUL API WITH EXPRESS & SEQUELIZE**
### **Sequelize**
Sequelize adalah ORM (Object Relational Mapping) Node JS yang berbasis promise.
### **ORM**
ORM adalah suatu metode/teknik pemrograman yang digunakan untuk mengkonversi data dari lingkungan bahasa pemrograman berorientasi objek (OOP) dengan lingkungan database relational.
### **Installation Sequelize**
- Install Sequelize-cli
     <div align="justify">menginstall sequelize cli agar dapat menjalankan generator menggunakan terminal sehingga lebih mudah.
    
    ```
    npm install -g sequelize-cli
    ```
- Install Sequelize
    <div align="justify">Ketika kita melakukan inisiasi project kita pertama perlu menginstall sequelize menggunakan npm install sequelize dan perlu menginstall driver sql yang kita butuhkan
   
    ```
    Installing by NPM
    npm install --save sequelize
    install Driver Database
    npm install --save mysql
    ```
### **Generate Sequelize**
- **Sequelize init**
    <div align="justify">kita perlu melakukan inisialisasi di project kita terlebih dahulu agar dapat melakukan generate code.
   
    ```
    npm sequelize-cli init
    ```
- **Generate Model**
    - Membuat table todo dengan field
    
    ```
    npx sequelize-cli model:generate --name Todo --attributes title:string, description: string, startTime:date, status:string
    ```
    - Kita dapat menggunakan generate dan kita bisa mengecek ke database sehingga dapat kita gunakan untuk penimpanan DB
    
    ```
    npx sequelize-cli db:migrate
    ```
    - Jika ada yang salah, kita bisa mengembalikan (undo) menggunakan :
   
    ```
    npx sequelize-cli db:migrate:undo
    ```
- **Generate Seed**
    <div align="justify">Seed adalah data awal yang bisa kita gunakan untuk mengisi data di database untuk keperluan awal project menggunakan sequelize
  
    ```
    npx sequelize-cli seed: generate --name demo-todo
    ```
    - Menjalankan generate seed menggunakan sequelize 
   
        ```
        npx sequelize-cli db:seed: all
        ```
    
    - bisa mengembalikan (undo) menggunakan
       
        ```
        npx sequelize-cli db:seed: undo
        ```
