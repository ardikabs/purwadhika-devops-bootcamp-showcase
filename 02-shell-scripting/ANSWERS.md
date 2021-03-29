# Answers [Simple Shell Scripting](shell-scripting-1.md)
1. Shell script untuk memberikan output user dan user id beserta tanggal dan direktori saat shell dijalankan.
    ```bash
    #!/usr/bin/env bash
    echo $USER $(id -u $USER)
    date
    pwd
    ```

1. Shell script untuk memberikan output daftar file pada direktori `/etc/` yang memiliki ukuran sama dengan 10 KB.
    ```bash
    #!/usr/bin/env bash
    find /etc -type f -size 10k
    ```

1. Shell script untuk mengalihkan standard output menjadi standard error pada pengguna.
    ```bash
    #!/usr/bin/env bash
    echo "Error: Oops! Error pada file tersebut" >&2
    ```

1. Shell script untuk memodifikasi informasi error saat melakukan `cat` pada file yang tidak tersedia
    ```bash
    #!/usr/bin/env bash
    FILE='devops.academy'

    cat $FILE 2>/dev/null || echo -e "File '$FILE' tidak tersedia dong" >&2
    ```

1. Shell script untuk menunjukkan exit code apabila file tidak tersedia dan melanjutkannya membuat file tersebut dan diakhiri dengan menghapus file tersebut.
    ```bash
    #!/usr/bin/env bash
    FILE='devops.academy'

    ls $FILE 2>/dev/null
    echo "status: $?"
    touch $FILE; ls $FILE 2>/dev/null
    echo "status: $?"

    rm $FILE; echo "menghapus file" >&2
    ```

1. Shell script untuk membuat output daftar pengguna mesin Linux diurutkan secara ascending.
    ```bash
    #!/usr/bin/env bash
    awk -F: '{print $1}' /etc/passwd | sort
    ```

1. Shell script untuk membuat output daftar pengguna mesin Linux dan diurutkan berdasarkan UID secara ascending dengan format yang telah ditentukan.
    ```bash
    #!/usr/bin/env bash

    cat /etc/passwd | sort -t: -n -k3 | awk -F: '{printf("Username: %s | UID: %s | GID: %s\n", $1, $3, $4)}'
    ```

***
# Answers [Advanced Shell Scripting](shell-scripting-2.md)
not yet