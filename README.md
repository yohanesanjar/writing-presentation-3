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
