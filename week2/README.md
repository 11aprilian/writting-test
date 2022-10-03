# Writting Test Week 2

## JavaScript Scope dan Function

- Scope adalah konsep dalam flow data variabel. Menentukan suatu variabel bisa diakses pada scope tertentu atau tidak.

- Blocks adalah code yang berada didalam curly braces {}.Conditional, function, dan  looping menggunakan blocks.

- Global scope berarti variabel yang kita buat dapat diakses dimanapun dalam suatu file.Variabel harus dideklarasikan diluar Blocks.

    ```javascript
    let name = "Aprilian" ; 
    function greeting(){
        return name;
    }
        console.log(name);
    ```
- Local scope berarti kita mendeklarasikan variabel didalam blocks seperti function, conditional, dan looping.Variabel hanya bisa diakses didalam blocks saja.

    ```javascript
    function greetting(){
        let name = "Aprilian";
        return name;
    }
    console.log(gretting())
    console.log(name);
    ```

- Function adalah sebuah code blok dalam sebuah grup untuk menyelesaikan 1 task.

- Cara membuat function

    - Function clasic
        ```javascript
        function myFunction(condition) { }
        ```
    - Fanction variable
        ```javascript
        let myFunction = function (condition) { }
        ```
    - Arrow function
        ```javascript
        let myFunction = (condition) => { }
        ```

- Cara memanggil function
    ```javascript
    myFunction()
    console.log(myFunction());
    ```

- ### **Parameter Function**
    Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan task/tugas.
    Saat membuat function/fitur, kita harus tahu data-data yang dibutuhkan. Misalnya saat membuat function penambahan 2 buah nilai. Data yang dibutuhkan adalah 2 buah nilai tersebut.

    ```javascript
    function penambahan (a,b){ // (a,b) merupakan parameter
        return a + b;
    }
    ```

- Argumen Function
    Argumen adalah nilai yang digunakan saat memanggil function.
    Jumlah argumen harus sama dengan jumlah parameternya
    ```javascript
    function penambahan (a,b){ // (a,b) merupakan parameter
        return a + b;
    }
    console.log(penambahan(5,5)) // (5,5) adalah argumen
    ```

    <br>

## JavaScript Prototype and Method
Properties adalah nilai yang berkaitan dengan objek pada JavaScript.Properties biasanya dapat diubah, ditambahkan, dan dihapus, tetapi beberapa hanya dapat dibaca. Method JavaScript adalah properti yang berisi definisi fungsi. Metohd adalah fungsi yang disimpan sebagai properti objek

- ### **Data Type**

    - Type Data Primitive merupakan tipe data yang masih standar yang masih low level
    - Type Data Non-Primitive merupakan tipe data kembangan dari tipe data primitive.

        <br>

- **Type Data Primitive**
    - String
    - Number
    - Boolean 
    - Null  
    - Undefined 
    - Symbol 

-  **Type Data Non-Primitive**
    - Object, yaitu sebuah kumpulan pasangan properti dan nilai. Seperti objek dalam kehidupan sehari-hari saja.

    <br>

- ### **String JavaScript**

    Beberapa operasi yang paling sering digunakan pada string adalah memeriksa panjangnya, membangun dan menggabungkannya menggunakan operator string and, memeriksa keberadaan atau lokasi substring dengan metode indexOf(), atau mengekstrak substring dengan metode substring().

<br>

- ### **Number JavaScript**
    <div align="justify">Number merupakan tipe data yang digunakan untuk menunjukan angka, baik positif maupun negatif. 
    
    <br>

- ### Math JavaScript
    <div align="justify">Math adalah objek yang  telah di sediakan oleh javascript dengan math ini kita bisa bermain menolah data. 
    
    - Math memiliki berbagai macam properties 
        ```javascript
        console.log(Math.PI) // 3.141592653589793
        console.log(Math.LOG2E) // 1.4426950408889634
        ```
    - Method pada math mengembalikan nilai bulat
        ```javascript
        console.log(Math.abs(-5)) // 5
        ```
    - Mencari nilai hasil perpangkatan
        ```javascript
        console.log(Math.pow(3,2)) // 9
        ```
    - Mencari akar dari sebuah nilai
        ```javascript
        console.log(Math.sqrt(9)) // 3
        ```
    - Membulatkan angka
        ```javascript
        console.log(Math.round(123.123)) // 123
        ```
    - Membulatkan angka kebawah
        ```javascript
        console.log(Math.floor(20.5)) // 20
        ```
    - Membulatkan angka ke atas
        ```javascript
        console.log(Math.ceil(20.5)) // 21
        ```

## **Javascript : DOM**
DOM singkatan dari Document Object Model. DOM adalah Programing interface pada document web. DOM ini mempresentasikan halaman dimana kita bisa merubah struktur style , konten.

<br>

- ### **DOM - Traversing Elemets**
    <div align="justify">Menelusuri atau menjelajahi elemen - elemen menggunakan DOM. kali ini trafersing di kategorikan 3 bagian seperti berikut :

    <br>

    - Contoh file index.html
        ```javascript
        <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="UTF-8" />
            <meta http-equiv="X-UA-Compatible" content="IE=edge" />
            <meta name="viewport" content="width=device-width, initial-scale=1.0" />
            <title>Document</title>
        </head>
        <body>
            <h1 id="title">Hallo</h1>

            <ul class="list">
            <li class="item">satu</li>
            <li class="item">dua</li>
            <li class="item">tiga</li>
            </ul>

            <!-- Latihan -->
            <div class="hewan">
            <ul class="mamalia">
                <li>kucing</li>
                <li>kelinci</li>
                <li>kambing</li>
            </ul>

            <ul class="reptil">
                <li>kadal</li>
                <li>ular</li>
                <li>buaya</li>
            </ul>

            <ul class="unggas">
                <li>ayam</li>
                <li>bebek</li>
                <li>burung</li>
            </ul>
            </div>


            <script src="./script.js"></script>
        </body>
        </html>
        ```
