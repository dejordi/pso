`$ fdisk -l` - wypisywanie zamontowanych dysków

`*` - dysk rozruchowy





`sd[a|b|c...]`- SATA

`hda` - IDE





- MBR - Master Boot Record ( 4 partycje - max 1 rozszerzona (32 logiczne) )

- GPT - Guide Partition Table (128 partycji)





sda1, sda2, sda3, sda4 - partyzcje podstawowe (jedna logiczna)

sda5-36 - partycje logiczne





Patrycja rozszerzona musi mieć o 100MB więcej na obsługe



## fdisk

`$ sudo fdisk /dev/sda/` - program do zarządzania dyskiem

- `p` - informacje o dysku

- `i` - informacje o partycjach (type = file system)
- `t` - zmiana typu partycji

> Na GPT nie utworzymy partycji rozszerzonej!!!

- `n` - nowa partycja ( +rozmiar )

- `d` - usuń partycje

- `g` - konwersja dysku na GPT

- `o` - konwersja dysku na MBR (DoS)

- `w` - zapisz i wyjdź

- `q` - wyjdź bez zapisu


## gdisk - GPT fdisk

- `x` - tryb zaawansowany
- `z` - z GPT do DOSa



## Instalacja przy błędzie!!!

Jak jest błąd przy instalacji to:

```bash
sudo rm /var/lib/dpkg/lock
sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
```

Protip: `sudo find /var -name lock` żeby znaleźć te pliki jak się zapomni

I powtarzać to do skutku, czasami może jeszcze zadziałać po `sudo apt update`



## Mount

`mount` - wyświetlanie wszystkich zamontowanych dysków



## gparted

Fajny program z GUI, trzeba zapisać zmiany 

partycja > utwórz tablice partycji



## mkfs

Trzeba odmontować najpierw dysk!!! (`umount`)

```bash
sudo mkfs /dev/sdb[1-128]
# Jeśli GPT - kontynuujemy


$ mkfs.ext # wyświetla dostępne systemy plików ext

$ sudo mkfs.ext4 -L "zsk" /dev/sdb1 #tworzenie ext4 na /dev/sdb1 z labelem "zsk"

$ sudo mkfs.ntfs /dev/sdb2

$ sudo mkfs.vfat # fat32

$ sudo apt install exfat-utils
$ sudo mkfs.exfat /dev/sdb4
```



## parted

```bash
print - wyświetlenie partycji
print all - wyświetlenie wszystkich dysków

select /dev/sdb - wybranie dysku (jak SQL)

```





##  Pytania

- [ ] <s>`/dev/null`</s> - nie wiadomo

- [x] `dd` - diskdump jest najlepszą opcją
