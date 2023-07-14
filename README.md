# EfsTools ini digunakan untuk mengaktifkan volte pada device pixel,

- mbn yang digunakan default disini hanya untuk operator Telkomsel
- pilih mbn yang lain sesuai dengan operator yang anda gunakan (ada di folder mbn)
- dengan cara ini anda akan dapat mengaktifkan volte dan juga video calling

# tutorial

1. clone git repo ini
2. pilih mbn pada folder mbn
3. copy mbn dan paste kedalam root folder projek ini
4. flash module magisk yang ada didalam folder
5. eksekusi command ini

adb shell
su
resetprop ro.bootmode usbradio
resetprop ro.build.type userdebug
setprop sys.usb.config diag,diag_mdm,adb

6. ubah usb config, file transfer <-> no transfer file
7. eksekusi ini

EfsTools.exe efsInfo

8. jika ada error, pilih saja download dan install aplikasi yang di perlukan, sampai tidak ada error
9. eksekusi ini

EfsTools.exe writeFile -i mcfg_autoselect_by_uim -o /nv/item_files/mcfg/mcfg_autoselect_by_uim
EfsTools.exe writeFile -i mcfg_autoselect_by_uim -o /nv/item_files/mcfg/mcfg_autoselect_by_uim -s 1

EfsTools.exe uploadDirectory -i mcfg_sw.mbn -o / -v
EfsTools.exe uploadDirectory -i mcfg_sw.mbn -o / -s 1

10. -s 1 ini untuk sim kedua bila ingin mengaktikfkan volte nya juga
11. restart, dan volte sudah aktif

# ask me on telegram [@riloraspopo](https://t.me/riloraspopo)
