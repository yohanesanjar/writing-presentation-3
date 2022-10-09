# Yohanes Anjar Dewantara
# writing-presentation-3

## Javascript - Array<br>
### Pengertian Array
> Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.
### Contoh Array
```Javascript
let premiereLeague = ['Manchester United','Liverpool'.'Arsenal','Manchester City', 'Chelsea','Tottenham Hotspur']
console.log(premiereLeague)
```
### Membuat Array
> Array didefinisikan menggunakan square bracket [].
### Mengakses Array
- Array pada javascript dihitung dari index data ke-0.
- Data pertama adalah index ke-0.
- Contoh:
  ```Javascript
  let laukIni = ['Ayam Goreng','Ikan Goreng','Babi Guling']
  ```
  Penjelasan :
  - 'Ayam Goreng' adalah index ke-0
  - 'Ikan Goreng' adalah index ke-1
  - 'Babi Guling' adalah index ke-2
  - Kita bisa memanggi Ayam Goreng dengan
    ```Javascript
    console.log(laukIni[0])
    ```
### Update Array
```Javascript
let laukIni = ['Ayam Goreng','Ikan Goreng','Babi Guling']
laukIni[0] = 'Ayam Panggang'
console.log(laukIni) //Output : ['Ayam Panggang','Ikan Goreng','Babi Guling']
```
### Const in Array
- Jika menggunakan let, kita dapat mengubah array  dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain
- Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable).
- Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const
- Contoh :
  ```Javascript
  const merekMotor = ['Yamaha','Honda','Kawasaki']
  merekMotor = ['Suzuki'] //Output : Error
  ```
### Array Properties
- Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.
- .length Properties
  - length akan mengembalikan nilai dari jumlah panjang data suatu array.
  - Contoh :
    ```Javascript
    const merekMotor = ['Yamaha','Honda','Kawasaki']
    console.log(merekMotor.length) //Output : 3
    ```
### Array Method
- Array memiliki method atau biasa disebut built-in methods.
- Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan.
- Kita tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.
- Contoh Array Built-in Methods :
  - .push()
  > Method untuk menambahkan item  array pada urutan yang paling akhir.
  - .pop()
  > Method yang menghapus item array index terakhir.
  - .shift()
  > Method untuk menghapus item Array pada index pertama
  - .unshift()
  > Method untuk menambahkan item Array pada index pertama
  - .sort()
  > Method untuk mengurutkan secara Ascending atau Descending Alphanumeric
### Array - Looping
- Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach()
1. .map()
> Melakukan perulangan/looping dengan membuat array baru.
Contoh :
```Javascript
let angka = [1,2,3,4]
let kaliDua = angka.map(num => {
return num * 2
})
//Output : [2,4,6,8]
```
2. forEach()
> method untuk melakukan looping pada setiap elemen array.
Contoh :
```Javascript
const merekMotor = ['Yamaha','Honda','Kawasaki']
const forEach(element =>{
  console.log(element)
})
//Output : 'Yamaha','Honda','Kawasaki'
```
### Javascript - Multidimensional Array
- Multidimensional Array bisa dianalogikan dengan array of array. Ada array di dalam array.
  <br>Contoh :
  ```Javascript
  let inventory = [
  ['Celana',5],
  ['Baju', 10]
  ]
  
  console.log(inventory)
  ```
- Akses index multidimensional array
  <br>Contoh :
    ```Javascript
    let inventory = [
    ['Celana',5],
    ['Baju', 10]
    ]
  
    console.log(inventory[1][0]) //Output : Celana
    ```
