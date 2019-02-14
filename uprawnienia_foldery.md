`$ su <user>` - zmiana użytkownika

`$ (sudo) passwd <user>` - zmiana hasła 

`sudoers` - lista adminów



`~` - katalog domowy usera

`/` - root, katalog główny

`.` - current directory

`..` - upper directory, nadrzędny



`user@komp: pwd $`

`root@komp: pwd #`



 `$ id <user>` - identyfikator użytkownika

`uid` - user identyfikator, dla roota 0

`gid` - group idenntyfikator, sudo 27, dla każdego użytkownika tworzona jest własna grupa



`$ ls -l` - uprawnienia plików (long)

`$ ls -a` - ukryte pliki



`$ mkdir <name>` - stwórz folder

`mkdir -p` - automatyczne tworzenie folderów (np `mkdir -p test/test/2/test`)



`$ history` - historia komend



`$ cat <plik>` - wyświetlanie zawartości pliku



`$ rm` - usuwanie

`$ rm -r <folder>` - usuwanie folderu



`$ touch <nowy_plik>`



## Uprawnienia



`d` - katalog

`-` - plik

`l` - dowiązanie



`r` - read, 4

`w` - write, 2

`x` - execute, 1



User,  group, other



`$ chmod` - zmiana uprawnien

`$ chown` - zmiana właściciela

`$ chgrp` - zmiana grupy



```bash
chmod a-rwx <plik> #odebranie wszystkich uprawnień

chmod u+rwx,g+r <plik>

chmod -R 777 <folder> #zmiana rekursywna

#-- chown

chown <user> <plik>
chown <user>:<group> <plik>
```

```bash
mkdir -m 740 nowy #nowy katalog z uprawnieniami
```