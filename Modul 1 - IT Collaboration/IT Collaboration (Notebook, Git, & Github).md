# **IT Collaboration (Notebook, Git, & Github)**
Pada pertemuan GWE yang pertama ini, kita akan membahas mengenai tools-tools yang akan teman-teman pakai selama belajar di Study Group EDM. Mulai dari Notebook hingga Github, tools-tools ini dibutuhkan karena kalian akan berkolaborasi dalam sebuah kelompok untuk mengerjakan suatu projek.
## What is Notebook and How to Use It?
**Notebook** adalah lingkungan interaktif untuk menulis dan menjalankan kode, membuat visualisasi, serta menambahkan teks naratif dalam satu dokumen yang dapat diakses dan dibagikan.
### Tools
**Jupyter Notebook** adalah aplikasi web open-source yang memungkinkan pengguna untuk membuat dan berbagi notebook yang berisi kode Python (atau bahasa pemrograman lainnya), teks, dan visualisasi.

**Google Colab** adalah platform cloud berbasis Jupyter Notebook yang disediakan oleh Google, memungkinkan pengguna untuk membuat, menjalankan, dan berbagi notebook Python secara gratis dengan akses ke GPU dan TPU secara gratis.

**Kaggle** menyediakan lingkungan Jupyter Notebook (Kaggle Kernels) yang memungkinkan pengguna untuk menjalankan kode Python dan R di cloud dengan akses ke dataset Kaggle, kompetisi data, dan integrasi dengan komunitas data scientist.

**Perbedaan antara ketiganya:**
1. Jupyter Notebook: Memerlukan instalasi dan pengelolaan sendiri, dapat dijalankan secara lokal.
2. Google Colab: Platform cloud dengan akses gratis ke GPU/TPU, integrasi dengan Google Drive, dan kolaborasi real-time.
3. Kaggle Kernels: Lingkungan cloud untuk analisis data dan kompetisi, dengan akses ke dataset Kaggle dan komunitas data scientist.

### [Example of Machine learning project using Google Colab Notebook](https://colab.research.google.com/github/ageron/handson-ml2/blob/master/02_end_to_end_machine_learning_project.ipynb#scrollTo=tmJG3W51lp2G)

### How to read and using data for processing on Google Colab Notebook
Berikut cara ketika data sudah didownload dan dimasukkan ke Gdrive yang sudah terhubung dengan Google Colab.
> ### Step 1: Mount the Google Drive

    Langkah pertama adalah mounting Google Drive ke notebook Google Colab . Ini akan memungkinkan untuk mengakses file Google Drive langsung dari notebook. Untuk mounting Google Drive, bisa menggunakan kode berikut:

    from google.colab import drive
    drive.mount('/content/drive')

> ### Step 2: Navigate to the file you want to read

    Setelah mounting Google Drive, kita dapat mengakses file yang ingin  dibaca. Google Colab menyediakan penjelajah file yang dapat digunakan untuk menjelajahi Google Drive. Untuk membuka penjelajah file, berikut kodenya:

    !ls "/content/drive/My Drive/"

    Kode di atas akan menampilkan daftar isi dari direktori utama Google Drive. Kita dapat mengganti /My Drive/ dengan jalur ke direktori yang berisi file kita.

> ### Step 3: Read the file into your notebook

Setelah menavigasi ke file yang ingin dibaca, kita dapat membacanya ke dalam notebook. Metode yang digunakan untuk membaca file akan bergantung pada jenis file yang dikerjakan. 

Berikut adalah beberapa contohnya:

- ### Reading a text file

    with open('/content/drive/My Drive/example.txt', 'r') as f:
        text = f.read()
    print(text)

- ### Reading a CSV file
    import pandas as pd
    data = pd.read_csv('/content/drive/My Drive/my_data/data.csv')
    print(data.head())

- ### Reading an image file
    from PIL import Image
    import matplotlib.pyplot as plt
    image = Image.open('/content/drive/MyDrive/saturn-cloud-saturn-cloud.png')
    plt.imshow(image)

