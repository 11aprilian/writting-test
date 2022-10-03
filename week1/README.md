# **Writing and Presentation Test Week 1**

## **Unix Command Line Dan GitHub**

###  **Command Line Interface (CLI)**
  <div align="justify">CLI atau Command Line Interface adalah sebuah program yang memungkinkan user mengetik perintah atau command yang akan mmemerintahkan perangkat komputer untuk melakukan suatu tugas tertentu.
  
  <br>

  ### **Shell**
  <div align="justify">Shell adalah user interface pengelola CLI dan berperan sebagai perantara yang menghubungkan user dan sistem operasi. Maka dari itu user memerlukan yang namanya shell.

  <br>
 
  ### **Terminal**
  <div align="justify">User dan komputer dihubungkan dengan namanya terminal, yaitu tempat/aplikasi dimana user dapat mengetikan atau memberikan suatu perintah. Disinilah tempat dimana shell akan berperan.

  <br>

  ### **File System Structure**

  <div align="justify">Struktur dimana mengatur cara bagaimana data disimpan dalam sistem. Contoh dalam Sistem Operasi Windows struktur file yang disimpan menggunakan struktur yang bentuknya mirip sebuah pohon seperti gambar dibawah.

  <br>

    ## Berikut adalah tampilan dari Command Line Interface :


- ## Beberapa perintah navigation files dan directory

  - pwd (print working directory), untuk melihat current working directory 
  - ls (list), untuk melihat isi file di dalam directory
  - ls - la ,untuk melihat files yang di hidden 
  - cd (change directory), untuk masuk ke directory tertentu
  - cd .. ,merupakan command untuk berpindah directory
  - mkdir ,digunakan untuk membuat directory baru
  - dir (directory), untuk melihat directory
  - touch, untuk membuat file directory
  - ni, digunakan untuk membuat file di windows
  - cp (copy), untuk menyalin file directory
  - cp -r ,digunakan untuk menyalin directory 
  - mv (move), untuk memindahkan file directory
  - rm (remove), untuk menghapus file directory

  <br>
 
  ### Perbedaan  Git dan GitHub
- **Git**
  <div align="justify">Git adalah sebuah software berbasis Version Control System (VCS) yang bertugas untuk mencatat perubahan seluruh file atau repository suatu project.

  <br>
- **GitHub**
  <div align="justify">GitHub merupakan layanan cloud yang berguna untuk menyimpan dan mengelola sebuah project yang dinamakan repository (repo git).

  ### Alasan kenapa Git dan Github tools yang wajib digunakan
  Dengan menggunakan GIT dan Github, kamu akan bisa bekerja dalam sebuat tim. **Tujuan besarnya** adalah kamu bisa berkolaborasi mengerjakan proyek yang sama tanpa harus repot copy paste folder aplikasi yang terupdate.
  Kamu juga tidak perlu menunggu rekan dalam satu tim kamu menyelesaikan suatu program dahulu untuk berkolaborasi. Kamu bisa membuat file didalam projek yang sama atau membuat code di file yang sama dan menyatukannya saat sudah selesai.
  
&nbsp;

### Langkah bekerja dengan Git untuk mempublish ke GitHub

<br>

- Masuk ke dalam git bash dengan cara klik kanan pada file yang akan di      publish lalu klick "Git Bash Here"

- membuat Repository dengan masuk ke dalam Aplikasi GitHub

