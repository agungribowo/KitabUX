# Mikrotik



{% tabs %}
{% tab title="Setting Dasar Hotspot Mikrotik" %}
Router Mikrotik memiliki banyak fitur, salah satu fitur yang cukup populer dan banyak digunakan adalah Hotspot. Kita sering menemukan sinyal internet _wifi_ yang di _password_. Jadi jika ingin mengakses _wifi tersebut_ harus tahu _password_-nya terlebih dahulu. Namun berbeda dengan Hotspot, kebanyakan _wifi_ hotspot tidak di _password_ dan semua user bisa _connect_ dan akan diarahkan ke halaman login di Web Browser. Tiap user bisa login dengan _username_ dan _password_ yang berbeda-beda. Metode semacam inilah yang sering kita temukan di Kampus, wifi Cafe, Sekolah, Kantor, maupun area publik lainnya.

Sebenarnya hotspot tidak hanya bisa diaplikasikan untuk jaringan wireless saja, namun juga bisa untuk jaringan kabel. Kelebihan Hotspot adalah kita dapat mengkonfigurasi jaringan yang hanya bisa digunakan dengan username dan password tertentu. Kita juga dapat melakukan manajemen terhadap user-user tersebut. Misalnya, mengatur durasi total penggunaan hotspot per user, membatasi berapa besar data yang dapat di download tiap user, mengatur konten apa saja yang boleh diakses user, dll.

Hotspot merupakan fitur gabungan dari berbagai service yang ada di Mikrotik, antara lain :

* DHCP server, digunakan untuk memberi layanan IP otomatis ke user
* Firewall NAT, untuk mentranslasi IP user ke IP yang bisa dikenali ke internet
* Firewall filter, untuk memblock user yang belum melakukan login
* Proxy, untuk memberikan tampilan halaman login
* dan sebagainya

Tetapi beruntungnya, service-service tersebut tidak perlu kita buat secara manual. Bagaimana langkahnya, bisa dijabarkan sebagai berikut :

Buka di menu **IP &gt; Hotspot &gt; Hotspot Setup.**

![Hotspot Setup](.gitbook/assets/image%20%2818%29.png)

Dengan menekan tombol Hotspot Setup, wizard Hotspot akan menuntun kita untuk melakukan setting dengan menampilkan kotak-kotak dialog pada setiap langkah nya.

![seting wlan1](.gitbook/assets/image%20%287%29.png)

Langkah pertama, kita diminta untuk menentukan interface mana Hotspot akan diaktifkan. Pada kasus kali ini, Hotspot diaktifkan pada wlan1, dimana wlan1 sudah kita set sebagai access point \(ap-bridge\). Selanjutnya klik Next.

![set access point](.gitbook/assets/image%20%288%29.png)

Jika di interface wlan1 sudah terdapat IP, maka pada langkah kedua ini, secara otomatis terisi IP Address yang ada di wlan1. Tetapi jika belum terpasang IP, maka kita bisa menentukan IP nya di langkah ini. Kemudian Klik Next.

![](.gitbook/assets/image%20%2812%29.png)

Langkah ketiga, tentukan range IP Address yang akan diberikan ke user \(DHCP Server\). Secara default, router otomatis memberikan range IP sesuai dengan prefix/subnet IP yang ada di interface. Tetapi kita bisa merubahnya jika dibutuhkan. Lalu klik Next.

![](.gitbook/assets/image%20%2810%29.png)

Langkah selanjutnya, menentukan SSL Certificate jika kita akan menggunakan HTTPS untuk halaman loginnya. Tetapi jika kita tidak memiliki sertifikat SSL, kita pili**h** none, kemudian klik Next

![](.gitbook/assets/image%20%281%29.png)

Jika diperlukan SMTP Server khusus untuk server hotspot bisa ditentukan, sehingga setiap request SMTP client diredirect ke SMTP yang kita tentukan. Karena tidak disediakan smtp server, IP 0.0.0.0 kami biarkan default. Kemudian klik Next.

