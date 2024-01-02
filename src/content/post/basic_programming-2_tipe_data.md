---
title: "2. tipe data dan variable"
publishDate: "2 Januari 2024"
description: "Basic Programming - Cerita tentang variable dan tipe data"
tags: ["BasicProgramming"]
---

# tipe data - _Datatype_
data adalah satu atau sekumpulan informasi tentang sesuatu. misalnya dikantong celana atau bajumu sekarang ada uang Rp 10.000, maka kita bisa mengatakan bahwa hari ini kamu membawa uang cash sebesar Rp 10.000. informasi yang kita punya ada dua, pertama kamu punya uang cash, kedua besar uang cahs-nya Rp 10.000. dua informasi tersebut adalah data. tipe informasinya adalah angka, atau nominal uang, label nya adalah itu uang cash milikmu.

pemrograman sebenarnya berbicara tentang kegiatan menyimpan data dan memroses data menjadi data yang baru. jika kita melihat contoh di paragraph atas, kita punya data yang berbentuk angka atau nominal, apakah data hanya angka? dalam pemrograman ada beberapa tipe data yang bisa kita tulis atau gunakan.

    - angka
    - character
    - kata
    - benar atau salah

tipe data di atas ada di semua bahasa pemrograman, karena sesungguhnya, proses coding hanya memroses tipe tipe data tersebut. 4 tipe data itu disebut juga _primitive datatype_. tapi sebenarnya, bagaimana sih data data kita disimpan di komputer jika tipe nya berbeda beda?

## memori komputer
seperti yang sudah dijelaskan, komputer kita hanya mengerti sistem biner yaitu 0 dan 1. kenapa hanya itu? karena sebenarnya komputer cuma mengerti sinyal sinyal listrik antara 0V sampai 5V (yang terbaru 0 - 3.3V, dan sekarang sedang dicoba untuk diturunkan lagi). jadi sebenarnnya data kita itu disimpan dalam bentuk sinyal listrik. ketika bekerja, komponen di komputer yang bertugas untuk melakukan operasi terhadap data adalah CPU. tapi, data tidak disimpan di CPU melainkan di sistem memory. gambarnya ada dibawah



jika dilihat di gambar, ada beberapa level memori, tidak akan dijelaskan di sini, tapi intinya adalah data kita tersebar di beberapa level memori itu. proses memilih mana level memori yang cocok untuk data kita, dikerjakan oleh operating system atau OS. tapi sekali lagi, data tetap disimpan dalam bentuk 1 dan 0, atau binary digit, atau disingkat jadi _bit_. yang menarik disini adalah, entah itu angka, kata, benar salah, semua disimpan dalam bentuk yang sama. 1 dan 0. misal benar itu 1 salah itu 0, tapi apa bedanya 1 sebagai benar dan 1 sebagai angka 1?


## jadi tipe data itu bagaimana?
nah disinilah gunanya compiler. ketika kita menulis code, kita menulis code kita dalam bahasa manusia (atau bahasa inggris sebenarnya) dan compiler akan menerjemahkannya. tapi perlu diingat, ketika kita mau mengoperasikan sesuatu, contohnya code kalkulator sederhana dibawah

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

di dalam main function atau entry point, kita akan menjumlahkan dan mengurakangkan dua angka, num1 dan num2. ketika kita menulis num1 dan 2, kita memberi annotation notasi atau penanda berupa int. ini lah yang disebut datatype di programming. ini adalah cara untuk memberi tau compiler bahwa, "hey compiler, aku mau menyimdan data angka 10 di num1, ingat ya 10 itu angka karena aku pake int", lalu compiler akan membuat perintah dalam bahasa mesin untuk menulis ke memori bahwa ada data angka 10 yang akan disimpan sebagai angka.

jadi ada apa saja primitive datatype yang umum di semua bahasa pemrograman?
)
	- angka : int, float, double
	- character : char
    - kata : string
	- biner (benar salah) : boolean

dengan memberi notasi tipe data sebelum nama data kita, sebenarnya ini cara kita untuk memberi tau compiler bagaimana dia harus menyimpan data kita. penjelasan untung masing masing data type bisa teman teman cari sendiri di internet atau di kelas ya! intinya adalah memberi tipe data adalah kewajiban kita ketika menulis code, untuk memberi tau compiler bentuk atau tipe  dari data kita.

## tipe data di bahasa pemrograman

di bahasa pemrograman lama (yang lahir sebelum 2000an) rata rata mengharuskan kita untuk menulis tipe data ketika kita ingin menyimpan data. karena begitulah compiler jaman dulu di-design. dan ini biasanya jadi batu sandungan kedua untuk para programmer yang masih belajar atau pemula. biasanya ketika baru belajar coding, kita bingung untuk memilih tipe data apa yang harus kita pakai. atau biasanya kita sudah memilih, tapi ternyata keadaannya membutuhkan kita untuk memakai tipe data yang lain. 

