# pickle rick tryhackme
- langkah pertama yang bisa di lakukan adalah menganalisa source codenya untuk mengetahui bagaiman aplikasi bekerja
- setelah menganalisa source codenya, kita bisa menemukan Username: `R1ckRul3s` di dalam komentar
- lalu jalankan `dirsearch -u <urltarget>` untuk mendapatkan list direktori pada web tersebut
- setelah proses dirsearch selesai, kita mendapatkan 3 direktori yang dapat di akses(assests/login.php/robots.txt) lalu kita coba akses ke 3nya
- di robots.txt kita mendapatkan `Wubbalubbadubdub`, kita tidak tahu ini untuk apa, tapi untuk sekarang kita simpan saja dulu
- di assets tidak ada yang menarik, lalu kita coba login.php menggunakan username  `R1ckRul3s`, dan mungkin passwordnya `Wubbalubbadubdub`
- dan kita berhasil login,kita jalankan perintah `ls` untuk menampilkan direktori yang ada,`Sup3rS3cretPickl3Ingred.txt`,`clue.txt` cukup menarik, coba kita lihat isinya dengan menggunakan `cat namafilenya`
- ternyata di command panel ada beberapa perintah yang di disabled termasuk cat. ok mari kita coba menggunakan less untuk membaca isi filenya
- isi dari `clue.txt` `Look around the file system for the other ingredient.`, isi dari `Sup3rS3cretPickl3Ingred.txt`, `mr. meeseek hair`, mungkin ini salah satu ingredient
- menurut clue.txt, ada ingredient lain di sekitar file sistem, mari kita cari, jika kita jalankan `ls /home`, kita akan mendapatkan rick dan ubuntu, di dalam `/home/rick`, ada direktori second ingredients
- sekarang kita jalankan perintah, `less /home/rick/"second ingredients"` dan kita akan mendapatkan ingredient ke 2 yaitu `1 jerry tear`
- sekarang kita cari ingredient ke 3, mungkin ingredient ke 3 berada di direktori root, coba kita jalankan `sudo -l` untuk melihat daftar perintah sudo yang bisa kita gunakan
- kita bisa menggunakan semua perintah sudo tanpa password kecuali di( env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin)
- sekarang kita cek direktori root, apakah ada ingredient lain, jalankan perintah `sudo ls /root`, disana kita bisa melihat ada file `3rd.txt`
- selanjutnya tinggal kita buka filenya menggunakan `sudo less /root/3rd.txt`, dan ingredient ke3 `3rd ingredients: fleeb juice`