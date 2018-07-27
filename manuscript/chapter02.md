Bermain dengan variabel
Anda tahu bagaimana menggunakan JavaScript untuk menampilkan nilai-nilai. Namun, untuk membuat aplikasi yang akan benar-benar berguna, harus mampu menyimpan data, seperti informasi yang dimasukkan oleh pengguna. Seperti contoh berikut ini.
TL;DR
•	Variabel adalah area penyimpanan informasi. Setiap variabel memiliki nama, nilai dan jenis. Dalam JavaScript, jenis variabel disimpulkan dari nilai tersimpan di dalamnya: JavaScript adalah bahasa dinamis diketik.
•	Sebuah variabel dinyatakan menggunakan kata kunci biarkan diikuti dengan nama variabel. Untuk menyatakan konstan (variabel nilai awal yang tidak akan pernah berubah), itu lebih baik untuk menggunakan kata kunci const sebagai gantinya.
•	Untuk memberikan nilai ke variabel, kami menggunakan operator tugas =. Untuk nomor variabel, + = operator dapat meningkatkan dan operator ++ dapat kenaikan nilai mereka.
•	Lingkup variabel adalah bagian dari program mana variabel terlihat. Variabel dinyatakan dengan membiarkan atau const scoped blok. Blok kode adalah bagian dari sebuah program yang dibatasi oleh sepasang pembukaan dan penutupan kurung kurawal {...}.
•	Ekspresi adalah sepotong kode yang menggabungkan variabel, nilai-nilai dan operator. Mengevaluasi ekspresi menghasilkan nilai, yang memiliki tipe.
•	Ekspresi diikutkan dalam string yang dibatasi oleh sepasang backticks ('). Sebuah string disebut template harfiah.
•	Jenis konversi mungkin terjadi secara implisit selama evaluasi ekspresi, atau secara eksplisit dengan menggunakan perintah Number() dan String(), untuk mendapatkan masing-masing sejumlah atau string.
•	Perintah prompt() dan alert() berurusan dengan informasi masukan dan tampilan di bawah bentuk kotak dialog.
•	Penamaan variabel sangat penting untuk visibilitas program. Mengikuti konvensi penamaan seperti camelCase adalah praktik yang baik.

VARIABEL
Peran Variabel
Peran suatu variabel Program komputer menyimpan data menggunakan variabel. Variabel adalah area penyimpanan informasi. Kita dapat membayangkannya sebagai kotak di mana Anda dapat menyimpan dan menyimpan barang-barang!.
Properti variabel
Sebuah variabel memiliki tiga properti utama:
•	Namanya, yang mengidentifikasi itu. Nama variabel dapat berisi huruf besar dan kecil, angka (bukan di posisi pertama) dan karakter seperti tanda dolar ($) atau garis bawah (_).
•	Nilainya, yang merupakan data yang disimpan dalam variabel.
•	Jenisnya, yang menentukan peran dan tindakan yang tersedia untuk variabel.

	Anda tidak perlu mendefinisikan tipe variabel secara eksplisit dalam JavaScript. Jenisnya disimpulkan dari nilai yang disimpan dalam variabel dan dapat berubah ketika program berjalan. Itu sebabnya kami mengatakan bahwa JavaScript adalah bahasa yang diketik secara dinamis. Bahasa lain, seperti C atau Java, membutuhkan tipe variabel untuk selalu didefinisikan. Ini disebut mengetik statis.

Mendeklarasikan variabel
	Sebelum Anda dapat menyimpan informasi dalam variabel, Anda harus membuatnya! Ini disebut mendeklarasikan variabel. Mendeklarasikan variabel berarti komputer menyimpan memori untuk menyimpan variabel. Program ini kemudian dapat membaca atau menulis data di area memori ini dengan memanipulasi variabel.

Berikut contoh kode yang mendeklarasikan variabel dan menunjukkan isinya:
let a;
console.log(a);

Dalam JavaScript, Anda mendeklarasikan variabel dengan kata kunci kelanjutan diikuti oleh nama variabel. Dalam contoh ini, variabel yang dibuat disebut a.
Dalam versi bahasa sebelumnya, variabel dideklarasikan menggunakan kata kunci var.
Inilah hasil eksekusi untuk program ini.

 
	Perhatikan bahwa hasilnya “undefined”. Ini adalah jenis JavaScript khusus yang menunjukkan tidak ada nilai. Saya menyatakan variabel, menyebutnya, tetapi tidak memberikan nilai!

Tetapkan nilai ke variable
Saat program berjalan, nilai yang disimpan dalam variabel dapat berubah. Untuk memberikan nilai baru ke variabel, gunakan operator = yang disebut operator penugasan. Lihat contoh di bawah ini:
let a;
a = 3.14;
console.log(a);

 
Kami memodifikasi variabel dengan menetapkan nilai. a = 3.14 dibaca sebagai "a menerima nilai 3.14".

	Berhati-hatilah agar tidak membingungkan operator penugasan = dengan persamaan matematis! Anda akan segera melihat bagaimana mengekspresikan kesetaraan dalam JavaScript.

	Anda juga dapat menggabungkan mendeklarasikan variabel dan menetapkan nilai dalam satu baris. Ketahuilah bahwa, dalam garis ini, Anda melakukan dua hal yang berbeda sekaligus:

let a = 3.14;
console.log(a);

Mendeklarasikan variabel konstan
Jika nilai awal variabel tidak akan pernah berubah selama sisa eksekusi program, variabel ini disebut konstanta. Keteguhan ini dapat ditegakkan dengan menggunakan kata kunci const bukannya membiarkan untuk menyatakannya. Dengan demikian, program ini lebih ekspresif dan upaya lebih lanjut untuk memodifikasi variabel dapat dideteksi sebagai kesalahan.
const a = 3.14; // The value of a cannot be modified
a = 6.28;       // Impossible! 
Menambah jumlah variable
	Anda juga dapat meningkatkan nilai angka dengan + = dan ++. Yang terakhir disebut operator kenaikan, karena memungkinkan peningkatan (peningkatan sebesar 1) dari nilai variabel.

Dalam contoh berikut, baris 2 dan 3 masing-masing meningkatkan nilai variabel b sebesar 1.

let b = 0;      // b contains 0
b += 1;         // b contains 1
b++;            // b contains 2
console.log(b); // Shows 2

Ruang lingkup variable
	Ruang lingkup variabel adalah bagian dari program di mana variabel terlihat dan dapat digunakan. Variabel yang dideklarasikan dengan let atau const adalah blok-cakupan: visibilitas mereka terbatas pada blok di mana mereka dideklarasikan (dan setiap sub-blok, jika ada). Dalam JavaScript dan banyak bahasa pemrograman lainnya, blok kode adalah bagian dari program yang dibatasi oleh sepasang tanda kurung buka dan tutup. Secara default, program JavaScript membentuk satu blok kode.

let num1 = 0;
{
  num1 = 1; // OK : num1 is declared in the parent block
  const num2 = 0;
}
console.log(num1); // OK : num1 is declared in the current block
console.log(num2); // Error! num2 is not visible here


Ekspresi
Ekspresi adalah bagian kode yang menghasilkan nilai. Ekspresi dibuat dengan menggabungkan variabel, nilai, dan operator. Setiap ekspresi memiliki nilai dan tipe. Menghitung nilai ekspresi disebut evaluasi. Selama evaluasi, variabel diganti oleh nilainya.
// 3 is an expression whose value is 3
const c = 3;
// c is an expression whose value is the value of c (3 here)
let d = c;
// (d + 1) is an expression whose value is d's + 1 (4 here)
d = d + 1; // d now contains the value 4
console.log(d); // Show 4

Prioritas operator di dalam ekspresi sama seperti dalam matematika. Namun, ekspresi dapat mengintegrasikan tanda kurung yang mengubah prioritas ini.
let e = 3 + 2 * 4; // e contains 11 (3 + 8)
e = (3 + 2) * 4;   // e contains 20 (5 * 4)

Adalah mungkin untuk memasukkan ekspresi dalam string dengan menggunakan backticks (`) untuk membatasi string. String seperti itu disebut template literal. Di dalam literal template, ekspresi diidentifikasi oleh sintaks $ {expression}. Ini sering digunakan untuk membuat string yang mengandung nilai beberapa variabel.
const country = "France";
console.log(`I live in ${country}`); // Show "I live in France"
const x = 3;
const y = 7;
console.log(`${x} + ${y} = ${x + y}`); // Show "3 + 7 = 10"


Tipe konversi
Evaluasi ekspresi dapat menghasilkan konversi jenis. Ini disebut konversi implisit, karena terjadi secara otomatis tanpa campur tangan programmer. Sebagai contoh, menggunakan operator + antara string dan nomor menyebabkan penggabungan dari dua nilai menjadi hasil string.
const f = 100;
// Show "Variable f contains the value 100"
console.log("Variable f contains the value " + f);
JavaScript sangat toleran dalam hal konversi jenis. Namun, terkadang konversi tidak dimungkinkan. Jika nilai gagal diubah menjadi angka, Anda akan mendapatkan hasil NaN (Bukan Nomor).
const g = "five" * 2;
console.log(g); // Show NaN
Sometimes you'll wish to convert the value of another type. This is called explicit conversion. JavaScript has the Number() and String() commands that convert the value between the parenthesis to a number or a string.
const h = "5";
console.log(h + 1); // Concatenation: show the string "51"
const i = Number("5");
console.log(i + 1); // Numerical addition: show the number 6

Interaksi pengguna 
Memasukkan informasi
Setelah Anda mulai menggunakan variabel, Anda dapat menulis program yang bertukar informasi dengan pengguna.
const name = prompt("Enter your first name:");
alert(`Hello, ${name}`);


Selama eksekusi, kotak dialog muncul, menanyakan nama Anda.
 

Ini adalah hasil dari command prompt JavaScript ("Masukkan nama depan Anda:"). Ketikkan nama Anda dan klik OK. Anda akan mendapat sambutan pribadi.
 
	Nilai yang Anda masukkan di kotak dialog pertama telah disimpan sebagai string dalam nama variabel. Peringatan perintah JavaScript () kemudian memicu tampilan kotak kedua, yang berisi hasil penggabungan string "Halo," dengan nilai variabel nama.

Menampilkan informasi
Baik console.log () (ditemui di bab sebelumnya) dan alert () dapat digunakan untuk menampilkan informasi kepada pengguna. Tidak seperti alert (), console.log () tidak menghentikan eksekusi program dan seringkali merupakan pilihan yang lebih baik. console.log () juga dapat menampilkan beberapa nilai yang dipisahkan koma sekaligus.
const temp1 = 36.9;
const temp2 = 37.6;
const temp3 = 37.1;
console.log(temp1, temp2, temp3); // Show "36.9 37.6 37.1"

Memasukkan angka
	Terlepas dari data yang dimasukkan, perintah prompt () selalu mengembalikan nilai string. Jika nilai ini akan digunakan dalam ekspresi numerik, maka harus diubah menjadi angka dengan perintah Number ().
const input = prompt("Enter a number:"); // input's type is string
const nb = Number(input); // nb's type is number

Kedua operasi dapat digabungkan dalam satu baris untuk hasil yang sama.
const nb = Number(prompt("Enter a number:")); // nb's type is number

Dalam contoh ini, input pengguna secara langsung dikonversi dalam nilai angka dengan perintah Number () dan disimpan dalam variabel nb.

Penamaan variable
Untuk menutup bab ini, mari kita bahas penamaan variabel. Komputer tidak peduli dengan nama variabel. Anda dapat menamai variabel Anda menggunakan contoh klasik dari satu huruf (a, b, c ...) atau pilih nama yang tidak masuk akal seperti burrito atau puppieskittens90210.

Meskipun demikian, menamai variabel dengan baik dapat membuat kode Anda lebih mudah dibaca. Lihat dua contoh berikut:
const a = 5.5;
const b = 3.14;
const c = 2 * a * b;
console.log(c);

const radius = 5.5;
const pi = 3.14;
const perimeter = 2 * pi * radius;
console.log(perimeter);

Mereka berfungsi dengan cara yang sama, tetapi versi kedua jauh lebih mudah dimengerti. 
Menamai sesuatu adalah bagian penting dari pekerjaan programmer. Lihat apendiks untuk beberapa saran yang bermanfaat.
 Waktu coding! Bangun kebiasaan memilih nama variabel yang bagus di semua latihan, dimulai dengan yang ini.
 Halo yang ditingkatkan Tulis sebuah program yang meminta pengguna untuk nama depannya dan nama belakangnya. 
Program kemudian menampilkannya dalam satu kalimat. Nilai akhir Amati program berikut dan coba untuk memprediksi nilai akhir dari variabel-variabelnya.

let a = 2;
a -= 1;
a++;
let b = 8;
b += 2;
const c = a + b * b;
const d = a * b + b;
const e = a * (b + b);
const f = a * b / a;
const g = b / a * a;
console.log(a, b, c, d, e, f, g);

Periksa prediksi Anda dengan mengeksekusinya. 
Perhitungan PPN Tulis sebuah program yang meminta pengguna untuk harga mentah. Setelah itu, menghitung harga akhir yang terkait menggunakan tarif PPN 20,6%.
Dari Celsius ke derajat Fahrenheit Tulis program yang meminta suhu dalam derajat Celcius, lalu tampilkan dalam derajat Fahrenheit. 
Konversi antara skala diberikan oleh rumus: [° F] = [° C] x 9/5 + 32.

Variabel swapping 
Perhatikan program berikut.
let number1 = 5;
let number2 = 3;

// TODO: type your code here (and nowhere else!)

console.log(number1); // Should show 3
console.log(number2); // Should show 5


Tambahkan kode yang diperlukan untuk menukar nilai variabel nomor1 dan angka2. 
Latihan ini memiliki beberapa solusi yang valid. Anda dapat menggunakan lebih dari dua variabel untuk menyelesaikannya.
