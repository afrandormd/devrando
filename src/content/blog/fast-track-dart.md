---
author: Dev Rando
pubDatetime: 2024-10-08
modDatetime: 2024-01-08
title: Dart Fundamental
featured: false
draft: false
tags:
  - dart
categories:
  - fast track begginer
# canonicalURL: https://smale.codes/posts/setting-dates-via-git-hooks/
description: Dart merupakan bahasa pemrograman yang digunakan pada pengembangan Flutter. 
---

## Table of Contents

# Section 2: Dart Fundamental

## Hubungan Dart dengan Flutter?

**Dart** merupakan bahasa pemrograman yang digunakan pada pengembangan **Flutter**. Oleh karena itu, materi dart ini perlu dipelajari guna menunjang keberlangsungan pembelajaran Flutter kedepannya.

## Struktur Kode Program Dart

Seluruh kode perintah dart ditulis dalam **function main** agar dapat dijalankan.

Fungsi **main** adalah fungsi yang pertama kali dijalankan oleh komputer, seluruh baris program harus ditulis di dalamnya agar dapat di eksekusi / dijalankan.

```dart
void main() {
// kode perintah
}
```

**Notes:**

- **void:** digunakan jika fungsi tidak akan mengembalikan(return) nilai apapun.
- **hilangkan keyword void:**  jika fungsi akan mengembalikan nilai tertentu.

## Karakeristik Dart

- **Statically typed**
    
    Dart adalah bahasa pemrograman yang statically typed, kita perlu mendefinisikan variabel sebelum digunakan.
    
    **Contoh:**
    
    ```dart
    var greetings = "Hello World!";
    print(greetings);
    ```
    

- **Type Inference**
    
    Karakteristik ini dapat membuat suatu variabel akan mengikuti tipe data dari valuenya. Namun, hal tersebut tidak berlaku jika kita sudah memberi tipe data pada variabelnya.
    
    **Contoh:**
    
    ```dart
    // variabel greetings secara otomatis jadi String
    var greetings = "Hello World";
    
    // tidak akan berubah ke int -> malah jadi error
    String greetings = 10;
    
    print(greetings);
    ```
    

- **String Expressions**
    
    Kita dapat menggunakan tanda `$` untuk menampilkan suatu variabel bertipe apapun ke bentuk `String`. Hal ini dapat kita sebut sebagai **String Interpolation.**
    
    **Contoh:**
    
    ```dart
    var greetings = "Hello World";
    String language = "Dart";
    
    print("$name - bahasa yang digunakan : $language");
    ```
    

- **Object Oriented Programming**
    
    Dart berfokus pada pardigma **OOP** yang mana berorientasi pada object.
    
    ---
    

# Tipe Data Dart

## String

Tipe data string identik dengan tanda kutip, baik itu `'` atau `"`.

**Contoh:**

```dart
String name = "Rando";
String hobby = 'Hiking';

print(name); // Rando
print(hobby) // Hiking
```

Dart menyediakan beberapa method yang bisa digunakan pada tipe data `String`

**Contoh Penggunaan Method:**

```dart
String greetings = "hello WORLD";

print(greetings.toLowerCase()); // hello world
```

## bool

Tipe data bool adalah tipe data kondisi yang hanya memiliki 2 nilai yakni `true` atau `false`.

**Contoh:**

```dart
bool isMerried = false;

print(isMerried); // false
```

## num

Tipe data num adalah tipe data yang dapat diberi nilai bilangan bulat atau bilangan desimal.

**Contoh:**

```dart
num age = 45;
num phi = 3.14;

print(age); // 45
print(phi); // 3.14
```

## Double

Tipe data double adalah tipe data bilangan desimal. Meskipun tipe data double dapat diberi bilangan bulat, output yang dihasilkan akan tetap menjadi bilangan desimal.

**Contoh:**

```dart
double height = 175.5;
double weight = 60;

print(height); // 175.5
print(weight); // 60.0
```

## int

