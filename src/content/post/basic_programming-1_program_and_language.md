---
title: "1. Apa Itu Pemrograman?"
publishDate: "22 December 2023"
description: "Basic Programming - Cerita tentang Pemrograman dan Bahasa Pemrograman"
tags: ["BasicProgrammingWithC++"]
---

# Bagaimana Komputer bekerja?
komputer atau _Computer_ diambil dari kata dalam bahasa inggris _compute_ yang berarti menghitung. arti sebenarnya dari komuter adalah
alat yang diciptakan untuk membantu manusia melakukan banyak hal secara digital.

| INPUT	| => | PROCESS | => | OUTPUT |

komputer bekerja dengan menerima input dari manusia atau sistem lain, memrosesnya, lalu mengeluarkan hasil.

# Apa itu _Program_?
Program adalah sekumpulan baris instruksi yang dijalankan oleh CPU (central processing unit) di dalam sebuah komputer.
Jika dilihat dari penjelasan di atas, program adalah input dari manusia yang berupa baris instruksi yang kemudian berjalan sistem pemrosesan.

ketika seseorang ingin membuat program, program disusun dengan bahasa tertentu yang disebut _bahasa pemrograman_ yang kemudian diterjemahkan menjadi bahasa mesin yang dimengerti oleh CPU.

## Analogi
bayangkan kamu sedang berada di restoran untuk memesan makan malam. sebelum makan, kamu harus memilih menu dan memesannya dengan memanggil pelayan. Setelah pelayan menuliskan pesanan, juru masak akan menerima pesanannya dan mulai membuatkan makanan dan minuman. Setelah proses masak selesai, pesanan akan diantarkan ke kamu.

- proses memesan makanan ini sama seperti proses menulis program sebagai input, kamu menuliskan urutan perintah menu apa saja yang ingin kamu makan
- proses pelayan menulis pesanan adalah proses menterjemahkan pesanan kamu ke dalam bahasa yang dimengerti oleh juru masak
- juru masak memasak pesanan sama seperti proses eksekusi program. Progam yang sudah ditulis akan di jalankan sesuai urutan
- setelah makanan jadi, hasilnya akan di tampilkan ke kamu, sama seperti program yang mengeluarkan hasil apapun yang kamu harapkan ketika membuat program

## kenapa harus diterjemahkan menjadi bahasa mesin?
CPU bekerja secara digital, yang berarti mesin hanya mengenali perintah 0 dan 1 (sistem biner). Sedangkan manusia membuat program dengan bahasa yang mudah dimengerti oleh manusia lain, sehingga perlu dilakukan proses penterjemahan.

# Bahasa Pemrograman
bahasa pemrograman adalah sekumpulan aturan dan cara untuk menulis instruksi dalam program tertentu yang bisa dibaca oleh manusia atau _human friendly_.
Bahasa pemrograman sama seperti bahasa manusia yang juga memiliki pola dan aturan, contohnya bahasa indonesia yang memiliki pola SPOK atau bahasa inggris dengan Subject-Verb-Object.
 
 Bahasa pemgrograman diciptakan untuk mempermudah manusia menulis instruksi yang mudah dibaca namun juga mudah diterjemahkan ke dalam bahasa mesin. Di dunia ini ada beberapa pabrikan yang memproduksi CPU seperti Intel, AMD yang memproduksi chip berbasis arsitektur x64, TSMC dan Apple yang memproduksi chip berbasis ARM, dan lainnya. tiap arsitektur chip memiliki bahasa mesin masing - masing yang mirip namun tidak sama. bayangkan jika manusia harus menghapal semua kombinasi bahasa mesin untuk setiap chip, akan sangat merepotkan.

 maka dari itu diciptakanlah bahasa pemrograman yang akan mempermudah manusia menulis program, dan kemudian akan diterjemahkan secara otomatis ke masing masing chip CPU sesuai arsitekturnya. proses menerjemahkan ini disebut _COMPILE_ dan program juga disebut _CODE_ sehingan kegiatan menulis program juga sering disebut _CODING_.

 ## Contoh Bahasa Pemgrograman
 para computer scientist menciptakan bahasa bahasa pemrograman sesuai kebutuhan mereka. sehingga, ada beberapa cara bagaimana sebuah bahasa pemrograman berjalan.