- Operation using map in multidimensional array
  <br>Contoh :
  ```Javascript
  let inventory = [
  ['Celana',5],
  ['Baju', 10]
  ]
  
  inventory.map(dataInventory => {
    terjual = 100 - dataInventory[1]
    dataInventory[2] = terjual
  })
  
  console.table(inventory)
  ```
  Result :
  <br>![image](https://user-images.githubusercontent.com/100120189/194701355-20c2fb76-7a8d-46df-ac96-060f2d3c88fd.png)
- Looping For Multidimensional Array
  <br>Contoh :
  ```Javascript
  let inventory = [
  ['Celana',5],
  ['Baju', 10]
  ]
  
  inventory.forEach(baris) => {
    baris.forEach(column) => {
    console.log(column)
    }
  }
  //Output :
  //Celana
  //5
  //Baju
  //10
  ```
<br>
  
## Javascript Object
### Object
- Object adalah tipe data pada variabel yang menyimpan properti dan fungsi (method). Properti adalah data lengkap dari sebuah object. Method adalah action dari sebuah object.
- Membuat sebuah object** Sama seperti tipe data sebelumnya. Object dapat diassign kedalam sebuah variabel. Contoh script :
   ```
   let siswa = {
    nama : 'terra',
    umur : 17,
    hobi : 'memancing', 
    "nomor handphone" : 08256814086
    }
    console.log(siswa);
    ```
- Cara akses object
  - Dalam mengakses object terdapat 2 cara yaitu menggunakan dot notation dan bracket. Selain itu, bisanya dalam mengakses object yaitu menggunakan console.log(object).
  - dot notation, misalnya ``console.log(siswa.nama);`` maka output yang dihasilkan yaitu terra
  - bracket, misalnya ``console.log(siswa['nama']);`` 
- Memanggil nama object dengan variable
  <br>Contohnya :
    ```
    let properti = "umur"
    console.log(siswa[properti]);
    ```
- Menambahkan properti baru ke dalam object
  <br>Contoh script:
    ```
    Cara 1
    let buku = {
     Judul : "Mantan jadi manten",
     Penulis : "Hayati",
     "Jumlah halaman" : 250,
     };
     buku.tahun : 2022;
     buku.terjual : 3000;
     console.log(bukuu);
     //Output :
     Judul : Mantan jadi manten
     Penulis : Hayati
     Jumlah halaman : 250
     buku.tahun : 2022
     buku.terjual : 3000
     
     Cara 2
     buku["penerbit"] : "gramedia";
     console.log(buku);
     //Output :
     Judul : Mantan jadi manten
     Penulis : Hayati
     Jumlah halaman : 250
     buku.tahun : 2022
     buku.terjual : 3000
     penerbit : gramedia
     ```
- Ganti properti lama
  <br>Contoh script : 
     ```
     Cara 1
     let hewan = {
      nama : 'kucing',
      kaki : 4,
      warna : 'putih',
     };
     hewan.nama : 'kelinci',
     hewan.warna : 'hitam',
     console.log(hewan);
     //Output 
     nama : kelinci
     kaki : 4
     warna : hitam
     
     Cara 2
     hewan["kaki"]=2;
     console.log(hewan)
     nama : kelinci
     kaki : 2
     warna : hitam
     ```
- Delete Properti
  <br>Contoh script :
     ```
      let hewan = {
      nama : 'kucing',
      kaki : 4,
      warna : 'putih',
     };
     delete.hewan.warna;
     delete.hewan.kaki;
     console.log(hewan);
     //Output : nama : kucing
     ```
- Method
  <br>Method adalah ketika ingin menambahkan sebuah function. Ada 2 method dalam object, yaitu :
  - const greeting
    <br>Contoh script :
        ```
        const greeting = {
          welcome : function(){
          return "halo selamat datang";
        };
        afterpay:function(){
          return "terimakasih sudah membeli produk kami";
        }
        };
        console.log(greeting.welcome()); //Output : halo selamat datang
        ```
  - nested object
    <br>Contoh script :
    ```
    let buku = {
     Judul : "Tips jago Javascript",
     Tahun : 2022;
     Penulis {
        Penulis1 : {
           Nama : "Reyhan",
           Umur : 28,
           Kota : "Jakarta"
           }
        Penulis2 : {
           Nama : "Fala",
           Umur : 25,
           Kota : "Madiun"
           }
        Penulis3 : {
           Nama : "Diana",
           Umur : 20,
           Kota : "Bandung"
           }
         }
    };
     console.log(buku.penulis.penulis1.nama);//Output : Reyhan
    ```
- Built In Method (Object menjadi array)
  ```
  let siswa = {
    nama : "Fala",
    umur : 20,
    hobi : "Berenang",
  };
  console.log(object.keys.(siswa)); //Output : 'nama', 'umur', 'hobi'
  console.log(object.values.(siswa)); //Output : 'Fala', '20', 'Berenang'
  ```
- Looping Object (Looping sendiri berarti perulangan.)
  <br>Contoh scriptnya :
    ```
    let siswa = {
     nama : "Reyhan",
     umur : 22,
     kota : "Jakarta",
    };
    for(let key in siswa){
      console.log(siswa[key]); 
    //Output :
    Reyhan
    22
    Jakarta
    ```
- Array of Object
  - Array of Object adalah array yang menyimpan banyak object sebagai nilainya.
  - Contoh script :
    ```
    let users = {
      {
       Nama : "Reyhan",
       Umur : 28,
       Kota : "Jakarta",
      },
      {
       Nama : "Fala",
       Umur : 20,
       Kota : "Bandung",
      },
      {
       Nama : "Diana",
       Umur : 24,
       Kota : "Madiun",
      },
    };
    console.log(user);
    
    Dengan menggunakan Map, maka
    let data = users.map((el) => {
     console.log(el.nama);
    });
    //Output :
    Reyhan
    Fala
    Diana
    ```
### Rekrusif dan Modules
- Rekrusif
  - Rekursif adalah function atau algoritma yang memanggil dirinya sendiri sampai kondisi tertentu. Rekrusif ini mirip seperti looping. Misalnya pada gambar ada gambar di dalam gambar. Terdapat 2 kunci pada rekrusif,yaitu base case atau titik berhenti dan recrusion case atau titik memanggil function.
  - Contoh script :
    ```
    Menampilkan bilangan 1 2 3 4 5
  
    function deretAngka(n){
      if (n == 1) {
      console.log(n)
    } else {
      deretAngka(n-1)
      console.log(n);
      }
    }
    deretAngka(3)
    ```
  - Contoh lain :
    ```
    // Mencari angka faktorial
    // Misalnya 5!
    // Solusinya jika dijabarkan 5 x 4 x 3 x 2 x 1

    function faktorial(n) {
      if (n == 1) {
      return 1
    } else {
      return n * faktorial(n - 1)
      }
    }
    console.log(faktorial(3))
    //Output = 6
    ```
- Modules
  - Modules adalah cara untuk memisahkan kode ke file yang berbeda. Keuntungan dari modules yaitu mudah untuk mengelola kode serta kode tidak menumpuk di dalam satu file. Terdapat 2 kata kunci pada modules yaitu export dan import.
  - Contoh script :
    ```
    // File Jepang.js
    export let motor = ["suzuki", "yamaha", "honda", "kawasaki"]
  
    let entertainment = ["anime", "manga", "wibu", "dorama"]
    export default entertainment
  
    export function sayHello() {
    console.log("hallooo")
    }
  
    import {apple} from './amerika.js';
    console.log(apple);
    
    // File Indonesia.js
    import {motor} from "./Jepang.js"
    console.log(motor);
   
    import Entertainment, { motor as motorJepang, sayHello  } from "./jepang.js"
    console.log(Entertainment);
  
    // File Amerika.js
    let apple = ["iphone", "macbook", "imac"]
    export {apple}
    ```
    Berdasarkan script diatas,
    - Indonesia hanya bisa import, karena dia file utama.
    - Jepang bisa melakukan import dan export.
    - Amerika hanya melakukan export.
  - Hal hal yang harus dilakukan saat membuat modules adalah menambahkan type="module" pada script utama, lalu siapkan script ke-2 dan sebagainya untuk melakukan export, serta lakukan import pada file atau script utama.
