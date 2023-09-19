Nama    :   Alwan Takahashi Aditaman
NPM     :   2206828853
Kelas   :   PBP E

==========================================================================================
                                            Tugas 3
==========================================================================================

1. Apa perbedaan antara form POST dan form GET dalam Django?
    POST : adalah sebuah request yang digunakan untuk mengirimkan data ke server. POST digunakan ketika data yang direquest ingin di ubah atau dimodifikasi kedalam database.
    GET : adalah request yang digunakan untuk membaca atau mengembalikan data dari web server. GET digunakan ketika ingin menampilkan data yang diperoleh dari database system

2. Apa perbedaan utama antara XML, JSON, dan HTML dalam konteks pengiriman data?
    HTML (Hypertext Markup Language)
    adalah sebuah bahasa yang digunakan untuk membuat template struktur website untuk memuat dan menampilkan konten-konten yang ingin ditampilkan kepada user. Secara garis besar, HTML berpean sebagai wadah dari setiap elemen-elemen yang ingin ditampilkan kepada user. Elemen-elemen tersebut dapat berupa data, gambar, text, ataupun video.
    
    XML (Extensible Markup Language)
    Dalam pertukaran data, file dengan format XML membutuhkan XML DOM sebagai alat ekstraksi data yang ada didalam file tersebut. Dengan menggunakan XML DOM, struktur data yang ada didalam format XML akan dimanipulasi sehingga data-data yang ada dapat diestrak dan diakses serta dapat disimpan dalam suatu variabel. Namun, pengaksesan data harus diakses berdasarkan hirarki/tingkatan yang sama dengan file XML

    JSON (JavaScript Objec Notation0)
    Dalam pertukaran data, file dengan format JSON dapat diekstrak menjadi objek JavaScript. Proses ekstraksi ini dapat menggunakan fungsi JSON.parse() untuk menghubahnya menjadi objek JavaScript. Setelah mengekstraksi menjadi objek JavaScrpit, data-data yang ada dapat diakses berdasarkan key properti yang sama seperti yang ada pada file JSON tersebut.

3. Mengapa JSON sering digunakan dalam pertukaran data antara aplikasi web modern?
    Secara garis besar, penggunaan JSON lebih populer dalam pertukaran data dikarekanakn format yang digunakan JSON sederhana. Secara sintaks, file data yang berformat JSON mudah dibaca, baik untuk manusia maupun komputer. Selain itu, JSON juga dianggap lebih ringan dan mudah diproses oleh komputer dibandingkan menggunakan file berformat XML yang dikenal dengan sintaksisnya cukup rumit dan perlu menggunakan XML DOM untuk mengesktraksinya.

4. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)

    ⦿   Membuat input form untuk menambahkan objek model pada app sebelumnya.
    
    Pertama yang perlu dilakukan adalah membuat file dengan nama forms.py. File ini berfungsi untuk menerima input dari user berupa data. Pada file ini perlu mendefinisikan fields sesuai dengan data apa yang dibutuhkan dari user. Dari field tersebut juga perlu mendefinisikan dimana tempat menyimpan tiap input yang dimasukan oleh user. Oleh sebab itu, pada file models.py juga perlu di sesuaikan dengan input dari user dengan mendefinisikan variabel untuk tempat menyimpan input dari user.

    Untuk membuat form field yang dapat dilihat dan diisi oleh user, kita perlu menambahkan template html yang dapat menampilkan form field tersebut. Dalam membuat halaman html yang berisi form field, perlu adanya tombol yang executeable untuk mensubmit/menyimpan data yang dimasukan oleh user. Tombol tersebut harus dapat mengirimkan request untuk melakukan penyimpanan data. Dalam hal ini, tombol yang di pencet harus mengirimkan request ke view. Nantinya file views.py akan melakkuan penyimpanan kedalam database dengan menggunakan method .save()

    ⦿   Tambahkan 5 fungsi views untuk melihat objek yang sudah ditambahkan dalam format HTML, XML, JSON, XML by ID, dan JSON by ID.

    Untuk melihat objek apa saja yang sudah ditambahkan dalam format tertentu, pertama yang dilakukan adalah dengan mengambil data yang ada di data base. Hal yang dapat dilakukan adalah dengan memanggil fungsi Product.objects.all() dan menyimpannya kedalam variabel. Fungsi ini adalah fungsi yang bertujuan untuk mengambil semua objek yang sudah ditambahkan didalam database. Setelah data diambil, web server perlu meresponnya dengan fungsi HttpResponse(). Akan tetapi, sebelum melakukan itu perlu adanya prosesn translate objek menjadi format lain yang diinginkan (JSON/XML/dll) dengan menggunakan fungsi seriliaze() dari serializers.

    Untuk melakukan pemanggilan objek by ID dapat dilakukan hal yang sama. Akan tetapi data yang diambil hanya dipanggil berdasarkan ID yang diminta, yaitu dengan menggunakan fungsi Product.objects.filter(pk=id)

    ⦿   Membuat routing URL untuk masing-masing views yang telah ditambahkan pada poin 2.

    Untuk melihat objek apa saja yang di input, perlu url yang bersesuain padda file urls.py didalam list urlspatterns. Sebagai contoh jika ingin menampilkan data by id dengan format json perlu menambahkan baris kdode dibawh ini:
            path('json/<int:id>/', show_json, name='show_json')
    Sesuaikan jika ingin menampilkan semua data dengan format XML

    ⦿  Mengakses kelima URL di poin 2 menggunakan Postman
    Untuk dapat mengakses database yang ada pada direktori ini, pertama yang dilakukan adalah menjalanlank virtual environtment dengan menggunakan env\Scripts\activate.bat. Setelah itu copy link local host dan memilih opsi GET untuk mengambil data didalam database dan menampilkannya. Untuk menampilkan datanya bisa menggunakan tampilan JSON maupun XML. Cara nya bisa menambahkan url berupa JSON atau XML, contoh: http://localhost:8000/json atau http://localhost:8000/xml. Jika ingin menampilkan data berdasarkan ID bisa menambahkan nomor ID setelah url tersebut. Contoh http://localhost:8000/json/1, artinya menampilkan data yang memiliki ID.

==========================================================================================
                                            Tugas 2
==========================================================================================

1. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial).
    ⦿ Membuat sebuah proyek Django baru.
        Dalam membuat proyek django perlu untuk mengimport library, framework, atau package yang diperlukan. Tujuannya adalah untuk memanfaatkan kode yang sebelumnya sudah ada untuk dipakai dan membantu dalam mengembangkan proyek agar lebih mudah

    ⦿ Membuat aplikasi dengan nama main pada proyek tersebut.
        untuk membuat aplikasi dengan nama main, perlu menuliskan "python manage.py startapp main". Fungsi ini akan membuat berkas yang diperlukan seperti admin.py, urls.py, dll. Struktur ini nantinya akan berguna untuk mengorganisir logika dari aplikasi yang dibuat.

    ⦿ Melakukan routing pada proyek agar dapat menjalankan aplikasi main.
        Setelah membuat folder main, perlu menambahkan "main" pada list INSTALLED_APPS didalam file settings.py. Fungsinya adalah agar Django tahu bahwa ada aplikasi main yang harus digunakan dalam proyek ini.

    ⦿ Membuat model pada aplikasi main dengan nama Item dan memiliki beberapa atribut wajib.
        Untuk membuat model pada aplikasi main harus mengubah berkas models.py. Kegunaan utama dari berkasi ini adalah memungkinkan pihak developer untuk berinteraksi dengan data-data, dibandingkan membuat database sendiri menggunakan SQL Querry.

    ⦿ Membuat sebuah fungsi pada views.py untuk dikembalikan ke dalam sebuah template HTML yang menampilkan nama aplikasi serta nama dan kelas kamu
        File views.py ini mempunyai tanggung jawab dalam menangani permintaan yang masuk dari pengguna. Nantinya views ini akan menghasilkan respon dan mengirimkan baik berupa halaman HTML sesuai dengan kehendak dari user.

    ⦿ Membuat sebuah routing pada urls.py aplikasi main untuk memetakan fungsi yang telah dibuat pada views.py.
        urls.py ini berfungsi untuk merespon dan mengkaitkan url yang diterima dari perlakukan-perlakuan user. Nantinya urls ini akan mengarahkan views mana yang ingin ditampilkan kepada user


