# **Writing and Presentation Test Week 3**

## Array dan Multidimensional Array
Array adalah tipe data list order yang dapat menyimpan tipe data apapun 
- Contoh Array
    ```javascript
    let key = ["Aprilian", 11 , true] // array dapat menyimpan berbagai macam tipe data 
    console.log(key) 
    ```
- Membuat array
    
    Array didefinisikan menggunakan square brackets [ ]

- Memanggil Array
    
    Array pada javascript dihitung dari index data ke-0. Data pertama adalah index ke-0.
   
    ```javascript
    let key = ["Aprilian", 11 , true] // array dapat menyimpan berbagai macam tipe data 

    console.log(key)
    // hasil
     0 : "Aprilian" // index 0
     1 : 11  // index 1
     2 : true  // index 2
     length : 3 // panjang array

     console.log(key[0]) // Output : "A"
     console.log(key[2]) // Output : true
    ```
- Update Array

    ```javascript
    let key = ["Aprilian", 11 , true]
    key[0] = "Ihza";

    console.log(key)
    // output : ["Ihza", 1 , true]
    ```


  ## Const in Array

    - Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
    - Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.

        ```javascript
        let motor = ['kawasaki', 'honda', 'suzuki'];
        motor = ['yamaha']
        console.log(motor) // error

        motor[2] = ['yamaha']
        console.log(motor) 
        // Output : ['kawasaki', 'honda', 'yamaha'];
        ```

- Array Properties
    
    Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype.

- Array Method
    - Array memiliki method atau biasa disebut built-in methods.
    - Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan.

    - Contoh Array Built-in Methods
        - .push
            
            method untuk menambahkan item  array pada urutan yang paling akhir.

            ```javascript
            let motor = ['kawasaki', 'honda', 'suzuki'];
            motor.push('yamaha');
            console.log(motor)
            // Output : ['kawasaki', 'honda', 'suzuki', 'yamaha'];
            ```
        - .pop()
           
           method yang menghapus item array index terakhir.

            ```javascript
            let motor = ['kawasaki', 'honda', 'suzuki', 'yamaha'];
            motor.pop()
            console.log(motor)
            // Output : ['kawasaki', 'honda', 'suzuki'];
            ```
        - .shift()
            
             method untuk menghapus item Array pada index pertama
            
            ```javascript
            let motor = ['kawasaki', 'honda', 'suzuki', 'yamaha'];
            motor.shift()
            console.log(motor)
            // Output : ['honda', 'suzuki', 'yamaha'];
            ```
        - .unshift() 
            <div align="justify">method untuk menambahkan item Array pada index pertama.

            ```javascript
            let mobil = ['honda', 'suzuki', 'yamaha'];
            motor.unshift('kawasaki')
            console.log(motor)
            // Output : ['kawasaki', 'honda', 'suzuki', 'yamaha']
            ```
        - .sort()
            
            method untuk mengurutkan secara Ascending atau Descending Alphanumeric
            
            ```javascript
            let numb = [1, 4, 3, 2]
            numb.sort()
            console.log(numb)
            // Output : [1, 2, 3, 4]
            ```
- Looping pada Array
    - built in method looping array .map() dan .forEach()
        - .forEach()
            
            method untuk melakukan looping pada setiap elemen array.

            ```javascript
            let motor = ['honda', 'suzuki', 'yamaha'];
            motor.forEach(element => {
            console.log(element); 
            // Output : 'honda', 'suzuki', 'yamaha'
            })
            ```
        - map() 
             
             melakukan perulangan/looping dengan membuat array baru.

             ```javascript
             let numb = [1, 3, 4, 2]
             let double = numb.map(num =>{
                return num * 2
             })

             console.log(double)
             // Output : [2, 6, 8, 4]
             ```

<br>

## **JavaScript Object & Array of Object**
Object adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method)

- ### Membuat sebuah object

    ```javascript
    let person = {
        name : 'Aprilian',
        age : 20,
        isVerified : true
    }
    ```
