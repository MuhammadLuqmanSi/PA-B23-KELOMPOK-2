# PROJECT AKHIR ASD&DBMS
## Sistem Informasi Perkotaan dan Pemukiman Berkelanjutan (SIP2B)
### KELOMPOK 2 / B / 2024
- Muhammad Daffa Ezra Putra 	(2309116052)
- Muhammad Luqman	(2309116068)
- Vincenz Reynard Citro 	(2309116080)
- Muhammad Fa’iz	(2309116086)
### aplikasi yang digunakan :
[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

[![Visual Studio](https://badgen.net/badge/icon/visualstudio?icon=visualstudio&label)](https://visualstudio.microsoft.com)

### Deskipsi program 
Tujuan:
- Menyediakan sistem informasi terintegrasi dan mudah diakses tentang perkotaan dan pemukiman di Indonesia.
- Membantu para pemangku kepentingan dalam membuat kebijakan yang tepat dan efektif untuk pembangunan perkotaan dan pemukiman yang berkelanjutan.
  
Masukan:
- Data tentang perkotaan dan pemukiman dari berbagai :
   - Kementerian Pekerjaan Umum dan Perumahan Rakyat (PUPR) 
   - Kementerian Agraria dan Tata Ruang/Badan Pertanahan Nasional
   - Kementerian Sosial
   - Kementerian Keuangan (Kemenkeu)
     
Keluaran:
- Alat dan platform untuk mendukung pengambilan keputusan terkait pembangunan perkotaan dan pemukiman yang berkelanjutan.
  
Algoritma:
- Sistem SIP2B akan menggunakan berbagai algoritma dan teknik data science untuk mengolah dan menganalisis data tentang perkotaan dan pemukiman.
- Algoritma ini akan digunakan untuk menghasilkan laporan, peta, dan visualisasi data yang dapat membantu para pemangku kepentingan dalam memahami kondisi perkotaan dan pemukiman di Indonesia.
  
Batasan:
- Sistem SIP2B masih dalam tahap pengembangan, dan data yang tersedia mungkin belum lengkap atau akurat.
- Sistem ini mungkin tidak dapat menjawab semua pertanyaan tentang perkotaan dan pemukiman di Indonesia.
  
Manfaat:
- Sistem SIP2B dapat membantu para pemangku kepentingan dalam:
  - Memahami kondisi perkotaan dan pemukiman di Indonesia.
  - Mengidentifikasi masalah dan tantangan yang dihadapi perkotaan dan pemukiman di Indonesia.
  - Mengembangkan kebijakan dan program yang tepat dan efektif untuk pembangunan perkotaan dan pemukiman yang berkelanjutan.
  - Memantau dan mengevaluasi kemajuan pembangunan perkotaan dan pemukiman yang berkelanjutan.

Sistem Informasi Perkotaan dan Pemukiman Berkelanjutan (SIP2B) dengan menganut konsep kota komunitas berkelanjutan telah menjadi solusi yang inovatif untuk menghadapi permasalahan kota modern sekarang. SIP2B dirancang untuk mengatasi tantangan-tantangan tersebut dengan menyediakan sistem informasi yang terintegrasi dan mudah diakses tentang perkotaan dan pemukiman di Indonesia. SIP2B diharapkan dapat membantu para pemangku kepentingan dalam membuat kebijakan yang tepat dan efektif untuk pembangunan perkotaan dan pemukiman yang berkelanjutan.

### Struktur Project

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/1.png?raw=true)

- import mysql.connector: Baris ini mengimpor modul mysql.connector, yang menyediakan fungsi untuk terhubung dan berinteraksi dengan database MySQL di Python.
- from mysql.connector import Error: Ini mengimpor kelas Error secara khusus dari modul mysql.connector. Kelas ini kemungkinan digunakan untuk menangani kesalahan yang mungkin terjadi selama operasi database.
- import prettytable: Baris ini mengimpor modul prettytable, yang menawarkan alat untuk membuat tabel menarik secara visual untuk menampilkan data. Biasanya digunakan untuk menampilkan hasil query database dalam format yang jelas dan teratur.
- import getpass: Baris ini mengimpor modul getpass, yang menyediakan cara aman untuk meminta kata sandi pengguna tanpa menampilkannya di konsol. Ini sering digunakan saat terhubung ke database yang membutuhkan autentikasi.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/2.png?raw=true)

- mydb = mysql.connector.connect(...): Baris ini mencoba untuk terhubung ke database MySQL menggunakan fungsi mysql.connector.connect(). Fungsi ini menerima argumen sebagai berikut:
  - host: Nama host atau alamat IP dari server MySQL (dalam kasus ini, "sql6.freesqldatabase.com").
  - user: Username untuk mengakses database ("sql6701169").
  - password: Password untuk user tersebut ("Lh6evPczGK").
  - database: Nama database yang akan dihubungi ("sql6701169").
- Jika koneksi berhasil, fungsi connect() akan mengembalikan objek koneksi, yang disimpan dalam variabel mydb.
- mycursor = mydb.cursor(): Baris ini membuat objek kursor menggunakan metode cursor() dari objek koneksi mydb. Kursor bertindak sebagai penunjuk yang dapat digunakan untuk menjalankan pernyataan SQL dan mengambil hasil dari database.
- except Error as e:: Blok ini mendefinisikan penanganan pengecualian yang menangkap segala kesalahan (dari tipe Error) yang mungkin terjadi selama proses pembuatan koneksi. Bagian as e menetapkan kesalahan yang ditemui ke variabel e untuk diproses lebih lanjut.
- print("Error saat menghubungkan ke database:", e): Jika terjadi kesalahan, baris ini mencetak pesan informatif ke konsol: "Error saat menghubungkan ke database:" diikuti oleh detail kesalahan yang disimpan dalam e. Ini membantu dalam memecahkan masalah koneksi.
- exit(): Fungsi exit() menghentikan eksekusi program setelah mencetak pesan kesalahan. Ini adalah pendekatan umum untuk mencegah program melanjutkan dengan data atau tindakan yang mungkin salah.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/3.png?raw=true)