### Compile langsung ke bahasa mesin
proses compile langsung ke bahasa mesin adalah proses paling simple. biasanya bahasa programming ini juga disebut bahasa _native_ walaupun tidak semua yang disebut _native_ berarti memilih cara ini. _native_ berarti codenya berjalan langsung di mesin tanpa perantara. Seperti yang sudah dijelaskan di atas, bahasa dengan sistem ini memiliki _compiler_ yang akan menterjemahkan Coding yang sudah kita tulis ke bahasa mesin sesuai yang kita harapkan.

contoh dari bahasa yang menggunakan sistem ini
- C++
- C
- Go
- Rust

tiap bahasa pemrograman di atas memiliki compiler masing masing yang bahkan memiliki banyak compiler, contohnya C dan C++ yang memiliki GCC, CLANG, dan VCC. namun yang standard digunakan oleh para coder adalah CLANG.

proses compile juga akan memberi tau ketika ada salah tulis (typo) atau salah pola (syntax error) dan kesalahan kesalahan lain. proses compile tidak akan selesai sampai semua error diselesaikan. proses ini membuat code kita berjalan dengan aman walaupun bukan berarti code kita bebas dari masalah masalah lain. 

### Transpile dan berjalan dengan runner
ada bahasa pemrograman yang tidak membutuhkan proses compile, karena code yang dibuat akan dibaca oleh program lain dan dijalankan oleh program lain tersebut. program lain itu disebut _runner_. bahasa dengan jenis ini biasa juga disebut bahasa _scripting_. untuk menggunakan bahasa ini, kamu harus menginstall terlebih dahulu runner nya di komputer lalu setelah itu kamu bisa menjalankan hasil coding mu.

Contoh dari bahasa yang menggunakan sistem ini
- Javascript
- Python
- PHP

karena tidak melalui proses compile, baris code dengan bahasa ini akan dibaca satu persatu ketika code nya dijalankan oleh runner, tidak seperti compile yang akan membaca semua baris code. sehingga masalah masalah atau error hanya akan ketahuan ketika runner sedang menjalankan baris tertentu tidak seperti compile yang semua error bisa diketahui di awal. dan seringnya error yang terjadi tidak bisa di deskripsikan dengan jelas oleh runner sehingga butuh waktu untuk menyelesaikannya.

Javascript dahulu hanya bisa berjalan di dalam browser seperti Chrome, mozilla, atau safari. namun di medio 2000-an diciptakanlah NodeJS oleh facebook yang membuat runner javascript di luar browser sehingga sekarang code javascript bisa berjalan di luar browser seperti bahasa scripting lain.

runner dibuat dengan bahasa native seperti python yang runner nya dibuat dengan bahasa C.

### Penggabungan kedua konsep di atas
Perusahaan pemgrogaman besar seperti Oracle (yang sekarang sudah dibeli oleh Google) dan microsoft pun juga membuat bahasa pemrograman sendiri yang mereka design untuk bisa berjalan dengan lebih efisien seperti di sistem operasi windows yang seringnya berjalan di chip intel x64. Sistem ini menggabungkan 2 metode diatas yaitu melakukan proses compile namun tidak menerjemahkannya ke dalam bahsa mesin, melainkan ke dalam bentuk lain, yang kemudian hasil compilenya akan  dijalankan oleh runner.

contoh bahasa pemrograman yang menggunakan sistem ini
- C#
- Java

C# memiliki compiler yang disebut msbuild yang akan melakukan compile yang hasilnya menjadi file dengan ekstensi .dll. file ini kemudian akan di baca oleh runner C# yang bernama .NET atau dotnet. microsoft juga membuat bahasa lain dengan konsep serupa namun untuk keperluan lain seperti F# dan Visual Basic (VB). sedangkan untuk Java hasil dari compile nya akan menjadi file .jar dan runner nya adalah JVM dan DVM untuk android.

# Kesimpulan
- Program atau code adalah sekumpulan instruksi yang akan dijalankan oleh CPU dalam komputer
- aktifitas menulis code disebut juga coding
- Program ditulis dengan bahasa pemrograman dan nantinya akan diterjemahkan menjadi bahasa yang dimengerti oleh CPU di berbagai arsitektur
- bahasa pemrograman ada banyak dan memiliki cara masing masing untuk penterjemahan ke dalam bahsa mesin 