- ### Mengakses Object dan Property Object
    - Akses seluruh object
        ```javascript
        let person = {
            name : 'Aprilian',
            age : 20,
            isVerified : true
        }
        console.log(person)
        ```
    - Gunakan single quote pada key jika menggunakan spasi seperti ‘current address’
        ```javascript
        let person = {
            name : 'Aprilian',
            age : 20,
            ‘current address’ : 'Tulungagung, East Java'
        }
        console.log(person)
        ```
    - Mengakses properti object
        ```javascript
        let person = {
            name : 'Aprilian',
            age : 20,
            isVerified : true
        }
        console.log(person.name) // 'Aprilian'
        ```

    - Bracket Notation

        ```javascript
        let person = {
            name : 'Aprilian',
            age : 20,
            isVerified : true
        }
        console.log(person['name']) // 'Aprilian'
        console.log(person['age']) // 20
        ```
- ### Update Object

    - Do’s
        - Object dapat mengupdate value dari key yang sudah tersedia
        - Object dapat menambahkan key dan value baru

    - Update data pada Object
        ```javascript
        let person = {
            name : 'Aprilian',
            age : 20,
            isVerified : true
        }
        person.age = 19;
        person,addres = 'Tulungagung, Jawa Timur';

        console.log(person)
        /* Output :
        {
            name : 'Aprilian',
            age : 19,
            isVerified : true
            addres : 'Tulungagung, Jawa Timur'
        } */
        ```

        - Jika menggunakan constant pada variable object.
            ```javascript
            const person = {
                name : 'Aprilian',
                age : 20,
                isVerified : true
            }
            person.age = 19;
            person,addres = 'Tulungagung, Jawa Timur';

            console.log(person) // error
            ```
        - Jadi jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel.

- ### Delete Object Property
    - Kita dapat menghapus properti dari object menggunakan delete operator.
        ```javascript
            const person = {
                name : 'Aprilian',
                age : 20,
                isVerified : true
            }
            delete person.age;
            console.log(person) 
            /* Output :
            {
                name : 'Aprilian',
                isVerified : true
            }

        ```
- ### Method
    - Kita bisa membuat method custom untuk kita gunakan pada aplikasi kita.
   
        ```javascript
        const greeting = {
            welcome : function () {
                return 'Hallo';
            },
            goodBye : function () {
                return "Bye";
            },
        };

        console.log(greeting.welcome()); // Hallo
        console.log(greeting.goodBye()); // Bye
        ```

- ### Nested Object
    - Pada real application nanti kalian pasti menemukan data object yang kompleks. Object yang berasal dari turunan object lainnya.
    - Contoh : Data article pada sebuah aplikasi berita
        ```javascript
        const news = {
            title: 'Impact Byte',
            description: 'Hello Guys',
            author : {
                person : {
                    name : 'Aprilian',
                    age : 20,
                    city : 'Tulungagung'
                }
            }
        };
        console.log('news:', news.title);
        console.log('Article publised by', news.author.person);
        ```

- ### Looping Object
    - Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping.
        ```javascript
        for(let key in object){
            //..
        }
        ```
- ### **Array of Object**
    - Object sama seperti Array yang bisa menyimpan banyak data.

        ```javascript
        let students = [
            {
                name : "Aprilian",
                age : 20,
                isVerified : true
            },
            {
                name : "Ihza",
                age : 21,
                isVerified : false
            },
            {
                name : "Dhea",
                age : 20,
                isVerified : true
            }
        ];

        // gunakan forEach jika object dalam array
        students.forEach((ListStudent) => {
            console.log(ListStudent)
        })
        ```
        
## **JavaScript Rekursif**
- Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Recursive kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation.
 
- A New Paradigm:
    - procedural
    - conditional
    - looping
    - modular (function)
    - recursive

- Ciri dari rekursif:
    - Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
    - Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.


## **JavaScript Modules**
- Js Modules adalah cara untuk memisahkan kode file yang berbeda
- Keuntungan menggunakan modules : 
    - mudah untuk mengelola file
    - kode tidak menumpuk pada satu file

- Membuat Js Modules :
    - tambahkan type= "module" pada script utama
        ```javascript
        <script src="indonesia.js" type="module"></script>
        ```
    - siapkan script ke-2 dan seterusnya untuk melakukan export
    - lakukan import pada file/script utama

