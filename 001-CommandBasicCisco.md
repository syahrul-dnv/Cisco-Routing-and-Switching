# Cisco Systems, Inc. 
Adalah perusahaan jaringan terbesar di dunia yang mengembangkan, memproduksi dan menjual perangkat keras jaringan, peralatan telekomunikasi dan layanan serta teknologi lainnya. Cisco memiliki banyak anak perusahaan yang di akuisisi di antaranya layanan yang menawarkan fungsi DNS seperti <b>OpenDNS, WebEx, Jabber dan Jasper</b>, Cisco mengkhususkan diri ke pasar teknologi tertentu, seperti <b>Internet of Things (IoT),</b> keamanan domain dan manajemen energi.

Cisco memproduksi berbagai perangkat keras, perangkat lunak, hingga sistem operasi sendiri untuk produk yang di tawarkannya, salah satunya adalah Cisco Router dengan sistem operasi Cisco IOS (Internet Operating system), dalam artikel kali ini kita akan membahas perintah dasar cisco khususnya pada perangkat Cisco Router dengan sistem operasi Cisco IOS atau Anda dapat mempraktikannya menggunakan emulator jaringan yang powerfull bernama Cisco Packet Tracer.

<pre>1. router>enable</pre>

Secara default, CLI (Command Line Interface) akan masuk ke mode user, tandanya adalah simbol “>” yang ada di bagian depan nama host (dalam hal ini “router”), pada mode user Anda tidak dapat mengkonfigurasi apapun, oleh karena itu Anda perlu beralih ke mode privileged (juga di kenal sebagai EXEC-level mode) dengan perintah “router>enable” kemudian tekan Enter, apabila perintah berhasil tereksekusi, maka simbol di depan nama host akan berubah menjadi “#” (misalnya “router#”).

<pre>2. router#show ?</pre>

Perintah “router#show ?” di gunakan untuk melihat daftar perintah yang tersedia untuk di eksekusi.

<pre>3. router#show running-config</pre>

Perintah “router#show running-config” di gunakan untuk menampilkan file konfigurasi yang sedang di jalankan pada RAM.

<pre>4. router#show startup-config</pre>

Perintah “router#show startup-config” di gunakan untuk menampilkan file konfigurasi yang di jalankan saat startup, file konfigurasi tersebut di simpan pada NVRAM (Non Volatile Random Access Memory), berbeda dengan SRAM (Static Random Access Memory) atau DRAM (Dynamic Random Access Memory). Penyimpanan data yang dilakukan saat daya listrik mengalir, NVRAM tetap menyimpan file konfigurasi sekalipun perangkat router di matikan.

Perlu di ingat bahwa NVRAM tidak sama dengan Flash SIMM (Single In-line Memory Module). Perbedaan antara NVRAM sama dengan Flash SIMM seperti perbedaan RAM dan hardisk drive (walaupun pada kenyataannya RAM dengan NVRAM juga berbeda), Flash SIMM sendiri lebih mirip hard disk drive yang menyimpan file sistem operasi Cisco IOS dan file lain yang di perlukan.

<pre>5. router#copy running-config startup-config</pre>

Perintah “router#copy running-config startup-config” di gunakan untuk menyimpan pengaturan yang sedang berjalan (running connfiguration) pada RAM ke NVRAM sehingga dapat di terapkan pada saat router di nyalakan (start-up).

<pre>6. router#erase startup-config</pre>

Perintah “router#erase startup-config” di gunakan untuk menghapus file konfigurasi yang di simpan pada NVRAM (Non Volatile Random Access Memory)

<pre>7. router#copy running-config tftp</pre>

Selain menyimpan running-config ke startup-config, Anda juga dapat meyimpan running-config ke TFTP Server secara remote (jarak jauh), caranya cukup dengan mengeksekusi perintah “router#copy running-config tftp”.

<pre>8. router#show users</pre>

Perintah “router#show users” di gunakan untuk menampilkan pengguna yang sedang terhubung ke jaringan (router) yang bersangkutan.

<pre>9. router #show arp</pre>

Perintah “router #show arp” di gunakan untuk menampilkan tabel ARP, ARP atau Address Resolution Protocol merupakan sebuah protokol yang memetakan fungsi IP address ke alamat fisik mesin (di kenal juga sebagai alamat MAC) yang di kenali oleh jaringan lokal. Tabel ARP atau di kenal juga dengan sebutan ARP Cache di gunakan untuk memelihara korelasi antara alamat MAC dengan alamat IP.

<pre>10. router #show history</pre>

Perintah “router #show history” di gunakan untuk menampilkan riwayat perintah yang telah di eksekusi sebelumnya, perintah ini akan sangat berguna jika Anda hendak mengulangi perintah serupa tanpa mengetik ulang perintahnya.