Tipe data int adalah tipe data khusus bilangan bulat. Jika tipe data int diberi bilangan desimal, maka ia akan error.

**Contoh:**

```dart
int age = 20;
int long = 45.5;

print(age); // 20
print(long); // error
```

### Penggunaan Fungsi `num` `double` `int`

Ketiga tipe data tersebut merupakan tipe data angka, oleh karena itu mereka dapat menggunakan method yang sama di dart.

**Contoh:**

```dart
num age = -20;
double height = 175.5;
int weight = 60;

// abs() digunakan untuk mengubah menjadi bilangan absolute
print(age.abs()); // 20

// ceil() digunakan untuk membulatkan bilangan ke atas
print(height.ceil()); // 176

// Penggunaan string interpolation di tipe data angka beserta methodnya
print("Dia berusia ${age.abs()} tahun, dengan tinggi ${height.ceil()} cm, dan berat $weight kg");
// Output: Dia berusia 20, dengan tinggi 176 cm, dan berat 60 kg
```

## List

Tipe data list adalah tipe data yang dapat menampung lebih dari satu nilai, tipe data ini menggunakan tanda `[ ]` sebagai pembungkus.

**Contoh:**

```dart
List favoriteColor = ["Red", "Yellow", "Green"];

print("Warna fav: $favoriteColor");
// Output: Warna fav: [Red, Yellow, Green]
```

**Penjelasan**

Syntax di atas akan menghasilkan list dari **favoriteColor** yang bertipe data **dynamic** bernilai **Red, Yellow, Green.**

Default dari tipe data **List** adalah <dynamic> yang dimana kita dapat memberi nilai beragam tipe data.

> **Tipe data dynamic** adalah tipe data yang dapat menampung seluruh tipe data lain.
> 

**Contoh Lain**

```dart
List<String> favoriteColor = ["Red", "Yellow", "Green"];

print("Warna fav: $favoriteColor");
// Output: Warna fav: [Red, Yellow, Green]
```

**Penjelasan**

Syntax di atas adalah kumpulan list yang berisikan nilai bertipe data **String**, apa bila kita menambahkan nilai baru bertipe data selain **String** maka dia akan error.

**Cara mengambil data yang ada di List**

Untuk mengambil data yang ada di list, caranya menggunakan **indeks** posisi dari data yang akan di ambil.

**Contoh**

```dart
List<String> favoriteColor = ["Red", "Yellow", "Green"];

print("Pilih warna fav ke-1: ${favoriteColor[0]}");
// Output: Pilih warna fav ke-1: Red
```

**Penjelasan**

Syntax di atas akan mengambil data urutan pertama yaitu **Red**, karena indeks dimulai dari angka **0** maka kata **Red** yang akan tampil.

## Map

Tipe data map adalah tipe data yang dapat menampung lebih dari satu nilai dengan menggunakan **key** dan **value**. Berbeda dengan tipe data List, Map menggunakan tanda `{}` untuk membungkus nilainya.

**Contoh**

```dart
Map kendaraan = {
	"mobil": "Civic Turbo",
	"motor": "Yamaha XSR",
};

print("Kendaraan: $kendaraan");
// Output: Kendaraan: {mobil: Civic Turbo, motor: Yamaha XSR}
```

**Cara mengambil data yang ada di Map**

Untuk mengambil nilai yang ada di map, kita hanya perlu memanggil **key** dari value tersebut.

**Contoh**

```dart
Map kendaraan = {
	"mobil": "Civic Turbo",
	"motor": "Yamaha XSR",
};

print("Motor: ${kendaraan["motor"]}");
// Output: Motor: Yamaha XSR
```

Karena Map menggunakan **key** untuk mengambil data bukan menggunakan **index,** maka posisi urutan tidak berpengaruh.

## Dynamic

Tipe data dynamic adalah tipe data yang dapat menampung seluruh tipe data lain.

Secara default, jenis dari tipe data **List** dan **Map** adalah <dynamic> yakni beragam.

# Final vs Const

Dengan menggunakan keyword **final & const** kita tidak dapat mengisi / mengubah nilai dari variabel yang sudah ada di kemudian hari.