- contoh Export Import js module
    - script Amerika.js
        ```javascript
        let apple = ["iphone", "macbook", "imac"]
        export {apple}
        ```
    - script jepang.js
        ```javascript
        import {apple} from './amerika.js';
        console.log(apple);

        let motor = ["suzuki", "yamaha", "honda", "kawasaki"]
        const smartPhone = ["sony", "samsung", "fujitsu", "LG"]

        let dokumenNegara = "Hello"

        export function sayHello() {
        console.log("hallooo")
        }
        let entertainment = ["anime", "manga", "wibu", "dorama"]

        // kita dapat melakukan export pada variabel, function, class
        // "export" dapat melakukan banyak export
        // "export" di tangkap (import) menggunakan kurung kurawal
        // "export default" cuma bisa 1 aja yg di export
        // "export default" ditangkap tanpa kurung kurawal
        export { motor, smartPhone as smartPhoneJepang}
        export default entertainment
        ```
    - script indonesia.js
        ```javascript
        // import dari file jepang dan amerika
        import Entertainment, { motor as motorJepang, smartPhoneJepang, sayHello } from "./jepang.js"
        import {apple} from './amerika.js';

        sayHello()

        console.log(Entertainment);
        console.log(smartPhoneJepang);

        console.log(motorJepang);

        motorJepang.splice(1, 1)

        console.log(motorJepang)
        console.log(apple);
        ```
        <br>

## **JavaScript Asynchronous**

### **Introduction**
- Penjelasan 
    
    Javascript adalah bahasa pemrograman single-thread yang artinya hanya dapat mengeksekusi satu task pada satu waktu atau biasa disebut synchronous.

- Pada konsep pemrograman (web development pada case kita) dikenal istilah Asynchronous.
- Asynchronous mengizinkan komputer memproses task yang lain sambil menunggu proses yang masih berlangsung.
- Kita bisa membuat asynchronous secara simulasi artinya tidak murni asynchronous dengan beberapa cara:
    - Callback
    - Promises
    - Async/Await

### **Callback**
- Callback function adalah function yang kita letakan di dalam argumen/parameter pada function, dan function tersebut akan dieksekusi setelah function pertama menyelesaikan tugasnya.
    ```javascript
    const mainFunc = (number1, number2, callBack) => {
        console.log(number1 + number2)
        callBack()
    }

    const myCallback = () => {
        console.log('Done !')
    }
    main(1,2,myCallback) // Output : 3 Done !
    ```
- Proses asynchronous identik dengan delay, dimana hasil dari proses tersebut membutuhkan selang waktu tertentu untuk menghasilkan output. 

- synchronous atau lawan dari asynchronous
    <div align="justify">yaitu program dijalankan sesuai urutan code
    
    ```javascript
    function p1(){
            console.log('p1 berhasil di jalankan')
    }
    function p2(){
        console.log('p2 berhasil di jalankan')
    }
    function p3(){
        console.log('p3 berhasil di jalankan')
    }
    p1();
    p2();
    p3();
    /* Output : 
    p1 berhasil di jalankan
    p1 berhasil di jalankan
    p1 berhasil di jalankan */
    ```
- Pada asynchronous kita menggunakan setTimeOut untuk simulasinya. Proses function pada p2 kita lewati sambil menunggu selesai, program lanjut ke function p3
    ```javascript
    const p1() => {
            console.log('p1 telah selesai di jalankan')
    }
    function p2() =>{
        setTimeout(() => {
        console.log('p2 berhasil di jalankan')
        }, 3000)
    };
    const p3() =>{
        p1();
        p2();
        console.log('p3 berhasil di jalankan')
    }
    p3();
    ```
    - setTimeout digunakan untuk simulasi asynchronous. Karena sebenarnya kita tidak bisa membuat proses asynchronous murni.

### **Promises** 
- Promise adalah salah satu fitur baru di ES6, biasa digunakan untuk melakukan http request/fetch data dari API.
- Dalam pengambilan data, promise memiliki 3 kemungkinan state.
    - Pending(sedang dalam proses)
    - Fulfilled (berhasil)
    - Rejected (gagal)
    ```javascript
    console.log("PROMISES")
    // pembuatan promise.............
    let nontonPromise = new Promise((resolve, reject) => {
    if (true) {
        resolve("nonton terpenuhi") // berhasil
    } 

    reject("gagal"); // gagal
    });

    // eksekusi proses..............
    console.log("A");

    nontonPromise
    .then((result) => {
        console.log(result);
        return `${result} bareng doi`
    })
    .then((result) => {
        console.log(result)
    })
    .catch((err) => {
        console.log(err);
    });

    console.log("C");
    ```

