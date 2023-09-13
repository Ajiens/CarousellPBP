Nama    :   Alwan Takahashi Aditama
NPM     :   2206828853
Kelas   :   PBP E

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
