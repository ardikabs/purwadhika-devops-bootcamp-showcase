# Answers [01-linux-administration](README.md)
1. Memastikan pengguna untuk mengganti password saat pertama kali login.
    ```bash
    $ adduser linux1
    ...
    ...
    ...

    # to enforce user to change password on the first login,
    # we need to set the current password to be expired
    $ passwd --expire linux1
    ```

1. Menambahkan pengguna ke dalam group
    ```bash
    # just after add user to the selected group
    # need to relogin on any login session of the user
    # to be effectively affected
    $ usermod -aG sudo newadmin
    ```

1. Mencari file pada direktori `/etc/` yang memiliki permission read dan write pada user dan read pada group dan others.
    ```bash
    $ find /etc -type f -perm 644 > /tmp/644-file-result
    ```

1. Membuat custom output dari file `/etc/passwd`
    ```bash
    $ awk -F: '{print $1,$3}' /etc/passwd | tr '[:lower:]' '[:upper:]'
    ```

1. Membuat file archive untuk direktori `/var/log`
    ```bash
    $ tar cvzf /tmp/var-log.tgz /var/log
    ```