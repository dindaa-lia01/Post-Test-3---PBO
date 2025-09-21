Nama: Dinda Aulia Rizky NIM: 2409116076 KELAS: B'24

# ***Manajemen Daftar Obat di Apotek***

Program manajemen obat di apotek ini tidak hanya mendukung operasi CRUD, tetapi juga sudah menerapkan konsep utama pemrograman berorientasi objek (OOP). Pertama, konsep encapsulation diterapkan dengan menjadikan atribut di setiap class sebagai private, lalu menyediakan method getter dan setter untuk mengakses serta mengubah nilainya. Hal ini menjaga keamanan data obat agar tidak bisa diubah sembarangan dari luar class.

Selanjutnya, program juga menggunakan inheritance dengan menjadikan class Obat sebagai superclass yang menyimpan atribut umum, kemudian diturunkan ke dua subclass yaitu ObatBebas dan ObatResep. Masing-masing subclass memiliki tambahan atribut khusus sesuai jenisnya, sehingga kode menjadi lebih terstruktur dan tidak perlu menulis ulang atribut yang sama. Selain itu, program menerapkan overriding pada method tampilkanObat(). Dengan overriding, setiap subclass dapat menampilkan informasi tambahan sesuai kebutuhan, misalnya ObatBebas menampilkan golongan obat dan anjuran label, sedangkan ObatResep menampilkan nomor resep dan anjuran dokter.

Dengan penerapan ketiga konsep ini, program menjadi lebih aman, rapi, dan fleksibel. Data obat terjaga konsistensinya, kode lebih mudah dipahami, serta program siap dikembangkan lebih lanjut jika ingin menambah jenis obat baru di masa depan.

## A. Penjelasan Encapsulation

Penerapan encapsulation ini diterapkan pada package models, yakni pada class obat.

 - Package dan Import
     
   Kode ini menunjukkan bahwa kelas Obat berada dalam package bernama models, yang biasanya digunakan untuk menyimpan struktur data atau entitas. Selain itu, terdapat import java.time.LocalDate; yang digunakan untuk mengimpor class LocalDate dari library Java. LocalDate dipakai untuk menyimpan informasi tanggal kedaluwarsa obat, sehingga lebih akurat dibandingkan hanya menggunakan String.

   <img width="271" height="62" alt="image" src="https://github.com/user-attachments/assets/aa949e34-6297-4e5c-8ff4-18a67e0a9ad6" />

  - Deklarasi Kelas dan Konstruktor

    Kode ini mendefinisikan sebuah kelas bernama Obat yang berada dalam konsep Object-Oriented Programming (OOP). Di dalamnya terdapat atribut privat yaitu namaObat, kategori, expiredDate, stok, dan harga. Atribut-atribut ini diset sebagai private agar hanya bisa diakses melalui method khusus (getter dan setter), sehingga mendukung prinsip enkapsulasi. Pada bagian konstruktor public Obat(...), terdapat parameter untuk mengisi data awal dari atribut kelas. Keyword this digunakan untuk membedakan antara variabel lokal dengan atribut kelas, contohnya this.namaObat = namaObat;. Pada class obat ini akan dijadikan sebagai superclass, dimana nantinya akan menjadi kelas induk yang mewariskan  property dan method pada subclass

      <img width="895" height="438" alt="image" src="https://github.com/user-attachments/assets/0d93ec87-6292-4064-aee7-bf8450cd4a56" />

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

     Method tampilkanObat() dioverride di dalam class ObatBebas. Tujuannya agar saat data obat bebas ditampilkan, program tidak hanya menampilkan informasi umum dari superclass Obat, tetapi juga menambahkan informasi khusus untuk obat bebas. Di awal, dicetak label [Obat Bebas], lalu dipanggil super.tampilkanObat() untuk menampilkan atribut umum seperti nama, kategori, tanggal kedaluwarsa, stok, dan harga. Setelah itu, ditambahkan dua baris tambahan untuk menampilkan golongan obat dan anjuran penggunaan yang memang menjadi ciri khas obat bebas.

     <img width="501" height="230" alt="Screenshot 2025-09-21 144109" src="https://github.com/user-attachments/assets/e39092d9-f121-4d1e-b8a4-56d7805f0107" />
   
