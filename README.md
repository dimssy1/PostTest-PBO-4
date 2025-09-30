# PostTest-PBO-4

# 🏀Sistem Basis Data Eskul Basket🏀
*Dimas Aji Mukti 2409116107*

Konsep OOP (Object Oriented Progrmming) yang diterapkan :
1. **Encapsulation**  
  - Atribut di setiap class diset sebagai private agar tidak bisa diakses langsung dari luar.
  - Data hanya bisa diakses atau diubah melalui getter dan setter.
  - Semua atribut (nama, usia, posisi, spesialisasi) dibuat private.
  - Diakses melalui getter dan setter agar lebih aman dan terkontrol.

2. **Inheritance**  
  - Superclass: Anggota (menyimpan data umum seperti id, nama, kelas).
  - Subclass:
    Pemain → menambahkan atribut khusus posisi.
    Pelatih → menambahkan atribut khusus spesialisasi.
    Pemain dan Pelatih adalah subclass yang mewarisi atribut & method dari abstract class Anggota.
    Contoh: Pemain extends Anggota, Pelatih extends Anggota. Dengan inheritance, kode lebih efisien karena atribut umum tidak perlu ditulis ulang di subclass.

3. **Polymorphism**  
  - Method tampilInfo() di Anggota diturunkan ke subclass.
  - Namun, setiap subclass melakukan overriding agar menampilkan data sesuai kebutuhan:
      Pemain → menampilkan id, nama, kelas, posisi.
      Pelatih → menampilkan id, nama, spesialisasi.
  - Overriding
    1. Method latihan() dioverride berbeda di Pemain dan Pelatih.
    2. Pemain → menampilkan posisi latihan.
    3. Pelatih → menampilkan spesialisasi latihan.
    4. Method infoAnggota() juga dioverride agar menampilkan informasi sesuai jenis anggota.
  - Overloading
    1. Method tambahAnggota() dibuat dua versi di AnggotaService:
    2. tambahAnggota(Pemain p) → menambah pemain.
    3. tambahAnggota(Pelatih pl) → menambah pelatih.

4. **Abstraction**
   
   - Dibuat abstract class Anggota yang berisi:
   - Atribut umum (nama, usia).
   - Abstract method latihan() → wajib dioverride oleh Pemain dan Pelatih.

📂 Struktur Proyek
  📋 Fitur Program
  
    1. Tambah Pemain
    2. Lihat Daftar Pemain
    3. Tambah Pelatih
    4. Lihat Daftar Pelatih
    5. Ubah Data Anggota
    6. Hapus Anggota
    7. Cari Anggota
    8. Keluar

⚙️ Alur Program

  1. Membuat beberapa objek Pemain dan Pelatih.
  2. Menambahkan mereka ke dalam service (AnggotaService) menggunakan method overloading.
  3. Menampilkan daftar anggota (pemain & pelatih) lewat method tampilPemain() dan tampilPelatih().
  4. Menjalankan method latihan() yang menunjukkan polymorphism overriding.
