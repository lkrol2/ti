<b>
Dodawanie klucza publicznego do github.com za pomoca Terminal Guake<b><br>
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
* podaje klucz prywatny id_rsa i publiczny id_rsa.pub

```c
pjakusz@p137-03:~$ ls ~/.ssh/
id_rsa  id_rsa.pub  known_hosts
```
* trzeba pokazać klucz id_rsa.pub

```c
pjakusz@p137-03:~$ cat ~/.ssh/id_rsa.pub
```
* wyswietli

```c
ssh-rsa AAASMy57+u0uNwy9EPa/zkkQ0xa7h290z75fCb9G/uxK+3SsR9Zzxdkvrc2u6o8OCcIdJxnm29P4WJPRtmKqAKJX7nFEKHcyrK7Msd6dk1EIbvrpbHcBmr7bxveqSCoqdyHNWOrXReU/a2Xid31KwzoBVPZWq4IIHYgEy4Xpci7Vn0KwZaZcWpCx5fovVih52m39PcolCeLLBMJ8UEO5+1M3+xtuWSuZxkjAgAgoDTEhVcLWJeynY0JIL8ZtTzsqY6zHayx pjakusz@p137-03
```
* kopujemy całosc i wklejamy do key w github.com
* clonujemy rspozytorium do komputera
* kopiujemy ades po nacisnieciu SSH na respozytorium pj czyli to 
<br>git@github.com:p0j0/jp.git <br>za pomoca <b>git clone<b>

```c
pjakusz@p137-03:~$ git clone git@github.com:p0j0/jp.git
```
* otrzymujemy

```c
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
```
* wejscie do repozytorium jp

```c
pjakusz@p137-03:~$ cd jp/
```
* listowanie pliki

```c
pjakusz@p137-03:~/jp$ ls
2III.md  README.md  zaj1
```
* usuwanie pliku <b>git rm<b>

```c
pjakusz@p137-03:~/jp$ git rm zaj1
rm 'zaj1'
```
* sprawdzamy status

```c
pjakusz@p137-03:~/jp$ git status
# On branch master
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#  deleted:    zaj1
#
```
* koniecznie trzeba napisac komentarz uzywajac <b>get commit -m "tekst"<b><br>bo inaczej nie zapisze zmian

```c
pjakusz@p137-03:~/jp$ git commit -m "usunięto plik zaj1"
```
* otrzymamy

```c
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
```
* połączenie z github i przeniesienie zmian

```c
pjakusz@p137-03:~/jp$ git push
...