- Node: Ini adalah nama yang diberikan untuk kelas. Nama ini mencerminkan tujuan kelas, yaitu untuk mewakili node dalam struktur data tertaut.
- def __init__(self, data):: Ini adalah metode konstruktor kelas, yang dipanggil saat membuat instance baru dari kelas Node.
  - self: Parameter ini merujuk pada objek Node yang baru dibuat.
  - data: Parameter ini menampung nilai yang akan disimpan dalam node.
- self.data: Ini adalah atribut privat (private attribute) dari kelas Node. Atribut ini menyimpan nilai yang terkait dengan node.
  - data: Tipe data atribut ini tidak ditentukan dalam kode yang diberikan.
- self.next: Ini adalah atribut privat lainnya dari kelas Node. Atribut ini menunjuk ke node berikutnya dalam struktur data tertaut.
  - None: Nilai awal self.next adalah None, menunjukkan bahwa node baru tidak terhubung ke node lain pada saat pembuatan.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/4.png?raw=true)

- LinkedList: Ini adalah nama yang diberikan untuk kelas. Nama ini mencerminkan tujuan kelas, yaitu untuk mewakili struktur data tertaut.
- def __init__(self):: Ini adalah metode konstruktor kelas, yang dipanggil saat membuat instance baru dari kelas LinkedList.
  - self: Parameter ini merujuk pada objek LinkedList yang baru dibuat.
- self.head: Ini adalah atribut privat (private attribute) dari kelas LinkedList. Atribut ini menyimpan referensi ke node pertama (head) dalam struktur data tertaut.
  - None: Nilai awal self.head adalah None, menunjukkan bahwa linked list masih kosong pada saat pembuatan.
 
![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/5.png?raw=true)

- append: Nama ini menunjukkan fungsi dari metode, yaitu untuk menambahkan (append) data baru ke linked list.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode append.
- data: Parameter ini berisi nilai data yang akan disimpan dalam node baru yang akan ditambahkan.
- new_node = Node(data): Baris ini membuat sebuah node baru menggunakan kelas Node. Nilai data yang diberikan sebagai parameter diteruskan ke konstruktor kelas Node untuk disimpan dalam atribut data dari node baru tersebut.
- if not self.head:: Baris ini mengecek apakah linked list masih kosong (atribut head bernilai None).
  - self.head = new_node: Jika linked list kosong, node baru yang dibuat langsung ditetapkan sebagai node pertama (head) menggunakan self.head = new_node.
  - return: Setelah menetapkan head, fungsi append langsung dihentikan menggunakan return.
- last_node = self.head: Baris ini menyimpan referensi ke node pertama (head) ke dalam variabel last_node.
- while last_node.next:: Ini adalah perulangan while yang akan terus berjalan selama last_node.next tidak bernilai None. Atribut next dari sebuah node menunjuk ke node berikutnya dalam linked list.
  - last_node = last_node.next: Di dalam perulangan, last_node diperbarui untuk menunjuk ke node berikutnya, sehingga iterasi perulangan akan menelusuri linked list hingga mencapai node terakhir.
- last_node.next = new_node: Setelah perulangan selesai, last_node akan menunjuk ke node terakhir dalam linked list. Baris ini menetapkan atribut next dari node terakhir tersebut untuk menunjuk ke node baru (new_node). Ini essentially menghubungkan node baru ke akhir linked list.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/6.png?raw=true)

