1. Buatlah sebuah shell script untuk menunjukkan nama pengguna serta uid pengguna tersebut, diikuti dengan tanggal hari ini serta nama direktori yang saat script dijalankan.
    Output:
    ```
    linux1 2001
    Wed Mar 24 17:45:15 UTC 2021
    /tmp
    ```
1. Buatlah sebuah shell script yang mampu untuk mendapatkan daftar file pada direktori `/etc` yang memiliki ukuran sama dengan 10 kilobyte.
    Output:
    ```
    /etc/locale.gen
    /etc/nanorc
    /etc/vmware-tools/vgauth/schemas/xmldsig-core-schema.xsd
    /etc/vmware-tools/vm-support
    /etc/vmware-tools/tools.conf.example
    ```
1. Buatlah sebuah shell script yang mampu mengalihkan standard output menjadi standard error sebagai informasi kepada pengguna:
    Output:
    ```
    Error: Oops! Error pada file tersebut
    ```
1. Buatlah sebuah shell script yang mampu melakukan modifikasi informasi error saat melakukan `cat` pada file yang tidak tersedia:
    Output:
    ```
    File 'devops.academy' tidak tersedia dong
    ```
1. Buatlah sebuah shell script digunakan untuk:
    * Menunjukkan status exit code saat menjalankan perintah `ls` pada file yang tidak tersedia
    * Kemudian membuat file tersebut, dan menjalankan perintah `ls` sekali lagi, lalu informasikan status exit code pada pengguna sekali lagi
    * Diakhiri dengan menghapus file yang telah dibuat di langkah sebelumnya.
    * Pastikan user hanya mendapatkan output yang diinginkan
    Output:
    ```
    status: 2
    status: 0
    menghapus file
    ```
1. Buatlah sebuah shell script yang menunjukkan daftar lengkap pengguna pada mesin linux, lalu urutkan sesuai dengan abjad
    Output:
    ```
    angkasa
    bandung
    cilacap
    darius
    enggano
    filipina
    gajah
    harimau
    ...
    ```
1. Buatlah sebuah shell script yang dapat memanipulasi file `/etc/passwd` untuk menunjukkan format berikut ini dan terurut berdasarkan UID:
    Output:
    ```
    Username: angkasa | UID: 10 | GID: 10
    Username: cilacap | UID: 21 | GID: 10
    Username: gajah | UID: 31 | GID: 1001
    Username: darius | UID: 101 | GID: 89
    ...
    ```