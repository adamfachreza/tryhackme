# Perintah nmap yang sering digunakan

## Scanning Default
 Ini adalah perintah dasar untuk melakukan pemindaian pada target.
    `nmap target`

## Ping Scan
Melakukan pemindaian tanpa port (hanya melakukan ping untuk mengetahui keberadaan host)
    `nmap -sn target`

## TCP SYN Scan
Pemindaian TCP SYN, sering digunakan untuk mendeteksi port yang terbuka.
    `nmap -sU target`

## UDP Scan
Pemindaian UDP, digunakan untuk mendeteksi layanan yang berjalan di atas UDP.
    `nmap -sU target`

## Intense Scan (Aggressive)
Pemindaian intensif dengan mendeteksi versi layanan, sistem operasi, dan melakukan skrip NSE (Nmap Scripting Engine).
    `nmap -A target`

## Operating System Detection
 Melakukan deteksi sistem operasi pada host target.
    `nmap -O target`

## Version Detection
Mendeteksi versi layanan yang berjalan pada port yang terbuka.
` nmap -sV target`

## Service Script Scanning
Menjalankan skrip NSE tertentu untuk melakukan pemindaian lebih lanjut.
`nmap --script <script> target`

## Output to File
Menyimpan hasil pemindaian ke dalam file teks.
`nmap -oN output.txt target`

## Verbose Output
Menampilkan output secara lebih detail.
`nmap -v target`

## Top Port Scan
Melakukan pemindaian pada 10 port teratas yang paling umum.
`nmap --top-ports 10 target`

## Pemindainan Subnet
Melakukan pemindaian pada seluruh subnet.
`nmap 192.168.1.0/24`

## Pemindaian Range Port
Melakukan pemindaian pada range port tertentu.
`nmap -p 1-100 target`

## Pemindaian dengan Traceroute
Melakukan pemindaian dan menampilkan jalur traceroute ke target.
`nmap --traceroute target`