2. Subclass ObatResep

  - Konstruktor dan Atribut
 
    Pada gambar ini, class ObatResep diturunkan dari class Obat menggunakan extends. Class ini menambahkan dua atribut baru, yaitu anjuranDokter untuk menyimpan aturan pemakaian obat sesuai instruksi dokter, serta nomorResep untuk menyimpan kode resep sebagai identitas resmi obat tersebut. Konstruktor ObatResep menerima data umum obat seperti nama, kategori, tanggal kadaluarsa, stok, dan harga, lalu meneruskannya ke superclass dengan super(...). Setelah itu, atribut khusus obat resep diinisialisasi agar data obat lebih lengkap.
     
   <img width="910" height="313" alt="image" src="https://github.com/user-attachments/assets/84280f02-d158-47da-99b4-c588f8fd4573" />

  - Getter dan Setter

    Gambar ini menunjukkan penerapan encapsulation. Atribut anjuranDokter dan nomorResep bersifat private, sehingga tidak bisa diakses langsung dari luar class. Untuk itu, dibuat method getter (getAnjuranDokter(), getNomorResep()) untuk mengambil data, dan setter (setAnjuranDokter(), setNomorResep()) untuk mengubah data. Dengan cara ini, keamanan dan keteraturan data lebih terjaga karena hanya bisa diakses melalui method yang sudah disediakan.

    <img width="829" height="187" alt="image" src="https://github.com/user-attachments/assets/4665640a-f6ac-410c-8837-e5bd07ca6a9b" />

  - Overriding Method

    Method tampilkanObat() juga dioverride, tetapi di dalam class ObatResep. Sama seperti sebelumnya, program pertama menampilkan label [Obat Resep], kemudian memanggil super.tampilkanObat() untuk menampilkan atribut umum dari obat. Selanjutnya, ditambahkan informasi tambahan yang hanya dimiliki oleh obat resep, yaitu nomor resep sebagai identitas resmi pembelian, dan anjuran dokter sebagai aturan penggunaan sesuai instruksi tenaga medis. Dengan cara ini, data obat resep menjadi lebih jelas dan berbeda dari obat bebas.

    <img width="512" height="224" alt="Screenshot 2025-09-21 144133" src="https://github.com/user-attachments/assets/9cdf1add-3e51-4774-ab83-1e70621919cd" />

3. Pembaruan pada package service

   Pembaruan pada package service ini dilakukan karena adanya penambahan inheritance pada package models sebelumnya.

   - Konstruktor

     Pada bagian ini, konstruktor obatService() langsung menambahkan beberapa data obat contoh ke dalam daftarObat. Data tersebut menggunakan subclass ObatBebas dan ObatResep. Tujuannya agar saat program pertama dijalankan, sudah ada data obat yang bisa ditampilkan tanpa harus menambahkannya secara manual dulu. Ini juga menunjukkan implementasi inheritance, karena objek dari subclass bisa dimasukkan ke ArrayList yang bertipe Obat (superclass).

     <img width="962" height="385" alt="Screenshot 2025-09-21 145900" src="https://github.com/user-attachments/assets/aa13aec0-054f-46f9-961d-47e50a59963d" />

     - Method tambahObat()
       
       Method ini digunakan untuk menambah obat baru. Program menampilkan pilihan jenis obat (bebas atau resep), kemudian meminta input dari pengguna untuk mengisi data dasar seperti nama obat, kategori, tanggal kedaluwarsa, stok, dan harga. Input ini berlaku untuk semua jenis obat, karena bagian ini masih mencakup atribut dari superclass Obat.

       <img width="737" height="782" alt="Screenshot 2025-09-21 150121" src="https://github.com/user-attachments/assets/bd970dde-c128-4925-8f4c-e22976c8d109" />

     Bagian ini memisahkan logika berdasarkan pilihan jenis obat:

     - Jika Obat Bebas, pengguna diminta mengisi anjuran label dan golongan obat. Namun, jika golongan obat diisi "KERAS", program akan menolak dengan pesan bahwa obat keras tidak bisa dibeli tanpa resep dokter.

     - Jika Obat Resep, pengguna diminta memasukkan nomor resep dan anjuran dokter.
