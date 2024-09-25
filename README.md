# PRAKTIKUM 5 Job Control

## Nama : Ramiya Nola Azhara
## Kelas : SK3B
## NIM : 09011182328089

### Tugas

1. Eksekusi seluruh profile yang ada :
a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :
**echo “Profile dari /etc/profile”**


    ![no 1](https://github.com/user-attachments/assets/81f2bc64-d5d0-4651-84d7-fbc2a30ee00a)

  


b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :
/home/stD02001/.bash_profile
/home/. stD02001/.bash_login
/home/mahasiswa/.profile
/home/mahasiswa/.bashrc
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :
**echo “Profile dari .bash_profile”**
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang
bersangkutan.

**/home/stD02001/.bash_profile**

![no 1 (sudo nano bash profile)](https://github.com/user-attachments/assets/6d7e4d97-a741-48d7-b2b3-d5155a747490)

![no 1 (echo bash profile)](https://github.com/user-attachments/assets/39bcfebf-93c1-4bdd-a863-2303662267d3)


**/home/. stD02001/.bash_login**

![no 1 (sudo nano bash login)](https://github.com/user-attachments/assets/df632e5c-1a3d-4d23-951d-c501c7ea48d6)

![no 1 (echo bash login)](https://github.com/user-attachments/assets/217dae72-4639-418b-86e2-753caecd3484)

/home/mahasiswa/.profile

![no 1 (sudo nano profile)](https://github.com/user-attachments/assets/0ea3a9ac-dcbc-4045-bd4f-e668bc4b5a91)


![no 1 (echo bash profile)](https://github.com/user-attachments/assets/757b825d-c262-40ff-8c56-1b82ffce50c6)


/home/mahasiswa/.bashrc


![no 1 (sudo nano bashrc)](https://github.com/user-attachments/assets/6a391e70-6811-4676-8888-9b80f8c1dba1)


![no 1 (echo bashrc)](https://github.com/user-attachments/assets/103c41b7-816c-48f9-9568-e179cf904968)


c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:
$ su mahasiswa
$ exit
kemudian gunakan opsi – sebagai berikut :
$ su – mahasiswa
$ exit
Jelaskan perbedaan kedua utilitas tersebut.






2. Prompt String (PS)
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell
PS1=‟> „
export PS1



b. Eksperimen hasil PS1 :
$ PS1=“\! > “
69 > PS1=”\d > “
Mon Sep 23 > PS1=”\t > “
10:10:20 > PS1=”Saya=\u > “
Saya=mahasiswa > PS1=”\w >”
~ > PS1=\h >”




3. Logout
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout
Echo “Terima kasih atas sesi yang diberikan”
Sleep 5
clear



4. Bash script
a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :
p1.sh
#! /bin/bash
echo “Program p1”
ls –l










p2.sh
#! /bin/bash
echo “Program p2”
who





p3.sh
#! /bin/bash
echo “Program p3”
ps x





b. Jalankan script tersebut sebagai berikut :

$ ./p1.sh ; ./p3.sh ; ./p2.sh





$ ./p1.sh &






$ ./p1.sh $ ./p2.sh & ./p3.sh &




$ ( ./p1.sh ; ./p3.sh ) &