2. Buatlah bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya dan jelaskan pada bagan tersebut kaitan antara urls.py, views.py, models.py, dan berkas html.

    ![ClientUser (1)](https://github.com/Ajiens/CarousellPBP/assets/124881916/12780284-485b-4f5d-a19d-0bbf4012059e)

   
    Pertama, client atau user akan mengirimkan request. Request dapat berupa ketika user menekan button, atau yang lainnya. Kemudian request dari user tersebut akan ditangkap oleh HTTP Server. HTTP server ini dapat diimplementasikan dengan bermacam-macam bahasa. Sebelum masuk kedalam sistem web yang menggunakan Django, request dari HTTP Server telebih dahulu diterjemahkan oleh WSGI. Hal tersebut dilakukan supaya sistem Django tahu ada request yang dilakukan oleh user.

    Setelah itu, request akan memasuki sistem yang ada pada Django. Request kemudian akan dicek terlebuh dahulu dengan menggunakan request middleware. Request middleware ini akan memanipulasi request tersebut sebelum mencapai view. Setelah itu Django akan mengkonfigurasi routing yang ada didalam file urls.py. Setelah memeriksa yang ada didalam file urls.py,  Django akan mencocokan request berupa URL yang diterima sesuai yang ada pada file urls.py.

    Jika ada kecocokan antara request dan url, django akan menjalankan view sesuai dengan hasil kecocokan tadi. View akan melakukan permintaan kepada data base untuk memproses data-data mana yang ingin ditampilkan jika perlu. Namun, jika tidak ada kecocokan antara request dan url, akan terjadi exception dan kemudian akan menampilkan error (biasanya eror 404).

    Dari hasil ekstraksi data-data yang dibutuhkan, Django kemudian akan memnaggil file berupa .html untuk menampilkan tampilan yang sesuai dengan template html yang telah dibut. Kemudian akan di translate kembali menggunakan WSGI yang nantinya siap untuk ditampilkan oleh HTTP Server dan user dapat melihat sesuai dengan request yang diminta

4. Jelaskan mengapa kita menggunakan virtual environment? Apakah kita tetap dapat membuat aplikasi web berbasis Django tanpa menggunakan virtual environment?
    Ya, aplikasi web yang menggunakan Django dapat berjalan tanpa menggunakan virtual environtment. Namun, hal tersebut sangat tidak disarakan karena beberapa sebab. Tujuan utama menggunakan virtual environtment ketika menggunakan Django adalah untuk memisahkan atau mengisolasi proyek yang sedang dikerjakan agar konflik antar versi python tidak terjadi. Karena jika hal tersebut terjadi karena tidak menggunakan virtual environtment akan menyebabkan masalah yang sulit untuk didiagnosis dan diperbaiki. Dengan melakukan isolasi ini juga akan membantu developer dalam menjaga kebersihan dan proyek dapat terorganisir dengan baik.

5. Jelaskan apakah itu MVC, MVT, MVVM dan perbedaan dari ketiganya.
    Pada dasarnya MVC, MVT, dan MVVM adalah rangkaian arsitektur yang digunakan untuk memisahkan antara visualisasi, pemrosesan, dan manajemen data untuk mengembangkan sebuah aplikasi
    
    ⦿ MVC (Model-View-Controller)
        Arsitektur MVC adalah arsitektur yang menghubungkan antra model dan view dengan menggunakan Controller. Secara teknis, setiap kali model diperbarui, model akan memberi tahu controller untuk mengenerate view ulang dengan data baru. Singkatnya Controller bertanggung jawab untuk menjagai kesinkronan antara view dan model

    ⦿ MVT 
        MVT adalah sebuah arsitektur yang digunakan dalam framework Django. Dengan menggunakan arsitektur ini, sebagai developer dapat dengan mudah mengambil data dari database yang ada tanpa menuliskan SQL Query. Dari data tersebut Django secara otomatis akan membangun tampilan web tersebut berdasarkan data yang ada. 
        
    ⦿ MVVM
        Arsitektur MVVM adalah arsitektur yang menggunakan View-Model sebagai jembatan yang menghubungkan view dengan model. Dalam arsitektur ini, view yang mempunyai tugas utama dalam menskinkronisasi model dan view. View akan melakukan operasi yang diperlukan untuk mengubah data yang ada di Model untuk bisa melakukan formatting sesuai dengan view. 