**Contoh final**

```dart
final String name = "Rando";
const int age = 21;
name = "Afrando";
age = 22;

print(name);
print(age);
// Output: Error: Can't assign to the final variable 'name'
// Error: Can't assign to the const variable 'age'
```

**Perbedaan final & const**

**Final**

Jika menggunakan **final**, kita dapat mendeklarasikan atau membuat variabelnya terlebih dahulu sebelum memberi nilai / mengisinya.

**Contoh**

```dart
final String name;
name = "Rando";

print(name);
// Output: Rando
```

**Const**

Jika menggunakan **const,** kita wajib langsung memberi atau mengisi nilai dari variabel tersebut.

**Contoh**

```dart
const String age = 22;

print(age);
// Output: 22
```

# Comments

comments adalah sebuah baris kode yang tidak di eksekusi oleh komputer.

**Syntax Penulisan**

```dart
// -> Comments 1 baris

/*
-> Comments multi baris 
-> (lebih dari 1 baris)
*/

/// Comments Documentation [1 baris]
/**
* Comments Documentation [multibaris]
*/
```

# Functions

Functions adalah serangkaian baris kode yang dibuat untuk mengerjakan suatu tugas.

**Contoh**

```dart
void main(){
	// Memanggil fungsi penjumlahan
	penjumlahan();
}

// fungsi penjumlahan
void penjumlahan(){
    print(10 + 5);
}
// Output: 15
```

**Penjelasan**

Syntax di atas merupakan konsep sederhana **pembuatan** dan **pemanggilan** functions.

### Parameter & Argument

**Parameter**

Parameter adalah variabel di functions yang menampung nilai.

**Argument**

Argument adalah nilai yang diberikan ke functions dan ditampung di parameter yang nantinya akan di olah di dalam functions.

**Contoh**

```dart
void main(){
	// Memanggil fungsi penjumlahan
	penjumlahan(10, 5);
}

// fungsi penjumlahan
void penjumlahan(int angka1, int angka2){
    print(angka1 + angka2);
}
// Output: 15
```

**Penjelasan**

- `int angka1` & `int angka2` pada functions **penjumlahan** merupakan **parameters** yang bertipe data **int.**
- `10` & `5` yang ada pada saat pemanggilan function **penjumlahan** merupakan **arguments.**
- Parameters boleh dibuat maupun tidak, dapat dibuat lebih dari 1, namun umumnya parameters efektifnya dibuat sebanyak 2.
- Pemberian argument harus sesuai dengan jumlah dan ketentuan parameters.

**Cara menyimpan hasil dari fungsi**

**Contoh**

```dart
void main(){
	// Memanggil fungsi perkalian & menyimpan di variabel
	int hasilPerkalian = perkalian(5, 5, 5);
	
	print(hasilPerkalian); // Output: 125
}

// fungsi perkalian
int perkalian(int angka1, int angka2, int angka3){
    int hasil = (angka1 * angka2 * angka3);
    return hasil;
}

```

**Penjelasan**

Syntax di atas merupakan contoh gambaran dari fungsi yang mengembalikan nilai ****yang dimana fungsi perkalian akan mengembalikan nilai berupa integer yang merupakan **hasil** dari perkalian, lalu hasil tersebut dikembalikan ke pemanggil fungsi tersebut.

**Private Variable**

Variabel **hasil** yang ada di dalam fungsi perkalian merupakan **private variable** artinya kita tidak bisa memanipulasi variabel tersebut diluar fungsinya. Konsep ini masuk ke dalam **Variable Scoop.**

- **Maksud dari return**
    
    **return** adalah sebuah perintah yang digunakan untuk **mengembalikan hasil** dari suatu fungsi kepada bagian lain dari program. 
    
    Jadi, ketika sebuah fungsi dijalankan dan ada sesuatu yang ingin "dikirim balik" ke pemanggil fungsi tersebut, kita menggunakan `return`.
    

# Asynchronous

