# PRAKTIKUM 5 Job Control

## Nama : Ramiya Nola Azhara
## Kelas : SK3B
## NIM : 09011182328089

### Tugas

## **1. Eksekusi seluruh profile yang ada :**
   
a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :
**echo “Profile dari /etc/profile”**


![no 1](https://github.com/user-attachments/assets/81f2bc64-d5d0-4651-84d7-fbc2a30ee00a)

![no 1](https://github.com/user-attachments/assets/570d7cb1-2310-48c6-ad38-34e523909a39)


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


**/home/mahasiswa/.profile**

![no 1 (sudo nano profile)](https://github.com/user-attachments/assets/0ea3a9ac-dcbc-4045-bd4f-e668bc4b5a91)


![no 1 (echo profile)](https://github.com/user-attachments/assets/a17e8fda-234c-4039-a193-130b3ad6ad8b)



**/home/mahasiswa/.bashrc**


![no 1 (sudo nano bashrc)](https://github.com/user-attachments/assets/6a391e70-6811-4676-8888-9b80f8c1dba1)


![no 1 (echo bashrc)](https://github.com/user-attachments/assets/103c41b7-816c-48f9-9568-e179cf904968)


c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:

**$ su mahasiswa**

**$ exit**

![1C (su vboxuser)](https://github.com/user-attachments/assets/25127776-856c-457b-981b-ba5634662047)

kemudian gunakan opsi – sebagai berikut :

**$ su – mahasiswa**

**$ exit**

![1C (su - vboxuser)](https://github.com/user-attachments/assets/4a4c648d-c48d-4ea8-bfc2-5e3ab35f9283)

Jelaskan perbedaan kedua utilitas tersebut.

= Perbedaannya adalah jika menggunakan perintah su mahasiswa, hanya identitas pengguna yang berubah sementara lingkungan (environment) dari pengguna sebelumnya tetap dipertahankan. Sebaliknya, perintah su - mahasiswa melakukan login baru sepenuhnya, termasuk memuat ulang seluruh lingkungan pengguna baru dari awal.



## **2. Prompt String (PS)**
   
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell
PS1=‟> „
export PS1

![no 2 (sudo nano)](https://github.com/user-attachments/assets/1829de07-030f-4e45-9852-31573d4bdcd7)

![no 2A](https://github.com/user-attachments/assets/b23ae9cc-0af8-4e41-bb37-6124b274137d)




b. Eksperimen hasil PS1 :
$ PS1=“\! > “
69 > PS1=”\d > “
Mon Sep 23 > PS1=”\t > “
10:10:20 > PS1=”Saya=\u > “
Saya=mahasiswa > PS1=”\w >”
~ > PS1=\h >”

![no 2b](https://github.com/user-attachments/assets/6079b069-1dde-46ce-9977-97dc1861c692)



## **3. Logout**

Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout
Echo “Terima kasih atas sesi yang diberikan”
Sleep 5
clear

![no 3 ke 1](https://github.com/user-attachments/assets/32b3625a-7028-448a-9472-a3caacf954df)


![NO 3](https://github.com/user-attachments/assets/0348c6a7-ebb4-4cef-9daf-cf5bf852fa6c)


![no 3 ke 2](https://github.com/user-attachments/assets/c77a6a4e-1405-4859-b2d5-6293f49a13dc)



## **4. Bash script**

a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :

**p1.sh**

#! /bin/bash

echo “Program p1”

ls –l

![no 4a (membuat p1)](https://github.com/user-attachments/assets/186f5321-a234-4db7-99b4-db85b1e22c6a)

![no 4a (isi p1)](https://github.com/user-attachments/assets/656935a8-faf6-4ea5-b7f9-fcf3e152a50e)



**p2.sh**

#! /bin/bash

echo “Program p2”

who

![no 4a (membuat p2)](https://github.com/user-attachments/assets/f6b1c215-b26d-4496-8767-b6b37cd419f3)

![no 4a (isi p2)](https://github.com/user-attachments/assets/c848d779-80ba-4cbd-b6b4-7d32f5d47e6d)



**p3.sh**

#! /bin/bash

echo “Program p3”

ps x


![no 4a (membuat p3)](https://github.com/user-attachments/assets/bf94ebe8-d9c9-4bf4-bb3c-51bac82e71b9)

![no 4a (isi p3)](https://github.com/user-attachments/assets/0f240680-9656-4bf3-97c9-d2489f7ce98f)



b. Jalankan script tersebut sebagai berikut :

**$ ./p1.sh ; ./p3.sh ; ./p2.sh**

![no 4b (urutan 1)](https://github.com/user-attachments/assets/8a0ab9eb-ba5c-4a7c-8fc2-94102e2bc633)

![no 4b (urutan 2)](https://github.com/user-attachments/assets/5ce9f2df-a92d-4565-a705-b20041546bec)

![no 4b (urutan 3)](https://github.com/user-attachments/assets/c17bd95a-8c25-4c12-91ec-e73eb3bb92ac)


**$ ./p1.sh &**

![no 4b (bagian 2)](https://github.com/user-attachments/assets/27725b0e-9162-4f53-a70c-da4cf349637e)



**$ ./p1.sh $ ./p2.sh & ./p3.sh &**

![no 4b (bagian 3)](https://github.com/user-attachments/assets/c0fdf112-b6d5-43df-8326-1fcc51a27db4)



**$ ( ./p1.sh ; ./p3.sh ) &**

![no 4b (bagian 4)](https://github.com/user-attachments/assets/68003681-b77a-4e8b-982d-0834edfb7efe)


## **5. Jobs**

**a.** Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.

#!/bin/bash
while [ true ]

do

date >> hasil

sleep 10

done

![no 5a (bagian 1)](https://github.com/user-attachments/assets/266735d0-2bd8-4387-bcf8-4fbe39903a31)

![no 5a (bagian 2)](https://github.com/user-attachments/assets/394c6af1-e3d9-4102-b45a-47539acc2929)



**b.** Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background sebagai berikut :

$ jobs

$ find / -print > files 2>/dev/null &

$ jobs


![no 5b](https://github.com/user-attachments/assets/e3652868-ac94-436a-8c6c-8360d11a216b)



**c.** Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background

$ fg %1

$ bg

![no 5c](https://github.com/user-attachments/assets/9bb1cdb1-7ef6-46a8-9045-5e586cb2d54a)



**d.** Stop program background dengan utilitas kil

$ ps x

$ kill [Nomor PID]

![no 5d](https://github.com/user-attachments/assets/963b19e5-7d3c-4ffb-b0b0-085c0a056604)



## **6. History**

**a.** Ganti nilai HISTSIZE dari 1000 menjadi 20

$ HISTSIZE=20

$ h

![no 6a](https://github.com/user-attachments/assets/2378f1db-cd96-41f3-848f-1d1be8da388a)



**b.** Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan

$ !-5

![no 6b](https://github.com/user-attachments/assets/58427641-3d2d-4617-9a38-c86d1ac2ab39)



**c.** Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer

$ !!

![no 6c](https://github.com/user-attachments/assets/6c568695-5631-4990-9cd0-7a4164dd5af3)



**d.** Ulangi instruksi pada history bufer nomor 150

$ !150

![no 6d](https://github.com/user-attachments/assets/4e2e9d8b-3c9a-4bde-9585-3a229016d9ed)



**e.** Ulangi instruksi dengan prefix “ls”

$ !ls

![no 6e](https://github.com/user-attachments/assets/86e2b46b-a4f5-4bad-a3bb-e94b6a19a691)