<pre>11. router#show interfaces</pre>

Perintah “router#show interfaces” di gunakan untuk menampilkan statistik dari semua interface yang tersedia, perintah “router#show interfaces” akan menampilkan informasi yang mencakup interface, status interface (baik fisik maupun data link), dan IP address. Perintah “router#show interfaces” juga mencakup informasi tambahan termasuk subnet mask IP interface, pengaturan bandwidth, pengaturan delay, konfigurasi antrian, informasi protokol data link (dalam hal ini tipe duplex, ARP), dan sejumlah counter yang  berbeda yang dapat di gunakan untuk memantau interface.

<pre>12. router#show host</pre>

Perintah “router#show host” di gunakan untuk menampilkan cache dari host yang tersedia.

<pre>13. router#show flash</pre>

Perintah “router#show flash” di gunakan untuk menampilkan informasi mengenai memori Flash yang terdapat pada perangkat router Cisco. Informasi yang di tampilkan termasuk file yang ada di dalamnya, ruang kosong, ruang yang di gunakan, total ruang (kapasitas) yang tersedia hingga ukuran ‘processor board System Flash’.

<pre>14. router#show protocols</pre>

Perintah “router#show protocols” menunjukkan status protokol layer ketiga pada perangkat yang telah di konfigurasi. Layer ketiga yang di maksud adalah bagian dari model OSI layer, layer ketiga adalah network layer, fungsi network layer salah satunya adalah menyediakan sarana fungsional dan prosedural untuk mentransfer data ke node lain yang terhubung dalam jaringan yang berbeda, router adalah salah satu perangkat yang bekerja di layer ketiga ini.

<pre>15. router#show ip interface</pre>

Perintah “router#show ip interface” di gunakan untuk menampilkan informasi mengenai pengaturan IP interface secara lengkap, termasuk alamat IP dan informasi mask, access list configuration (ACL), jenis switching yang digunakan (bagaimana lalu lintas IP di proses oleh perangkat), pengaturan kompresi, dan lain sebagainya.

<pre>16. router#show ip interface brief</pre>

Perintah “router#show ip interface brief” di gunakan untuk menampilkan output dari status IP address suatu interface secara ringkas. Informasi penting yang akan di tampilkan meliputi interface, IP address dari interface tersebut, status (secara fisik) dan status protokol (data link).

<pre>17. router#show ip protocol</pre>

Perintah “router#show ip protocol” di gunakan saat protokol routing dinamis di jalankan pada perangkat. Output dari perintah ini dapat digunakan untuk memverifikasi konfigurasi protokol routing sedang di proses seperti yang di harapkan. Output yang tepat dari perintah ini bergantung pada dynamic routing protocol yang di konfigurasi.

<pre>18. router#show ip route</pre>

Perintah “router#show ip route” di gunakan untuk menampilkan konten tabel routing IP saat ini. Output dari perintah “router#show ip route” bisa sangat lama ketika beberapa jaringan di kelola oleh satu perangkat.

<pre>19. router#show logging</pre>

Perintah “router#show logging” di gunakan untuk verifikasi beberapa hal yang di anggap tidak sesuai. Perintah “router#show logging” dapat mengakses log dan menampilkannya. Dengan begitu Anda dapat mem-verifikasi apabila terdapat beberapa hal yang di anggap tidak sesuai (biasanya antara konfigurasi yang di terapkan dengan hasil yang di harapkan yang tidak sesuai).

<pre>20. router#show clock</pre>

Perintah “router#show clock” di gunakan untuk menampilkan jam dari sistem saat ini, ingat bahwa router Cisco menggunakan sistem operasi tersendiri sehingga jam pada sistem Cisco dengan jam pada sistem Host mungkin berbeda, mencocokkan jam pada keduanya berguna untuk singkronisasi log sehingga memudahkan verifikasi.

<pre>21. router#ping</pre>

Perintah “router#ping” di gunakan untuk memverifikasi ketergapaian (reachability) host tujuan dengan mengirim lima paket ICMP (Internet Control Message Protocol) ke host tujuan, dan host tujuan akan mengembalikan atau menjawab kiriman tersebut dengan paket yang serupa.

<pre>22. router#traceroute</pre>

Perintah “router#traceroute” di gunakan untuk memverifikasi operasi jaringan dengan mengirimkan paket sesuai jalur yang telah di tentukan dari jalur sumber ke jalur tujuan yang memanfaatkan fungsi TTL (Time to Live) yang terdapat pada IP header, prinsipnya sama dengan perintah “router#ping”, apabila host tujuan tidak merespon (paket tidak sampai ke tujuan) maka pesan “unreachable” (tak tergapai).

