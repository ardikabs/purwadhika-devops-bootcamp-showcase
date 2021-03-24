# Shell Scripting

* Manipulating Text
    * `head` : Read from the first line of file
    * `tail` : Read from last recent line of file
    * `sed` : Stream editor
    * `awk` : Extract and print then construct output from content of a file
    * `strings` : Read string from unreadable output (ex. binary)
    * `paste` : Combine field output from 2 different files, also possible with custom delimiter.
    * `join` : An enhance version of `paste`. Join content from 2 different files using similar pattern from both files.
    * `split` : Used to break up file from large file into multiple files with equal-sized segment. For ex, 1000 lines break up to 4 different files each of file had 250 lines.
* Regular Expression (regex)
* Compare Two Files
    * `diff`

### Simple Bash Scripting
* know the environment variable. `printenv`

```bash
$ cat > /tmp/findls.sh <<EOF
#!/bin/bash
find . -name "*.c" -ls
EOF

$ bash /tmp/findls.sh
```
```bash
$ cat > /tmp/findls-with-param.sh <<EOF
#!/bin/bash
find . -name "$1" -ls
EOF

$ chmod +x /tmp/findls-with-param.sh
$ /tmp/findls-with-param.sh "*.c"
```
```bash
$ cat > /tmp/find-interactive <<EOF
#!/bin/bash
echo "Directory to find: "
read directory

echo "Pattern to find: "
read name

find $directory -name "$name" -ls
EOF
$ chmod +x /tmp/find-interactive
$ mv /tmp/find-interactive /usr/local/bin/
$ find-interactive
```

### Exit Status Code
exit status code in bash shell is simple:
* zero status code is **success**
* **non-zero** status code is **failure**

### Basic Syntax and Special Character
* `#`: comment
* `\`: indicate continuation into next line
* `;`: used to interpret what follows as a new command to be executed next. Ignoring error
* `$`: variable keyword
* `>`: redirect output
* `>>`: append output
* `<`: redirect input
* `|`: Pipe, used to forward result to the next command

```bash
$ sudo apt install curl \
    ca-certificates \
    certbot \
    docker.io -y

$ curl https://google.com -w %{http_code} -o /dev/null; whoami
$ curl https://domain-should-be-error.com -o /dev/null && whoami
$ curl https://google.com || cat /tmp/file-not-found
```