- display_admin: Nama ini menunjukkan fungsi dari metode, yaitu untuk menampilkan (display) data admin.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode display_admin.
- current = self.head: Baris ini menyimpan referensi ke node pertama (head) dari linked list ke dalam variabel current. Variabel ini akan digunakan untuk iterasi (menelusuri) linked list.
- x = PrettyTable(): Baris ini membuat objek dari library PrettyTable (kemungkinan library pihak ketiga yang belum didefinisikan sebelumnya). Objek ini mungkin digunakan untuk memformat tampilan data admin.
- x.field_names = ["ID Admin", "Nama Admin", "Email Admin", "Password Admin", "Role"]: Baris ini menetapkan nama kolom untuk tabel yang akan dibuat. Nama kolom ini sesuai dengan properti (atribut) yang mungkin dimiliki oleh objek admin yang tersimpan dalam node linked list.
- while current:: Ini adalah perulangan while yang akan terus berjalan selama current tidak bernilai None. Ingat current menunjuk ke node saat ini dalam linked list.
  - x.add_row(current.data): Di dalam perulangan, baris ini menambahkan baris baru ke tabel yang dibuat sebelumnya. current.data mengacu pada data yang tersimpan dalam node saat ini (kemungkinan berupa objek admin). Diasumsikan bahwa objek admin tersebut memiliki properti (atribut) yang sesuai dengan nama kolom yang telah ditetapkan sebelumnya.
  - current = current.next: Baris ini memperbarui current untuk menunjuk ke node berikutnya dalam linked list, sehingga iterasi selanjutnya akan memproses data admin dari node berikutnya.
- print(x): Setelah iterasi selesai, baris ini mencetak tabel yang telah diisi dengan data admin dari linked list menggunakan fungsi print.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/7.png?raw=true)

- display_perkotaan: Nama ini menunjukkan fungsi dari metode, yaitu untuk menampilkan (display) data perkotaan.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode display_perkotaan.
- current = self.head: Baris ini menyimpan referensi ke node pertama (head) dari linked list ke dalam variabel current. Variabel ini akan digunakan untuk iterasi (menelusuri) linked list.
- x = PrettyTable(): Baris ini membuat objek dari library PrettyTable (kemungkinan library pihak ketiga yang belum didefinisikan sebelumnya). Objek ini mungkin digunakan untuk memformat tampilan data perkotaan.
- x.field_names = ["ID", "Nama Kota", "Provinsi", "Jumlah Penduduk", "Luas Wilayah", "indeks keberlanjutan_kota", "ID ADMIN"]: Baris ini menetapkan nama kolom untuk tabel yang akan dibuat. Nama kolom ini sesuai dengan properti (atribut) yang mungkin dimiliki oleh objek perkotaan yang tersimpan dalam node linked list.
- while current:: Ini adalah perulangan while yang akan terus berjalan selama current tidak bernilai None. Ingat current menunjuk ke node saat ini dalam linked list.
  - x.add_row(current.data): Di dalam perulangan, baris ini menambahkan baris baru ke tabel yang dibuat sebelumnya. current.data mengacu pada data yang tersimpan dalam node saat ini (kemungkinan berupa objek perkotaan). Diasumsikan bahwa objek perkotaan tersebut memiliki properti (atribut) yang sesuai dengan nama kolom yang telah ditetapkan sebelumnya.
  - current = current.next: Baris ini memperbarui current untuk menunjuk ke node berikutnya dalam linked list, sehingga iterasi selanjutnya akan memproses data perkotaan dari node berikutnya.
- print(x): Setelah iterasi selesai, baris ini mencetak tabel yang telah diisi dengan data perkotaan dari linked list menggunakan fungsi print.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/8.png?raw=true)

