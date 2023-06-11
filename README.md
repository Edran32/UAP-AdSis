# UAP-AdSis
1. Buat direktori dengan nama UAP-Adsis, isi dengan file txt dengan format penamaan catatannya- <nama kamu>.txt, kemudian isi file txt tersebut dengan nama dan NIM kamu. Kemudian atur permission view-only pada file tersebut untuk user biasa. Tunjukkan bukti berupa screenshot yang menunjukkan bahwa file tersebut berhasil diatur permissionnya menjadi view-only untuk user biasa

a. Membuat sebuah direktori baru yang diberi nama `UAP-Adsis` menggunakan perintah mkdir
   ![Screenshot_5371](https://github.com/Edran32/UAP-AdSis/assets/50135710/0240e11c-4a4b-4758-95e2-46433b8a8500)              
b. Menggunakan perintah touch untuk membuat sebuah file txt yang diberi nama `catatannya-edran`
   ![Screenshot_5377](https://github.com/Edran32/UAP-AdSis/assets/50135710/ded9e0e8-4884-4507-99fa-7abaaa8a6e82)                 
c. Menjalankan perintah nano untuk membuka file text yang dibuat sebelumnya, kemudian menambahkan nama dan NIM di dalam file tersebut.     
   ![Screenshot_5378](https://github.com/Edran32/UAP-AdSis/assets/50135710/9d594082-4b87-4e26-9da1-59eda16433c5)                 
   ![Screenshot_5376](https://github.com/Edran32/UAP-AdSis/assets/50135710/8a88e4c8-e727-4213-9fb1-172e0a925459)          
d. Untuk mengatur permission view-only pada file tersebut untuk user biasa, maka perlu menjalankan perintah perintah sudo chmod 444 pada file `catatannya-edran.txt`.           
   ![Screenshot_5380](https://github.com/Edran32/UAP-AdSis/assets/50135710/8cc838b7-7329-475a-bf6a-54a50dc1d8cf)      
e. Menjalankan perintah ls -l, dapat dilihat bahwa pengguna biasa tidak dapat mengubah, menulis, atau menjalankan file tersebut, hanya dapat membacanya (read-only).          
   ![Screenshot_5379](https://github.com/Edran32/UAP-AdSis/assets/50135710/1a84e8c2-05a5-44af-a4e3-014867b03cb2)      
   ![Screenshot_5382](https://github.com/Edran32/UAP-AdSis/assets/50135710/bcc461a6-30ea-475c-9312-ea3e5426e9e8)     
  
2. Lakukan konfigurasi alamat IP address sementara pada sistem dan default gateway. (petunjuk 192.168.56.x | x adalah nomor absen)

a. Melakukan konfigurasi alamat IP address dan default gateway-nya, saya menggunakan `192.168.56.11`, angka 11 di sini merupakan nomor absen saya di mata kuliah Administrasi Sistem.      
Syntax: `*sudo ifconfig ens33 192.168.56.11 netmask 255.255.255.0*`     
![Screenshot_5383](https://github.com/Edran32/UAP-AdSis/assets/50135710/7cab568a-5d64-45ef-b402-58ab6a6d8d85)     
![Screenshot_5384](https://github.com/Edran32/UAP-AdSis/assets/50135710/1dbc22e6-e890-4477-a9f4-46c2d45c986c)       

3. Lakukan Instalasi Webmin lalu buatlah user bernama nama anda, lalu buat group Adsis_(kelas masing-masing) dan masukkan nama anda di group.  
  
4. Lakukan ping ke alamat ip anda dan coba lakukan reject dan drop di webmin, lalu analisis apa yang terjadi?
  
5. Buatlah perintah otomatis yang berfungsi untuk ping www.filkom.ub.ac.id
