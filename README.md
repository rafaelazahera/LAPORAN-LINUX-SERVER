# LAPORAN REMOTE LINUX SERVER 
**NAMA** = RAFAELA ZAHERA VRIODONA <BR>
**NIM** = 09011282328094<BR>
**KELAS** = SK3A <BR>
**MATA KULIAH** = SISTEM OPERASI <BR>
**DOSEN PENGAMPU** = Adi Hermansyah, S.Kom., M.T.
 ## 1. INSTALASI UBUNTU SERVER <BR>
 Pertama-tama saya menginstall Ubuntu Server pada VirtualBox ![image](https://github.com/user-attachments/assets/66f53c95-b6ff-4db1-bba4-483a288185f1)

jika sudah terinstall maka dilakukan konfigurasi awal di VirtualBox Pada tahap ini, Proses ini mencakup pengaturan jaringan yang penting untuk memastikan konektivitas yang baik, alokasi memori yang tepat untuk memenuhi kebutuhan sistem, serta pengaturan disk untuk meningkatkan performa dan efisiensi penyimpanan. Dengan langkah-langkah ini,
diharapkan dapat tercipta lingkungan virtual yang stabil dan optimal bagi operasional Ubuntu Server. ![WhatsApp Image 2024-10-30 at 19 56 28_c1deec1b](https://github.com/user-attachments/assets/9c438918-4663-46af-b44f-d2dfeb127366)
Setelah proses instalasi selesai, Ubuntu Server dikonfigurasi untuk mendukung layanan dan akses jarak jauh melalui protokol SSH. Konfigurasi ini memungkinkan pengguna untuk terhubung dan mengelola server secara remote dengan aman, sehingga memudahkan administrasi dan pengelolaan server tanpa perlu berada di lokasi fisik.
## 2 MENYIAPKAN SSH UBUNTU SERVER
###  INSTALASI OpenSSH Server
*sudo apt install openssh-server* <BR>

![WhatsApp Image 2024-10-30 at 20 12 41_5fe906bf](https://github.com/user-attachments/assets/7bd8ff38-6f42-4c0f-ba29-f2a0cdda3a06)
Perintah ini akan memperbarui daftar paket dan menginstal OpenSSH Server, memungkinkan akses jarak jauh ke server melalui SSH. Setelah instalasi selesai, layanan SSH akan aktif secara otomatis, dan pengguna dapat terhubung ke server menggunakan klien SSH. <BR>
 ### Mengaktifkan dan Mengecek Status Layanan SSH
 Setelah OpenSSH terinstal, layanan SSH perlu diaktifkan agar bisa berjalan otomatis setiap kali server dinyalakan. Ini penting supaya akses ke server melalui SSH bisa dilakukan tanpa harus mengaktifkan layanan secara manual setelah restart.<br>
 *sudo systemctl enable ssh* <br>
*sudo systemctl start ssh*
 ![WhatsApp Image 2024-10-30 at 20 14 49_22f2df1a](https://github.com/user-attachments/assets/6bd94e83-b79d-4f6a-bd72-3e4b2e89a3a5)
Perintah ini memastikan bahwa SSH akan aktif saat server booting. Dengan pengaturan ini, pengelolaan server menjadi lebih mudah dan akses tetap tersedia kapan saja.
### Melihay status layanan SSH
*sudo systemctl status ssh*
 ![WhatsApp Image 2024-10-30 at 20 14 49_22f2df1a](https://github.com/user-attachments/assets/6bd94e83-b79d-4f6a-bd72-3e4b2e89a3a5)
Perintah ini akan menampilkan status layanan SSH, memberikan informasi apakah layanan tersebut aktif dan berjalan tanpa masalah. Jika semuanya berjalan lancar, akan ada keterangan bahwa layanan sedang aktif dan siap menerima koneksi.