- display_pemukiman: Nama ini menunjukkan fungsi dari metode, yaitu untuk menampilkan (display) data pemukiman.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode display_pemukiman.
- current = self.head: Baris ini menyimpan referensi ke node pertama (head) dari linked list ke dalam variabel current. Variabel ini akan digunakan untuk iterasi (menelusuri) linked list.
- x = PrettyTable(): Baris ini membuat objek dari library PrettyTable (kemungkinan library pihak ketiga yang belum didefinisikan sebelumnya). Objek ini mungkin digunakan untuk memformat tampilan data pemukiman.
- x.field_names = ["ID Pemukiman", "Nama Pemukiman", "ID Perkotaan", "Jenis Pemukiman", "Akses Air Bersih", "Akses Sanitasi Layak", "ID ADMIN"]: Baris ini menetapkan nama kolom untuk tabel yang akan dibuat. Nama kolom ini sesuai dengan properti (atribut) yang mungkin dimiliki oleh objek pemukiman yang tersimpan dalam node linked list.
- while current:: Ini adalah perulangan while yang akan terus berjalan selama current tidak bernilai None. Ingat current menunjuk ke node saat ini dalam linked list.
  - x.add_row(current.data): Di dalam perulangan, baris ini menambahkan baris baru ke tabel yang dibuat sebelumnya. current.data mengacu pada data yang tersimpan dalam node saat ini (kemungkinan berupa objek pemukiman). Diasumsikan bahwa objek pemukiman tersebut memiliki properti (atribut) yang sesuai dengan nama kolom yang telah ditetapkan sebelumnya.
  - current = current.next: Baris ini memperbarui current untuk menunjuk ke node berikutnya dalam linked list, sehingga iterasi selanjutnya akan memproses data pemukiman dari node berikutnya.
- print(x): Setelah iterasi selesai, baris ini mencetak tabel yang telah diisi dengan data pemukiman dari linked list menggunakan fungsi print.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/9.png?raw=true)

- display_proyek: Nama ini menunjukkan fungsi dari metode, yaitu untuk menampilkan (display) data proyek.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode display_proyek.
- current = self.head: Baris ini menyimpan referensi ke node pertama (head) dari linked list ke dalam variabel current. Variabel ini akan digunakan untuk iterasi (menelusuri) linked list.
- x = PrettyTable(): Baris ini membuat objek dari library PrettyTable (kemungkinan library pihak ketiga yang belum didefinisikan sebelumnya). Objek ini mungkin digunakan untuk memformat tampilan data proyek.
- x.field_names = ["ID Proyek", "Nama Proyek", "ID Pemukiman", "Deskripsi Proyek", "Jenis Proyek", "Dana Proyek", "Status Proyek", "ID ADMIN"]: Baris ini menetapkan nama kolom untuk tabel yang akan dibuat. Nama kolom ini sesuai dengan properti (atribut) yang mungkin dimiliki oleh objek proyek yang tersimpan dalam node linked list.
- while current:: Ini adalah perulangan while yang akan terus berjalan selama current tidak bernilai None. Ingat current menunjuk ke node saat ini dalam linked list.
  - x.add_row(current.data): Di dalam perulangan, baris ini menambahkan baris baru ke tabel yang dibuat sebelumnya. current.data mengacu pada data yang tersimpan dalam node saat ini (kemungkinan berupa objek proyek). Diasumsikan bahwa objek proyek tersebut memiliki properti (atribut) yang sesuai dengan nama kolom yang telah ditetapkan sebelumnya.
  - current = current.next: Baris ini memperbarui current untuk menunjuk ke node berikutnya dalam linked list, sehingga iterasi selanjutnya akan memproses data proyek dari node berikutnya.