- ### Reading data from kaggle (Additional)
    Steps:
    1)	Download API Credentials
    2)	Upload file kaggle.json ke Google Colab
    3)	Instalasi (seperti library dll) pada Google Colab
    4)	Download dataset dengan mencari nama dari dataset pada kaggle

        [Untuk detail dan lebih jelas klik disini](https://www.analyticsvidhya.com/blog/2021/06/how-to-load-kaggle-datasets-directly-into-google-colab/)

## What is Git & Github and How to Use It?
Git dan GitHub, dua platform yang dibuat oleh perusahaan yang sama, memiliki tujuan yang serupa tetapi fitur yang berbeda. Keduanya memberikan dukungan yang besar bagi para pengembang perangkat lunak dalam mengelola kode sumber secara kolaboratif. Dengan menggunakan sistem kontrol versi, pekerjaan tim dapat dipantau dan dievaluasi dengan efisien.
### Clarification of misconceptions and explanation of both platforms
**Git** adalah perangkat lunak berbasis Version Control System (VCS) yang digunakan untuk merekam setiap perubahan dalam file atau repositori proyek. Pengembang sering menggunakan Git untuk distribusi revisi (VCS terdistribusi), memungkinkan penyimpanan database tidak hanya di satu lokasi tetapi diakses oleh semua anggota tim yang terlibat dalam pengembangan kode. Komponen penting dalam Git adalah "commit" yang digunakan untuk menyimpan catatan perubahan pada file. Dengan melakukan commit, pengembang dapat dengan mudah kembali ke versi sebelumnya menggunakan perintah "checkout". Penggunaan Git memerlukan instalasi perangkat lunak terlebih dahulu agar dapat digunakan secara offline. Perangkat lunak ini tersedia secara gratis melalui situs resmi unduhan Git.

**GitHub** adalah platform manajemen proyek, sistem versioning kode, dan komunitas sosial bagi para pengembang di seluruh dunia. Perlu diketahui, GitHub memiliki versi induknya yaitu Git yang merupakan software version controlled system yang dilakukan secara offline. GitHub menyediakan layanan cloud untuk menyimpan dan mengelola berbagai proyek atau repositori Git. Dengan sifatnya yang berbasis online, GitHub memungkinkan pengguna untuk berkolaborasi dalam pengeditan repositori atau proyek dari lokasi yang berbeda. Hal Ini memudahkan pengguna dan tim dalam mengorganisir folder yang berisi file terkait pemrograman yang sedang dikerjakan.

Meskipun beberapa **perbandingan antara Git dan GitHub** mungkin tidak selalu jelas, keduanya sebenarnya sangat berbeda. Untuk memahami perbedaan ini, mari lihat dari sisi dasarnya. Git adalah sistem yang digunakan untuk melacak perubahan pada kode agar hidup programmer lebih mudah. Di sisi lain, GitHub adalah sebuah layanan hosting. Apa yang di-host oleh layanan ini? Itu cukup sederhana - GitHub meng-host repositori Git. Dalam istilah yang lebih sederhana, Git adalah alat yang digunakan untuk mengelola kode, sementara GitHub adalah layanan yang digunakan untuk menyimpan dan berbagi proyek tersebut. Cara yang baik untuk memahaminya adalah dengan analogi mobil; Git adalah mobil yang digunakan untuk mengendarai, sedangkan GitHub adalah tempat parkir untuk menyimpan mobil tersebut. Jadi, meskipun Git adalah alat yang digunakan, ada berbagai layanan hosting seperti GitHub yang dapat dipilih untuk menyimpan dan berbagi repositori Git Anda. GitHub hanyalah salah satu dari banyak pilihan yang tersedia.

### How to Connect Git to Github
Steps:
1)	Membuat akun Github
	Sebelum menggunakan git kita sebaiknya membuat akun github terlebih dahulu karena akun github ini yang akan dijadikan sebagai repository central nya.
2)	Install Git
	Selanjutnya download software git, sesuaikan dengan sistem operasi yang digunakan. Setelah download, maka lakukan instalasi software seperti instalasi pada umunya sampai selesai.
3)	Konfigurasi Git
	Setelah menginstall git selanjutnya kita lakukan config terlebih dahulu. Kenapa kita memerlukan config pada git?  
karena Git akan selalu menggunakan informasi tersebut untuk apapun yang Anda lakukan pada sistem tersebut.

    Berikut untuk perintahnya:

    git config --global user.name "nama lengkap"

    git config --global user.email "emailkamu@example.com"

    Perintah di atas bermaksud agar Git dapat terhubung dengan akun 				Github yang telah kalian buat, agar nantinya dapat diupload ke 				repository yang telah kalian buat di akun Github kalian tadi.

### Basic collaboration in Git & Github

Banyak cara untuk berkolaborasi dalam proyek menggunakan GitHub. Pembahasan pada modul ini akan membantu  kalian yang baru memulai bekerja dengan tim dan belum menetapkan alur git atau belum tahu harus mulai dari mana dalam menetapkannya.

Steps:
1)	Buat repository baru pada Github
	Pergi ke Github dan klik tombol ‘+’ di sudut kanan atas dan pilih ‘New Repository’.
![Alt text](image.png)

    ![Alt text](image-1.png)
2)	Kalo sudah diisi nama repository nya lalu create repository. Maka akan muncul seperti gambar dibawah ini
![Alt text](image-2.png)

    Kemudian setelah dibuat di github respository nya lalu kembali lagi ke visual studio code. 

    Kemudian buat repository di git dengan memasukan perintah : 

    git init

    Perintah ini akan membuat repository dengan nama git dan akan tersembunyi file nya. Yang harus diperhatikan yaitu apabila sudah pernah membuat git di folder tersebut maka tidak bisa lagi membuat git karena akan saling menimpa dan akan konflik. 
    
    Lalu perintah selanjutnya yaitu :
    
    git add .

    Perintah ini merupakan perintah yang akan menambah file ke github. Selanjutnya yaitu :

    git commit -m "initialization commit"
    
    Perintah diatas sebagai commit yang pertama. Untuk penambahan commit harus diperhatikan karena akan menjadi history setiap perubahan. 
    
    Selanjutnya yaitu : 

    git remote add origin "isi link dari github kalian"

    Perintah diatas yaitu perintah untuk dapat menghubungkan dari repository lokal ke repository central yaitu github. 
    
    Ketika kita akan banyak melakukan perubahan kita bisa membuat branch lain agar tidak langsung merubah di master/main nya. 
    
    Perintah untuk membuat branch baru yaitu :

    git branch <name> 
    atau 
    git checkout -b <nama branch lain> #untuk menambah branch
    
    Yang terkahir yaitu :

    git push origin "nama branch"

    
    Perintah ini yang akan memasukan program yang telah dibuat dan tersimpan di git repository lokal ke repository central yaitu github dan bisa diakses oeh developer yang lain. Tunggu hingga proses pengiriman file berhasil dan 100% terkirim semuanya.