![](.gitbook/assets/image%20%284%29.png)

Di langkah ini, kita meentukan alamat DNS Server. Anda bisa isi dengan DNS yang diberikan oleh ISP atau dengan open DNS. Sebagai contoh, kita menggunakan DNS Server Google. Lalu klik Next.

![](.gitbook/assets/image%20%286%29.png)

Selanjutnya kita diminta memasukkan nama DNS untuk local hotspot server. Jika diisikan, nantinya setiap user yang belum melakukan login dan akan akses ke internet, maka browser akan dibelokkan ke halaman login ini. Disini DNS name sebaiknya menggunakan format FQDN yang benar. Jika tidak diisikan maka di halaman login akan menggunakan url IP address dari wlan1. Pada kasus ini, nama DNS-nya diisi "hotspot.mikrotik.co.id". Lalu klik Next.

![](.gitbook/assets/image%20%2817%29.png)

Langkah terakhir, tentukan username dan pasword untuk login ke jaringan hotspot Anda. Ini adalah username yang akan kita gunakan untuk mencoba jaringan hotspot kita.

Sampai pada langkah ini, jika di klik Next maka akan muncul pesan yang menyatakan bahwa _setting_ Hotspot telah selesai.

![](.gitbook/assets/image%20%285%29.png)

Selanjutnya kita akan mencoba mengkoneksikan laptop ke wifi hotspot yang sudah kita buat. Kemudian buka browser dan akses web sembarang \(pastikan Anda mengakses web yang menggunakan protokol http, karena hotspot mikrotik belum mendukung untuk redirect web yang menggunakan https\), maka Anda akan dialihkan ke halaman login hotspot seperti pada gambar berikut ini:

![](.gitbook/assets/image%20%2811%29.png)

Untuk mencobanya, silahkan coba login dengan username dan password yang telah Anda buat pada langkah sebelumnya. Jika berhasil login maka akan membuka halaman web yang diminta dan membuka popup halaman status Hotspot.
{% endtab %}

{% tab title="Fitur-Fitur Hotspot Mikrotik" %}
Tidak ada habisnya kalau mengulas implementasi fitur-fitur Mikrotik. Salah satu dari sekian banyak fitur yang banyak digunakan adalah Hotspot.

Sudah banyak yg mengimplementasikan fitur Hotspot Mikrotik di lapangan, mungkin anda salah satunya.

Kebanyakan orang menyebut jika terdapat akses internet yg di sebarkan via wireless di public area \(cafe,mall,dsb\) itu adalah layanan Hotspot, Sedangkan sebenarnya Hotspot di Mikrotik adalah sebuah system untuk memberikan fitur autentikasi pada user yang akan menggunakan jaringan. Jadi untuk bisa akses ke jaringan, client diharuskan memasukkan username dan password pada login page disediakan.

Dari penjelasan diatas, berarti Hotspot tidak hanya menunjuk ke jaringan wireless saja. Fitur Hotspot ini bisa diterapkan di semua tipe interface jaringan seperti ethernet base.

![](.gitbook/assets/image.png)

Untuk membangun sistem authentikasi pada Hotspot, sebenarnya Hotspot merupakan gabungan dari fungsi Proxy, Firewall, DNS, DHCP dan lain-lain. Tetapi anda untuk membuat sebuah hotspot server tidak perlu khawatir akan kekomplekan fungsi tersebut karena di Mikrotik anda diberikan "Bantuan" dalam bentuk Setup Wizard untuk membuatnya.  


Selain authentikasi, Hotspot pada Mikrotik juga mempunyai banyak fitur yang cukup menarik untuk diimplementasikan di jaringan anda. Fitur apa saja itu, mari kita ulas :  
  
**Limitasi**  
Dengan menggunakan hotspot server di jaringan anda, anda nanti bisa melakukan limitasi berdasarkan berapa lama user akses jaringan \(_**uptime**_\), kecepatan akses \(_**data rate**_\), banyak data yang sudah digunakan \(_**quota based**_\), bahkan kebijakan _**policy firewall**_.  
Limitasi ini bisa diterapkan per user atau mungkin per group dari jaringan anda.