- print(x): Setelah iterasi selesai, baris ini mencetak tabel yang telah diisi dengan data proyek dari linked list menggunakan fungsi print.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/10.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama quick_sort untuk mengurutkan elemen dalam list arr. Ini kemungkinan menggunakan algoritma pengurutan quicksort.
- arr: List yang berisi elemen-elemen yang akan diurutkan.
- ascending (opsional): Nilai boolean yang menentukan urutan pengurutan. True untuk urutan menaik (ascending), False untuk urutan menurun (descending). Default-nya adalah True (menaik).
- if len(arr) <= 1:: Baris ini mengecek apakah panjang list arr kurang dari atau sama dengan 1. Jika iya, maka list tersebut sudah terurut atau berisi tunggal elemen, dan langsung dikembalikan menggunakan return arr.
- pivot = arr[len(arr) // 2][0]: Baris ini memilih elemen pivot. Di sini, pivot diambil sebagai elemen tengah dari list arr (indeks len(arr) // 2). Kemudian, elemen pada indeks tersebut diakses menggunakan [0] untuk mendapatkan nilai pertamanya
- left = [x for x in arr if x[0] < pivot]: Baris ini membuat list baru bernama left yang berisi elemen-elemen dari arr yang lebih kecil dari nilai pivot. Ini menggunakan list comprehension untuk memfilter elemen-elemen yang memenuhi kondisi.
- middle = [x for x in arr if x[0] == pivot]: Baris ini membuat list baru bernama middle yang berisi elemen-elemen dari arr yang sama persis dengan nilai pivot.
- right = [x for x in arr if x[0] > pivot]: Baris ini membuat list baru bernama right yang berisi elemen-elemen dari arr yang lebih besar dari nilai pivot.
- if ascending:: Blok kode ini menangani pengurutan secara menaik.
  - return quick_sort(left, ascending) + middle + quick_sort(right, ascending): Baris ini memanggil fungsi quick_sort secara rekursif untuk mengurutkan list left dan right terlebih dahulu. Setelah itu, elemen-elemen dari left (yang sudah terurut), middle (pivot), dan right (yang sudah terurut) digabungkan menggunakan operator + untuk membentuk list yang terurut secara keseluruhan.
- else:: Blok kode ini menangani pengurutan secara menurun (descending).
  - return quick_sort(right, ascending) + middle + quick_sort(left, ascending): Perhatikan bahwa urutan pemanggilan fungsi quick_sort dibalik untuk mendapatkan urutan menurun. Elemen-elemen dari right (yang lebih besar) diurutkan terlebih dahulu, kemudian diikuti dengan middle dan left (yang lebih kecil).
- except Exception as e:: Blok kode ini menangani kemungkinan adanya kesalahan (exception) selama proses pengurutan.
  - print("Error saat melakukan sorting:", e): Jika terjadi kesalahan, pesan error akan dicetak ke konsol.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/11.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama jump_search untuk mencari elemen x dalam list arr.  Fungsi ini kemungkinan menggunakan teknik pencarian lompatan (jump search).
- arr: List yang berisi elemen-elemen yang akan dicari.
- x: Nilai yang ingin dicari dalam list arr.
- n = len(arr): Baris ini mendapatkan panjang dari list arr dan disimpan di variabel n.
- step = int(n ** 0.5): Baris ini menghitung nilai lompatan awal (step) berdasarkan akar pangkat dua dari panjang list n. Nilai ini dibulatkan menjadi integer menggunakan int().
- while arr[min(step, n)-1][0] < x:: Perulangan while ini berlanjut selama elemen pada indeks min(step, n)-1 (dikurangi 1 karena indeks dimulai dari 0) memiliki nilai yang lebih kecil dari nilai yang dicari x.
  - min(step, n) digunakan untuk memastikan indeks tidak melebihi batas akhir list arr.
- prev = step: Di dalam perulangan, nilai prev diperbarui dengan nilai step untuk menandai indeks lompatan selanjutnya.
- step += int(n ** 0.5): Nilai lompatan step diperbesar dengan nilai lompatan awal yang dihitung sebelumnya.
- if prev >= n:: Kondisi ini mengecek apakah prev sudah melewati batas akhir list arr. Jika ya, maka pencarian dihentikan dan fungsi mengembalikan -1 menandakan elemen tidak ditemukan.
- while arr[prev][0] < x:: Perulangan while kedua ini melakukan pencarian linear lokal di sekitar indeks yang diperoleh dari lompatan terakhir (prev). Perulangan berlanjut selama elemen pada indeks prev memiliki nilai yang lebih kecil dari nilai yang dicari x.
- prev += 1: Di dalam perulangan, indeks prev diincrement untuk memeriksa elemen selanjutnya.
- if prev == min(step, n): Kondisi ini mengecek apakah prev sudah mencapai batas akhir lompatan yang ditentukan sebelumnya (min(step, n)). Jika ya, maka pencarian lokal dihentikan dan fungsi mengembalikan -1 menandakan elemen tidak ditemukan.
- if arr[prev][0] == x:: Kondisi ini mengecek apakah elemen pada indeks prev sama persis dengan nilai yang dicari x. Jika ya, maka indeks tersebut (prev) dikembalikan sebagai hasil pencarian.
- return -1: Jika kesesuaian tidak ditemukan pada kondisi sebelumnya, maka fungsi mengembalikan -1 menandakan elemen tidak ditemukan dalam list arr.
- except Exception as e:: Blok kode ini menangani kemungkinan adanya kesalahan (exception) selama proses pencarian.
  - print("Error saat melakukan pencarian:", e): Jika terjadi kesalahan, pesan error akan dicetak ke konsol.
  - return -1: Fungsi tetap mengembalikan -1 untuk menandakan adanya kesalahan.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/12.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama read_admin kemungkinan untuk membaca data admin dari database dan menampilkannya.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan myresult).
- Class LinkedList telah didefinisikan sebelumnya dan memiliki fungsi append untuk menambahkan data dan display_admin untuk menampilkan data admin dalam format tabel.
- try:: Blok ini digunakan untuk mencoba menjalankan code di dalamnya. Jika terjadi kesalahan, blok except akan menangani.
- mycursor.execute("SELECT * FROM admin"): Baris ini mengirimkan query ke database untuk mengambil semua data dari tabel admin. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- myresult = mycursor.fetchall(): Baris ini mengambil semua hasil query yang dikembalikan oleh database dan disimpan di variabel myresult. Diasumsikan myresult berupa list yang berisi record-record data admin.
- ll = LinkedList(): Baris ini membuat objek baru dari class LinkedList dan disimpan di variabel ll. Objek ini kemungkinan digunakan untuk menyimpan data admin yang akan ditampilkan.
- for data in myresult:: Perulangan for ini iterasi melalui setiap record data admin yang ada di myresult.
  - ll.append(data): Di dalam perulangan, setiap record data admin (data) ditambahkan ke linked list ll menggunakan fungsi append.
