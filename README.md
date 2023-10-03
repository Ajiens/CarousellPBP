Nama    :   Alwan Takahashi Aditaman <br>
NPM     :   2206828853 <br>
Kelas   :   PBP E <br>

================================== Tugas 5 ===============================================
1.  Jelaskan manfaat dari setiap element selector dan kapan waktu yang tepat untuk menggunakannya. <br>
    **Universal Selector**
    Dengan menggunakan tanda * dalam formatting css, maka semua konten yang ada di html akan berubah.
    <br>**Type Selector**
    sebuah tag langsung di spesifikkan bagaimana keinginan stylenya. Sehingga ketika melakukan styling desain yang berlaku akan diterapkan pada semua tag yang ada
   <br>**Class Selector**
    Sebuah tag dapat dikelompokan berdasarkan nama class yang dibuat untuk diubah style nya. Hampir sama dengan istilah grouping. Anak dari kelas yang didefinisikan juga bisa di tentukan sendiri.
    <br>**ID Selector**
    Sesuai dengan namanya, id seelector dapat ditargetkan secara mandiri untuk di styling di CSS. dan memberikan entitas yang eksklusif dalam stylingnya. Contoh sebuah kata
    <br>**Child Selector**
    Dengan menggunakan tanda >. Contoh penggunaannya seperti ini: <tag_A> > <tag_B> artinya <tag B> merupakan anak dari <tag A>. Maksut dari kata anak dari adalah <tag B> harus berada didalam <tag A>.
    <br>**Decendent Selector**
    Sama halnya dengan child selector, tapi ini tidak membutuhkan tanda > maupun tanda lainnya, jadi hanya spasi saja. Contoh penggunannya seperti ini: tag_A tag_Z. Prinsipnya sama dengan Child Selector, namun Decendent Selector ini bisa melangkah, seperti tag_A>...>tag_Z. Tidak peduli isi dari tag di titik-titik itu apa, asalkan tag_Z berada didalam tag_A.
    <br>**Adjacent Sibling Selector (First Child)**
    Dengan menggunakan tanda +. Contoh penggunaannya seperti ini: <tag_A> + <tag_B> artinya cari <tag B> yang sesudah <tag A>, maka itu yang di select.
    <br>**General Sibling selector (all child)**
    Kebalikannya dengan Adjacent Sibling Selector. Dia bisa menggunakan tanda ~. Contoh penggunaannya seperti ini: <tag_A> ~ <tag_B> artinya cari <tag B> yang setelah <tag A>, maka itu yang di select.

2. Jelaskan HTML5 Tag yang kamu ketahui.
   Tag b ```("<b>")``` -> Memberikan efek bold
   Tag strong ```("<strong>")``` -> memberikan efek seolah-olah important text
   Tag i ```("<i>")``` -> memberikan efek tulisan miring
   Tag mark ```("<mark>")``` -> memberi efek highlight pada text
   Tag heading ```("<h1>")``` -> memberikan efek tulisan besar layakknya judul
   Tag list ```("<list>")``` -> memberikan bullet untuk mengelist
   Tag table ```("<table>")``` -> untuk membuat table
   Tag input ```("<input>")``` -> untuk memberikan field input

3. Jelaskan perbedaan antara margin dan padding.
   Margin adalah jarak antara element satu dengan element yang lainnya. Padding adalah jarak antara element dan batasan containernya
   
========================================================================================== <br>
                                            Tugas 4
========================================================================================== <br>
1. Apa itu Django UserCreationForm, dan jelaskan apa kelebihan dan kekurangannya? <br />
    UserCreationForm adalah sebuah template field yang dapat langsung digunakan untuk membuat atau user baru ketika ingin memasuki sebuah website. <br />
    Kelebihan:
        * Mudah untuk dipakai karena tidak perlu menulis ulang kode <br />
        * Mempunyai default format field yang sangat berguna untuk memperkuat keamanan dari data pengguna, seperti aturan dalam membuat password. <br />
        * Mempunyai fitur untuk memvalidasi dalam pembuatan password <br />
        * Dapat mengkostumisasi tampilan dari default form field dengan menggunakan html dan css <br />
    Kekurangan: <br />
        * Hanya memiliki tiga fieldutama formulir, yaitu usernam, email, dan password. Oleh karena itu usercreationform cocok digunakan untuk menangani hal yang umum dalam pembuatan id user <br />
        * Secara default, tampilan yang diberikan hanya tampilan standar dan perlu mengedit dan mengkustomisasi jika mengingkan tampilan yang bagus
 <br />
