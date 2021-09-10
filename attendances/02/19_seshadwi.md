Android Basic XML Layouts
Linear layout merupakan permodelan yang paling umum, mirip dengan Java swing box layout.
Umumnya, desain UI yang kompleks dihasilkan dari kombinasi kotak yang sederhana sehingga menunjukan bagian dalamnya menggunakan orientasi horizontal atau vertical.

Ringkasan container android yang umumnya digunakan:

1. LinearLayout (kotak model)
2. RelativeLayout (model berbasis aturan)
3. Tablelayout (model grid)
4. Scrollview(desain container yang dirancang untuk membantu mengimplementasikan)
5. Lainnya (listview, gridview,webview, mapview)

Layout sederhana dari android dinamakan frame layout
Frame layout sebuah container persegi Panjang
Menambahkan beberapa tampilan pada frame layout hanya menumpuk satu diatas yang lain.

1. Linear layout
   Adalah sebuah kotak model, widget atau anak wadah merupakan garis diatas sebuah kolom.
   Untuk mengetahui linearlayout, ada 5 utama rea untuk control disamping itu terdapat konten- konten:

- Orientasi atau awalan
  Menunjukan apakah linearlayout mewakili baris atau kolom
  Menambahkan property android : orientation ke linearlayout kemudian elemen dalam tata letak XML, atur nilainya menjadi horizontal untuk baris atau vertical untuk kolom.

- Pengisian model
  Widget memiliki ukuran natural berdasarkan pada pesan yang bersamanya.
  Ketika ukuran gabungannya tidak sama persis dengan lebar layer dari perangkat android, mungkin memiliki masalah tentang apa yang harus dilakukan dengan ruang yang tersisa.
  Semua widget dalam sebuah linearlayout harus menyediakan atribut dimensi
  Android: layout_width dan android:layout_height
  Nilai yang terpakai untuk membedakan ukuran dan berat adalah:

1. Spesifikasi sebuah dimensi particular, 125dip
2. Menyediakan wrap content, yang merupakan widget harus terisi oleh ruang yang natural.
3. Menyediakan fill parent, yang merupakan widget harus terisi oleh ruang yang tersedia.

- Berat
  Linear layout : berat ini digunakan untuk menetapkan ruang secara proporsional ke widget dalam tampilan
  Kamu akan mengatur android: layout_weight ke nilai (1,2,3…)
  Untuk menunjukan berapa proporsi ruang kosong yang harus digunakan untuk widget itu.

- Gravitasi
  Digunakan untuk menunjukan bagaimana control akan disejajarkan dilayar
  Secara default, widget diratakan kiri dan atas.
  Dapat menggunakan property XML
  Android:layout_gravity”…”
  Untuk mengatur kemungkinan pengaturan lain : kiri, tengah, kanan, atas , bawah dll
  Perbedaan antara android: gravity dengan android:layout gravity

1. Android gravity
   Menentukan bagaimana menempatkan konten suatu objek pada sumbu x dan y di dalam objek itu sendiri. Android:gravity=”center”
2. Android: layout gravity
   Memposisikan tampilan sehubungan dengan induknya (yaitu yang terkandung dalam tampilan). Android: layout gravity=”center”

- Lapisan
  Padding menentukan berapa banyak ruang yang terdapat diantara batas sel widget dan konten widget yangs sebenarnya.
  Jika ingin menambah spasi internal antara tepi dan isinya, maka akan menggunakan
  Android : padding property
  Atau dengan memanggil setPadding() saat melakukan runtime pada objek Java widget.

1. Linear layout : internal margin menggunakan padding
   Contoh:
   Kotak textedit sudah diganti menjadi display 30dip pada semua padding atau lapisan.
2. Relative layout
   Berada di widget berdasarkan hubungan antara widget dalam container dan induk container.

- Batas
  Secara default, widget dikemas dengan rapat di samping satu sama lain.
  Untuk menambah ruang di antara mereka, gunakan atribut android:layout_margin
- Relative layout
  RelativeLayout menempatkan widget berdasarkan hubungannya dengan widget lain di wadah dan wadah induk.
- Relative layout – mengacu pada wadah
  Tata Letak Relatif - Mengacu pada wadah
  Beberapa properti XML posisi (boolean) yang memetakan widget menurut lokasinya sehubungan dengan tempat induknya.
- Tata Letak Relatif – Mengacu pada widget lain
  Untuk menggunakan Notasi Relatif di Properti, Anda harus secara konsisten:
  Letakkan pengidentifikasi (android:atribut id) pada semua elemen yang perlu Anda tangani.
  Sintaksnya adalah: @+id/... (misalnya kotak EditText bisa disebut XML: Android:id="@+id/ediUserName")
- Tata Letak Meja
  TableLayout Android memungkinkan Anda untuk memposisikan widget Anda dalam kotak yang terbuat dari baris dan kolom yang dapat diidentifikasi.
  Kolom mungkin menyusut atau meregang untuk mengakomodasi isinya.
- Tata Letak Meja
  Baris dideklarasikan oleh Anda dengan menempatkan widget sebagai anak-anak dari TableRow di dalam keseluruhan TableLayout.
  Jumlah kolom ditentukan oleh Android ( Anda mengontrol jumlah kolom secara tidak langsung).
- Tata Letak Meja
  Namun, satu widget dapat mengambil lebih dari satu kolom dengan menyertakan properti android:layout_span, yang menunjukkan jumlah kolom yang dibentangkan widget (ini mirip dengan atribut colspan yang ditemukan di sel tabel dalam HTML)
  Secara default, setiap kolom akan berukuran sesuai dengan ukuran "alami" widget terluas di kolom tersebut.
- Tata Letak ScrollView
  Ketika kami memiliki lebih banyak data daripada yang dapat ditampilkan pada satu layar, Anda dapat menggunakan kontrol ScrollView.
  Ini menyediakan akses geser atau gulir ke data.
