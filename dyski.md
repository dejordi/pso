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

