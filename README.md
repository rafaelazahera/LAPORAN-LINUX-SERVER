# LAPORAN REMOTE LINUX SERVER 
- **NAMA** = RAFAELA ZAHERA VRIODONA <BR>
- **NIM** = 09011282328094<BR>
- **KELAS** = SK3A <BR>
- **MATA KULIAH** = SISTEM OPERASI <BR>
- **DOSEN PENGAMPU** = Adi Hermansyah, S.Kom., M.T.
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
### Melihat status layanan SSH
*sudo systemctl status ssh*
 ![WhatsApp Image 2024-10-30 at 20 14 49_22f2df1a](https://github.com/user-attachments/assets/6bd94e83-b79d-4f6a-bd72-3e4b2e89a3a5)
Perintah ini akan menampilkan status layanan SSH, memberikan informasi apakah layanan tersebut aktif dan berjalan tanpa masalah. Jika semuanya berjalan lancar, akan ada keterangan bahwa layanan sedang aktif dan siap menerima koneksi.
### Mengubah Port SSH Menjadi Port 40
Untuk mengubah port SSH, buka file konfigurasi sshd_config dan ubah port menjadi 40 dengan cara berikut:<br>

Gunakan editor teks seperti nano untuk membuka file konfigurasi: <br>

*sudo nano /etc/ssh/sshd_config*<br>
dibagian port #Port 22, dibuah menjadi Port 40, setelah itu disimpan dan enter.
- Linux Server
![WhatsApp Image 2024-10-30 at 20 17 22_5365f47d](https://github.com/user-attachments/assets/e5e0c56f-64bc-48af-8be2-c19a3f87b2a2)<br>
- Linux Dekstop
<img width="599" alt="image" src="https://github.com/user-attachments/assets/221f089e-2138-413b-be49-3e771a3f0da6"><br>

### Restart SSH

Setelah melakukan perubahan pada port SSH, langkah selanjutnya adalah merestart layanan SSH agar konfigurasi baru dapat diterapkan. Untuk melakukannya, gunakan perintah berikut:<br>
*sudo systemctl restart ssh*
![WhatsApp Image 2024-10-30 at 20 41 43_f78ff1a0](https://github.com/user-attachments/assets/050da68a-b3c8-46e0-9660-b4bf85a78f66)
Dengan perintah ini, layanan SSH akan dimulai ulang, dan perubahan yang telah dibuat pada port akan mulai berlaku. Ini memastikan bahwa koneksi ke server menggunakan port baru yang telah ditentukan.
## KESIMPULAN LAPORAN
Dari percobaan ini, dapat disimpulkan bahwa instalasi dan konfigurasi SSH Server pada Ubuntu Server melalui VirtualBox telah berhasil. Proses ini mencakup instalasi Ubuntu Server dan OpenSSH Server, serta perubahan port SSH dari 22 menjadi 40 untuk meningkatkan keamanan, dan semua langkah tersebut berjalan dengan baik. Koneksi remote dari Linux Desktop juga berhasil dilakukan setelah port baru dikonfigurasi dan perintah yang diperlukan dijalankan dengan benar. Proses ini memberikan pemahaman yang jelas tentang pengaturan SSH untuk akses jarak jauh di server dan menekankan pentingnya aspek keamanan dalam administrasi server jarak jauh.



