# UAP-AdSis

## 1. Buat direktori dengan nama UAP-Adsis, isi dengan file txt dengan format penamaan catatannya-<nama kamu>.txt, kemudian isi file txt tersebut dengan nama dan NIM kamu. Kemudian atur permission view-only pada file tersebut untuk user biasa. Tunjukkan bukti berupa screenshot yang menunjukkan bahwa file tersebut berhasil diatur permissionnya menjadi view-only untuk user biasa

a. Membuat sebuah direktori baru yang diberi nama `UAP-Adsis` menggunakan perintah mkdir      
   Syntax: `mkdir catatannya-edran`     
   ![Screenshot_5371](https://github.com/Edran32/UAP-AdSis/assets/50135710/0240e11c-4a4b-4758-95e2-46433b8a8500)              
b. Menggunakan perintah touch untuk membuat sebuah file txt yang diberi nama `catatannya-edran`      
   Syntax: `touch catatannya-edran.txt`     
   ![Screenshot_5377](https://github.com/Edran32/UAP-AdSis/assets/50135710/ded9e0e8-4884-4507-99fa-7abaaa8a6e82)                 
c. Menjalankan perintah nano untuk membuka file text yang dibuat sebelumnya, kemudian menambahkan nama dan NIM di dalam file tersebut.      
   Syntax: `nano catatannya-edran.txt`     
   ![Screenshot_5378](https://github.com/Edran32/UAP-AdSis/assets/50135710/9d594082-4b87-4e26-9da1-59eda16433c5)                 
   ![Screenshot_5376](https://github.com/Edran32/UAP-AdSis/assets/50135710/8a88e4c8-e727-4213-9fb1-172e0a925459)          
d. Untuk mengatur permission view-only pada file tersebut untuk user biasa, maka perlu menjalankan perintah perintah sudo chmod 444 pada file `catatannya-edran.txt`.     
   Syntax: `sudo chmod 444 catatannya-edran.txt`
   ![Screenshot_5380](https://github.com/Edran32/UAP-AdSis/assets/50135710/8cc838b7-7329-475a-bf6a-54a50dc1d8cf)      
e. Menjalankan perintah ls -l, dapat dilihat bahwa pengguna biasa tidak dapat mengubah, menulis, atau menjalankan file tersebut, hanya dapat membacanya (read-only).     
   Syntax: `ls -l`     
   ![Screenshot_5379](https://github.com/Edran32/UAP-AdSis/assets/50135710/1a84e8c2-05a5-44af-a4e3-014867b03cb2)      
   ![Screenshot_5382](https://github.com/Edran32/UAP-AdSis/assets/50135710/bcc461a6-30ea-475c-9312-ea3e5426e9e8)     
  

## 2. Lakukan konfigurasi alamat IP address sementara pada sistem dan default gateway. (petunjuk 192.168.56.x | x adalah nomor absen)

a. Melakukan konfigurasi alamat IP address dan default gateway-nya, saya menggunakan `192.168.56.11`, angka 11 di sini merupakan nomor absen saya di mata kuliah Administrasi Sistem.      
   Syntax: `sudo ifconfig ens33 192.168.56.11 netmask 255.255.255.0`       
   ![Screenshot_5383](https://github.com/Edran32/UAP-AdSis/assets/50135710/7cab568a-5d64-45ef-b402-58ab6a6d8d85)     
   ![Screenshot_5384](https://github.com/Edran32/UAP-AdSis/assets/50135710/1dbc22e6-e890-4477-a9f4-46c2d45c986c)       
b. Melakukan konfigurasi IP address default gateway dengan perintah route add      
   Syntax: `sudo route add default gw 192.168.56.11 ens33`        
   ![Screenshot_5385](https://github.com/Edran32/UAP-AdSis/assets/50135710/becba3b3-149e-49c1-a39f-47ce68aa2e70)            

c. Menjalankan perintah route untuk memastikan informasi pada routing table      
   Syntax: `sudo route -n`     
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/46bac9a5-04d0-4d6d-bbed-d7803322dfaf)           

## 3. Lakukan Instalasi Webmin lalu buatlah user bernama nama anda, lalu buat group Adsis_(kelas masing-masing) dan masukkan nama anda di group.  
a. Menjalankan perintah `sudo nano /etc/apt/sources.list`, lalu menambahkan `deb http://download.webmin.com/download/repository sarge contrib` pada bagian akhir file.    
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/21b67b18-c6a5-4007-b9b1-460634a49065)       
   ![Screenshot_5370](https://github.com/Edran32/UAP-AdSis/assets/50135710/9a27a5a5-bab7-494d-8b5c-1a7647f50de3)    
b. Menambahkan kunci PGP Webmin pada sistem operasi Linux agar sistem mempercayai repositori Webmin yang telah ditambahkan sebelumnya.     
   Syntax: `wget http://www.webmin.com/jcameron-key.asc`
   ![Screenshot_5372](https://github.com/Edran32/UAP-AdSis/assets/50135710/b484ec2a-c3b0-4d81-a2a0-eb67b6a69334)   
c. Memperbarui daftar paket pada sistem operasi Linux agar menyertakan repositori Webmin yang telah ditambahkan sebelumnya.     
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/a5de4631-780f-4598-8ca6-d41dbeafb5e3)      
d. Menginstall webmin dengan syntax sebagai berikut   
   Syntax: `sudo apt-get install webmin`  
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/f05f31dd-8f1c-4f3c-bf76-d25f9972505c)   
e. Untuk mengakses Webmin dapat dilakukan melalui memasukkan link `https://192.168.116.134:10000` pada, di mana IP tersebut merupakan IP komputer dan menggunakan port 10000. Setelah itu, lakukan login dengan menginputkan username dan password Linux Ubuntu.        
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/d04463ae-329d-4762-ba87-5b44de7e6ca3)    
f. Masuk ke menu `Users and Group` untuk membuat sebuah user baru bernama “ferdinandrey” dengan login shell /bin/bash dan membuat password untuk login requirement.      
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/e3353833-5616-41fa-ac65-8f0ebe279bea)     
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/09af4b04-3383-456c-896a-4bb6a1de7d71)   
   
   User "ferdinandrey" berhasil dibuat     
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/78f2a563-1d97-4cb8-8f26-85206b37c2c7)    
g. Membuat group baru dengan nama `Adsis_E` dan emasukkan user ferdinandrey ke dalam group   
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/e6e315a9-4efb-4311-ab16-8ad95762fe03)    
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/4f15b5b0-f721-490b-91d0-3b5739bf1979)    

   Seperti yang dapat dilihat pada gambar di bawah ini, user "ferdinandrey" berhasil ditamabahkan pada Group `Adsis-E`
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/7da17d2a-01c0-4b6e-90ac-d331e48e1be8)
  
## 4. Lakukan ping ke alamat ip anda dan coba lakukan reject dan drop di webmin, lalu analisis apa yang terjadi?
a. Melakukan ping ke IP address komputer.   
   Syntax: `ping 192.168.116.134 -t`   
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/ba8ce5c1-5dfd-48c6-a748-f8ad1da09a99)     
b. Masuk ke menu Networking, kemudian ke bagian Linux Firewall. Pada Incoming Packets (INPUT), tekan opsi Add rule dan set INPUT menjadireject ping. Setelah itu, Apply configuration.
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/69db0ea3-dd50-4785-832c-bbcc53bb1a24)      
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/2e2feb9d-a9b9-4a54-bf4c-a780b4200d45)          
c. Lakukan ping kembali menggunakan perintah yang sama pada langkah (a)
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/182a17e4-bc5c-4856-b5fc-bdadf13fa9ff)

  
## 5. Buatlah perintah otomatis yang berfungsi untuk ping www.filkom.ub.ac.id
a. Masuk dan konfigurasi file cron menggunakan perintah berikut, kemudian pilih opsi 1
   Syntax: `sudo crontab -e.`    
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/e6e2020a-7ea7-4108-bb8e-a46f7c669dca)            
b. Memasukkan perintah untuk ping filkom.ub.ac.id setiap 1 menit. Konfigurasi `*/1 * * * * ping filkom.ub.ac.id`. Hal ini bertujuan untuk melakukan ping otomatis ke alamat filkom.ub.ac.id setiap 1 menit.      
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/b85cc207-5c58-4bd4-abad-3c23cc4867ff)          
c. Mengetes otomatisasi menggunakan perintah `ps aux | grep ping`   
   Sistem menjalankan perintah ping filkom.ub.ac.id setiap 1 menit     
   ![image](https://github.com/Edran32/UAP-AdSis/assets/50135710/3c6d60ad-7095-4d78-9309-3a465ed3e7ab)     
    
   