<!-- ![image.png](image.png) -->

Bahasa dart terdapat 2 jenis pengeksekusian kode. Kode akan dijalankan secara **synchronous (sync)** atau **asynchronous (async)**. 

**Synchronous / Seri**

Pada eksekusi **synchronous**, proses A akan dijalankan terlebih dahulu. Setelah proses A selesai sepenuhnya, barulah proses B dapat dimulai. Ini berarti program harus menunggu hingga satu proses selesai sebelum memulai proses berikutnya. 

Jadi, jika proses A memakan waktu lama, seluruh alur akan menunggu hingga proses itu selesai sebelum melanjutkan ke proses B.

Dalam gambar, kita melihat bahwa proses B menunggu hingga proses A selesai sebelum dieksekusi.

**Asynchronous / Paralel**

Pada eksekusi **asynchronous**, ketika proses A berjalan, kita tidak perlu menunggu proses A selesai untuk memulai proses B. Proses B bisa berjalan bersamaan atau di sela waktu sambil menunggu hasil dari proses A. Proses A akan tetap berjalan di latar belakang, dan ketika sudah siap (misalnya menerima response), program akan kembali untuk menyelesaikan proses tersebut.

Pada gambar, kita melihat bahwa program dapat "terus bekerja" (Continue working) selama menunggu hasil dari proses yang sedang berjalan, dan ketika hasil (response) tersedia, proses tersebut dapat dilanjutkan tanpa harus menunggu idle di tengah-tengah.

**Kesimpulan**

- **Synchronous** berarti menunggu satu proses selesai sebelum memulai proses lain.
- **Asynchronous** berarti tidak perlu menunggu, sehingga dapat menjalankan beberapa proses "secara bersamaan" dan menindaklanjuti hasilnya nanti ketika tersedia.

**Contoh Synchronous**

```dart
void main(){
	print("A");
  print("B");
  print("C");
}
// Output: 
// A
// B
// C
```

**Penjelasan**

Syntax di atas akan menampilkan output berupa huruf **A,**  **B, C** secara berurutan, dan dilakukan dengan process yang berurutan mulai dari baris pertama, kedua, dan seterusnya.

**Contoh Asynchronous**

Untuk menggunakan konsep **async** di dart kita perlu menggunakan keyword `Future` yang didalamnya terdapat **anonymous function** `(){...}`

```dart
void main(){
	print("A");
  cetakB();
  print("C");
}

void cetakB(){
	Future((){
	  print("B");
  });
}
// Output:
// A
// C
// B
```

**Penjelasan**

Saat fungsi `main()` dijalankan:

- **`print("A")`** dieksekusi pertama kali, sehingga output pertama adalah "A".
- **`cetakB()`** dipanggil, yang di dalamnya terdapat **`Future()`**. Fungsi `Future` menjalankan kode di dalamnya secara **asynchronous**, yang berarti eksekusinya akan ditunda sampai ada waktu untuk menyelesaikannya.
- Kode lanjut ke **`print("C")`** tanpa menunggu eksekusi `Future` di dalam `cetakB()`, sehingga "C" dicetak sebelum "B".
- Setelah **`main()`** menyelesaikan semua tugas **synchronous**, barulah Dart menyelesaikan tugas **asynchronous** yang ada di dalam **`Future`**, sehingga "B" dicetak terakhir.

**Memberikan jeda / delay pada proses async**

Kita dapat memberikan jeda untuk menampilkan hasil / response pada proses async

**Contoh**

```dart
void main(){
	print("A");
  cetakB();
  print("C");
}

void cetakB(){
	Future.delayed(Duration(seconds: 2), (){
	  print("B");
  });
}
// Output:
// A
// C
// B
```

**Penjelasan**

- **`Future.delayed`** digunakan untuk menunda eksekusi bagian tertentu dari kode selama waktu yang ditentukan (dalam hal ini 2 detik).
- Karena Dart tidak menunggu operasi asynchronous selesai (seperti **`Future.delayed`**), program akan langsung melanjutkan eksekusi baris berikutnya.
- Jadi meskipun fungsi **`cetakB()`** dipanggil sebelum **`print("C")`**, output "C" tetap muncul terlebih dahulu, karena eksekusi kode di dalam **`Future.delayed`** ditunda selama 2 detik.