<br>

- Mengakses DOM dengan traversing
    - Traversing kategori Ke Bawah
        - getElementById
            <div align="justify">Mengembalikan data dalam bentuk kumpulan dari elemen berdasakan nama ID nya

            ```javascript
            let title = document.getElementById("title")
            console.log(title) // <h1 id="title">Hallo</h1>
            ```
            
        - getElementsByClassName
            <div align="justify">Mengembalikan data dalam bentuk kumpulan dari elemen berdasakan nama class nya

            ```javascript
            let items = document.getElementsByClassName("item")
            console.log(items[2]); // <li class="item">tiga</li>
            ```

        - getElementsByTagName
            <div align="justify">Mencari Element berdasarkan nama tag nya

            ```javascript
            let itemByTag = document.getElementsByTagName("li")
            console.log(itemByTag[1])
            console.log(itemByTag.item(1))
            console.log(itemByTag.length)
            ```
        - querySelector
            ```javascript
            let listQuery = document.querySelector(".list")
            console.log(listQuery);
            ```
        - querySelectorAll
            ```javascript
            let itemQueryAll = document.querySelectorAll(".item")
            console.log(itemQueryAll)

            let itemQueryAll = document.querySelectorAll(".item")
            console.log(itemQueryAll) // mendapatkan data dalam bentuk node list
            ```

        <br>

    - Traversing ke atas
        - parentElement
            <div align="justify">Akses Parentsnya 
            ```javascript
            console.log(itemQuery.parentElement); // <ul class="list">...</ul>
            ```
        - closest
            <div align="justify">akses parents terjauhnya
            ```javascript
            console.log(itemQuery.closest(".list"));
            ```
    
    - Traversing ke Samping
        <div align="justify">Akses sibling atau saudaranya (sebelum atau sesudah elementnya)

        - previousElementSiblingc

            ```javascript
            console.log(itemQuery.previousElementSiblingc);
            ```
        - nextElementSibling
            ```javascript
            console.log(itemQuery.nextElementSibling);
            ```

## **DOM Manipulation**
Teknik manipulasi DOM merupakan teknik yang sangat penting dalam pengembangan website untuk meningkatkan interaktivitas dan kedinamisan. Ada banyak teknik untuk memanipulasinya, seperti membuat elemen baru, menyisipkan elemen, mengubah atribut, mengubah style, menambahkan event, dsb.

- Memberikan konten pada html dangan *innerText* dan *innerHTML*
    
    ```javascript
    app.innerText = "<h1>apa kabs</h1>"
    app.innerHTML = "<h1>Hallo</h1>"
    ```

- Membuat elemen dengan menggunakan *createElement()*

    ```javascript
    let p = document.createElement("p")
    p.innerText = "ini adalah paragraf"
    ```

- Menambahkan child kedalam parent menggunakan *append() dan appendChild*

    ```javascript
    app.append(p)
    ```

    ```javascript
    // proses yg sama
    let p2 = document.createElement("p")
    p2.innerText = "paragraf ke-2"
    app.appendChild(p2)
    ```
    - Perbedaan append() dan appendChild :
        <div align="justify">appendChild tidak bisa input data string

        ```javascript
        app.append("menggunakan append")
        app.appendChild("appendChild") // error
        ```

- Menghapus element menggunakan remove()
    ```javascript
    let end = document.getElementById("end")
    end.remove()
    ```

- Menambahakan atribut 
    ```javascript
    link.setAttribute("id", "google") // add attribute
    ```

- Memberikan style
    <div align="justify">Kita bisa memberikan styling pada html dengan menggunakan javascript DOM

    ```javascript
    link.style.color = "black"
    link.style.border = "1px solid black"
    link.style.padding = "5px 20px"
    link.style.backgroundColor = "aqua"
    ```
- Mendapatkan style dari element
    ```javascript
    let tess = document.getElementById("tess")
    let tessStyle = getComputedStyle(tess)
    console.log(tessStyle.height)
    ```

- Menambahnkan dan menghapus class
    ```javascript
    container.classList.add("home") // menambabhkan class
    container.classList.remove("container") // menghapus class
    ```
    <br>

## **JavaScript : DOM Events dan Forms**
- Events adalah sebuah kejadian/kegiatan/interaksi yang user berikan kepada website.
- Cara memberikan event

    - HTML Attribute.

        ```javascript
        <h1 onclick="alert('selamat datang')">Hallo</h1>
        ```

    - Event propperty

        ```javascript
        <p id="paragraf">click me</p>
 
        paragraf.onclick = function () {
        alert("ini dari paragraf")
        }
        ```

        Atau bisa juga dengan tampilkan alert

        ```javascript
        paragraf.onclick = tampilkanAlert

        function tampilkanAlert () {
        alert("ini alert")
        }
        ```
    - addEventListener()
        ```javascript
        <button id="btn">klik saya</button>

        let button = document.getElementById("btn")
        button.addEventListener("click", function (event) {
        console.log(event.target)
        alert("ini dari button")
        })
        ```

        

    

    