2. Apa perbedaan antara autentikasi dan otorisasi dalam konteks Django, dan mengapa keduanya penting? <br />
    **Autentikasi** <br />
        Autentikasi adalah proses dibalik layar yang bertujuan untuk memverifikasi input dari user yang mencoba mengklaim identitas dirinya untuk masuk kedalam sebuah sistem. Tujuannya adalah untuk memeriksa input dari user tersebut, apakah data yang dimasukan cocok dengan data yang sudah tervalidasi untuk masuk kedalam sistem.
    **Otorisasi**  <br />
        Otorisasi adalah proses pembagian kewenangan kepada tiap-tiap penggunanya dalam mengakses sistem. Tujuannya adalah untuk membatasi interaksi-interaksi dari user yang tidak diizinkan agar tidak merusak sistem vital.
    <br />
    Secara garis besar, autentikasi digunakan untuk memverifikasi input dan otorisasi adalah untuk membagi kewenangan dalam mengakses sistem. Autentikasi dan otorisaai adalah dua hal yang sangat penting keberadaanya. Autentikasi berperdan dalam menjaga keamanan sistem dan otorisasi berperan dalam mengontrol segal aktifitas pengguna setelah berhasil masuk kedalam sistem. Sehingga dapat dikatakan kedua hal ini adalah dua hal yang saling berksinambungan dalam menjaga sebuah website yang dibuat.
 <br />
3. Apa itu cookies dalam konteks aplikasi web, dan bagaimana Django menggunakan cookies untuk mengelola data sesi pengguna?
    Cookies adalah mekainisme dalam website yang diperuntukan untuk menyimpan informasi dari pengguna yang ukurannya kcil. Keberadaan cookie dalam ini digunakan untuk mengingat dan menampung sementara identitas dari user yang berhasil masuk kedalam sistem untuk tetap berada didalam sistem tanpa harus mengauntentikasinya lagi.

    Untuk menggunakan cookies dalam mengelola data sesi pengguna, pertama yang dilakukan adalah saat pengguna pertama kali berhasil masuk kedalam sistem Django mengirimkan sebuah unik ID serta informasi sesi lainnya yang kemudian disimpan dipihak user. Unik ID akan digunakan oleh sistem setiap kali request auntentikasi diperlukan, sehingga user tidak perlu login dan mengautentikasi terus menerus setiap kali sistem mengirimkan sinyal request autentikasi.
 <br />
4. Apakah penggunaan cookies aman secara default dalam pengembangan web, atau apakah ada risiko potensial yang harus diwaspadai?
    Penggunaan Cookie secara general adalah menyimpan data user yang digunakan untuk mengakses suati sistem. Dengan menggunakan cookie yang dapat mengakses sebuah sistem cookie tersebut memungkinkan disalahgunakkan jika cookie tidak dilakukan dengan baik. Beberapa risiko yang dapat terjadi antara lain: <br />
    * Ketika Cookie tidak dilakukan pengamanan yang baik, cookie dapat dimanfaatkan peretas untuk mengakses masuk kedalam sistem sebagai pengguna yang sah dan memungkinkan pencurian data sensitif dari pengguna tersebut. <br />
    * Jika menggunakan presistent cookie yang menyimpan cookie di pihak user dan cookie tersebut dapat bertahan dalam waktu yang cukup panjang dapat membahayakan privasi dari user tersebut. Karena dengan menggunakan presistent cookie yang tidak diatur dengan benar memungkinkan peretas untuk menggunakan cookie tersebut untuk mengakes data yang sensitif
 <br />
