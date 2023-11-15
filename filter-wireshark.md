# Filter Wireshark

## Berdasarkan Protokol

Menampilkan hanya paket TCP.`tcp`
Menampilkan hanya paket UDP. `udp`
Menampilkan hanya paket ICMP. `icmp`

## Berdasarkan IP

Menampilkan paket yang melibatkan alamat ip tertentu `ip.addr == ip-add`
menampilkan hanya paket yang berasal dari alamat ip tertentu `ip.src == ip-add`
menampilkan hanya paket yang ditujukan ke alamat ip tertentu `ip.dst == ip-add`

## Berdasarkan port
hanya paket TCP yang melibatkan port 80 `tcp.port == 80`
hanya paket UDP yang melibatkan port 53 `udp.port == 53`

## Berdasarkan Hostname
Menampilkan hanya paket `dns`
Menampilkan hanya paket HTTP yang terkait host tertentu `http.host == "www.example.com"`

## Berdasarkan MAC Address
Menampilkan hanya paket yang melibatkan alamat MAC tertentu `eth.addr == macaddress`

## Berdasrkan Jenis Trafik
menampilkan hanya paket ICMP Echo Request `icmp.type == 8`
menampilkan hanya paket ICMP Echo Reply `icmp.type == 0`

## Berdasarkan Teks dalam Payload
menampilkan paket yang payload-nya mengandung kata "username" `frame contains "username"`

## Kombinasi
menampilkan hanya paket tcp yang melibatkan ip dan port 80 `ip.addr == 192.168.1.1 && tcp.port == 80`

## Berdasarkan Ranges dan Notasi CIDR
menampilkan paket yang berasal dari subnet tertentu `ip.src in 192.168.1.0/24`

## Berdasarkan Waktu
menampilkan paket yang muncul setelah 5 detik `frame.time_relative > 5`

## Berdasarkan Protocol Hierarki
hanya menampilkan http `http`
hanya menampilkan paket dengan RTT akumulasi lebih dari 0.1 detik `tcp.analysis.ack_rtt > 0.1`

## Berdasarkan Status Tautan
menampilkan hanya paket yang merupakan jenis manajemen 802.11 untuk asosiasi `wlan.fc.type_subtype == 0x0008`

## Berdasarkan Teks di URL
 Menampilkan paket HTTP di mana URL permintaan mengandung kata "login"
 `http.request.uri contains "login"`
 Menampilkan respon HTTP dengan status 200 dan payload yang mengandung kata "success". `http.response.code == 200 and frame contains "success"`

 ## Berdasarkan Port Range
 Menampilkan paket TCP yang melibatkan salah satu dari port 80, 8080, atau 443.`tcp.port in {80 8080 443}`