- Lakukan beberapa Command di dalam git
  - git init <nama_proyek>, untuk membuat repositori baru

    ```
    git init namarepo
    ```
    <div align="justify">Karena kita sudah membuat repositoy sebelumnya maka kita bisa gunakan ini langsung tanpa harus memberi nama repo baru

    ```
    git init.
    ```
  - git status, digunakan untuk melihat apakah terjadi perubahan atau tidak pada git
    ```
    git status
    ```
  - git add <nama_file>, di gunakan untuk manambah file baru/ menambah perubahan pada file
    ```
    git add namafile   
    ```
    ```
    git add . 
    ```
  - git commit -m "Pesan", di gunakan untuk menyimpan perubahan pada git
      ```
      git commit -m "Pesan"
      ```
  - git remote, digunakan untuk menghubungkan project local yang tlah kita buat ke repository
    ```
    git remote add origin "Link repository pada GitHub"
    ```
  - git push, diguanakan untuk mengirim perubahan file ke remote repository
    ```
    git push -u origin master
    ```

  <hr>
  <br>

## **HTML**

- ### **Penejelasan HTML**
  <div align="justify">HTML adalah singkatan dari Hypertext Markup Language. HTML adalah bahasa komputer yang digunakan untuk membuat kerangka atau struktur untuk Web pages (halaman website) di internet.
  Fungsi HTML adalah sebagai 'kerangka' dari sebuah website.

  <br>
  Catatan : 
  
  > HTML bukanlah sebuah bahasa pemrograman, artinya HTML tidak bisa dinamis mengolah data.

 - ### **HTML Structure**
```html
  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <p>Hello World</p>
</body>
</html>
  ```

-  ### HTML Element
    <div align="justify">terdiri atas opening tag, content, closing tag
    <br>

    - opening tag :
    
      ```html
      <p>
      ```
    - content : Hello world
    - closing tag :

      ```html
      </p>
      ```
- ### HTML Atribut
  Property dari subah element HTML. Contohnya id, class, name.

- ### Single Tag atau Singular Tag 

  ```html
  <br> <!-- Membuat baris baru -->
  <hr> <!-- Membuat Garis Horizontal -->
  <img src=""/> <!-- Untuk Menmapilkan gambar-->
  ```

- ### Paired Tag atau Double Tag

  ```html
  <h1></h1> 
  <p></p>
  ```

- ### HTML Command
  <div align="justify">Digunakan untuk memberikan komentar atau keterangan pada suatu line code

  ```html
  <!-- Komentar -->
  ```

  <hr>

## **CSS**
- ### Penjelasan CSS
  <div align="justify">CSS (Cascading Style Sheets)adalah bahasa yang digunakan untuk mendesain halaman website.
  Dengan CSS, kita bisa mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya.

  <br>

- ### Struktur CSS
  ```css
  .elementshtml{
    property : value
  }
  ```
- ### CSS Comment
  <div align="justify">Dengan menggunakan CSS Comment, kita dapat memberikan penjelasan maksud dari line code yang kita kerjakan.

  ```css
  /* Komentar */
  ```

   ## 3 Cara Menggunakan CSS
  - **Inline Styles**
    <div align="justify">Inline styles adalah kita menambahkan CSS pada attribute element HTML

    ```html
    <P style="color : blue; font-size : 40px">Hello world</p>
    ```

  - **Internal CSS**
    <div align="justify">Menambahkan kode Style pada html di bagian head. contohnya seperti berikut :

    ```html
    <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
          <style>
              h1 {
                  color : blue;
                  font-size: 40px;
              }
          </style>
      </head>
      <body>
          <h1>Hello World</h1>
      </body>
      </html>
    ```

  - **Eksternal CSS**
    <div align="justify">Jika kita membutuhkan banyak code pada CSS, direkomendasikan untuk memisahkan code CSS di file tersendiri (extension .css) dan terpisah dari file HTML.
    <br>

    - Pada file index.html
      ```html
      <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
          <link rel="stylesheet" href="style.css">
      </head>
      <body>
          <h1>Hello World</h1>
      </body>
      </html>
      ```

    - Pada file style.css
      ```css
      h1 {
        color : blue;
        font-size : 40px;
      }
      ```

## **Algoritma Dan Struktur Data**

