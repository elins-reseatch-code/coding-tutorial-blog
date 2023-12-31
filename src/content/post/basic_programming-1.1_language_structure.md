---
title: "1.1. Struktur Bahasa Pemrograman"
publishDate: "22 December 2023"
description: "Basic Programming - Cerita tentang Pemrograman dan Bahasa Pemrograman"
tags: ["BasicProgramming"]
---

# Struktur Di Bahasa Pemrograman
Semua bahasa pemrograman, terutama yang populer, memiliki struktur yang hampir mirip satu dan lainnya. perbedaan biasanya terletak di syntax, serpeti ada yang butuh semicolon (;) di tiap akhir baris dan ada yang tidak, atau beberapa keyword dengan fungsi yang sama namun ditulis dengan nama yang berbeda. hal ini bisa terjadi karena ketika computer scientist mendesign sebuah bahasa pemrograman baru, mereka meniru konsep konsep yang mereka suka atau yang sudah umum di bahasa pemrograman sebelumnya. Tujuannya adalah agar bahasa pemrograman mereka familiar sehingga banyak yang mau menggunakan namun tetap bisa menyelesaikan masalah masalah yang mereka anggap tidak dapat diselesaikan di bahasa pemrograman yang mereka coba tiru.

## nama file
struktur yang pertama adalah program sesungguhnya cuma kumpulan text yang disimpan di satu file. file tersebut harus disimpan dengan extensi tertentu supaya bisa dibaca oleh compiler. contohnya di C++ file programnya harus disimpan dengan extensi .cpp. misalnya kita punya program untuk menulis hello world, jadi file nya bisa dinamakan hello_world.cpp. beberapa nama file di bahasa pemrograman lain:
- java > .java
- C# > .cs
- Golang > .go
- Javascript > .js atau .ts jika menggunakan typescript
- python > .py
- dan lain lain

## struktur penulisan
berikutnya ketika kita mulai menulis program, kita harus menggunakan struktur penulisan yang umum. dalam C++ contoh nya seperti di bawah ini 

```C++
#include <iostream> // baris 1

int main() // baris 2
{
   std::cout << "Hello world!";
   return 0;
}

```