- ll.display_admin(): Baris ini memanggil fungsi display_admin dari objek ll. Fungsi ini kemungkinan bertugas untuk menampilkan data admin yang tersimpan di linked list dalam format tabel yang rapi.
- except Error as e:: Blok ini akan dieksekusi jika terjadi kesalahan (exception) selama proses pembacaan data atau interaksi dengan database.
  - print("Error saat membaca data admin:", e): Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/13.png?raw=true)

- kode yang diberikan mendefinisikan sebuah fungsi bernama tambah_data_admin yang kemungkinan digunakan untuk menambahkan data admin baru ke database.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- try:: Blok ini digunakan untuk mencoba menjalankan code di dalamnya. Jika terjadi kesalahan, blok except akan menangani.
- nama_admin = input("Masukkan Nama Admin: "): Baris ini meminta pengguna untuk memasukkan nama admin dan disimpan di variabel nama_admin.
- email_admin = input("Masukkan Email Admin: "): Baris ini meminta pengguna untuk memasukkan email admin dan disimpan di variabel email_admin.
- password_admin = input("Masukkan Password Admin: "): Baris ini meminta pengguna untuk memasukkan password admin dan disimpan di variabel password_admin.
- role = input("Masukkan Role Admin: "): Baris ini meminta pengguna untuk memasukkan role admin dan disimpan di variabel role.
- query = f""": Baris ini memulai pembuatan string query SQL menggunakan f-string.
- INSERT INTO admin (nama_admin, email_admin, password_admin, role) VALUES ('{nama_admin}', '{email_admin}', '{password_admin}', '{role}'): Bagian ini berisi query SQL untuk menambahkan data admin baru ke tabel admin. Nilai-nilai yang dimasukkan (nama_admin, email_admin, password_admin, role) diambil dari variabel yang sudah diinput sebelumnya.
- """: Baris ini menutup pembuatan string query SQL.
- mycursor.execute(query): Baris ini menjalankan query SQL yang telah dibuat sebelumnya pada database. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- mydb.commit(): Baris ini melakukan komit perubahan ke database. Artinya, data admin baru yang ditambahkan akan disimpan secara permanen.
- print("Data Admin berhasil ditambahkan"): Baris ini mencetak pesan ke konsol untuk memberitahu pengguna bahwa data admin telah berhasil ditambahkan.
- except Error as e:: Blok ini akan dieksekusi jika terjadi kesalahan (exception) selama proses penambahan data admin.
- print("Error saat menambahkan data admin:", e): Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/14.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama hapus_data_admin kemungkinan untuk menghapus data admin dari database berdasarkan ID.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- try:: Blok ini digunakan untuk mencoba menjalankan code di dalamnya. Jika terjadi kesalahan, blok except akan menangani.
- id_admin = int(input("Masukkan ID Admin yang ingin dihapus: ")): Baris ini meminta pengguna untuk memasukkan ID admin yang ingin dihapus. input akan mengembalikan string, sehingga dilakukan konversi ke integer menggunakan int() untuk memastikan ID berupa angka.
- query = f"DELETE FROM admin WHERE id_admin = {id_admin}": Baris ini membuat query SQL untuk menghapus data admin dari tabel admin. Query tersebut akan mencari record yang memiliki id_admin sesuai dengan nilai yang dimasukkan pengguna (id_admin).
- mycursor.execute(query): Baris ini menjalankan query SQL yang telah dibuat sebelumnya pada database. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- mydb.commit(): Baris ini melakukan komit perubahan ke database. Artinya, penghapusan data admin akan disimpan secara permanen.
- print("Data Admin berhasil dihapus"): Baris ini mencetak pesan ke konsol untuk memberitahu pengguna bahwa data admin telah berhasil dihapus.
- except ValueError:: Blok ini akan dieksekusi jika terjadi kesalahan ValueError selama konversi input ID admin menjadi integer. ValueError biasanya muncul ketika pengguna memasukkan input yang bukan angka.
  - print("Masukkan ID Admin yang valid."): Baris ini menampilkan pesan kepada pengguna untuk memasukkan ID admin yang valid (berupa angka).