- ### Penjelasan Algoritma
  <div align="justify">Programming itu justru identik dengan memecahkan suatu permasalahan, maka dari itu algoritma merupakan pemeran utamanya, bahasa pemrograman hanyalah pemeran pendamping. Belajar algoritma sama aja dengan mengingat kembali alur berfikir yg terstruktur.
  
<br>

## Jenis Proses Algoritma

  - Sequence, Instruksi yang dijalankan secara berurutan.
  - Selection, Instruksi yg dijalankan jika memenuhi suatu kondisi.
  - Iteration, Instruksi yg berulang kali dijalankan selama memenuhi suatu kondisi.
  - Concurrent, Instruksi yg dijalankan secara bersamaan.

  <br>

##  Penyajian Algoritma

  - Deskriptif, Penulisan algoritma dengan cara deskriptif seperti kita menulis tutorial (tata cara) dengan bahasa sehari-hari.
  - Flow Chart, Flow chart atau diagram alir, penyajian algoritmanya lebih mudah dibaca karena memiliki tampilan visual. Flow chart menggunakan simbol bangun datar sebagai representasi dari proses yg dilakukan.
  - Pseudo Code, Penulisan algoritma yg hampir menyerupai penulisan pada kode pemrograman.

  <br>

## **JAVASCRIPT DASAR**

 ## Penjelasan Javascript
  <div align="justify">Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website. Javascript juga dapat membuat website menjadi interaktif dan dinamis.Javascript dijalankan melalui browser pada device setiap user. 


 ## Syntax Dan Statement
  <div align="justify">Syntax bisa dianalogikan seperti kosa kata (vocabulary) dan tata cara (grammar) pada bahasa pemograman.Kita menggunakan syntax tertentu untuk membuat statement program, instruksi untuk djalankan/dieksekusi oleh web browser, compiler, ataupun intrepreter.

 ## Contoh Syntax Javascript
 - Alert()
 - Prompt()
 - Confirm()

 ## Console Log
 <div align="justify">Console log adalah tempat kita untuk cek logic pemograman web yang kita kembangkan. Console log juga tempat kita untuk melakukan debugging (mengetahui error pada code) pada pemograman web.

   ```js
  console.log()
  ```

  <br>

## Comments
<div align="justify">Comments adalah sintaks yang digunakan untuk memberi keterangan tentang suatu statement. Menggunakan bahasa inggris atau bahasa indonesia. Comments tidak akan dijalankan oleh program karena hanya untuk dibaca oleh sesama programmer ataupun diri sendiri untuk memahami maksud dan tujuan sebuah statement/syntax.

- Single Comment

   ```js
   // comments
  console.log()
  ```

- Multiline Comment
  ```js
   /*
  This all commented
  console.log()
  */
  ```

## Tipe Data
<div align="justify">Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming.

<br>

Ada 6 tipe data fundamental pada Javascript :
- number
- string
- boolean
- null
- undefined
- object

## Variabel
<div align="justify">Variable adalah container/tempat untuk menyimpan sebuah nilai.
<br>
3 Cara penulisan tipe data :

<br>

- Var
  ```js
  var nama = "ihza";
  console.log(nama); //Output "ihza"
  ```
- Let, value dapat diubah
  ```js
  let nama = "ihza";
  console.log(nama) //Output "ihza"
  ```
- Const, value tidak dapat diubah
  ```js
  const nama = "ihza";
  console.log(nama); //Output "ihza"
  ```

<br>

## Operator
- Assignment Operator, digunakan untuk menyimpan sebuah nilai pada variabel. (=)
- Increment dan Decrement, untuk menambah atau mengurangi sebesar 1 nilai. (++, --)
- Arithmetic Operator, operator yang melibatkan operasi matematika. (+, -, *, /, %)
- Comparisson Operator, membandingkan satu nilai dengan nilai lainnya. (<, >, <=, >=, ===, !==)
- Logical Operator, digunakan untuk sebuah CONDITIONAL pada pemograman. (&&, ||, !)


















