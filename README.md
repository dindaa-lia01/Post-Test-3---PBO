Nama: Dinda Aulia Rizky NIM: 2409116076 KELAS: B'24

# ***Manajemen Daftar Obat di Apotek***

Program manajemen obat di apotek ini tidak hanya mendukung operasi CRUD, tetapi juga sudah menerapkan konsep utama pemrograman berorientasi objek (OOP). Pertama, konsep encapsulation diterapkan dengan menjadikan atribut di setiap class sebagai private, lalu menyediakan method getter dan setter untuk mengakses serta mengubah nilainya. Hal ini menjaga keamanan data obat agar tidak bisa diubah sembarangan dari luar class.

Selanjutnya, program juga menggunakan inheritance dengan menjadikan class Obat sebagai superclass yang menyimpan atribut umum, kemudian diturunkan ke dua subclass yaitu ObatBebas dan ObatResep. Masing-masing subclass memiliki tambahan atribut khusus sesuai jenisnya, sehingga kode menjadi lebih terstruktur dan tidak perlu menulis ulang atribut yang sama. Selain itu, program menerapkan overriding pada method tampilkanObat(). Dengan overriding, setiap subclass dapat menampilkan informasi tambahan sesuai kebutuhan, misalnya ObatBebas menampilkan golongan obat dan anjuran label, sedangkan ObatResep menampilkan nomor resep dan anjuran dokter.

Dengan penerapan ketiga konsep ini, program menjadi lebih aman, rapi, dan fleksibel. Data obat terjaga konsistensinya, kode lebih mudah dipahami, serta program siap dikembangkan lebih lanjut jika ingin menambah jenis obat baru di masa depan.

## A. Penjelasan Encapsulation

Penerapan encapsulation ini diterapkan pada package models, yakni pada class obat.

 - Package Main (class apotek)
     
   Kode ini menunjukkan bahwa kelas Obat berada dalam package bernama models, yang biasanya digunakan untuk menyimpan struktur data atau entitas. Selain itu, terdapat import java.time.LocalDate; yang digunakan untuk mengimpor class LocalDate dari library Java. LocalDate dipakai untuk menyimpan informasi tanggal kedaluwarsa obat, sehingga lebih akurat dibandingkan hanya menggunakan String.

   <img width="269" height="63" alt="image" src="https://github.com/user-attachments/assets/75a4b801-4ee7-41f9-89bd-0e9f99091421" />

  - Deklarasi Kelas dan Konstruktor

    Kode ini mendefinisikan sebuah kelas bernama Obat yang berada dalam konsep Object-Oriented Programming (OOP). Di dalamnya terdapat atribut privat yaitu namaObat, kategori, expiredDate, stok, dan harga. Atribut-atribut ini diset sebagai private agar hanya bisa diakses melalui method khusus (getter dan setter), sehingga mendukung prinsip enkapsulasi. Pada bagian konstruktor public Obat(...), terdapat parameter untuk mengisi data awal dari atribut kelas. Keyword this digunakan untuk membedakan antara variabel lokal dengan atribut kelas, contohnya this.namaObat = namaObat;.

    <img width="882" height="440" alt="image" src="https://github.com/user-attachments/assets/9cd6930d-9aed-45e8-841d-33f6faff98a3" />

  - Getter dan Setter

    Bagian ini berisi kumpulan getter dan setter untuk setiap atribut. Getter seperti getNamaObat() berfungsi mengembalikan nilai dari atribut tertentu, sedangkan setter seperti setNamaObat(String namaObat) berfungsi mengubah nilai atribut tersebut. Pola ini berlaku untuk semua atribut: namaObat, kategori, expiredDate, stok, dan harga. Dengan adanya getter dan setter, akses data menjadi lebih aman dan fleksibel, karena program tidak langsung memanipulasi atribut, tetapi melalui method yang sudah disediakan.

    <img width="529" height="607" alt="image" src="https://github.com/user-attachments/assets/f6bc6a83-b071-47f9-93cb-14691026ab90" />

    <img width="519" height="603" alt="image" src="https://github.com/user-attachments/assets/67dcb2e7-5307-48d2-85d2-f866b8763b38" />

 - Method tampilkanObat()

   <img width="528" height="229" alt="image" src="https://github.com/user-attachments/assets/d4163333-1fe4-4834-990b-adcf134d4542" />

   Pada bagian ini terdapat method tampilkanObat() yang bertugas untuk menampilkan informasi detail dari objek obat yang dibuat. Data yang ditampilkan mencakup nama obat, kategori, tanggal kedaluwarsa, stok, dan harga. Setiap informasi dicetak ke layar dengan System.out.println(). Method ini berguna agar data objek bisa dilihat dengan mudah oleh pengguna dalam format yang rapi.
   