- except Error as e:: Blok ini akan dieksekusi jika terjadi kesalahan (exception) lain selama proses penghapusan data admin.
  - print("Error saat menghapus data admin:", e): Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/15.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama perbarui_data_admin untuk memperbarui data admin di database.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- try:: Blok ini digunakan untuk mencoba menjalankan code di dalamnya. Jika terjadi kesalahan, blok except akan menangani.
- id_admin = int(input("Masukkan ID Admin yang ingin diperbarui: ")): Baris ini meminta pengguna untuk memasukkan ID admin yang ingin diperbarui. Input dikonversi ke integer menggunakan int() untuk memastikan ID berupa angka.
- nama_admin = input("Masukkan Nama Admin Baru: "): Baris ini meminta pengguna untuk memasukkan nama admin baru.
- email_admin = input("Masukkan Email Admin Baru: "): Baris ini meminta pengguna untuk memasukkan email admin baru.
- password_admin = input("Masukkan Password Admin Baru: "): Baris ini meminta pengguna untuk memasukkan password admin baru.
- role = input("Masukkan Role Admin Baru: "): Baris ini meminta pengguna untuk memasukkan role admin baru.
- query = f""": Baris ini memulai pembuatan string query SQL menggunakan f-string.
- UPDATE admin: Bagian ini menunjukkan bahwa query akan melakukan update pada tabel admin.
- SET nama_admin = '{nama_admin}', email_admin = '{email_admin}', password_admin = '{password_admin}', role = '{role}': Bagian ini berisi daftar kolom yang akan diperbarui beserta nilai barunya. Nilai-nilai baru diambil dari variabel yang sudah diinput sebelumnya.
- WHERE id_admin = {id_admin}: Bagian ini menentukan kondisi WHERE untuk memperbarui hanya record yang memiliki id_admin sesuai dengan ID yang dimasukkan pengguna.
- """: Baris ini menutup pembuatan string query SQL.
- mycursor.execute(query): Baris ini menjalankan query SQL yang telah dibuat sebelumnya pada database. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- if mycursor.rowcount == 0:: Blok ini mengecek apakah ada record yang diperbarui dengan menggunakan mycursor.rowcount. rowcount akan mengembalikan jumlah record yang terpengaruh oleh query.
  - print("ID Admin tidak ditemukan."): Jika rowcount 0, berarti tidak ada record yang ditemukan dengan ID yang diberikan, dan pesan ini akan dicetak ke konsol.
- else:: Blok ini dijalankan jika ada record yang diperbarui (karena rowcount > 0).
  - mydb.commit(): Baris ini melakukan komit perubahan ke database. Artinya, pembaruan data admin akan disimpan secara permanen.
  - print("Data Admin berhasil diperbarui"): Baris ini mencetak pesan ke konsol untuk memberitahu pengguna bahwa data admin telah berhasil diperbarui.
- except ValueError:: Blok ini akan dieksekusi jika terjadi kesalahan ValueError selama konversi input ID admin atau input data lainnya ke format yang sesuai.
  - print("Masukkan ID Admin dalam bentuk bilangan bulat."): Baris ini menampilkan pesan kepada pengguna untuk memasukkan ID admin dalam bentuk bilangan bulat (jika terjadi error konversi ID admin).
- except Exception as e:: Blok ini akan dieksekusi jika terjadi kesalahan (exception) lain selama proses pembaruan data admin.
  - print("Terjadi kesalahan:", e): Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/16.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama read_perkotaan kemungkinan untuk membaca dan menampilkan data perkotaan dari database.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- Class LinkedList dan fungsi quick_sort dan jump_search telah didefinisikan sebelumnya.
- mycursor.execute("SELECT * FROM perkotaan"): Baris ini menjalankan query SQL untuk mengambil semua data dari tabel perkotaan.
- myresult = mycursor.fetchall(): Baris ini mengambil semua hasil query yang dikembalikan oleh database dan disimpan di variabel myresult. Diasumsikan myresult berupa list yang berisi record-record data perkotaan.
- data_list = []: Baris ini membuat list kosong bernama data_list untuk menyimpan data perkotaan.
- for data in myresult:: Perulangan for ini iterasi melalui setiap record data perkotaan di myresult.
  - data_list.append(data): Di dalam perulangan, setiap record data perkotaan (data) ditambahkan ke list data_list.
