# Panel_Server

Panel Server yang berhasil di instal
- [Aapanel](https://www.aapanel.com/new/index.html)
- [CyberPanel](https://www.aapanel.com/new/index.html)
- [Webuzo](https://www.aapanel.com/new/index.html)


## Installation Aapanel
Installation Command

Centos
```sh
yum install -y wget && wget -O install.sh http://www.aapanel.com/script/install_6.0_en.sh && bash install.sh aapanel
```

Ubuntu/Deepin
```sh
wget -O install.sh http://www.aapanel.com/script/install-ubuntu_6.0_en.sh && sudo bash install.sh aapanel
```

Debian
```sh
wget -O install.sh http://www.aapanel.com/script/install-ubuntu_6.0_en.sh && bash install.sh aapanel
```
Akan muncul Do you want to install aaPanle to the /www directory now?. Ketik `Y` untuk melanjutkan proses instalasi.

## Installation CyberPanel

Langkah 1 : Update Server

Ubuntu :
```sh
sudo apt update && sudo apt upgrade -y
```
CentOS/Alma/Rocky :
```sh
sudo yum check-update
sudo yum update
```
Langkah 2 : Install CyberPanel
```sh
sh <(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)
```
Jika karena alasan tertentu Anda tidak dapat masuk sebagai root, Anda dapat menggunakan perintah ini
```sh
sudo su - -c "sh <(curl https://cyberpanel.net/install.sh || wget -O - https://cyberpanel.net/install.sh)"
```
Langkah 3 : Pilih versi LiteSpeed yang ingin di gunakan

Pilih versi LiteSpeed yang akan diinstal. Jika Anda memilih LiteSpeed Enterprise, pastikan Anda telah memperoleh kunci lisensi terlebih dahulu. Ini gratis untuk 1 domain, tetapi Anda masih perlu mendapatkan kuncinya.
```sh
CyberPanel Installer v2.1.2

RAM check : 184/981MB (18.76%)

Disk check : 7/30GB (27%) (Minimal 10GB free space)

1. Install CyberPanel with OpenLiteSpeed.

2. Install Cyberpanel with LiteSpeed Enterprise.

3. Exit.


  Please enter the number[1-3]:
```
Langkah 4 : Pilih opsi dan add-on

`Full Service (default Y):`
```sh
PowerDNS - open-source DNS server
Postfix  - open-source mail transfer agent
Pure-FTPd - open-source FTP server
```
`Remote MySQL (default N):`
```sh
Izinkan Database Anda diinstal pada server jarak jauh
```
`CyberPanel Version (default Latest Version):`
```sh
Anda dapat memilih untuk menginstal CyberPanel versi sebelumnya, atau tekan Enter untuk menginstal versi terbaru
```
`Password (default “1234567”):`
```sh
Disarankan agar Anda menggunakan “s” untuk mengatur kata sandi Anda sendiri yang kuat
```
`Memcached (default Y):`
```sh
Sistem caching objek memori terdistribusi
```
`Redis (default Y):`
```sh
Penyimpanan struktur data dalam memori, digunakan sebagai database, cache, dan pesan rusak
```
`Watchdog (default Yes):`
```sh
Pengawas kernel digunakan untuk memantau apakah suatu sistem sedang berjalan. Seharusnya secara otomatis me-reboot sistem yang hang karena kesalahan perangkat lunak yang tidak dapat dipulihkan
```
Langkah 5 : Installation

Proses instalasi akan berjalan secara otomatis. Ini akan memakan waktu 5-10 menit, tergantung kecepatan server Anda.

Langkah 6 : Finalize Installation

Di akhir proses instalasi, Anda akan disajikan layar berikut yang berisi informasi penting tentang konfigurasi Anda. Pilih dan salin ke lokasi yang aman untuk referensi di masa mendatang.

```sh
###################################################################
                CyberPanel Successfully Installed

                Current Disk usage : 7/30GB (26%)

                Current RAM  usage : 313/981MB (31.91%)

                Installation time  : 0 hrs 11 min 0 sec

                Visit: https://<your server's IP address>:8090
                Panel username: admin
                Panel password: <the password you set during installation>
                Visit: <your server's IP address>:7080
                WebAdmin console username: admin
                WebAdmin console password: TSXMwny4zVeDg37K

                Visit: https://<your server's IP address>:8090/rainloop/?admin
                Rainloop Admin username: admin
                Rainloop Admin password: gQKFWm9O3nr7Xn

             Run cyberpanel help to get FAQ info
             Run cyberpanel upgrade to upgrade it to latest version.
             Run cyberpanel utility to access some handy tools .

              Website : https://www.cyberpanel.net
              Forums  : https://forums.cyberpanel.net
              Wikipage: https://docs.cyberpanel.net
              Docs    : https://cyberpanel.net/docs/

            Enjoy your accelerated Internet by
                CyberPanel & OpenLiteSpeed
###################################################################
If your provider has a network-level firewall
Please make sure you have opened following port for both in/out:
TCP: 8090 for CyberPanel
TCP: 80, TCP: 443 and UDP: 443 for webserver
TCP: 21 and TCP: 40110-40210 for FTP
TCP: 25, TCP: 587, TCP: 465, TCP: 110, TCP: 143 and TCP: 993 for mail service
TCP: 53 and UDP: 53 for DNS service
Your provider seems blocked port 25 , E-mail sending may not work properly.
```

Langkah 7 : Restart Server

`Would you like to restart your server now? [y/N]:`
Masukkan “y” untuk memulai kembali. Atau masukkan “reboot” nanti setelah Anda melakukan operasi lain yang diinginkan.

Langkah 8 : Access CyberPanel

Setelah instalasi berhasil, Anda dapat mengakses CyberPanel menggunakan rincian di bawah ini (pastikan untuk mengubahnya):

```sh
URL: https://<Your Server's IP Address>:8090 
Username: admin
Password: <the password you set during installation>
```

## Installation Webuzo

Installation 
```sh
wget -N https://files.webuzo.com/install.sh
```
```sh
chmod 0755 install.sh 
```
```sh
./install.sh
```

Default Apps
`Parameter --install bersifat opsional dan jika tidak dilewati, Webuzo akan menginstal aplikasi berikut secara default:
Apache 2.4, MySQL 8.0, PHP 7.3, Pure-FTPd, Bind, Exim, Dovecot, GIT, Web Disk`

`Jika Anda ingin Webuzo menginstal aplikasi default, silakan gunakan perintah berikut:`
```sh
./install.sh
```

No Apps
```sh
./install.sh --install=none
```

Selected Apps
```sh
./install.sh --install=apache2,mariadb108,bind,exim,dovecot,php81,php80,php74
```
`Web Servers`
- apache2
- openlitespeed
- lsws
- nginx
- nodejs
- nodejs14
- nodejs16
- nodejs17
- nodejs18
- nodejs19

`Database Servers`
- mysql80
- mysql57
- mariadb109
- mariadb108
- mariadb107
- mongodb
- pgsql
- sqlite

`Scripting Languages`
- php82
- php81
- php80
- php74
- php73
- php72
- php71
- perl
- python2
- python3

`Utilities`
- exim
- dovecot
- bind
- pureftpd
- sa (SpamAssasin)
- jailshell
- webdisk
- varnish
- django
- passenger

`Security`
- csf
- clamav
- cxs
- ImunifyAV
- ImunifyAV+
- Imunify360

Select Mirror (Optional)
Anda dapat mengatur mirror untuk mengunduh aplikasi, berikut adalah daftar mirror kami :
s0, s1, s2, s3, s4, s5, s7, s8
Contoh:
```sh
./install.sh --mirror=s8
```
Login To The Admin Panel
```sh
Untuk login ke Panel Admin Webuzo, kunjungi URL berikut :
https://IP-Anda:2005/
ATAU
http://IP-Anda:2004/
Nama pengguna dan kata sandi akan menjadi detail kredensial root server Anda.
```

## Merubah Root

Untuk mengganti password pengguna root di Ubuntu, jalankan perintah berikut sebagai pengguna sudo:
```sh
sudo passwd root
```
Ketika Anda mengetikkan Password, maka password tidak ditampilkan di layar.
```sh
Outuput

Enter new UNIX password:
Retype new UNIX password:
passwd: password updated successfully
```
Menonaktifkan akun root
```sh
sudo passwd -dl root
```
Atau
```sh
sudo passwd --delete --lock root
```
Tambah user
```sh
sudo adduser nama_user
```
Mengubah password user tertentu
```sh
sudo passwd nama_user
```
Tambahkan user ke grup sudo
```sh
sudo usermod -aG sudo nama_user
```
Uji akses sudo
```sh
sudo ls
```