contoh misalnya di coding kalkulator basi kita di atas, karena kita memakai int maka kita bisa menghitung angka, tapi bisakah kita menghitung angka desimal dengan koma? misal 10.5? jika kita coba jalankan, kita akan mendapatkan compile error. karena tipe data untuk angka bulat berbeda dengan tipe data angka desimal dengan koma. di sinilah letak kenapa programmer pemula merasa kesulitan.

akhirnya beberapa computer scientist menciptakan konsep baru di bahasa pemrograman yang lebih modern atau lebih muda umur releasenya. diperkenalkanlah konsep dynamic datatype atau juga disebut dynamic typing. intinya kita tidak perlu menulis anotasi tipe data di setiap kita menulis data. nanti compiler yang akan membantu kita untuk memilih, tipe data apa yang cocok. konsep ini diadopsi di python, javascript, ruby, golang, dan bahasa bahasa lain yang biasanya lahir setelah tahun 2000. apakah ini berarti kita tidak bisa menulis tipe data di bahasa dengan dynamic typing? tentu tidak. rule-nya hanya tidak wajib, tapi kita tetap bisa menuliskannya walau ini akan membuat code kita jadi tidak standard dengan codde lain secara umum.

dynamic typing mengganti anotasi tipe data dengan _let_, _var_, _const_, atau bahkan tidak memakai anotasi sama sekali seperti di python dan ruby. let dan var digunakan untuk membuar data yang nantinya nilainya bisa berubah, let untuk data di dalam scope yang hanya bisa diakses di scope yang sama, sedangkan var untuk data yang bersifat global. sedangkan const untuk data yang hanya bisa di definiskan sekali dan tidak akan diubah lagi, diambli dari kata constant.

jadi kita sekarang punya 2 konsep cara menentukan dataype, static typing yaitu wajib menuliskan tipe data di setiap data. dan dynamic typing yaitu tidak perlu / tidak wajib menuliskan tipedata.

konsep dynamic typing ini biasanya sangat mempermudah pemula untuk belajar menulis code, selain tidak harus menulis semicolon(;) kita juga tidak harus menulis tipe data, jadi kita bisa fokus hanya ke logic dari code kita. karena konsep ini populer, bahasa pemrograman tua pun akhrinya juga mau tidak mau mengadopsi konsep ini ke rule set bahasa pemrogramannya.

di C# dan java, selain dengan cara wajib menulis datatype, kita juga bisa mengganti data type nya dengan anotasi _var_. hal yang sama juga berlaku di C++ walaupun penggunaan var di bahasa bahasa ini adalah hal yang dihindari karena menambah beban ke compiler dan juga membuat coding kita jadi tidak sama dengan best practice.

# Variable
jika kita lihat di contoh kalkulator sederhana di atas, kita menyimpan data input 10 dan 5 sebagai num1 dan num2. num1 dan num2 ini adalah cara kita untuk menamain data atau informasi kita. num1 dan num2 ini di dunia coding disebut juga sebagai variable. jadi sebenrnya artinya adalah memory yang diberi nama dan tipedata. kenapa harus diberi nama? agar mudah dibedakan dan berfunsi sebagai identifikasi. contoh nya kita punya 2 teman yang namanya sama sama agus, biasanya agar tidak bingung, akhirnya nama mereka akan di ubah oleh teman temannya menjadi agus1 - agus2, atau agus gendut - agus kurus, dan lainnya. nah fungsi dari variable intinya sama saja, secara teknis adalah kita memberi identifikasi ke compiler untuk menyimpan dua data ini di tempat yang berbeda dengan id yang berbeda.

identifikasi di memori tidak menggunakan nama variable. memori menggunakan memori address yang biasanya kombinasi angka dan huruf. contohnya 1b2001 abc002 dan lainnya. cara penamaan ini efisien untuk mesin tapi tidak cocok untuk manusia, sehingga dibuatlah konsep variable agar programmer bisa menamai data mereka sesuka hati.

jadi sekarang jika teman teman melihat bagian di code seper dibawah 
``` c++
int num1 = 10;
```
atau di dynamic typing
``` python
num1 = 10
let num2 = 5
```
kita tau bahwa artinya num1 dan num2 adalah variable yang datatype nya dalah integer atau untuk angka dan value data nya adalah 10 dan 5.

## variable berdasarkan posisi pembuatannya
posisi pembuatan variable berpengaruh terhadap keadaan apakah dia bisa digunakan secara bebas atau tidak. kita sudah belajar tentang konsep scope di materi sebelumnya. scope berarti cakupan dari code kita yang di tandai dengan anotasi curly bracket {} atau indentasi.