<pre>23. router#show version</pre>

Perintah “router#show version” di gunakan untuk menampilkan versi Cisco IOS (Internet Operating System) yang di gunakan.

<pre>24. router#configure terminal</pre>

Jika Anda perhatikan, perintah di atas hanya untuk melihat atau menampilkan informasi tertentu (beberapa ada yang di gunakan untuk meng-copy), untuk dapat mengkonfigurasi router misalnya mengubah running-configuration Anda harus masuk ke Global Configuration Mode, lihat kembali perintah “router#copy running-config startup-config” pada poin ke 5 dan perintah “router#copy running-config tftp” ke 7, di sana hanya menjelaskan mengenai perintah untuk menyimpan running-config ke startup-config atau tftp, cara mengkonfigurasi running-config itu sendiri belum di paparkan.

Untuk dapat melakukan konfigurasi, Anda harus mengeksekusi perintah “router#configure terminal” untuk masuk ke Global Configuration Mode, indikator pada nama host nantinya akan berubah menjadi “router(config)#” yang artinya Anda telah masuk ke Global Configuration Mode.

<pre>25. router(config)#hostname</pre>

Perintah “router(config)#hostname” di gunakan untuk mengganti nama host, secara default host bernama “router”, untuk menggantinya dengan nama lain misalnya “dosenit”, cukup ketikkan perintah “router(config)#hostname dosenit” dan indikator pada CLI akan berubah menjadi “dosenit(config)#”.

<pre>26. router(config)#banner motd</pre>

Perintah “router(config)#banner motd” di gunakan untuk menambahkan MotD (Message of the Day) sebagai banner, pesan tersebut nantinya akan tampil pada antarmuka pengguna yang mengakses antarmuka router, pesan dapat di tambahkan dengan perintah “router(config)#banner motd # isi pesan #”.

<pre>27. router(config)#no banner motd</pre>

Perintah “router(config)#no banner motd” di gunakan untuk menghapus pesan (MotD, Message of the Day) dari banner.

<pre>28. router(config)#do<?</pre>

Ingat, bahwa saat ini Anda berada pada Global Configuration Mode, Anda tidak dapat mengeksekusi perintah yang ada pada Privilege Mode atau EXEC Level Mode, misalnya “router#show running-config” tidak dapat Anda akses dengan perintah “router(config)#show running-config”, namun Anda tetap dapat menjalankan perintah Privilege Mode/EXEC Level Mode (misalnya “show running-config”  di atas) walaupun Anda berada pada Global Configuration Mode dengan “router(config)#do”, misalnya “router(config)#do show running-config”.

<pre>29. router(config)#enable password</pre>
Perintah “router(config)#enable password” di gunakan untuk mengaktifkan fitur password.

<pre>30. router(config)#line console</pre>
Perintah “router(config)#line console” di gunakan untuk masuk ke Line Console Mode, dengan masuk ke Line Console Mode Anda dapat mengakses berbagai pengaturan yang tidak tersedia pada Global Configuration Mode misalnya menetapkan exec-timeout (akan kita bahas kemudian) dan lain sebagainya, indikator pada Line Console Mode akan berubah menjadi “router(config-line)#”.

<pre>31. router(config-line)#password admin</pre>
Perintah “router(config-line)#password admin” di gunakan untuk menetapkan password untuk login dengan password “admin”, Anda dapat mengganti password dengan teks lain yang Anda kehendaki.

<pre>32. router(config-line)#login</pre>
Perintah “router(config-line)#login” di gunakan untuk mengaktifkan fitur login, saat pengguna masuk ke mode konfigurasi (dengan hak akses lebih tinggi) maka pengguna di haruskan memasukkan password terlebih dahulu.

<pre>33. router(config-line)#exec-timeout 1 30</pre>
Perintah “router(config-line)#exec-timeout 1 30” di gunakan untuk mengatur fitur auto log off (apabila fitur login di aktifkan), nilai “1” pada perintah tersebut merupakan nilai “menit” sedangkan nilai “30” merupakan nilai “detik”, artinya pengguna akan secara otomatis log off apabila tidak ada aktifitas selama 1 menit 30 detik, untuk mengatur agar pengguna tidak log off otomatis, maka perintah yang di jalankan adalah “router(config-line)#exec-timeout 0 0”.

Demikian pembahasan mengenai perintah dasar Cisco, semoga bermanfaat untuk Anda yang membutuhkan atau setidaknya untuk menambah pengetahuan dan referensi kita mengenai beragam teknologi khususnya dalam bidang jaringan yang saat ini semakin berkembang pesat, selamat mencoba.