### preprocessor untuk meanggil library
jadi, semua bahasa pemrograman dimulai dari baris 1 yaitu prepocessor. di C++, preprocessor ditandai dengan simbol hashtag (#). fungsi paling umum dari preprocessor adalah untuk menggunakan library atau code dari file lain sehingga bisa kita pakai di file yang sekarang sedang kita kerjakan. di C++ preprocessor juga bisa digunakan untuk memberikan statement selain include. ada dua cara ji=ka kita mau menggunakan library atau code di file lain, yaitu dengan #include <> atau #include(). simbol <> digunakan untuk memanggil code yang menjadi standard library dari program kita, contoh nya iostream yang sebenarnya berisi code untuk input dan output di C++. sedangkan () atau bracket digunakan untuk memanggil code kita di file lain yang tidak termasuk dalam library bawaan C++.

konsep yang sama juga di gunakan di bahasa lain namun dengan keyword yang berbeda
- java > import
- C# > using
- javascript > import
- Golang > import
- python > import
- dan lainnya

pemanggilan library juga ditulis dengan beberapa cara. ada yang berdasarkan filepath contohnya "src/main/" ataun menggunakan hierarki namespace contohnya yang digunakan di java. biasanya namespace juga sesungguhnya sama dengan struktur filepath, namun di bahasa pemrograman seperi C++, C#, Java atau semua bahasa pemrograman yang berbasis OOP namespace berguna sebagai penanda bagaimana sebuah file disimpan yang ditulis di dalam file nya. misal file helloworld.cpp disimpan di dalam filepath src/main/ sehingga namespace nya menjadi src.main.helloworld

### fungsi entry point
bagian utama dari sebuah bahasa pemrograman adalah fungsi atau _function_. fungsi biasanya di tulis dengan pola "nama_fungsi()". di semua bahasa pemrograman, ada fungsi yang digunakan oleh compiler dan runner sebagain pintu masuk dimana program dimulai. fungsi tersebut dinamakan _main function_ atau juga _entry point_. di C++ entry point nya adalah fungsi int main(). jadi agar programnya bisa dijalankan, semua perintah harus di masukkan ke dalam entry point.

entry point di beberapa bahasa pemrograman lain
- java > public static void main()
- C# > public void main()
- golang > func main()
- scripting language seperti python dan javascript tidak menggunakan konsep entry point
- dan lainnya

function main atau entry point ini harus ada di program yang kita buat, jika tidak, runner atau compiler akan bingung darimana program akan dijalankan sehingga biasanya terjadi error.

### endline dan scope
di C++, ketika kita selesai menuliskan satu baris perintah, seperti std::cout << "Hello world!", kita harus selalu memberi tanda semicolon(;). tanda ini adalah tanda untuk memberi tau compiler bahwa baris ini berhenti disini. jika tidak diberi tanda, compiler akan bingung dimana perintah berhenti dan biasanya ketika bertabrakan dengan perintah berikutnya akan menyeabkan error. beberapa bahasa pemrograman yang mengadopsi konsep endline ini adalah C#, java, dan bahasa pemrograman lain yang berbasis OOP. sedangkan untuk bahasa yang diciptakan belakangan seperi Golang, javascript dan python kita tidak perlu menulis semicolon karena compiler dan runner bisa memutuskan sendiri dimana letak pergantian baris perintah.

sayangnya hal ini yang biasanya jadi batu sandungan pertama untuk orang yang ingin belajar bahasa pemrograman, mereka seringnya lupa untuk menulis semicolon sehingga seringnya membuat stress beberapa pemula. oleh karena itu biasanya untuk pemula lebih mudah untuk memulai belajar pemrograman dari bahasa seperti python atau javascript.

dalam menulis program kita juga harus memberi penanda dimana fungsi kita dimulai dan selesei. penanda ini dinamakan dengan _scope_. sekali lagi di bahasa pemrograman berbasis OOP seperti C/C++, C# dan Java kita perlu menulis curly bracket atau {} untuk menandai area fungsi kita. ini juga diperlukan ketika kita menulis statement seperti boolean statemen dan conditional statement yang akan diajarkan di materi lain. sama seperti aturan syntax semicolon, syntax curly bracket ini juga tidak berlaku di python dan golang, namun masih semi berlaku terutama di javascript dan golang. di python penanda mulai dan selesai menggunakan indentation atau tab atau berapa spasi yang ada di tiap awal baris. contoh membuat fungsi yang sama seperti contoh di atas dalam python akan menjadi seperti ini

``` Python
def printHelloWorld():
    print("Hello,world")
```

# Compiler Dan Versi
sekarang kita sudah punya file program yang berisi perintah, yaitu memunculkan tulisan "Hello world". lalu apa yang akan terjadi ketika kita jalankan compiler dan program kita?

## versi bahasa
sebelum ke compiler, kita perlu tau bahwa tiap bahasa pemrograman memiliki versi yang di-release beberapa tahun sekali, atau bahkan tiap tahun. versi ini nantinya berkaitan dengan versi compiler yang akan kita gunakan dan juga berkaitan dengan fitur fitur apa saja yang bisa kita gunakan. gampangnya, semakin naik versi nya, semakin banyak fitur yang bisa kita gunakan, tapi sayangnya kenaikan versi juga kadang berarti ada beberapa fitur lama yang dibuang atau diganti. sehingga sebelum membuat coding, kita perlu menentukan versi mana yang akan kita gunakan. tentunya yang paling mudah adalah memakai versi yang paling terbaru atau versi yang paling umum digunakan di dunia. yang paling umum tidak berarti yang paling terbaru.

contonya di C++, ada beberapa versi yang sekarang umum exist yaitu : C++11, ++14, C++17 dan C++20. angka di belakang versi itu menandakan tahun release. untuk C++ sendiri versi yang paling umum digunakan adalah C++11 dan C++20. biasanya dosen di kampus masih mengajarkan mahasiswanya dengan menggunakan versi dibawah C++11, bahkan mungkin versi C++98. hal ini juga terjadi di bahasa pemrograman lain, contohnya untuk golang yang umu sekarang adalah veri go 1.18, dan yang lain misalnya python13, C#22 dan lainnya. 

## proses compile
compile dalam bahasa indonesia berarti mengumpulkan. jadi sesungguhnya compile di bahasa pemrograman bearti juga mengumpulkan semua code jadi satu lalu menterjemahkannya menjadi bahasa mesin. kenapa harus dikumpulkan? ketika mahasiswa belajar membuat code, biasanya kita hanya akan menulis perintah di dalam entry point, misal kita membuat program calculator, atau program untuk menentukan bilangan ganji dan genap, karena perintah yang digunakan simple dan pendek, kita hanya perlu menulis semua logika dan perintah di dalam main function atau entry point.

sayangnya ketika kita mengerjakan project atau membuat sesuatu di dunia kerja, yang terjadi adalah sebaliknya. biasanya sebuah software terdiri dari puluhan - ratusan file .cpp dan ribuan function. sedangkan ketika di compile, mesin hanya bisa menjalankan satu program yang biasa disebut file executable. jika kalian familiar dengan OS windows maka kalian pasti tau dengan .exe atau di android menjadi .apk. file file tersebut sebenarnya adalah executable hasil dari proses compile. jika di decompile atau deconstruct (ada caranya), kalian akan melihat code kalian sebenarnya dikumpulkan menjadi satu oleh si compiler sehingga output dari banyak file dan fungsi itu menjadi satu file executable saja. executable juga biasa disebut binary file karena sebenarnya isinya adalah perintah dalam bentuk biner yang dimengerti oleh CPU / mesin.

jadi pada intinya proses compile terdiri dari
1. penggabungan code yang disebut proses inlining
2. penterjemahan code ke bahasa assembly sesuai target arsitektur

contoh katakanlah kita punya code untuk operasi tambah dan kurang sederhana seperti di bawah ini 

```C++
#include <iostream>

int addition(int num1, int num2) {
    return num1 + num2;
}

int subtraction(int num1, int num2) {
    return num1 - num2;
}

int main() {
    int num1 = 10;
    int num2 = 5;
    
    int sum = addition(num1, num2);
    int difference = subtraction(num1, num2);
    
    std::cout << "Sum: " << sum << std::endl;
    std::cout << "Difference: " << difference << std::endl;
    
    return 0;
}

```

bisa kita lihat sekarang kita punya 2 fungsi lain selain entry point yaitu addition() dan subsctraction(). nantinya ketika kita compile hasil akhir sebenarnya akan menjadi speerti ini

```C++
#include <iostream>

int main() {
    int num1 = 10;
    int num2 = 5;
    
    int sum = num1 + num2;
    int difference = num1 - num2;
    
    std::cout << "Sum: " << sum << std::endl;
    std::cout << "Difference: " << difference << std::endl;
    
    return 0;
}

```
jika dilihat sekilas,kita bisa berpendapat apa untungnya di contoh yang pertama perintah pengurangan dan pertambahan di pisahkan dari main funtion, sedagkan pada akhrinya akan digabung juga? jawabannya adalah ada beberapa cara yang umum dilakukan atau biasa disebut _best practice_ di dunia programming yang mengharuskan kita menulis code seperti contoh yang pertama. seperti yang sudah dijelaskan di atas, di dunia kerja code tidak hanya terbatas di 2 atau 3 fungsi tapi puluhan - ratusan. contoh disini hanya untuk mengambarkan bagaimana proses inlining bekerja.

## Warning Dan Error Saat Compile
saat proses inlining ini, compiler juga akan memvalidasi baris per baris apakah ada syntax error seperti tidak ada semicolon atau kurang kurung tutup, salah penamaan, dan lainnya. compiler akan memunculkan compile error jika ditemukan ada baris yang bermasalah. biasanya juga disertai dengan nama file dan nomer baris untuk memudahkan programmer untuk memperbaiki masalahnya.

compiler juga terkadang memunculkan warning yang biasanya di tandai dengan text berwarna kuning. warning sesungguhnya juga sesuatu yang bsia diperbaiki oleh programmer walaupun tidak menjadi suatu keharusan sehingga bisa juga diabaikan.

## proses build
untuk mendapatkan binary file, kita harus melakukan proses build. build berarti menjalakan compiling dan lalu membuat hasil compile menjadi file yang bisa dijalankan oleh mesin . komputer kita. hasil build biasanya disesuaikan dengan komputer apa yang ssedang kita gunakan, binary file yang di build di sistem windows tidak bisa berjalan di linux ataupun mac. begitu juga sebaliknya. hasil build sebarnya adalah file berisi bahasa mesin atau bahasa pemrograman assembly. assembly adalah bahasa pemrograman low level yang dimengerti oleh pcoessing unit seperti CPU dan GPU. 

contoh perintah untuk menjalankan proses build di C++

``` Console
g++ helloworld helloworld.cpp
```

atau dibahasa lain

``` console
python helloworld.py // python

dotnet main.cs //C#

go build main.go //golang
```

# kesimpulan
bahasa bahasa pemrograman terutama yang populer memiliki pola penulisan code yang mirip. sehingga belajar satu bahasa pemrograman harapannya juga mempermudah kita untuk langsung memahami bahasa pemrograman lainnya. untuk bahasa pemrograman yang membutuhkan compile, proses akan dijalankan oleh compiler sesuai dengan versi yang kita gunakan / install. hasil akhir dari proses build adalah binary file atau executable yang bisa kita jalankan di komputer kita.