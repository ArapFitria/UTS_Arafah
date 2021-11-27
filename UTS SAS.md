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
  ![1](https://user-images.githubusercontent.com/92453574/143672341-f35dbb0d-0084-4ef4-91bc-4ad8efee0ae8.PNG)

2. Buka Server Manager, "Add Roles adn Features"
  ![2](https://user-images.githubusercontent.com/92453574/143672350-e2a96edf-8bf9-4084-9e25-a43ea43fb8b0.PNG)

3. "Next"
  ![3](https://user-images.githubusercontent.com/92453574/143672354-d944e242-0895-4e5c-a1b6-c5ba03f40d7f.PNG)

4. Pilih "Role-based or feature-based installation" dan "Next"
  ![4](https://user-images.githubusercontent.com/92453574/143672357-4bcaeed9-4b03-4f27-92ee-f789902a271d.PNG)

5. Pada bagian ini pilih "Select a server from the server pool" kemudian pilih direktori penyimpanan lokal, dan "Next"
  ![5](https://user-images.githubusercontent.com/92453574/143672359-e3ba5ec8-c32a-4d77-ab7e-42889066a600.PNG)

6. Centang "Active Directory Domain Service" dan klik "Add Features"
  ![6](https://user-images.githubusercontent.com/92453574/143672423-caaeaf66-5d47-4456-87bf-421241ad6553.PNG)
  ![7](https://user-images.githubusercontent.com/92453574/143672421-92d8d6d9-aed1-4887-b3dc-57c3ca491785.PNG)
  
7. Centang juga "Group Policy Management" dan "Next"
  ![9](https://user-images.githubusercontent.com/92453574/143672509-ac8ed0ff-c125-4d63-bb39-940c259e00b8.PNG)

8. "Next"
  ![10](https://user-images.githubusercontent.com/92453574/143672515-8d1df8ff-a327-4e8d-a4f7-41ebd8551e16.PNG)

9. dan "Install"
  ![11](https://user-images.githubusercontent.com/92453574/143672526-5a9ee071-52b0-40f7-82ae-39bda5c0c65e.PNG)

10. Tunggu sampai instalasi selesai
  ![12](https://user-images.githubusercontent.com/92453574/143672529-48efb78e-43bd-47ec-86c0-f0fddcfadc01.PNG)




**INSTALASI DNS SERVER DAN NET FRAMEWORK 3.5**

1. Ikuti Langkah pada Instalasi Adds No. 1 - 5
2. Centang "DNS Server" dan klik "Add features"
  ![1](https://user-images.githubusercontent.com/92453574/143672546-5318eb1b-b504-4fa9-9dc5-7da08c98aa17.PNG)
  ![2](https://user-images.githubusercontent.com/92453574/143672554-d01e29ed-33ba-4bf4-8c20-1e99176e342a.PNG)
  
3. Centang “.NET Framework 3.5 features"
  ![4](https://user-images.githubusercontent.com/92453574/143672593-f565f8e3-cb72-49d2-97da-6664e84d44a5.PNG)

4. "Next"
  ![5](https://user-images.githubusercontent.com/92453574/143672595-caa5ccb2-422f-45d1-9bf2-1e6d46476412.PNG)

5. "Install"
  ![6](https://user-images.githubusercontent.com/92453574/143672601-6020e629-9e73-4463-9e76-0b2270659e72.PNG)

6. Tunggu sampai instalasi selesai
  ![7](https://user-images.githubusercontent.com/92453574/143672606-ab759231-0cee-4a55-aceb-207894e791f9.PNG)



**PROMOTE SERVER TO A DOMAIN CONTROLLER**

1. Buka CMD, ketik <u>sconfig</u>
  ![1](https://user-images.githubusercontent.com/92453574/143672642-1726bd37-15a3-4efe-83e7-271d5bc64264.PNG)

2. Tunggu sampai muncul tampilan menu seperti di bawah, pilih "1" untuk mengatur IP Server ADDS
  ![2](https://user-images.githubusercontent.com/92453574/143672737-2cd0dc3e-9c87-44ce-a9ef-89d85a3eea21.PNG)

3. Isi konfigurasi IP
  ![5](https://user-images.githubusercontent.com/92453574/143672750-bdce50dc-234a-4072-b61c-7527ec5f1b72.PNG)

4. Atur agar DNS terarah ke IP ADDS
  ![6](https://user-images.githubusercontent.com/92453574/143672757-8b9bdf0f-1c74-4770-b56b-5437a3b37948.PNG)

5. Buka Server Manager, klik "Promote this server to a domain controller untuk konfigurasi ADDS"
  ![7](https://user-images.githubusercontent.com/92453574/143672762-128d32ed-7756-4064-b978-f900cfe678c8.PNG)

6. Pilih "Add a new forest", kemudian tambahkan domain dan "Next"
  ![8](https://user-images.githubusercontent.com/92453574/143672772-228390ab-037e-4d9c-8903-0aacd65c7ffc.PNG)

7. Atur password, klik "Next"B
  ![9](https://user-images.githubusercontent.com/92453574/143672776-6e0896fe-2c25-4d64-985f-b4b35a1b2a14.PNG)

8. "Next"
  ![10](https://user-images.githubusercontent.com/92453574/143672781-701cb798-2122-4716-942c-b2587a00e22f.PNG)

9. Bagian ini langsung terisi domain name, klik "Next"
  ![11](https://user-images.githubusercontent.com/92453574/143672840-c94280cc-1af4-45fe-91bd-5c52fb9c5ba1.PNG)

10. "Next"
  ![12](https://user-images.githubusercontent.com/92453574/143672843-f060c4ae-e9f8-40ff-92d1-0e0a98e5d701.PNG)

11. "Next"
  ![13](https://user-images.githubusercontent.com/92453574/143672845-7193217c-7b3e-49b8-94ab-e3a10151836f.PNG)

12. "Install", jika pada bagian ini error coba direstart terlebih dahulu kemudian ulangi langkan ini dan "Install"
  ![14](https://user-images.githubusercontent.com/92453574/143672847-bd969afe-b686-4e40-b9b4-aa305a52b92e.PNG)

13. Tunggu sampai instalasi selesai
  ![15](https://user-images.githubusercontent.com/92453574/143672853-a55b2606-59f3-49d4-a93b-1b7a413c34d6.PNG)

14. Buka cmd, ketik <u>netdom query fsmo</u> untuk mengecek hasil konfigurasi
  ![17](https://user-images.githubusercontent.com/92453574/143672856-247919b0-7db1-4e02-998a-2dabc683aaba.PNG)

15. Cek IP DNS
  ![18](https://user-images.githubusercontent.com/92453574/143672860-624cce4c-a0c0-4c73-905b-2a6bcd5ffa85.PNG)