## Cara lain asynchronous

Di Dart kita dapat menggunakan keyword `async` dan `await` untuk membuat program asynchronous.

**Contoh**

```dart
void main(){
	print("A");
	cetakB();
	print("C");
}

void cetakB() async {
	await Future.delayed(Duration(seconds: 2));
	
	print("B");
	print("Berhasil cetak B");
}
// Output:
// A
// C
// B
// Berhasil cetak B
```

**Penjelasan**

- **`await`** dalam **`cetakB()`** menyebabkan program menunggu hingga **`Future.delayed(Duration(seconds: 2))`** selesai sebelum melanjutkan ke kode berikutnya.
- Fungsi **`cetakB()`** dipanggil secara **asynchronous**, sehingga program tidak menunggu hingga fungsi tersebut selesai sebelum melanjutkan ke **`print("C")`**.
- Setelah **2 detik** berlalu, barulah "B" dan "Berhasil cetak B" dicetak secara **synchronous** dalam fungsi **`cetakB()`**.

## Method .then & .catchError

Di Dart kita dapat menggunakan method `then` dan `catchError` apabila menggunakan fungsi Future.

**`.then`** dan **`.catchError`** adalah **callback functions** dalam konteks **asynchronous programming** di Dart. Callback adalah fungsi yang dipanggil (dieksekusi) ketika suatu peristiwa atau operasi selesai, baik berhasil ataupun gagal.

**Contoh**

```dart
void main(){
	print("A");
	cetakB().then((data)=> print("SUKSES")).catchError((err)=> print("ERROR"));
	print("C");
}

Future<void> cetakB() async {
	await Future.delayed(Duration(seconds: 2));
	
	print("B");
	print("Berhasil cetak B");
}
// Output:
// A
// C
// B
// Berhasil cetak B
// SUKSES
```

**Penjelasan**

- **`print("A")`**:
    - Operasi ini **synchronous**, jadi output pertama yang muncul adalah **"A"**.
- **`cetakB()` dipanggil**:
    - Fungsi **`cetakB()`** adalah **asynchronous** dan mengembalikan **`Future<void>`**.
    - Setelah memanggil **`cetakB()`**, program akan langsung lanjut ke baris berikutnya tanpa menunggu **`cetakB()`** selesai.
- **`.then((data) => print("SUKSES"))`**:
    - **`.then`** adalah callback yang akan dieksekusi ketika **`Future`** dari **`cetakB()`** berhasil diselesaikan.
    - Setelah **`cetakB()`** selesai (setelah 2 detik), **`.then`** akan dijalankan, dan **"SUKSES"** akan dicetak.
- **`.catchError((err) => print("ERROR"))`**:
    - **`.catchError`** adalah callback yang menangani kesalahan/error jika **`Future`** gagal (misalnya, jika terjadi exception dalam **`cetakB()`**).
    - Dalam kasus ini, jika ada error dalam proses di **`cetakB()`**, maka **"ERROR"** akan dicetak.
    - Namun, karena kode ini tidak menyebabkan error, **`.catchError`** tidak akan dipanggil.
- **`print("C")`**:
    - Operasi ini langsung dieksekusi secara **synchronous** setelah pemanggilan **`cetakB()`**, sehingga **"C"** dicetak sebelum **"B"** dan **"SUKSES"**.
- **`Future.delayed(Duration(seconds: 2))`**:
    - Fungsi **`cetakB()`** menunggu 2 detik sebelum melanjutkan dan mencetak **"B"** serta **"Berhasil cetak B"**.
- **Output dari .then**:
    - Setelah 2 detik penundaan selesai, **`.then`** akan dieksekusi, dan **"SUKSES"** dicetak.

## Kondisi dalam asynchronous

<!-- ### Completed -->