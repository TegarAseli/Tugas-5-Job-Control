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

---
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

b.  Jalankan script tersebut sebagai berikut : 
```
$  ./p1.sh ; ./p3.sh ; ./p2.sh  
$  ./p1.sh &  
$  ./p1.sh $ ./p2.sh & ./p3.sh &  
$  ( ./p1.sh ; ./p3.sh ) & 
```

Jawab:

a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi yang telah ditentukan:

![Screenshot 2024-09-24 105555](https://github.com/user-attachments/assets/55f7d01a-a53b-42d9-a938-223b03e2187a)
---
- `p1.sh`
  
![Screenshot 2024-09-24 105355](https://github.com/user-attachments/assets/17adb255-cc1c-4a2c-8348-0772a269a8c7)

---
- `p2.sh`

![Screenshot 2024-09-24 105444](https://github.com/user-attachments/assets/cbeb20bd-5008-44be-815a-a678bf2da23a)
---
- `p3.sh`

![Screenshot 2024-09-24 105541](https://github.com/user-attachments/assets/349203af-4310-4d33-b460-0f6fbb33fdb1)
---

b.  Jalankan script tersebut menggunakan command pada soal:

- `$  ./p1.sh ; ./p3.sh ; ./p2.sh`
  
![Screenshot 2024-09-24 105818](https://github.com/user-attachments/assets/71767644-8c86-4f25-894f-83ff01ce90ee)

Muncul pemberitahuan "Permission denied" dikarenakan skrip tersebut tidak memiliki izin eksekusi. Untuk mengatasinya, gunakan perintah chmod +x pada file skrip untuk memberikan izin eksekusi.

![Screenshot 2024-09-24 105847](https://github.com/user-attachments/assets/30fc0756-260c-4be7-a44f-c5be4c3a74f5)
![Screenshot 2024-09-24 105859](https://github.com/user-attachments/assets/5bd6f0ea-48cf-4878-8eed-f8046aa11211)
![Screenshot 2024-09-24 110047](https://github.com/user-attachments/assets/b0757b7a-be41-4bfc-ae48-f10a8c2367bb)

---
- `$  ./p1.sh & `

![Screenshot 2024-09-24 110307](https://github.com/user-attachments/assets/71f7560d-a3b1-4b1c-b755-8d8564088e4a)

---
- `$  ./p1.sh $ ./p2.sh & ./p3.sh &`

![Screenshot 2024-09-24 110428](https://github.com/user-attachments/assets/8c32de2d-8bab-48ac-a646-4a1682df6e24)
![Screenshot 2024-09-24 110444](https://github.com/user-attachments/assets/976cf089-d926-44e6-a7e7-1e4355ae1f84)
![Screenshot 2024-09-24 110509](https://github.com/user-attachments/assets/20478f2a-7096-4bbe-973c-d6747be7a10a)
![Screenshot 2024-09-24 110824](https://github.com/user-attachments/assets/a4a86d10-23b3-4694-8651-7ace5c12c27a)

---
- `$  ( ./p1.sh ; ./p3.sh ) & `
![Screenshot 2024-09-24 111135](https://github.com/user-attachments/assets/7a5dec30-5320-4892-88d7-0a2c3d2ceb4a)
![Screenshot 2024-09-24 111148](https://github.com/user-attachments/assets/61e6e377-153f-437b-b972-e284cd6b9570)
![Screenshot 2024-09-24 111203](https://github.com/user-attachments/assets/bf844ea3-d875-4bb6-bd1d-2471f44393e4)
![Screenshot 2024-09-24 111220](https://github.com/user-attachments/assets/8b2fd6a3-0d18-4919-8f7b-b2807d0cb814)

---
## 5. Jobs  
a. Buat shell-script yang melakukan loop dengan nama `pwaktu.sh`,  setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil.  
```
#!/bin/bash  
while [ true ]  
do  
date >> hasil  
sleep 10  
done 
```

b.  Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background 
sebagai berikut :  
```
$ jobs  
$ find / -print > files 2>/dev/null &  
$ jobs
```
c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke 
background
```
$ fg %1  
$ bg  
d.  Stop program background dengan utilitas kil  
$ ps x  
$ kill [Nomor PID] 
```

Jawab:

![Screenshot 2024-09-24 111611](https://github.com/user-attachments/assets/aa86cbd7-bd16-4f41-a728-618ce8608068)

a. Pertama-tama gunakan command nano, kemudian isi shell-script dengan command pada soal di atas:

![Screenshot 2024-09-24 111447](https://github.com/user-attachments/assets/681af0be-9bdf-4cda-b900-592ea247329e)

b. Buat shell-script diatas menjadi executable, dangan menggunakan command `chmod +x pwaktu.sh`, kemudian jalankan script di background:

![Screenshot 2024-09-24 204355](https://github.com/user-attachments/assets/b3cac195-1f1d-47f4-a856-07a8690c2a7b)

Lalu jalankan perintah berikut :

- `jobs` dan `find / -print > files 2>/dev/null &`
![Screenshot 2024-09-24 111842](https://github.com/user-attachments/assets/c2107a4f-1466-4e17-85aa-e02c2eef55d5)

---
c.  Lalu kita gunakan command berikut :

- `fg %1` dan `bg`

![Screenshot 2024-09-24 111942](https://github.com/user-attachments/assets/422185a1-daad-4277-9f2d-89353eee9f15)

d. Untuk menghentikan program pada background, kita dapat menggunakan command kill. Tapi kita harus mengetahui nomor PID nya terlebih dahulu. Caranya kita bisa menggunakan command ps x.

![Screenshot 2024-09-24 112126](https://github.com/user-attachments/assets/9d4d9337-5765-4940-8b2d-43d2eb06f270)
![Screenshot 2024-09-24 112140](https://github.com/user-attachments/assets/1418ad13-43a8-494a-907a-142bd0249d30)

- fDisini sudah ditemukan program yang ingin dihentikan, sekarang kita dapat menggunakan command kill = nomor PID nya:
- 
![Screenshot 2024-09-24 114020](https://github.com/user-attachments/assets/34258de2-dc76-460f-8fc6-94dca22b2ea1)
![Screenshot 2024-09-24 114031](https://github.com/user-attachments/assets/7827f011-aa36-4ab1-8bcb-965df350c493)

Setelah melakukan eksekusi command kill ada tulisan Terminated ./pwaktu.sh, yang berarti proses nya sudah di stop.

---
## 6. History  
a. Ganti nilai HISTSIZE dari 1000 menjadi 20  
```
$ HISTSIZE=20  
$ h
```
b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir 
dilakukan  
```
$ !-5  
```
c. Ulangi instruksi yang terakhir.  Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer 
```
$ !!  
```
d.  Ulangi instruksi pada history bufer nomor 150  
```
$ !150 
```
e.  Ulangi instruksi dengan prefix “ls”  
```
$ !ls
```

Jawab:

a. Mengganti nilai HISTSIZE dari 1000 menjadi 20

![Screenshot 2024-09-24 114116](https://github.com/user-attachments/assets/7b2e2c83-a3bd-44d2-8468-23b306d8869c)

---
b. Menggunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan:

![Screenshot 2024-09-24 114156](https://github.com/user-attachments/assets/3c478bf7-e343-4380-941c-52dd03acac12)

---
c. Ulangi instruksi yang terakhir:

![Screenshot 2024-09-24 114234](https://github.com/user-attachments/assets/e5d93698-ae69-4acf-b780-7017ef4e6d29)

---
d. Ulangi instruksi pada history bufer nomor 150:

![Screenshot 2024-09-24 114301](https://github.com/user-attachments/assets/0ba1ffd8-b03e-4497-8ca3-ebec73f72e11)

---
e. Mengulangi instruksi dengan prefix “ls”

![Screenshot 2024-09-24 114330](https://github.com/user-attachments/assets/79d2ecc4-e025-46fd-9b7b-f03077b4758a)

Muncul pemberitahuan "event not found", itu dikarenakan command ls tidak ada didalam 20 daftar history.



