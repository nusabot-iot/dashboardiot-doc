# Pengenalan
> Dokumentasi / manual penggunaan ini diperuntukan bagi para pengembang yang menggunakan Dashboard IoT by Nusabot. Bagi para pengembang yang membuat proyek IoT bagi klien masing-masing maka perlu membuat manual penggunaan sendiri terkait dengan proyek yang dibuat.

Dashboard adalah platform IoT yang diperuntukan bagi para developer IoT khusus nya pemula untuk membuat prototype sampai dengan mempublikasikannya sebagai produk jadi. Dashboard dapat menampilkan data sensor dan mengendalikan aktuator secara *realtime* melalui jaringan internet dimanapun dengan menggunakan protokol MQTT.

Dengan menggunakan Dasboard, siapapun bisa membuat perangkat IoT tanpa harus bersusah payah menyiapkan infrastruktur IoT nya.

Anda bisa mengundang rekan tim Anda dengan jumlah personil tak terbatas untuk bersama membuat proyek di Dashboard sehingga proyek dapat dikerjakan bersama.

Proyek yang sudah dibuat dengan Dashboard siap untuk Anda publikasikan bagi *end-user*. Baik itu anggota keluarga, karyawan Anda, atau seseorang yang telah membayar untuk membeli produk Anda. Kami tidak memberikan batasan jumlah pengguna proyek yang sudah Anda buat di Dashboard.

## Memulai Cepat
> Dashboard memiliki 2 URL yang dapat Anda gunakan, keduanya memiliki fungsi yang berbeda.
>
> https://iot.nusabot.id sebagai tempat untuk Anda membuat dan mengatur proyek
>
> https://dashboard.nusabot.com sebagai URL yang dapat Anda bagikan kepada pengguna proyek Anda. Proyek yang sudah dibuat dapat digunakan melalui link ini.



Untuk dapat membuat proyek menggunakan Dashboard, Anda bisa membuat akun baru terlebih dahulu.

https://iot.nusabot.id/login

