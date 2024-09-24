# Tugas-5-Job-Control

### Nama   : Anugrah Tegar Noverzha
### NIM    : 09011282328029
### Kelas  : SK3B
___


## 1. Eksekusi seluruh profile yang ada :
   
a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :

`echo “Profile dari /etc/profile”`

b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :

```
  /home/stD02001/.bash_profile  
  /home/. stD02001/.bash_login  
  /home/mahasiswa/.profile  
  /home/mahasiswa/.bashrc  
```
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap  
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile :  

`echo “Profile dari .bash_profile”  `

Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang 
bersangkutan.

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut"
```
  $ su mahasiswa  
  $ exit  
  ```
kemudian gunakan opsi – sebagai berikut :
```
  $ su – mahasiswa  
  $ exit
```
Jelaskan perbedaan kedua utilitas tersebut. 

Jawab:
a.  Untuk melihat file /etc/profile, kita bisa menggunakan command sudo untuk mendapatkan hak akses super user, lalu menggunakan command nano untuk mengedit file tersebut.

![Screenshot 2024-09-24 103547](https://github.com/user-attachments/assets/b34e4083-3a3b-4e59-a0e6-c94a4a78df12)

Lalu kita tambahkan `echo “Profile dari /etc/profile”`

![Screenshot 2024-09-24 195811](https://github.com/user-attachments/assets/08391c3d-31a8-4eb0-8091-328ab4fbc8e5)

---
b. Mencantumkan instruksi echo misalnya pada /home/nama user/.bash_profile : echo “Profile dari .bash_profile”.

- `.bash_profile`

![Screenshot 2024-09-24 103929](https://github.com/user-attachments/assets/558768c7-6651-4e73-a379-f22f91a8dbba)
![Screenshot 2024-09-24 103909](https://github.com/user-attachments/assets/bb20dbce-f718-4b03-adea-d9518a58f1ae)


- `.bash_login`

![Screenshot 2024-09-24 104056](https://github.com/user-attachments/assets/f1bc9f09-a066-4ed5-a39f-57248223d362)
![Screenshot 2024-09-24 104037](https://github.com/user-attachments/assets/d39fb38b-bbec-4bee-832f-d6535b58c552)

 
 - `.profile` 

![Screenshot 2024-09-24 104247](https://github.com/user-attachments/assets/c426148e-ba8f-46a8-bccd-de3afc754b45)
![Screenshot 2024-09-24 104235](https://github.com/user-attachments/assets/6ac762a4-cb40-4ee6-aa51-b3261dbca039)

- `.bashrc `

![Screenshot 2024-09-24 104159](https://github.com/user-attachments/assets/5d567b38-1bd1-44b1-9a77-2fa558e2d3cf)
![Screenshot 2024-09-24 104145](https://github.com/user-attachments/assets/02773fbb-87e7-4978-9bc0-dbfc44b1c67b)

---
c. Jalankan instruksi subtitute user (su dan su -), kemudian keluar dengan perintah exit.

![Screenshot 2024-09-24 104359](https://github.com/user-attachments/assets/b0011829-b2b7-497f-ba41-10db10c7476c)
![Screenshot 2024-09-24 104448](https://github.com/user-attachments/assets/9d78a635-6070-47dd-9720-53db4dadb4f6)


Perbedaan dari kedua utilitas tersebut adalah, utilitas `su` berfungsi pengguna tanpa mengubah environment (hanya ganti user). sedangkan `su -` berfungsi untuk mengganti pengguna dan muat environment lengkap dari pengguna baru.

## 2. Prompt String (PS)  
a. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut:

Edit file `.bash_profile`, ganti prompt `PS1` dengan `>`. Instruksi export diperlukan dengan 
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell 

`PS1='> '  `
export PS1 

![Screenshot 2024-09-24 104619](https://github.com/user-attachments/assets/5e049258-66b6-4c55-a964-acbaafe4d3c3)

---
b.  Eksperimen hasil PS1 : 
```
$ PS1=“\! > “  
69 > PS1=”\d > “  
Mon Sep 23 > PS1=”\t > “  
10:10:20 > PS1=”Saya=\u > “  
Saya=mahasiswa > PS1=”\w >”  
~ > PS1=\h >”  
```

![Screenshot 2024-09-24 104957](https://github.com/user-attachments/assets/c1949f6b-08db-4522-98b6-c04c8fe7d4a6)

---

## 3. Logout  
Edit file `.bash_logout`, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout 
```
Echo “Terima kasih atas sesi yang diberikan”  
Sleep 5  
clear  
```

![Screenshot 2024-09-24 105237](https://github.com/user-attachments/assets/13bba22a-f853-45dd-96f4-28d07d21b823)
![Screenshot 2024-09-24 105137](https://github.com/user-attachments/assets/02d49363-4ffe-465c-9735-40ae0883b6f4)

---

## 4. Bash script  
a.  Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing : 
```
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
```





















