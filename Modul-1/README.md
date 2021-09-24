# Latihan Modul 1📝
1. Ketika mengakses suatu halaman web, berapakah port yang dituju oleh suatu paket? <br>
   **Jawab:** <br>
   Port untuk web adalah **http (80)** dan **https (443)**. <br>
   
2. Apa sajakah perbedaan ketika mengakses halaman utama website [its.ac.id](https://www.its.ac.id/) dan [monta.if.its.ac.id](https://monta.if.its.ac.id/)? <br>
   **Jawab:** <br>
   ping [its.ac.id](https://www.its.ac.id/) <br>
   ip = 103.94.189.5 <br>
   Capture display pada Wireshark ```host its.ac.id``` atau ```host 103.94.189.5``` <br>
   Port [its.ac.id](https://www.its.ac.id/) adalah 443 -> https (lebih secure)

   ping [monta.if.its.ac.id](https://monta.if.its.ac.id/) <br>
   ip = 103.94.190.11 <br>
   Capture display pada Wireshark ```host monta.if.its.ac.id``` atau ```host 103.94.190.11``` <br>
   Port [monta.if.its.ac.id](https://monta.if.its.ac.id/) adalah 80 -> http (less secure) <br>

3. Ada berapa paket yang dikirimkan oleh web server ketika mengunduh file? Mengapa terjadi seperti itu? <br>
   **Jawab:** <br>
   Sangat banyak karena yang dikirimkan berupa chunks (potongan-potongan). Untuk mengirimkan atau menerima data membutuhkan end-point satu dan end-point lainnya. Dikirimkan dalam bentuk chunks agar jika terjadi masalah pada bandwidth, tidak banyak data yang lost. Jika gagal satu part, yang diulang adalah part tersebut tidak semuanya. <br>

4. Dari hasil analisa paket, apa perbedaan ketika menggunakan persistent connection dan non-persistent connection? <br>
   **Jawab:** <br>
   Persistent dan non-persistent adalah dua tipe HTTP connections yang digunakan untuk menghubungkan client dengan webserver. Persistent mempunyai tipe ```1.1``` sedangkan Non-persistent mempunyai tipe ```1.0```. <br>
   * **Persistent connection:** link / sambungan yang tidak akan mati / tertutup ketika pengeksekusian scriptnya berakhir (keep alive, 1 request 1 koneksi saja), HTTP 1.1 <br> Connection Time: ```2 RTT```
   * **Non-persistent connection:** link/sambungan akan langsung ditutup / mati saat pengeksekusian script berakhir (tiap 1 request connect, disconnect. Kalau ada request connect lagi), HTTP 1.0 <br> Connection Time: ```2RTT + file transmission time``` <br>
   
   **Sample Problem** <br>
   Suppose 10 images need to be downloaded from the HTTP server. The total time taken to request and download 10 images in a non-persistent and persistent connection is: <br>
   * Persistent: ```2 RTT (Connection time) + 10 RTT= 12 RTT12RTT```
   * Non-persistent: ```2 RTT (Connection time) + 2 * 10 RTT= 22 RTT22RTT```
  
6. Apa perbedaan ketika autentikasi menggunakan method basic dengan digest?
7. Apa perbedaan ketika mengakses halaman web biasa dengan ketika proses login terjadi?
8. Apa saja yang selalu dikirimkan browser ke web server? Export data hasil paket capture!
9. Apakah ada paket yang dikirimkan oleh perangkat anda pada saat tidak sedang mengakses browser? Kalau ada, coba temukan domainnya?
10. Akses website http://www.columbia.edu/~fdc/sample.html, download gambar pada halaman tersebut lalu coba ambil gambar dari wireshark!

## References
* https://id.wikipedia.org/wiki/Porta_(jaringan_komputer)
* https://github.com/arsitektur-jaringan-komputer/Modul-Jarkom/tree/master/Modul-1
* https://www.washingtonpost.com/graphics/national/security-of-the-internet/bgp/