5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial) <br />
    ⦿     **Mengimplementasikan fungsi registrasi, login, dan logout untuk memungkinkan pengguna   untuk mengakses aplikasi sebelumnya dengan lancar.** <br />
        Untuk membuat registrasi form, kita dapat menggunakan UserCreationForm. UserCreationForm adalah modul bawaan yang dimiliki Django yang dapat memudahkan developer untuk membuat registrasi form tanpa menulis kode dari awal. Untuk dapat membuat user, requirement HTTP yang dibutuhkan adalah POST, yang mana requirement ini mengirimkan data ke server yang kemudian akan disimpan didalam database. Selain itu, kita juga perlu memvalidasi input dari field yang diisi oleh user sebelum melakukan perubahan/penyimpanan pada database. Untuk mengimplementasinya, perlu dibuat file.html sebagai template penampilan dan menghubungkannya dengan menambahkan path pada file urls.py
         <br />
        Untuk membuat login kita perlu menggunakan field apa saja yang dibutuhkan. Dalam kode saya, saya hanya menggunakan field usernam dan password. Username dan password kemudian akan di autentikasi, apakah username dan password sudah bersesuian dengan database atau belum. Dalam mengautentikasi, saya menggunakan method bawaan yang diberikan oleh Django. Lalu untuk logout, saya hanya perlu menambahkan tombol logout didalam sistem. Tombol logout ini akan mengirimkan request untuk untuk keluar dari sistem dan kembali ke halaman login.
     <br />
    ⦿   **Membuat dua akun pengguna dengan masing-masing tiga dummy data menggunakan model yang telah dibuat pada aplikasi sebelumnya untuk setiap akun di lokal.**
        Untuk dapat melakukan ini kita harus menmberikan requirement HTTP berupa POST. Namun sebelum itu kita harus memvalidasi input dari user agar seseuai dengan environtment database yang sudah kita buat sebelumnya. Sehingga setelah itu kita dapat mengirimkan requiremnt HTTP berupa POST tadi kedalam database.
     <br />
    ⦿  **Menghubungkan model Item dengan User**
        Untuk menampilkan produk yang sesuai dengan user tertentu kita dapat menggunakan bantuan ForeignKey. ForeignKey ini yang kemudian akan menjadi penghubung antara item/product dengan user yang menambahkan item/product tersebut. Dalam sistem database, setiap user mempunyai key/id yang sifatnya unik. Ketika produk dibuat dengan user tersebut, didalam database produk tersebut akan menyimpan key yang sifatnya unik dari user tersebut. Sehingga unik key pada produk yang akan menjadi penghubung antara user dengan item/productnya.
         <br />
        Untuk mengimplementasikannya, kita dapat menggunakan "user = models.ForeignKey(User, on_delete=models.CASCADE)". Kode tersebut akan membuat column khusus yang menyimpan unique key dari user tersebut. Lalu ketika user membuat produk/item baru field user akan diisi dengan objek User dari return value request.user yang sedang terotorisasi untuk menandakan bahwa objek tersebut dimiliki oleh pengguna yang sedang login. Lalu untuk menampilkan produk yang terotrisasi tersebut kita dapat memfilternya dengan products = Product.objects.filter(user=request.user.id) agar produk/item yang ditampilkan seseuai dengan user id nya
     <br />
    ⦿   **Menampilkan detail informasi pengguna yang sedang logged in seperti username dan menerapkan cookies seperti last login pada halaman utama aplikasi.**
        Untuk dapat mengimplementasikan ini, pertama yang kita lakukan adalah untuk mengeset cookie yang kita inginkan. Kita dapat mengeset cookie dengan menggunakan "response.set_cookie('last_login', str(datetime.datetime.now()))". Waktu yang tepat untuk mengeset cookie seperti ini adalah ketika user berhasil login dan masuk kedalam sistem. Kemudian jika kita mengiginkan untuk menampilkan cookie yang diset tersebut kita dapat menggunakan perintah request.COOKIES.get['last_login']. Lalu jangan lupa untuk menghapus cookie tersebut ketika pengguna logout/keluar dari sistem

========================================================================================== <br />
                                            Tugas 3
========================================================================================== <br />

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

========================================================================================== <br />
                                            Tugas 2
========================================================================================== <br />

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
