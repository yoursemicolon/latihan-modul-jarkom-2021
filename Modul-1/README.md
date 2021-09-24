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
   Port [monta.if.its.ac.id](https://monta.if.its.ac.id/) adalah 80 -> http -> (less secure) <br>

3. Ada berapa paket yang dikirimkan oleh web server ketika mengunduh file? Mengapa terjadi seperti itu? <br>
   **Jawab:** <br>
   Sangat banyak karena yang dikirimkan berupa chunks (potongan-potongan). Untuk mengirimkan atau menerima data membutuhkan end-point satu dan end-point lainnya. Dikirimkan dalam bentuk chunks agar jika terjadi masalah pada bandwidth, tidak banyak data yang lost. Jika gagal satu part, yang diulang adalah part tersebut tidak semuanya. <br><br>

4. Dari hasil analisa paket, apa perbedaan ketika menggunakan persistent connection dan non-persistent connection?
5. Apa perbedaan ketika autentikasi menggunakan method basic dengan digest?
6. Apa perbedaan ketika mengakses halaman web biasa dengan ketika proses login terjadi?
7. Apa saja yang selalu dikirimkan browser ke web server? Export data hasil paket capture!
8. Apakah ada paket yang dikirimkan oleh perangkat anda pada saat tidak sedang mengakses browser? Kalau ada, coba temukan domainnya?
9. Akses website http://www.columbia.edu/~fdc/sample.html, download gambar pada halaman tersebut lalu coba ambil gambar dari wireshark!

## References
* https://id.wikipedia.org/wiki/Porta_(jaringan_komputer)
* https://github.com/arsitektur-jaringan-komputer/Modul-Jarkom/tree/master/Modul-1
* https://www.washingtonpost.com/graphics/national/security-of-the-internet/bgp/
