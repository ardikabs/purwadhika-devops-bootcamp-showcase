# Linux

## Topics
* Linux Filesystem Hierarchy Standard (FHS)
* Linux Files and Directories
* Linux Permissions
* Linux Standard Stream
* Linux User and Group
* Linux Help
* Linux Essential Commands

## Showcase
1. Sebagai seorang system administrator, saya perlu memastikan bahwa setiap pengguna baru pada mesin Linux untuk melakukan pergantian password saat pertama kali masuk (login) ke dalam mesin Linux.
Dalam hal ini, terdapat seorang pengguna baru dari departement keuangan melakukan permintaan akses masuk ke dalam mesin Linux A, maka buatlah informasi pengguna tersebut pada mesin Linux A dengan memastikan aturan yang telah disebutkan berlaku.

    _*keyword: `passwd`*_

2. Sebagai seorang system administrator, saya perlu melakukan penambahan hak akses pada pengguna selaku pemiliki sumber daya mesin ke dalam group sudo. Dalam hal ini tambahkan pengguna `newadmin` ke dalam group sudo, dan pastikan pengguna tersebut telah memiliki akses sudo.

    _*keyword: `usermod`*_

3. Sebagai seorang system administrator, saya harus mampu mencari file pada direktori tertentu dengan spesifikasi yang diinginkan. Dalam hal ini, carilah file pada direktori `/etc` yang memiliki spesifikasi *permissions* **read/write** untuk user, **read** untuk group dan others lalu catat informasi tersebut dalam file `/tmp/644-file-result`

    _*keyword: `find`*_

4. Sebagai seorang system administrator, saya perlu memanfaatkan standard cli tools untuk melakukan manipulasi file sesuai dengan kebutuhannya. Dalam hal ini, dapatkan informasi list pengguna mesin Linux diikuti dengan UID disetiap baris outputnya dan pastikan untuk merubah semua huruf kecil menjadi huruf besar, catat output tersebut ke dalam file `/tmp/user-with-uid`

    _*keyword: `awk, tr`*_

5. Sebagai seorang system administrator, saya perlu melakukan backup secara berkala dalam mesin Linux yang ditujukan sebagai cadangan yang memungkinkan untuk digunakan di waktu mendatang. Dalam hal ini, buatlah file archive pada directory `/var/log/` dengan nama `/tmp/var-log.tgz`

    _*keyword : `tar`*_