![register](https://github.com/nusabot-iot/dashboardiot-doc/blob/master/docs/register.png?raw=true)

Setelah berhasil membuat akun maka Anda bisa langsung *login* menggunakan akun tersebut.

# Langkah Selanjutnya

Selamat, Anda telah berhasil membuat akun Dashboard, disini Anda bisa mengatur proyek dengan Dashboard.

Dashboard menggunakan sistem yang kami sebut dengan **Token**. Dimana token ini adalah saldo yang terdapat pada akun Anda. Token ini digunakan untuk **menampilkan** data dari perangkat keras IoT Anda (misalnya sensor) maupun untuk **mengendalikan** aktuator dan *display* pada perangkat keras IoT Anda (misalnya Servo dan LCD). Semakin banyak data yang ingin Anda tampilkan, maka semakin banyak juga Token yang dibutuhkan. Begitu juga untuk mengendalikan aktuator.

Token terbagi menjadi 2 jenis.

| Jenis Token  | Penjelasan                                                   |
| ------------ | ------------------------------------------------------------ |
| Token Akun   | Token yang dimiliki oleh setiap akun di Dashboard.<br />Token ini dapat diubah menjadi Token Proyek maupun ditransfer ke akun lain.<br />Token akun tidak dapat digunakan oleh akun lain kecuali melakukan transfer token. |
| Token Proyek | Token yang terdapat pada setiap proyek yang dibuat.<br />Token ini dapat diubah menjadi Token Akun dan dapat digunakan oleh seluruh akun personil tim yang terlibat pada pembuatan proyek, namun jika token ini ingin diubah menjadi Token Akun maka hanya bisa dijadikan Token Akun pemilik proyek yang bersangkutan.<br />Token ini yang akan berkurang seiring dengan banyaknya tampilan untuk mengambil data dan mengirim data. |

Selain Token, pada Dashboard juga Anda perlu mengenal komponen lain yaitu **Proyek, Halaman, dan Widget**.

## Proyek

Proyek adalah aplikasi yang ingin Anda buat menggunakan Dashboard. Bayangkan Anda memiliki 2 (dua) klien dimana masing-masing klien ingin dibuatkan sistem yang berbeda.

> Klien A ingin dibuatkan sistem pemantau suhu di semua gudang milik perusahaannya.
>
> Klien B ingin dibuatkan sistem penyiram taman di seluruh taman yang ada di Kota Jakarta.

Maka Anda perlu membuat 2 (dua) buah proyek. Proyek pertama untuk klien A dan proyek kedua untuk klien B.

> **Dashboard tidak membatasi jumlah proyek yang dapat dibuat. Untuk membuat proyek, Token TIDAK AKAN dikurangi.**



## Halaman

Halaman adalah segmentasi atau bisa dikatakan sebagai sub-proyek. Setiap halaman dapat menampilkan data yang beragam sesuai kebutuhan sekaligus dapat menampilkan tombol sebagai input untuk mengendalikan aktuator.

Kita ambil contoh pada klien A yang ingin dibuatkan sistem pemantau suhu di semua gudang milik perusahaannya. Ternyata klien A memiliki 10 gudang yang tersebar di seluruh Indonesia, maka Anda bisa membuat 10 halaman dimana setiap halaman akan berisi informasi mengenai suhu dari 1 (satu) gudang. Jika dibutuhkan, Anda juga bisa menampilkan data lain sesuai sensor dan aktuator yang ingin digunakan di setiap gudang nya.

> **Dashboard tidak membatasi jumlah halaman yang dapat dibuat. Untuk membuat halaman, Token TIDAK AKAN dikurangi.**



## Widget

Widget adalah sebuah objek yang dapat digunakan untuk menampilkan data maupun untuk mengirim data. Satu halaman dapat berisi banyak Widget, setiap widget yang Anda buat maka akan mengurangi saldo Token Proyek sesuai dengan jumlah token yang dibutuhkan pada setiap widget.

Jika proyek Anda kekurangan token, maka Anda dapat mengubah Token Akun Anda menjadi Token Proyek.

> **Hanya pemilik proyek yang dapat mengubah Token Proyek menjadi Token Akun dan sebaliknya**



## Skema Penggunaan Dashboard

Setelah Anda mengetahui mengenai konsep pada Dashboard, maka dapat disimpulkan melalui diagram berikut.



# Sidebar

![sidebar](https://github.com/nusabot-iot/dashboardiot-doc/blob/master/docs/sidebar.png?raw=true)

Saat Anda berhasil masuk maka Anda akan melihat sidebar di sebelah kiri. Disini adalah tempat Anda melakukan navigasi ke berbagai fasilitas yang ada pada Dashboard.



# Proyek

![Sidebar Proyek](https://github.com/nusabot-iot/dashboardiot-doc/blob/master/docs/proyek-sidebar.png?raw=true)

## Atur Proyek

Pada menu ini Anda bisa membuat proyek dan mengatur seluruh proyek milik Anda. Untuk menambahkan proyek baru Anda bisa meng-klik tombol ```Klik Untuk Membuat Proyek Baru```

| Nama Masukan    | Keterangan                                                   | Nilai              | Wajib |
| --------------- | ------------------------------------------------------------ | ------------------ | ----- |
| Nama Proyek     | Nama dari proyek yang akan dibuat                            | Teks               | Ya    |
| Status Proyek   | Status dari proyek yang akan dibuat. Jika memilih ```Privat```maka untuk dapat menggunakan proyek klien Anda harus melakukan login terlebih dahulu, namun tidak dengan ```Publik``` dimana siapapun dapat menggunakan proyek yang Anda buat. | Publik<br />Privat | Ya    |
| Deskripsi       | Sebagai penjelasan singkat tentang proyek yang dibuat agar lebih mudah diingat dan dipahami terutama oleh personil tim. | Teks               | Tidak |
| Kategori Proyek | Anda dapat mengkategorikan setiap proyek yang dibuat baik berdasarkan nama klien, jenis proyek, atau apapun terserah Anda. Kategori proyek untuk memudahkan Anda mencari proyek mana yang akan diatur. | Teks               | Ya    |
| Ikon            | Ikon dari proyek Anda menggunakan Font Awesome yang dapat dipilih [disini](https://fontawesome.com/search?m=free). | Teks               | Tidak |
| MQTT Broker     | Broker dari MQTT yang ingin digunakan untuk proyek ini. Broker yang digunakan harus memiliki fitur Websocket over TLS (wss://). Anda dapat menggunakan broker yang direkomendasikan oleh Dashboard. | Teks               | Ya    |
| Port Websocket  | Port dari websocket broker.                                  | Angka              | Ya    |
| Path            | Path dari websocket broker.                                  | Teks               | Tidak |
| Username        | Username broker.                                             | Teks               | Tidak |
| Password        | Password broker.                                             | Teks               | Tidak |
| Kolaborator     | Daftar seluruh kolaborator dari proyek. Kolaborator adalah akun yang memiliki akses untuk membuat halaman dan widget pada proyek. Biasanya kolaborator adalah personil tim Anda.<br /><br />Anda bisa menambahkan sebanyak apapun kolaborator dengan mengetikan alamat email nya dan dipisahkan dengan koma. Pastikan alamat email sudah terdaftar pada platform Dashboard. | Teks               | Tidak |
| Pengguna        | Daftar seluruh pengguna dari proyek. Pengguna adalah akun yang memiliki akses untuk menggunakan proyek Anda. Biasanya penggunakan adalah klien Anda.<br /><br />Anda bisa menambahkan sebanyak apapun pengguna dengan mengetikan alamat email nya dan dipisahkan dengan koma. Pastikan alamat email sudah terdaftar pada platform Dashboard. | Teks               | Tidak |

Setelah membuat proyek maka Anda bisa melihat seluruh proyek yang sudah dibuat.

![proyek](https://github.com/nusabot-iot/dashboardiot-doc/blob/master/docs/proyek.png?raw=true)

Sekarang Anda bisa melihat pada sidebar seluruh proyek yang sudah dibuat. Klik pada proyek tersebut untuk mengatur proyek Anda seperti menambahkan halaman dan mengatur widget.



## Atur Halaman

Untuk mengatur halaman yang ada pada proyek, Anda perlu membuka menu ```Proyek Kamu``` yang ada pada sidebar lalu pilih proyek yang ingin diatur. Pada saat proyek baru dibuat, maka Token Proyek berjumlah 0. Anda harus menambahkan token proyek dengan cara mengklik tombol ```Tambah Token Proyek```, Dashboard akan melakukan konversi dari Token Akun menjadi Token Proyek sesuai dengan jumlah yang diinputkan.

Anda juga dapat mengurangi Token Proyek dengan cara mengklik tombol ```Ambil Token Proyek```. Dashboard akan melakukan konversi dari Token Proyek menjadi Token Akun sesuai dengan jumlah yang diinputkan.

Untuk menambah halaman dapat dilakukan dengan mengklik tombol ```Klik Untuk Tambah Laman Baru```

| Nama Masukan        | Keterangan                                                   | Wajib |
| ------------------- | ------------------------------------------------------------ | ----- |
| Judul Laman         | Nama dari laman yang akan digunakan, Judul Laman akan ditampilkan pada aplikasi yang diakses oleh end-user atau klien Anda. | Ya    |
| Subscribe Topic     | Topic dari MQTT yang akan disubscribe. Akan menggunakan single level wildcard pada akhir path dari topic. Seluruh data yang akan ditampilkan pada halaman ini akan menggunakan masukan ini. | Ya    |
| Deskripsi           | Sebagai penjelasan singkat tentang halamanyang dibuat agar lebih mudah diingat dan dipahami terutama oleh personil tim. | Tidak |
| Urutan Posisi Laman | Daftar halaman pada tampilan end-user akan diurutkan posisi nya berdasarkan masukan ini. Halaman dengan angka Urutan Posisi Laman terkecil akan ditampilkan paling atas. | Ya    |
| Ikon                | Ikon dari halaman menggunakan Font Awesome yang dapat dipilih [disini](https://fontawesome.com/search?m=free). | Tidak |

 Setelah membuat halaman maka Anda bisa melihat seluruh halaman yang sudah dibuat.

![laman](https://github.com/nusabot-iot/dashboardiot-doc/blob/master/docs/laman.png?raw=true)

> Untuk menghapus halaman Anda harus menghapus terlebih dahulu seluruh widget yang ada pada halaman tersebut.



## Atur Widget

Anda bisa mengklik tombol atur widget yang ada pada halaman. Disini Anda bisa menambah dan menghapus widget. Untuk menambah widget maka perlu mengklik tombol ```Tambah```.

| Nama Masukan | Keterangan                                                   | Wajib |
| ------------ | ------------------------------------------------------------ | ----- |
| Nama Widget  | Sebagai indentifier setiap widget untuk memudahkan Anda dan personil tim mengetahui widget tersebut akan digunakan untuk mengambil data apa atau untuk mengirim data apa. | Ya    |
| Judul Widget | Judul widget akan tampil pada sisi end-user. Judul widget memudahkan end-user untuk mengetahui widget ini digunakan untuk menampilkan data apa. | Ya    |
| Jenis Widget | Pilihan jenis widget yang ingin digunakan untuk menampilkan atau mengirim data. | Ya    |











# Jenis Widget

## Kotak

![kotak](https://github.com/nusabot-iot/dashboardiot-doc/blob/master/docs/kotak.png?raw=true)

**Konsumsi Token: 100**

Menampilkan data dari topik tertentu.

| Properti                 | Keterangan                                                   | Wajib |
| ------------------------ | ------------------------------------------------------------ | ----- |
| Urutan / Prioritas       | Widget akan ditampilkan pada setiap halaman, widget dengan nilai urutan / prioritas terkecil akan ditampilkan terlebih dahulu pada halaman. | Ya    |
| Ukuran                   | Lebar dari widget yang dipilih.                              | Ya    |
| Subscribe                | Topik yang akan digunakan oleh widget untuk menampilkan data. Diawali dengan topik yang sudah diinputkan pada proyek sebelumnya. | Ya    |
| Satuan Unit              | Satuan yang akan ditampilkan setelah data. Sebagai contoh widget akan digunakan untuk menampilkan data suhu gudang maka satuan unit bisa diisi dengan ºC. | Tidak |
| Warna                    | Warna dari widget yang ingin digunakan.                      | Ya    |
| Ikon                     | Ikon dari widgetmenggunakan Font Awesome yang dapat dipilih [disini](https://fontawesome.com/search?m=free). | Tidak |
| Quality of Service (QoS) | QoS yang akan digunakan untuk melakukan subscribe widget ini. | Ya    |



## Info

![Info](https://github.com/nusabot-iot/dashboardiot-doc/blob/master/docs/info.png?raw=true)

**Konsumsi Token: 100**

Menampilkan data dari topik tertentu.

| Properti                 | Keterangan                                                   | Wajib |
| ------------------------ | ------------------------------------------------------------ | ----- |
| Urutan / Prioritas       | Widget akan ditampilkan pada setiap halaman, widget dengan nilai urutan / prioritas terkecil akan ditampilkan terlebih dahulu pada halaman. | Ya    |
| Ukuran                   | Lebar dari widget yang dipilih.                              | Ya    |
| Subscribe                | Topik yang akan digunakan oleh widget untuk menampilkan data. Diawali dengan topik yang sudah diinputkan pada proyek sebelumnya. | Ya    |
| Satuan Unit              | Satuan yang akan ditampilkan setelah data. Sebagai contoh widget akan digunakan untuk menampilkan data suhu gudang maka satuan unit bisa diisi dengan ºC. | Tidak |
| Warna                    | Warna dari widget yang ingin digunakan.                      | Ya    |
| Ikon                     | Ikon dari widgetmenggunakan Font Awesome yang dapat dipilih [disini](https://fontawesome.com/search?m=free). | Tidak |
| Quality of Service (QoS) | QoS yang akan digunakan untuk melakukan subscribe widget ini. | Ya    |

## Tombol Switch

![Tombol Switch](https://github.com/nusabot-iot/dashboardiot-doc/blob/master/docs/tombol-switch.png?raw=true)

**Konsumsi Token: 150**

Mengirimkan data dari topik tertentu berupa tombol.

| Properti                 | Keterangan                                                   | Wajib |
| ------------------------ | ------------------------------------------------------------ | ----- |
| Urutan / Prioritas       | Widget akan ditampilkan pada setiap halaman, widget dengan nilai urutan / prioritas terkecil akan ditampilkan terlebih dahulu pada halaman. | Ya    |
| Ukuran                   | Lebar dari widget yang dipilih.                              | Ya    |
| Publish                  | Topik yang akan digunakan oleh widget untuk mengirimkan data. | Ya    |
| Opsi Tombol              | Anda dapat membuat tombol pada widget ini. Sebagai contoh widget ingin digunakan untuk mengendalikan Lampu gudang maka perlu tombol untuk menyalakan lampu dan mematikan lampu. Untuk membuat tombol gunakan format ```topic_1=nilai_1,topic_2=nilai_2,......., topic_n=nilai_n```. Contoh: ```Nyala=1,Mati=0,Otomatis=2```. | Ya    |
| Warna                    | Warna dari widget yang ingin digunakan.                      | Ya    |
| Ikon                     | Ikon dari widgetmenggunakan Font Awesome yang dapat dipilih [disini](https://fontawesome.com/search?m=free). | Tidak |
| Quality of Service (QoS) | QoS yang akan digunakan untuk melakukan subscribe widget ini. | Ya    |



# Deploy

Setelah Anda mengatur proyek, mengatur halaman, serta mengatur widget maka proyek sudah siap dipublikasikan kepada end-user.

>Untuk melihat proyek Anda maka dapat menggunakan format URL berikut:
>
>**```https://dashboard.nusabot.com/{username}/{nama proyek}```**

Jika proyek Anda adalah privat maka pengguna diminta untuk login terlebih dahulu, namun jika proyek adalah publik maka siapapun bisa menggunakannya.

![dashboard](C:\Users\User\OneDrive\Dokumen\dashboardiot-doc\docs\dashboard.png)

Sebelah kiri adalah menu berupa halaman yang ada pada proyek. Widget dari halaman tersebut akan tampil pada bagian tengah layar.

Pojok kiri atas adalah status dari koneksi antara perangkat anda (web browser) dengan broker.

> Status **Terputus** biasanya disebabkan karena kesalahan input data broker pada proyek ataupun ada masalah dengan broker nya. Perangkat Anda langsung terhubung dengan broker tanpa melalui Dashboard, jadi ketika tejadi status Terputus maka kendala bukan timbul dari Dashboard.