sebuah variable hanya bisa diakses oleh operasi atau veriable lain ketika dia ada di dalam scope yang sama. kenapa? karena ini berkaitan dengan cara OS mengelola memori.

## cara kerja memori
jadi ketika OS menjalankan binary object hasil dari proses build coding kita, OS akan membaca instruksi bahasa mesin dari atas kebawah sesuai yang sudah ditulis oleh compiler. rule dari penulisan compiler adalah, OS hanya akan menulis ke memori ketika prosesnya masuk dalam satu scope, sedangkan ketika proses nya berjalan dan akhirnya keluar dari scope, memori tersebut akan dihapus. proses ini dilakukan karena sesungguhnya memori yang digunakan adalah memori sementara atau volatile memori yang lokasinya ada di dalam CPU yang juga disebut cache (lihat gambar). cache ukurannya sangat kecil, biasanya ada di orde megabyte. jadi akan sangant riskan bagi OS jika menyimpan semua variable secara permamen di cache.

jadi aturan utamanya adalah ketika masuk scope, semua variable yang di definisikan di di dalam scope akan dusimpan di memori ketika proses OS sampai di baris perintah terentu. dan semua memori pada akhirnya akan dihapus ketika proses OS keluar adari scope atau menyentuh baru kurung tutup.

variable yang di buat di dalam scope dan hanya bisa diakses did dalanya disebut _internal variable_. sedangkan variable yang di buat di luar scope, bahkan di scope utama, di sebut _global variable_. biasanya programmer membuat global variable dengan tujuan agar datanya tersimpan di memori untuk waktu yang lama sehingga bisa diakses dimanapun sesukanya.

## cara memberi nama variable
ada beberapa cara yang umum digunakan ketika membuat variable

- PascalCase
menulis variable dengan huruf depan dari kata memakai huruf kapital atau _upper case_. sering digunakan untuk menandai bahwa variable nya public / global. di bahasa pemrograman golan, digunakan untuk mengganti anotasi _public_

- camelCase
menulis variable dengan huruf depan selalu kecil atau _lower case_ sedangkan sisanya menggunakan kapital. sering digunakan untuk menandai 
    - variable internal
    - parameter fungsi
    - private attribute

- snake_case
menulis variable dengan semua awalan huruf kecil dan antar huruf disambung dengan garis bawah atau _under score_. biasa untuk menamain file. snake_case untuk nama file biasa ditemui di python, javascaript dan bahasa pemrograman dengan dynamic typing. SNAKE_CASE dengan semua huruf nya menggunakan kapital biasanya untuk membuat variable constant di semua bahasa pemrograman

- kebab-case
menulis varialbe dengan semua huruf kecil dan antar huruf disambung dengan garis atau _dash_. tidak ada use case khusus untuk penggunaan kebab-case dan style ini juga jarang digunakan di bahasa pemrograman apapun

pemilihan style antara 4 case ini penting karena tidak semua bahasa memiliki anotasi enkapsulasi (public, private, protected). jadi dengan penamaan use case dengan style tertentu bisa membuat programmer dengan cepat mengetahui tujuan awal dari kenapa variable ini dibuat. 

### memilih nama
ketika membuat variable, wajib menggunakan 
- kata benda atau noun, buka kata kerja atau keterangan.
- tidak mencampur angka dan huruf
- menggunakan kata yang berarti, tidak asal memilih kata
- menggunakan kata yang singkat, namun bukan singkatan
- menggunakan bahasa inggris!

# casting
-- on progres --

# Kesalahan umum oleh mahasiswa
beberapa kesalahan yang kerap dilakukan oleh mahasiswa ketika membuat variable dan memilih tipedata

## kesalahan pada tipe data numerical
ketika menulis code, kita harus menyesuaikan dengan dimana coding kita akan berjalan. coding yang berjalan di PC seperti laptop atau mini PC seperti raspberryPI akan sangat berbeda dengan coding untuk microcontroller seperti arduino atau bahkan applikasi mobile. perbedaan yang paling besar adalah besar performa dan memori yang dimiliki oleh CPU masing masing alat. PC jelas punya kapabilitas performa dan memori lebih besar dari mobile device atau bahkan microcontroller. sehingga memilih tipe data yang tepat bisa jadi sangat krusial 
	- berdasarkan ukuran : 
		- int16 / short
		- uint16
		- int32 / int
		- uint32
		- int64 / long
		- sama untuk float
		- double adalah 2 * float
