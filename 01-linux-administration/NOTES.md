### Sudoer Anatomy
```
spec: (User_list) (Host_List) = (Runas_Spec) (Tag_Spec* Cmnd)
english: <user/%group> <host> = <impersonate user> <command>
example:
1. jenkins ALL = (ALL:ALL) ALL
2. %operators ALL = (: ADMINGRP) /usr/sbin
3. user1 ALL = (ALL) NOPASSWD:ALL
```

* **jenkins** ALL = (ALL:ALL) ALL | Bagian pertama menunjukkan daftar user, dalam hal ini (jenkins).
* jenkins **ALL** = (ALL:ALL) ALL | Bagian kedua menunjukkan daftar host, dalam hal ini semua host (all hosts).
* jenkins ALL = (**ALL**:ALL) ALL | Bagian ketiga menunjukkan pengguna yang akan digunakan untuk menjalankan perintah, dalam hal ini semua pengguna (all users).
* jenkins ALL = (ALL:**ALL**) ALL | Bagian keempat menunjukan grup yang akan digunakan untuk menjalankan perintah, dalam hal ini semua grup (all groups).
* jenkins ALL = (ALL:ALL) **ALL** | Bagian kelima menunjukan daftar command yang digunakan, dalam hal ini semua command.