![](.gitbook/assets/image%20%289%29.png)

**Plug n Play Connectivity**  
Apakah anda pernah mengalami repotnya merubah-rubah IP setiap terkoneksi ke jaringan wireless orang lain? Atau mungkin ada kasus di perangkat User memiliki security yang mengakibatkan user tersebut tidak diijinkan merubah-rubah IP pada perangkatnya? Dengan menggunakan Hotspot Server, anda tidak perlu mengkhawatirkan hal itu lagi. User bisa menggunakan sembarang IP statik di perangkatnya atau DHCP, nanti secara otomatis Hotspot server akan melakukan _**one to one nat**_ agar client tersebut bisa akses ke jaringan kita.

![](.gitbook/assets/image%20%283%29.png)

**Bypass**  
Normalnya, semua koneksi dari berbagai perangkat yang ada dijaringan Hotspot kita akan diblock sebelum melakukan login / autentikasi ke hotspot server. Tetapi tidak semua perangkat bisa melakukan sistem autentikasi tersebut, misalnya : Printer server, IP Cam, VoIP server dan sebagainya. Atau ada user VIP yang memang istimewa tidak perlu melakukan login.  


Untuk perangkat-perangkat yang ingin anda bypass , tidak perlu melakukan login untuk akses ke jaringan, anda bisa menggunakan fitur yang namanya IP Binding.

![](.gitbook/assets/image%20%2814%29.png)

Atau bisa juga anda mempunyai kebijakan, untuk mengakses resource di jaringan lokal anda sendiri \(halaman web perusahaan / web server, mail server, file server dan sebagainya\) tidak perlu melakukan login. Tetapi pada saat user ingin akses ke internet \(misalnya browsing ke yahoo, facebook dan sebagainya\) baru anda minta user tersebut untuk melakukan login. Fitur yang bisa anda gunakan untuk hal tersebut dinamakan **Walled Garden**

![](.gitbook/assets/image%20%2816%29.png)

**Advertisement**  
Dengan menggunakan fitur _advertisement_ pada Hotspot server, anda bisa menampilkan _popup_ halaman sebuah web ke user anda dan _popup-popup_ yang akan muncul bisa anda atur intervalnya.

  
**Trial User**  
Mungkin bagi anda yang berkecimpung di dunia jasa layanan internet, ingin memberikan masa trial / uji coba ke calon pelanggan anda, dengan tujuan meyakinkan kualitas jaringan anda. Nah, di Hotspot server ini terdapat fungsi trial yang memungkinkan user tidak perlu melakukan login sampai batas waktu yang ditentukan. Setelah itu baru user diwajibkan untuk melakukan login.  
Biasanya dilapangan fungsi trial ini dikombinasikan dengan fungsi advertisement sebelumnya untuk membuat ajang promosi didalam layanan jasa internet **.**

![](.gitbook/assets/image%20%282%29.png)

**Voucher**  
Sudah pernah membeli voucher pulsa GSM? atau mungkin layanan internet di hotel-hotel yang mengharuskan kita meminta voucher di petugas?  
di Hotspot Mikrotik, anda juga bisa membuat sistem voucher prabayar untuk calon pelanggan jasa internet anda. Anda tentukan harga dan jenis / detil limitasinya, nanti setiap ada calon pelanggan yang datang anda tinggal generate voucher yang akan berisi custom username dan password.

![](.gitbook/assets/image%20%2815%29.png)

Bagaimana? cukup banyak fitur didalam hotspot yang bisa kita gunakan untuk menarik minat calon pelanggan kita bukan? Di artikel ini kami memang tidak akan membahas bagaimana cara membuat hotspot server, tetapi jika anda tertarik Cara membuat Hotspot server pada Mikrotik bisa dilihat pada artikel berikut
{% endtab %}
{% endtabs %}







