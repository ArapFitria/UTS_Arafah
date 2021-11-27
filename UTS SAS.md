**INSTALASI WINDOWS SERVER 2022**

1. Download ISO Windows Server 2022
2. Buat VM untuk Windows Server 2022, kemudian start
3. Pilih Bahasa yang ingin digunakan, kemudian klik "Install Now"
  ![1](https://user-images.githubusercontent.com/92453574/143671943-408c3574-8884-4b77-9c42-6adbe9c8b904.PNG)
  
  ![2](https://user-images.githubusercontent.com/92453574/143671958-f171156f-045c-4038-9866-56fc492b3f30.PNG)

4. Pilih sistem operasi yang ingin digunakan biasanya lebih ke CLI atau GUI, kemudian klik "Next"
  ![3](https://user-images.githubusercontent.com/92453574/143672001-ee16ff7e-cd56-4dc1-8ec0-4a05a1a2659a.PNG)

5. Agar bisa lanjut ke taha semua, centang pada kolom accept dan klik "Next"
  ![4](https://user-images.githubusercontent.com/92453574/143672006-26c76ddb-0795-482a-b58a-4a21d5a7b94a.PNG)

6. Pada langkah ini saya tidak membagi partisi, dan langsung klik "Next"
  ![6](https://user-images.githubusercontent.com/92453574/143672069-27c369f2-507c-449c-bee8-9e27af310c58.PNG)

7. Tunggu sampai instalasi selesai
  ![7](https://user-images.githubusercontent.com/92453574/143672076-8dead348-fd37-4c33-9932-ef94af4ec557.PNG)

8. Ketika Instalasi sudah selesai, klik "Restart Now" agar sistem direboot sebelum digunakan
  ![8](https://user-images.githubusercontent.com/92453574/143672084-f019827f-ab4a-4e44-9047-5b37b263ce2c.PNG)

9. Atur password dan "Finish"
  ![9](https://user-images.githubusercontent.com/92453574/143672088-75f872a6-f4eb-4576-8693-2dd58e59167e.PNG)

10. Pada menu VM bagian atas "Input – Keyboard – Insert Ctrl + Alt + Del" agar bisa masuk ke windows
   ![10](https://user-images.githubusercontent.com/92453574/143672098-497f6d24-58d9-4fc1-9e8b-9a9cf5c12052.PNG)

11. Atur password
  ![9](https://user-images.githubusercontent.com/92453574/143672117-5a768c5a-ce68-48e1-b7da-fc2ad7e110e6.PNG)

12. Pada manu VM bagian atas "Devices – Insert Guest Additions CD Image"
13. Masuk ke file explorer dan run VBoxWindowsAdditions
  ![11](https://user-images.githubusercontent.com/92453574/143672131-ae153b1e-0b80-494f-a0f5-f3fd631697e7.PNG)

14. "Next"
  ![12](https://user-images.githubusercontent.com/92453574/143672136-60897824-7c1f-450a-b9b7-6d76f8858921.PNG)

15. "Next"
  ![13](https://user-images.githubusercontent.com/92453574/143672141-ca369a2b-a1f9-4809-afa9-79d9f194fb44.PNG)

16. "Install" dan tunggu sampai instalasi selesai
  ![14](https://user-images.githubusercontent.com/92453574/143672166-1abf872a-3a55-413b-b3a9-3e84271cbb1e.PNG)
  
  ![15](https://user-images.githubusercontent.com/92453574/143672183-e4c4f30c-7031-4a01-a034-c68448015962.PNG)

17. Pilih "Reboot Now" dan "Finish"
  ![17](https://user-images.githubusercontent.com/92453574/143672187-6958ee46-983f-49d2-94e7-c35f6b7ac09c.PNG)



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
