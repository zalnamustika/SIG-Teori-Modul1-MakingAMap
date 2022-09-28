# Making A Map (membuat sebuah Peta)

Tutorial kali ini menunjukkan cara membuat peta Jambi dengan elemen peta standar seperti inset peta, kisi, panah utara, bilah skala, dan label.

## Data 
Saya Menggunakan Natural Earth dataset, dilengkapi dengan lapisan global bergaya indah yang dapat dimuat langsung ke QGIS.

Unduh Natural Earth Quickstart Kit [disini](https://naciscdn.org/naturalearth/packages/Natural_Earth_quick_start.zip)

## Prosedur

1. Unduh dan Natural Earth Quickstart Kit. Buka QGIS. Temukan folder di panel Browser . Perluas folder untuk menemukan proyek. Ini adalah file proyek yang berisi lapisan bergaya dalam format Dokumen QGIS. Klik dua kali proyek untuk membukanya.Natural Earth quick startNatural_Earth_quick_start_for_QGIS_v3

2. Kita mungkin memperhatikan bahwa peta memiliki label dalam bahasa Yunani. Proyek ini menggunakan variabel untuk mengatur bahasa. Kita dapat mengubah variabel dengan masuk ke Project Properties.

-------

Catatan:

Variabel proyek adalah cara yang bagus untuk menyimpan nilai spesifik proyek untuk digunakan di mana pun Anda dapat menggunakan ekspresi di QGIS. Proyek Natural_Earth_quick_start_for_QGIS_v3ini dilengkapi dengan banyak variabel prasetel yang digunakan untuk penataan gaya dalam proyek itu.

-------

3. Beralih ke tab Variabel dalam dialog Properti Proyek . Cari project_languagevariabel dan klik pada kolom Nilai untuk mengeditnya. Ubah bahasa menjadi name_endan klik OK .

4. Kembali ke jendela utama QGIS, klik tombol Refresh di Map Navigation Toolbar . Anda sekarang akan melihat peta yang dirender dengan label bahasa Inggris.

5. Gunakan kontrol geser dan zoom di Bilah Alat Navigasi Peta dan perbesar ke Indonesi, Jambi.

6. kita dapat menonaktifkan beberapa lapisan peta untuk data yang tidak kami perlukan untuk peta ini. Perluas folder dan hapus centang pada kotak di sebelah dan lapisan. Sebelum kita membuat peta yang cocok untuk dicetak, kita perlu memilih proyeksi yang sesuai. CRS default untuk proyek diatur ke.Ini adalah CRS yang populer digunakan untuk pemetaan web dan merupakan pilihan yang layak untuk tujuan kita, sehingga kita dapat membiarkannya pada nilai defaultnya. Pergi ke Proyek Tata Letak Cetak Baru .z5-1:18mne_10m_geography_marine_polysne_10m_admin_0_disputed_areasEPSG:3857 Pseudo-Mercator

-------

Catatan:
Untuk Jambi, jambi Plane Rectangular CS adalah sistem referensi koordinat yang diproyeksikan (CRS) yang dirancang untuk distorsi minimum. Ini dibagi dalam 18 zona dan jika Anda bekerja untuk wilayah yang lebih kecil di jambi,menggunakan CRS ini akan lebih baik.

-------

7.Anda akan diminta untuk memasukkan judul untuk tata letak. Anda dapat membiarkannya kosong dan klik Ok.

---------

Catatan:
Membiarkan nama tata letak kosong akan menetapkan nama default seperti .Layout 1

---------

8. Di jendela Print Layout, klik tombol Zoom full untuk menampilkan seluruh Layout.

9. Sekarang kita harus membawa tampilan peta yang kita lihat di Kanvas QGIS ke tata letak. Pergi ke Tambah Item Tambah Peta .

10. Setelah mode Tambah Peta aktif, tahan tombol kiri mouse dan seret persegi panjang di mana Anda ingin menyisipkan peta.

11. Kita akan melihat bahwa jendela persegi panjang akan ditampilkan dengan peta dari kanvas QGIS utama. Peta yang diberikan mungkin tidak mencakup seluruh area minat kami. Gunakan opsi Edit Pilih/Pindahkan item dan Edit Pindahkan Konten untuk menggeser peta di jendela dan memusatkannya di komposer.

12. Mari kita juga menyesuaikan tingkat zoom untuk peta. Klik pada tab Item Properties dan masukkan 10000000sebagai nilai Scale.

13. Sekarang kita akan menambahkan inset peta yang menunjukkan tampilan yang diperbesar untuk area jambi. Sebelum kita membuat perubahan pada lapisan di jendela utama QGIS, centang kotak Kunci lapisan dan Gaya kunci untuk lapisan . Ini akan memastikan bahwa jika kita mematikan beberapa lapisan atau mengubah gayanya, tampilan ini tidak akan berubah.

14. Beralih ke jendela QGIS utama. Matikan grup layer dan aktifkan grup. Grup lapisan ini memiliki gaya yang lebih sesuai untuk tampilan yang diperbesar. Gunakan kontrol pan dan zoom di Map Navigation Toolbar dan zoom di sekitar Tokyo.z5 - 1:18mz7 - 1: 4m.

15. Kami sekarang siap untuk menambahkan inset peta. Ganti jendela Print Layout . Pergi ke Tambah Item Tambah Peta .

16. Seret persegi panjang di tempat Anda ingin menambahkan inset peta. Anda sekarang akan melihat bahwa kami memiliki 2 objek peta di Tata Letak Cetak. Saat membuat perubahan, pastikan Anda memilih peta yang benar.

17. Pilih objek yang baru saja kita tambahkan dari panel Items . Pilih tab Properti item . Gulir ke bawah ke panel Frame dan centang kotak di sebelahnya. Anda dapat mengubah warna dan ketebalan batas bingkai sehingga mudah dibedakan dengan latar belakang peta.Map 2

18. Salah satu fitur rapi dari Tata Letak Cetak adalah ia dapat secara otomatis menyorot area dari peta utama yang diwakili di sisipan. Pilih objek dari panel Item . Di tab Properti item , gulir ke bawah ke bagian Ikhtisar . Klik tombol Tambahkan ikhtisar baru .Map 1

19. Pilih sebagai Bingkai Peta . Ini memberitahu Tata Letak Cetak untuk menyorot objek saat ini dengan tingkat peta yang ditampilkan di objek.Map 2Map 1Map 2

20. Sekarang setelah kita menyiapkan inset peta, kita akan menambahkan grid ke peta utama. Pilih objek dari panel Item . Di tab Properti item , gulir ke bawah ke bagian Kisi . Klik tombol Add a new grid , diikuti dengan Modify grid... .Map 1

21. Secara default, garis kisi menggunakan unit dan proyeksi yang sama dengan proyeksi peta yang dipilih saat ini. Namun, lebih umum dan berguna untuk menampilkan garis kisi dalam derajat. Kita dapat memilih CRS yang berbeda untuk grid. Klik tombol Ubah... di sebelah CRS .

22. Dalam dialog Pemilih Sistem Referensi Koordinasi4326 , masukkan dalam kotak Filter . Dari hasil, pilih sebagai CRS. Klik Oke .WGS84 EPSG:4326

23. Pilih nilai Interval sebagai 5derajat dalam arah X dan Y. Anda dapat menyesuaikan Offset untuk mengubah tempat munculnya garis kisi.

24. Gulir ke bawah ke bagian Bingkai kisi dan centang kotak Gambar koordinat . Format defaultnya adalah Degreestetapi muncul sebagai angka. Kita dapat menyesuaikan adalah dengan menambahkan simbol °. Pilih Customdan klik tombol Ekspresi di sebelahnya.

25. Masukkan ekspresi berikut untuk membuat string yang mengambil nomor grid dan menambahkan simbol ° ke dalamnya.
concat(to_string(@grid_number), '°    ')

26. Perhatikan bahwa kisi sekarang memiliki label khusus dari ekspresi. Sesuaikan pengaturan posisi untuk Kiri , Kanan , Atas dan Bawah sesuai keinginan Anda.

27. Sekarang kita akan menambahkan bingkai Rectangluar untuk menampung elemen peta lainnya seperti panah utara, skala, dan label. Pergi ke Add Item Add Shape Add Rectangle .

28. Kita dapat mengubah Gaya persegi panjang agar sesuai dengan latar belakang peta.

29. Sekarang kita akan menambahkan Panah Utara ke peta. QGIS hadir dengan koleksi gambar terkait peta yang bagus - termasuk banyak jenis Panah Utara. Klik Tambah Item Tambah Gambar .

30. Sambil menahan tombol kiri mouse Anda, gambarlah sebuah persegi panjang. Di panel sebelah kanan, klik pada tab Item Properties dan perluas bagian Search directory dan pilih gambar yang Kita sukai

31. Sekarang kita akan menambahkan bilah skala. Klik Add Item Add Scalebar.

32. Klik pada tata letak tempat Anda ingin bilah skala muncul. Di tab Properti Item , pastikan Anda telah memilih elemen peta yang benar untuk menampilkan bilah skala. Pilih Gaya yang sesuai dengan kebutuhan Anda. Di panel Segmen , ubah Lebar tetap menjadi satuan dan sesuaikan segmen sesuai keinginan Anda.Map 1200

33. Saatnya memberi label pada peta kita. Klik Tambah Item Tambah Label .

34. Klik pada peta dan gambar kotak di mana label seharusnya berada. Di tab Properti Item , perluas bagian Label dan masukkan label untuk peta. Demikian pula, tambahkan label lain untuk data dan kredit perangkat lunak.

35. Setelah Anda puas dengan peta, Anda dapat mengekspornya sebagai Gambar, PDF, atau SVG. Untuk tutorial ini, mari kita ekspor sebagai gambar. Klik Tata Letak Ekspor sebagai Gambar .

36. Simpan gambar dalam format yang Anda sukai. Di bawah ini adalah gambar PNG yang diekspor.

Lihat Gambar file.PNG [disini](https://github.com/zalnamustika11/SIG-Teori-Modul1-MakingAMap/blob/main/PetaJambi.png)

Lihat Hasil file.qpt [disini](https://github.com/zalnamustika11/SIG-Teori-Modul1-MakingAMap/blob/main/PetaJambi.qpt)