### ukuran
bayangkan kamu adalah seorang pejabat atau selebriti. lalu suatu hari kamu sakit atau mengalami sesuatu yang mengharuskan kamu untuk perawatan rawat inap di rumah sakit. yang sering terjadi ketika seorang selebriti atau pejabat mengalami hal tesebut adalah, kamu akan menyewa satu sampa dua lantai dengan alasan privasi dan kenyamanan. sebagai artis kamu akan merasa bahwa dirimu eksklusif sehingga kamu berpikir kamu harus men-steril-kan satu lantai agar kamu mendapatkan ketenangan padahal kamu hanya membutuhkan satu sampai dua kamar sedangkan lantai tesebut bisa bersisi puluhan kamar. sebagai public figure, kamu bisa melakukkannya karena kamu punya uangnya. 

efek dari perilaku ini adalah, bagi kamu, kamu melakukan hal yang benar karena kamu mementingkan privasi dan kenyamanan. tapi bagi urusan umum, atau dari POV rumah sakit, kamu melakukan inefesiensi karena kamu membuat orang lain tidak bisa menyewa kamar dan juga kamu berpotensi mengurangi pendapat rumah sakit tersebut.

hal yang sama terjadi ketika kamu salah memilih tipe data. misal untuk integer atau int, ada beberapa tipe int berdasarkan ukurannya yaitu 8, 16 dan 32 bit seperti yang sudah di tulis di atas. tiap tipe mengokupansi atau mengambil blok blok memori sesuai dengan ukuran yang kita pilih. misal int16 atau short, berarti kita memerintakan compiler untuk memesan 16 bit blok memori untuk menyimpan data kita. padahal, belum tentu kita memerlukan blok data sebannyak itu. untuk int16 kita bisa menulis data dari -32768 sampai 32767. misalnya kita mau menyimpan data untuk kecepatan motor robot line follower kita yang sebenarnya cuma mentok di 5 m/s. yang berarti range nya 0 - 5 saja. 0 - 5 cuma butuh 8 bit memori. tapi kalau kita menggunakan tipe data int yang sebenarnya artinya int32, berarti kita mebuang buang 24 bit blok memori karena hanya dipakai 8 bit.

### sebaliknya
yang terjadi sebaliknya, bagaimana ketika kita membuat variable yang datanya melebihi tipe data yang sudah kita tentukan. contohnya kita membuat variable dengan int8 atau short. misal variable yang kita pake di section di atas yaitu kecepatan robot line follower kita yang tadi nya maksimal 5 m/s. lalu coding yang sama kita pakai di robot yang lebih besar yang mana kecepatannya lebih besar dari 5. ketika variable kecepatan tersebut yang harusnya maksimal hanya bisa di isi 127 karena range dari int8 adalah -127 sampai 127, lalu kita butuh untuk mengisi nilai nya dengan value 300. yang akan terjadi adalah ketika variable tesebut menyentuh angka 127, dia akan balik ke angka -127 dan mencoba untuk mengisi sisanya sampai penuh lagi lalu di reset lagi.

hal ini yang disebut sebagai stackoverflow. stack adalah sebutan ketike OS menyimpan memori di memory stack yaitu cache. dan overflow karena memori yang dipesan adalah 8 bit tapi valunya butuh lebih dari 8 bit jadi overflow atau "tumpah". jadi sebelum memilih tipedata kita juga harus bisa memastikan range angka yang akan kita assign ke variable ketika programa berjalan.

### tanda
sebagaimana angka di duna nyata, kita perlu tau bahwa apakah angka yang kita gunakan adalah desimal atau bulat dan apakah ada angka negatif atau tidak. notasi angka negatif disebug sebagai signed dan positif sebagai unsigned. apalagi ketika kita bicara tentang operasi hitung matematika yang input angkanya ketika memiliki tanda yang berbeda, bisa mempengaruhi hasil akhir dari operasinya.

## tidak menggunakan variable (bug code smell, bug magic number)

## variable tidak diberi data awal / uninitialized  (bug floating point)
	- variable yang tidak diberi data awal akan mempunyai data random (C++)
	- beberapa bahasa pemrograman akan memberikan data default seperti 0 untuk angka atau "" untuk string
	- beberapa bahasa pemrograman akan menggagalkan proses _compile_ ketika ada variable yang uninitialized seperti Rust dan Go

## tidak memberi operator constant / const / readonly pada global variable yang nilainya tidak berubah (bug mutated, bug racing,bug deadlock)

## menggunakan terlalu banyak global variable (posible bug memory leak)

## tidak meletakkannya dekat dengan dimana variable itu dibutuhkan

# kesimpulan
variable adalah cara kita menyimpan data atau informasi ketika kita menulis code. semua bahasa pemrograman mengadopsi pola yang sama yaitu

``` console
tipe-data + namaVariable + = + value
```

