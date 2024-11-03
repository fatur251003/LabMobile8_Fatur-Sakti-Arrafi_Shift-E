Nama       : Fatur Sakti Arrafi <br>
NIM        : H1D022041<br>
Shift KRS  : A<br>
Shift Baru : E<br>

<h1>Screenshots</h1><br>

![alt text](https://github.com/fatur251003/LabMobile8_Fatur-Sakti-Arrafi_Shift-E/blob/main/images/Screenshot%202024-10-31%20094625.png)
![alt text](https://github.com/fatur251003/LabMobile8_Fatur-Sakti-Arrafi_Shift-E/blob/main/images/Screenshot%202024-10-31%20094618.png)

Berikut adalah cara kerja login pada halaman tersebut:

1. Tampilan Header: 
   Halaman login dimulai dengan `<ion-header>` yang menampilkan toolbar dan judul halaman "Login". Ini diatur menggunakan elemen `<ion-toolbar>` dan `<ion-title>`. 

2. Bagian Konten:
   Pada bagian konten `<ion-content>`, terdapat:
   - Header Kedua (Condensed): Header ini muncul saat halaman di-scroll, dan berfungsi untuk menampilkan judul yang lebih besar, "Login".
   
3. Form Input Username:
   - `<ion-item>` digunakan untuk membuat baris input.
   - Elemen `<ion-label>` menampilkan label "Username" dalam posisi floating, yaitu label akan muncul di atas input ketika pengguna mulai mengetik.
   - `<ion-input type="text">` adalah tempat pengguna memasukkan username. Atribut `[(ngModel)]="username"` mengikat input ini ke variabel `username` di dalam kode TypeScript, sehingga data dapat diambil dan diproses pada saat login. Input ini juga memiliki atribut `required="required"`, yang menandakan bahwa kolom ini wajib diisi.

4. Form Input Password:
   - Mirip dengan input username, terdapat `<ion-item>` dan `<ion-label>` dengan posisi floating.
   - `<ion-input type="password">` digunakan untuk memasukkan kata sandi, dengan atribut yang sama untuk mengikatnya ke variabel `password` menggunakan `[(ngModel)]="password"` dan menjadikannya input wajib (`required="required"`).

5. Tombol Login:
   - Tombol login diletakkan di dalam `<ion-row>` dan `<ion-col>` agar posisi dan ukuran tombol dapat diatur dalam tata letak grid.
   - `<ion-button>` digunakan untuk membuat tombol "Login" dengan warna utama (`color="primary"`) dan tipe submit.
   - Atribut `(click)="login()"` mengatur agar fungsi `login()` dipanggil saat tombol diklik.

6. Fungsi Login:
   - Fungsi `login()` yang ditetapkan dalam atribut `(click)="login()"` diharapkan ada di file TypeScript yang terhubung dengan HTML ini. Fungsi ini akan mengambil nilai `username` dan `password` dari input yang telah diikat menggunakan `[(ngModel)]`, dan kemudian memproses data untuk melakukan autentikasi.
   - Biasanya, fungsi `login()` ini akan memvalidasi input, memverifikasi kredensial pengguna dengan backend server atau layanan autentikasi, dan kemudian mengarahkan pengguna ke halaman berikutnya jika login berhasil atau menampilkan pesan error jika gagal.
