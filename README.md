Nama: Dinda Aulia Rizky NIM: 2409116076 KELAS: B'24

# ***Manajemen Daftar Obat di Apotek***

Program manajemen obat di apotek ini tidak hanya mendukung operasi CRUD, tetapi juga sudah menerapkan konsep utama pemrograman berorientasi objek (OOP). Pertama, konsep encapsulation diterapkan dengan menjadikan atribut di setiap class sebagai private, lalu menyediakan method getter dan setter untuk mengakses serta mengubah nilainya. Hal ini menjaga keamanan data obat agar tidak bisa diubah sembarangan dari luar class.

Selanjutnya, program juga menggunakan inheritance dengan menjadikan class Obat sebagai superclass yang menyimpan atribut umum, kemudian diturunkan ke dua subclass yaitu ObatBebas dan ObatResep. Masing-masing subclass memiliki tambahan atribut khusus sesuai jenisnya, sehingga kode menjadi lebih terstruktur dan tidak perlu menulis ulang atribut yang sama. Selain itu, program menerapkan overriding pada method tampilkanObat(). Dengan overriding, setiap subclass dapat menampilkan informasi tambahan sesuai kebutuhan, misalnya ObatBebas menampilkan golongan obat dan anjuran label, sedangkan ObatResep menampilkan nomor resep dan anjuran dokter.

Dengan penerapan ketiga konsep ini, program menjadi lebih aman, rapi, dan fleksibel. Data obat terjaga konsistensinya, kode lebih mudah dipahami, serta program siap dikembangkan lebih lanjut jika ingin menambah jenis obat baru di masa depan.

## A. Penjelasan Encapsulation

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
   
