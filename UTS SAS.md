**INSTALASI WINDOWS SERVER 2022**

1. Download ISO Windows Server 2022
2. Buat VM untuk Windows Server 2022, kemudian start
3. Pilih Bahasa yang ingin digunakan, kemudian klik "Install Now"
4. Pilih sistem operasi yang ingin digunakan biasanya lebih ke CLI atau GUI, kemudian klik "Next"
5. Agar bisa lanjut ke taha semua, centang pada kolom accept dan klik "Next"
6. Pada langkah ini saya tidak membagi partisi, dan langsung klik "Next"
7. Tunggu sampai instalasi selesai
8. Ketika Instalasi sudah selesai, klik "Restart Now" agar sistem direboot sebelum digunakan
9. Atur password dan "Finish"
10. Pada menu VM bagian atas "Input – Keyboard – Insert Ctrl + Alt + Del" agar bisa masuk ke windows
11. Masukkan password
12. Pada manu VM bagian atas "Devices – Insert Guest Additions CD Image"
13. Masuk ke file explorer dan run VBoxWindowsAdditions
14. "Next"
15. "Next"
16. "Install"
17. Pilih "Reboot Now" dan "Finish"



**INSTALASI ADDS**

1. Buka PowerShell, ganti nama komputer
2. Buka Server Manager, "Add Roles adn Features"
3. "Next"
4. Pilih "Role-based or feature-based installation" dan "Next"
5. Pada bagian ini pilih "Select a server from the server pool" kemudian pilih direktori penyimpanan lokal, dan "Next"
6. Centang "Active Directory Domain Service" dan klik "Add Features"
7. Centang juga "Group Policy Management" dan "Next"
8. "Next"
9. dan "Install"
10. Tunggu sampai instalasi selesai



**INSTALASI DNS SERVER DAN NET FRAMEWORK 3.5**

1. Ikuti Langkah pada Instalasi Adds No. 1 - 5
2. Centang "DNS Server" dan klik "Add features"
3. Centang “.NET Framework 3.5 features"
4. "Next"
5. "Install"
6. Tunggu sampai instalasi selesai



**PROMOTE SERVER TO A DOMAIN CONTROLLER**

1. Buka CMD, ketik <u>sconfig</u>
2. Tunggu sampai muncul tampilan menu seperti di bawah, pilih "1" untuk mengatur IP Server ADDS
3. Isi konfigurasi IP
4. Atur agar DNS terarah ke IP ADDS
5. Buka Server Manager, klik "Promote this server to a domain controller untuk konfigurasi ADDS"
6. Pilih "Add a new forest", kemudian tambahkan domain dan "Next"
7. Atur password, klik "Next"B
8. "Next"
9. Bagian ini langsung terisi domain name, klik "Next"
10. "Next"
11. "Next"
12. "Install", jika pada bagian ini error coba direstart terlebih dahulu kemudian ulangi langkan ini dan "Install"
13. Tunggu sampai instalasi selesai
14. Buka cmd, ketik <u>netdom query fsmo</u> untuk mengecek hasil konfigurasi
15. Cek IP DNS