- while True:: Perulangan while True ini membuat menu interaktif terus berjalan sampai pengguna memilih untuk kembali ke menu utama.
  - print("============================================================"): Baris ini mencetak garis pemisah untuk membatasi bagian menu.
  - print("|                 TAMPILKAN DATA PERKOTAAN                 |"): Baris ini mencetak judul menu.
  - print("============================================================"): Baris ini mencetak garis pemisah lagi.
  - print("|   1. Tampilkan Data (urutkan berdasarkan ID - A-Z)       |"): Baris ini menampilkan pilihan menu 1.
  - print("|   2. Tampilkan Data (urutkan berdasarkan ID - Z-A)       |"): Baris ini menampilkan pilihan menu 2.
  - print("|   3. Cari Data (berdasarkan ID)                          |"): Baris ini menampilkan pilihan menu 3.
  - print("|   4. Kembali ke Menu Utama                               |"): Baris ini menampilkan pilihan menu 4.
  - print("============================================================"): Baris ini mencetak garis pemisah lagi.
  - pilihan = input("Masukkan pilihan Anda: "): Baris ini meminta pengguna untuk memasukkan pilihan mereka.
- if pilihan == "1":: Blok ini dijalankan jika pengguna memilih menu 1.
  - sorted_data = quick_sort(data_list, ascending=True): Baris ini mengurutkan data di data_list secara ascending (dari kecil ke besar) menggunakan fungsi quick_sort.
  - ll = LinkedList(): Baris ini membuat objek baru dari class LinkedList dan disimpan di variabel ll.
  - for data in sorted_data:: Perulangan for ini iterasi melalui data yang sudah diurutkan (sorted_data).
  - ll.append(data): Di dalam perulangan, setiap data di sorted_data ditambahkan ke linked list ll.
  - ll.display_perkotaan(): Baris ini memanggil fungsi display_perkotaan dari objek ll untuk menampilkan data perkotaan yang sudah diurutkan.
-  elif pilihan == "2":: Blok ini dijalankan jika pengguna memilih menu 2.
  - sorted_data = quick_sort(data_list, ascending=False): Baris ini mengurutkan data di data_list secara descending (dari besar ke kecil) menggunakan fungsi quick_sort.
  - ll = LinkedList(): Baris ini membuat objek baru dari class LinkedList dan disimpan di variabel ll.
  - for data in sorted_data:: Perulangan for ini iterasi melalui data yang sudah diurutkan (sorted_data).
- elif pilihan == "3":: Blok ini dijalankan jika pengguna memilih menu 3 (pencarian data).
  - id_to_search = int(input("Masukkan ID yang ingin dicari: "))**: Baris ini meminta pengguna untuk memasukkan ID yang ingin dicari. Input dikonversi ke integer menggunakan int() untuk memastikan ID berupa angka.
  - result_index = jump_search(data_list, id_to_search)**: Baris ini menggunakan fungsi jump_search untuk mencari data dengan ID yang dimasukkan dalam list data_list. jump_search mengembalikan indeks data yang ditemukan (atau -1 jika tidak ditemukan).
  - if result_index != -1:**: Blok ini dijalankan jika data ditemukan (karena result_index bukan -1).
   - print("Data ditemukan:")**: Baris ini mencetak pesan bahwa data ditemukan.
   - x = PrettyTable()**: Baris ini membuat objek PrettyTable untuk menampilkan data dengan format tabel yang rapi.
   - x.field_names = ["ID", "Nama Kota", "Provinsi", "Jumlah Penduduk", "Luas Wilayah", "Indeks Keberlanjutan", "ID ADMIN"]**: Baris ini menentukan nama-nama kolom yang akan ditampilkan di tabel.
   - x.add_row(data_list[result_index])**: Baris ini menambahkan data yang ditemukan (pada indeks result_index) ke tabel PrettyTable.
   - print(x)**: Baris ini mencetak tabel PrettyTable yang berisi data yang ditemukan.
  - else:**: Blok ini dijalankan jika data tidak ditemukan (karena result_index = -1).
   - print("Data tidak ditemukan.")**: Baris ini mencetak pesan bahwa data tidak ditemukan.
- elif pilihan == "4":: Blok ini dijalankan jika pengguna memilih menu 4 (kembali ke menu utama).
  - break**: Kata kunci break digunakan untuk keluar dari perulangan while True dan kembali ke menu utama.
- else:: Blok ini dijalankan jika pengguna memasukkan pilihan yang tidak valid.
  - print("Pilihan tidak valid. Silakan pilih kembali.")**: Baris ini mencetak pesan bahwa pilihan yang dimasukkan tidak valid dan meminta pengguna untuk memilih kembali.
- except ValueError:: Blok ini dijalankan jika terjadi error ValueError selama konversi input (misalnya pengguna memasukkan ID yang bukan angka).
  - print("Input tidak valid.")**: Baris ini mencetak pesan bahwa input yang dimasukkan tidak valid.
- except Error as e:: Blok ini dijalankan jika terjadi error (exception) lain selama proses program.
  - print("Error saat membaca data perkotaan:", e)**: Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/17.png?raw=true)


