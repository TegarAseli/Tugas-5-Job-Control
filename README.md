# Tugas-5-Job-Control

### Nama   : Anugrah Tegar Noverzha
### NIM    : 09011282328029
### Kelas  : SK3B
___


1. Eksekusi seluruh profile yang ada :
   
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

![Screenshot 2024-09-24 103701](https://github.com/user-attachments/assets/103e7cdb-ea31-4d44-9a3a-8f7fa991d2ca)

