### **Async-Await**
- Async - await adalah salah satu fitur baru dari javascript yang digunakan untuk menangani hasil dari sebuah Promise.
- Sedangkan await berfungsi untuk menunda sebuah kode dijalankan sampai proses asynchronous berhasil.
- Cara penulisan Async/await menggunakan es6 dan tidak menggunakan es6.
    ```javascript
    async function hello(){
        let result = await 'Hello'
        return result
    }
    // es 6
    const hello1 = async () => {
        let result = await 'hello'
        return result
    }
    ```

### **HTTP Request fetch()**
- Fetch adalah native web API untuk melakukan HTTP calls dari external network.
- fetch() memiliki parameter utama yaitu URL/endpoint API, dan parameter kedua yaitu options, options ini berisi method, headers dan body. Tergantung keinginan kita.

<br>

## **JavaScript Web Storage**
- Ada beberapa cara untuk menyimpan data pengguna seperti pencarian, artikel berita, dan lain-lain ke lokal (browser) menggunakan web storage seperti cookies, local storage, dan session storage. 

### Cookies
- Cookies adalah data kecil yang dikirim dari situs web dan disimpan di komputer kita oleh web browser saat kita menjelajah. Disebut data kecil karena maksimum data yang dapat disimpan dalam cookies adalah 4096 bytes (4 KB).
- Biasanya data yang disimpan di cookies adalah access token pengguna saat login atau data pencarian saat melakukan pencarian pada situs web tertentu.

### **Local Storage**
- Dengan memanfaatkan local storage dan session storage, kita dapat menyimpan data lebih besar yaitu 5MB per page tanpa mempengaruhi kinerja situs web.
- Namun, penting untuk diketahui agar kita tidak menyimpan data sensitif seperti password ke dalam local storage ataupun session storage untuk menghindari serangan pencurian data.
- Pernahkah kita saat melakukan pencarian pada sebuah situs lalu situs tersebut menampilkan riwayat pencarian kita? Iya, data pencarian tersebut disimpan ke dalam local storage untuk diolah menjadi riwayat pencarian.
- Local storage memiliki karakteristik sebagai berikut:
    - Menyimpan data tanpa tanggal kadaluarsa.
    - Data tidak akan dihapus ketika web browser ditutup dan akan tersedia seterusnya selama kita tidak menghapus data local storage pada web browser.
    - Dapat menyimpan data hingga 5MB.
    - Hanya dapat menyimpan data string.

- Untuk menyimpan data pada local storage, kita menggunakan method setItem() yang membutuhkan 2 parameter. Parameter pertama adalah key yang ingin kita simpan dan parameter kedua adalah data (value) dari key yang akan disimpan.
    ```javascript
    localStorage.setItem('key', value);
    ```
- Untuk mengambil data yang telah tersimpan pada local storage, kita dapat menggunakan method getItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang kita inginkan.
    ```javascript
    localStorage.getItem('key');
    ```

- Untuk menghapus data yang telah tersimpan pada local storage, kita dapat menggunakan method removeItem() yang membutuhkan 1 parameter. Parameter tersebut adalah key dari data yang ingin kita hapus.
    ```javascript
    // menghapus key tertentu
    localStorage.removeItem("key");

    // menghapus semua key
    localStorage.clear();
    ```
### **Session Storage**
- Berbeda dengan local storage, walaupun masuk ke dalam web storage, data yang tersimpan pada session storage akan hilang ketika session dari sebuah laman berakhir.
- Session storage mempunyai beberapa karakteristik, yaitu:
    - Data yang disimpan pada session storage akan terus tersimpan selama browser terbuka dan tidak hilang jika laman di-reload.
    - Membuka banyak tab/window dengan URL yang sama, akan menciptakan session storage yang berbeda di masing-masing tab/window.
    - Menutup tab/window akan mengakhiri session dan menghapus data yang tersimpan di session storage pada tab/window tersebut.
    - Data yang tersimpan dalam session storage harus berbentuk string.
    - Hanya dapat menyimpan data sebanyak 5MB.

- sintaks untuk menyimpan data pada session storage adalah sebagai berikut:
    ```javascript
    // menambah session storage
    sessionStorage.setItem('key', value);
    ```
- cara mendapatkan data dari session storage juga menggunakan getItem(), seperti berikut ini:
    ```javascript
    // mendapatkan session storage
    sessionStorage.getItem('key');
    ```
- Syntax untuk menghapus data dari session storage ada 2, yaitu:
    ```javascript
    // menghapus session storage satu persatu berdasarkan key
    sessionStorage.removeItem('key');

    // menghapus seluruh session storage sekaligus
    sessionStorage.clear();
    ```