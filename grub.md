## Grub2

(recovery mode)



`/etc/default/grub` - plik konfiguracyjny gruba



`GRUB_TIMEOUT` - czas na wybór, -1 dla wymuszenia wybrania, 0 = 10s

`GRUB_DEFAULT` - domyślny system (id od 0)



`$ sudo update-grub` - aktualizacja ustawień gruba



`/etc/grub.d/` - katalog z konfiguracjami pozycji menu, jak odejmiemy wykonywanie to nie pojawi się w menu gruba

Numery w nazwach plików mówią o kolejności (`mv`)



`/boot/grub/grub.cfg` - plik konfiguracyjny gruba, tutaj można zmienić nazwę opcji



`/etc/grub.d/05_debian_theme` - do wyglądu

nie ma koloru `gray` , jest tylko `light-gray` lub `dark-gray`

`set menu_color_normal={text}/{bg}`



`/boot/grub/` - tutaj skopiować zdjęcie na tło