## B. Penjelasan Inheritance & Overiding

Penerapan inheritance ini dilakukan pada package models dengan menjadikan class obat menjadi superclass, lalu menambahkan 2 subclass yakni ObatBebas dan ObatResep.

1. Subclass ObatBebas

   - Konstruktor dan Atribut

     Class ObatBebas merupakan turunan dari Obat yang mewakili jenis obat yang bisa dibeli tanpa resep dokter. Class ini memiliki dua atribut tambahan, yaitu anjuranLabel untuk menyimpan petunjuk pemakaian obat yang biasanya tertera pada kemasan, serta golongan untuk menunjukkan kategori obat bebas (misalnya bebas, bebas terbatas, atau keras). Konstruktor ObatBebas menerima data umum obat lalu meneruskannya ke superclass dengan super(...), dan sekaligus menginisialisasi atribut tambahan khusus obat bebas.
     
    <img width="928" height="326" alt="Screenshot 2025-09-21 032314" src="https://github.com/user-attachments/assets/738aebed-895e-48e3-9def-a606ddc9ffa6" />
 
   - Getter dan Setter

     Method getter dan setter yang digunakan sebagai penerapan encapsulation. Method getAnjuranLabel() dan setAnjuranLabel() digunakan untuk mengambil dan mengubah aturan pemakaian obat yang tertera pada label, sedangkan getGolongan() dan setGolongan() digunakan untuk membaca serta mengubah kategori atau golongan obat. Dengan cara ini, data tetap terjaga karena atribut bersifat private dan hanya bisa diakses melalui method resmi.

     <img width="800" height="166" alt="Screenshot 2025-09-21 032616" src="https://github.com/user-attachments/assets/ec98bbf3-6d44-4a20-a23a-adb172e83724" />
     
   - Overriding Method

     Gambar ketiga memperlihatkan overriding method tampilkanObat(). Method ini pertama-tama memanggil super.tampilkanObat() untuk menampilkan informasi umum obat dari superclass, lalu menambahkan informasi khusus obat bebas, yaitu golongan obat dan anjuran pemakaian yang tertera pada label. Dengan overriding ini, tampilan data obat bebas menjadi lebih lengkap dan sesuai dengan kebutuhan nyata dalam manajemen obat di apotek.

     <img width="498" height="183" alt="Screenshot 2025-09-21 032638" src="https://github.com/user-attachments/assets/00ff565e-66b9-42ff-a437-a26e353afbc1" />
   
2. Subclass ObatResep

  - Atribut dan Konstruktor
 
    Pada gambar ini, class ObatResep diturunkan dari class Obat menggunakan extends. Class ini menambahkan dua atribut baru, yaitu anjuranDokter untuk menyimpan aturan pemakaian obat sesuai instruksi dokter, serta nomorResep untuk menyimpan kode resep sebagai identitas resmi obat tersebut. Konstruktor ObatResep menerima data umum obat seperti nama, kategori, tanggal kadaluarsa, stok, dan harga, lalu meneruskannya ke superclass dengan super(...). Setelah itu, atribut khusus obat resep diinisialisasi agar data obat lebih lengkap.
     
   <img width="910" height="313" alt="image" src="https://github.com/user-attachments/assets/84280f02-d158-47da-99b4-c588f8fd4573" />

  - Getter dan Setter

    Gambar ini menunjukkan penerapan encapsulation. Atribut anjuranDokter dan nomorResep bersifat private, sehingga tidak bisa diakses langsung dari luar class. Untuk itu, dibuat method getter (getAnjuranDokter(), getNomorResep()) untuk mengambil data, dan setter (setAnjuranDokter(), setNomorResep()) untuk mengubah data. Dengan cara ini, keamanan dan keteraturan data lebih terjaga karena hanya bisa diakses melalui method yang sudah disediakan.

    <img width="829" height="187" alt="image" src="https://github.com/user-attachments/assets/4665640a-f6ac-410c-8837-e5bd07ca6a9b" />

  - Overriding Method

    Pada gambar ini terdapat method tampilkanObat() yang dioverride dari superclass Obat. Pertama, method ini memanggil super.tampilkanObat() untuk menampilkan informasi umum obat, lalu menambahkan dua informasi tambahan yaitu nomor resep dan anjuran dokter. Dengan overriding ini, saat objek ObatResep ditampilkan, hasil output akan lebih lengkap dan sesuai dengan karakteristik obat resep.

    <img width="518" height="194" alt="image" src="https://github.com/user-attachments/assets/95aa1299-4ec3-44f3-80f7-4846c4b19338" />

3. Pembaruan pada package service

   Pembaruan pada package service ini dilakukan karena adanya penambahan inheritance pada package models sebelumnya.

   
























