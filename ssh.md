Terminal Guake<br>
Dodawanie klucza publicznego do github.com<br>
* Z górnej listy wejdz w Account settings
* wybierz SSH Keys
* wybierz Add SSH key
* wpisz Title czyli nazwe kompa z ktorego pracujesz
* wkopiuj klucz z treminala
* pokaż klucz

```c
pjakusz@p137-03:~$ ls ~/.ssh/
known_hosts
```
* jeżeli nie podaje klucza trzeba uruchomić program

```c
pjakusz@p137-03:~$ ssh-keygen
```
podaje klucz prywatny id-rsa i publiczny id-rsa.pub
```c
pjakusz@p137-03:~$ ls ~/.ssh/
id_rsa  id_rsa.pub  known_hosts
```
trzeba 
```c
Generating public/private rsa key pair.
Enter file in which to save the key (/home/studpoz/pjakusz/.ssh/id_rsa): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/studpoz/pjakusz/.ssh/id_rsa.
Your public key has been saved in /home/studpoz/pjakusz/.ssh/id_rsa.pub.
The key fingerprint is:
84:30:bd:a0:ff:1a:31:d2:08:8d:95:b6:db:5f:4f:47 pjakusz@p137-03
The key's randomart image is:
+--[ RSA 2048]----+
|  ..o.           |
| +o .o..         |
|o..o ....        |
| .oo  ..    E    |
|  o++   S  .     |
|  ..oo  . . .    |
|    .o . o .     |
|     .o   .      |
|    ..           |
+-----------------+
pjakusz@p137-03:~$ 
pjakusz@p137-03:~$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/studpoz/pjakusz/.ssh/id_rsa): 
/home/studpoz/pjakusz/.ssh/id_rsa already exists.
Overwrite (y/n)? y
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/studpoz/pjakusz/.ssh/id_rsa.
Your public key has been saved in /home/studpoz/pjakusz/.ssh/id_rsa.pub.
The key fingerprint is:
ae:29:ba:25:62:39:62:ac:ef:16:83:97:98:4d:46:93 pjakusz@p137-03
The key's randomart image is:
+--[ RSA 2048]----+
|   .             |
|  E              |
| . .             |
|  o              |
| B .    S        |
|= B    .         |
|oB.o.   .        |
|=.oo.  o         |
|.+=o .o          |
+-----------------+
pjakusz@p137-03:~$ ls~/.ssh/
bash: ls~/.ssh/: Nie ma takiego pliku ani katalogu
pjakusz@p137-03:~$ ls ~/.ssh/
id_rsa  id_rsa.pub  known_hosts
pjakusz@p137-03:~$ cat~/.ssh/id_rsa.pub
bash: cat~/.ssh/id_rsa.pub: Nie ma takiego pliku ani katalogu
pjakusz@p137-03:~$ cat ~/.ssh/id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC/67S13j3VfRqkk4HHdCoBu7VCmw3SiGoQTkXXScPdUWPFMVmIw5MAB6UEpBzPY56exCpPj52kGCCJWK0wSMy57+u0uNwy9EPa/zkkQ0xa7h290z75fCb9G/uxK+3SsR9Zzxdkvrc2u6o8OCcIdJxnm29P4WJPRtmKqAKJX7nFEKHcyrK7Msd6dk1EIbvrpbHcBmr7bxveqSCoqdyHNWOrXReU/a2Xid31KwzoBVPZWq4IIHYgEy4Xpci7Vn0KwZaZcWpCx5fovVih52m39PcolCeLLBMJ8UEO5+1M3+xtuWSuZxkjAgAgoDTEhVcLWJeynY0JIL8ZtTzsqY6zHayx pjakusz@p137-03
pjakusz@p137-03:~$ git clone git@github.com:p0j0/jp.git
Cloning into 'jp'...
You don't exist, go away!
fatal: The remote end hung up unexpectedly
pjakusz@p137-03:~$ git clone git@github.com:p0j0/jp.git
Cloning into 'jp'...
remote: Counting objects: 27, done.
remote: Compressing objects: 100% (22/22), done.
remote: Total 27 (delta 6), reused 0 (delta 0)
Receiving objects: 100% (27/27), 4.37 KiB, done.
Resolving deltas: 100% (6/6), done.
pjakusz@p137-03:~$ cd jp/
pjakusz@p137-03:~/jp$ ls
2III.md  README.md  zaj1
pjakusz@p137-03:~/jp$ git rm zaj1
rm 'zaj1'
pjakusz@p137-03:~/jp$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#  deleted:    zaj1
#
pjakusz@p137-03:~/jp$ ls
2III.md  README.md
pjakusz@p137-03:~/jp$ git commit -m "usunięto plik zaj1"
[master 4b8199a] usunięto plik zaj1
 Committer: Paweł Jakusz <pjakusz@p137-03.labpk.inf.ug.edu.pl>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 2 deletions(-)
 delete mode 100644 zaj1
pjakusz@p137-03:~/jp$ git status
# On branch master
# Your branch is ahead of 'origin/master' by 1 commit.
#
nothing to commit (working directory clean)
pjakusz@p137-03:~/jp$ ls
2III.md  README.md
pjakusz@p137-03:~/jp$ git push
...