Setelah data dilengkapi, objek obat baru dibuat sesuai jenisnya lalu dimasukkan ke dalam daftarObat.

       <img width="847" height="794" alt="Screenshot 2025-09-21 150315" src="https://github.com/user-attachments/assets/d902439a-2e59-4754-a137-089f2adcd4bd" />

     - Method updateObat()

       Method ini digunakan untuk memperbarui data obat yang sudah ada. Pertama, daftar obat ditampilkan lalu pengguna memilih nomor obat yang ingin diupdate. Setelah itu, program memberikan kesempatan untuk mengganti atribut umum seperti nama, kategori, stok, dan harga. Jika input dibiarkan kosong, maka data lama tetap dipakai.
       
      <img width="664" height="695" alt="Screenshot 2025-09-21 150357" src="https://github.com/user-attachments/assets/43dbddc0-603d-42c6-b27b-e030109e4166" />

     Bagian ini menggunakan instanceof untuk mengecek apakah obat yang dipilih merupakan ObatBebas atau ObatResep.

     - Jika ObatBebas, pengguna bisa memperbarui anjuran label dan golongan obat.

     - Jika ObatResep, pengguna bisa memperbarui nomor resep dan anjuran dokter. Dengan begitu, setiap jenis obat punya data spesifik yang bisa dikelola sesuai kebutuhannya.

       <img width="612" height="766" alt="Screenshot 2025-09-21 150413" src="https://github.com/user-attachments/assets/162d2c83-6c15-4245-9f25-749ebab17643" />
       
# B. Penjelasan Alur Output


1. Tampilkan Obat

   Program menampilkan semua obat yang ada di daftarObat, baik Obat Bebas maupun Obat Resep. Setiap obat ditampilkan dengan detail atributnya seperti nama, kategori, tanggal kedaluwarsa, stok, harga, serta atribut tambahan (misalnya golongan dan anjuran pada obat bebas, atau nomor resep dan anjuran dokter pada obat resep).
   
   <img width="487" height="705" alt="image" src="https://github.com/user-attachments/assets/0d780a62-d72d-44f8-a314-5631da10043d" />

   <img width="397" height="217" alt="image" src="https://github.com/user-attachments/assets/ab93de21-bed0-4a8e-8a5c-48a263ee7b2b" />
   
3. Tambah Obat

   Saat user memilih menu 2 (Tambah Obat) lalu memilih jenis Obat Bebas. User diminta mengisi data obat baru, termasuk nama, kategori, expired date, stok, harga, anjuran, dan golongan. Jika data valid, objek ObatBebas baru dibuat menggunakan constructor dan ditambahkan ke daftarObat. Pesan “Obat berhasil ditambahkan!” muncul sebagai konfirmasi.
   
   <img width="583" height="422" alt="image" src="https://github.com/user-attachments/assets/fd8fe64b-4a9d-4b97-baa0-dffe08e0337e" />

   <img width="460" height="221" alt="image" src="https://github.com/user-attachments/assets/8ff1ad4a-b919-4c8e-b7c9-c388aab92b94" />


5. Update Obat

   Saat user memilih menu 3 (Update Obat) lalu memilih obat nomor 4. Program menampilkan data lama obat (Vitamin C), lalu meminta input baru untuk tiap atribut. User dapat mengosongkan input jika tidak ingin mengubah nilai lama. Setelah update, obat tersebut diperbarui di dalam list dan ditampilkan pesan “Obat berhasil diupdate!”.
   
   <img width="975" height="189" alt="image" src="https://github.com/user-attachments/assets/68e265d8-0e7b-4f49-b4e0-de41fab5e550" />

   <img width="664" height="218" alt="image" src="https://github.com/user-attachments/assets/38024667-5203-4f38-a537-b9b392c8c291" />























