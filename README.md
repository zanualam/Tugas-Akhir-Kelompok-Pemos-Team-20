# 🌊TUGAS AKHIR KELOMPOK PEMOS TEAM 20🌊
_Repository_ ini dibuat untuk memenuhi Tugas Akhir Kelompok Praktikum Pemodelan Oseanografi 2022. _Repository_ ini memuat file berupa _script python_ (py) yang digunakan untuk memproses beberapa pemodelan oseanografi seperti Adveksi-Difusi dan Hidrodinamika. Pengerjaan _repository_ ini menggunakan bahasa pemrograman _python_ yang dapat dilakukan pada beberapa _platform_ seperti _Google Collaboratory_ atau _Jupyter Notebook_. _Mandatory library_ yang digunakan kali ini adalah _Numpy, Matplotlib, Python, Sys, Siphon_ dan _Pprint_. Seluruh _script_ yang dibuat adalah hasil Team 20 Oseanografi 2020. Semoga dapat bermanfaat!

## 🙋🏼‍♀️1. AUTHORS (TEAM 20)🙋🏼‍♂️
1. Doding Akka Damanik
2. Azalya Besari Noerazzahra Tilaar
3. Umar Abdul Aziz
4. Clarisa Wulandari
5. Ananda Annisa Fitriani
6. M. Zanugera Alamsyah 26050120120015 A
7. Olivia Rebeka Vera Wati Sinaga

## 🗒️2. CARA PENGGUNAAN SCRIPT🗒️
1. Pengguna dapat membuka folder _Kumpulan Script_ pada _repository_ ini. Di dalamnya terdapat 3 _script_, bisa dibuka salah satu.
![1](https://user-images.githubusercontent.com/105897134/169439922-6bd9c427-5733-41fc-80cb-f50c3f0425c6.png)
2. Tampilan _script_ akan muncul seperti gambar di bawah ini. 
![2](https://user-images.githubusercontent.com/105897134/169441338-d7256c02-e782-4407-aea9-a395260713d6.png)
3. Script dapat di-_copy_ untuk nantinya dipergunakan dan disesuaikan di _Jupyter Notebook_ maupun _Google Collaboratory._

## 🧮3. METODE PENGERJAAN📝
1. Modul 2: Adveksi-Difusi 2 Dimensi
2. Modul 3: Model Hidrodinamika 1 Dimensi Sederhana
3. Modul 4: Model Hidrodinamika 2 Dimensi

### 📒**3.1. Modul 2: Adveksi-Difusi 2 Dimensi**📒

#### 📌Definisi dan Persamaan📌
Adveksi 2 dimensi adalah proses pergerakan substansi atau materi oleh fluida akibat dipengaruhi gaya-gaya tertentu dalam arah vertikal dan horizontal.

![Adveksi 2D](https://user-images.githubusercontent.com/105897134/169457375-a9fa82d8-3b9d-4328-9fe2-c178e3d62e2d.png)

Difusi 2 dimensi adalah proses penyebaran substansi atau materi oleh fluida akibat dipengaruhi gaya-gaya tertentu dalam arah vertikal dan horizontal.

![Difusi 2D](https://user-images.githubusercontent.com/105897134/169457501-c4c608fa-3f05-459d-86ee-3362975ba08c.png)

Persamaan adveksi-difusi merupakan persamaan matematis yang dirancang untuk mempelajari fenomena transpor polutan. Persamaan adveksi-difusi dua dimensi merupakan model matematika yang menggambarkan proses transportasi suatu zat yang dipengaruhi gaya dalam dua dimensi. Persamaannya secara umum sebagai berikut:

![Adveksi-Difusi 2D](https://user-images.githubusercontent.com/105897134/169457432-c04c6964-4144-4fba-8312-d8f416b24cff.png)

#### 📌Metode Diskritisasi Beserta Hasilnya📌
Diskritisasi persamaan adveksi-difusi 2 dimensi menggunakan metode eksplisit upstream dimana persamaan beda hingga dengan metode ini menggunakan pendekatan beda maju untuk turunan waktu, sedangkan untuk turunan ruang dilakukan dengan melihat arah kecepatan _u_.
Jika _u_ > 0, turunan ruang menggunakan beda mundur. Jika _u_ < 0, digunakan pendekatan beda maju. Berikut adalah hasil diskritisasi untuk persamaan adveksi 2 dimensi.

![Diskritisasi Adveksi 2D](https://user-images.githubusercontent.com/105897134/169457504-4f6cd76c-eaed-4a65-8408-53f57042fc0a.png)

Model 2 dimensi untuk mekanisme transpor difusi dapat menggunakan pendekatan beda maju untuk turunan waktu dan beda pusat untuk turunan ruang. Berikut adalah hasil diskritisasi untuk persamaan difusi 2 dimensi.

![Diskritisasi Difusi 2D](https://user-images.githubusercontent.com/105897134/169457506-9fbe396c-701e-44b4-b9c9-5eb6394e468b.png)

Indeks _n_ untuk waktu, indeks _i_ untuk ruang dan koefisien difusi AD dianggap konstan terhadap ruang dan waktu. Berikut ini adalah hasil diskritisasi persamaan adveksi-difusi 2 dimensi.

![Diskritisasi Adveksi-Difusi 2D](https://user-images.githubusercontent.com/105897134/169457505-80ee0398-73f8-4c15-9d86-0d7bbfce05ad.png)

#### 📌Penentuan Nilai Batas dan Syarat Batas📌
Syarat batas merupakan suatu kondisi yang menggambarkan kondisi di batas (ruang maupun waktu) dari model yang dibangun. Syarat batas dari metode eksplisit upstream diberikan pada nilai awal (hulu) dan nilai akhir (hilir).

![Syarat Batas](https://user-images.githubusercontent.com/105897134/169457513-581f12b3-d391-4310-b1a1-71a25c1ec425.png)

#### 📌Saat Iterasi Dihentikan📌
Syarat awal yang digunakan dalam skenario model 2D adveksi-difusi ini adalah dengan memberikan harga 0 di semua titik konsentrasi polutan kecuali di titik-titik sumber yang tersebar dan sumber bersifat tidak kontinu.

![Iterasi](https://user-images.githubusercontent.com/105897134/169457510-64116b16-bf28-4cf3-99eb-7804c56fba14.png)

#### 📌Kriteria Kestabilan📌
Suatu metode untuk menentukan seberapa besar nilai stabilitas dari model yang digunakan.

![Kriteria Kestabilan](https://user-images.githubusercontent.com/105897134/169457512-b6746147-ed68-48e3-bd10-2db4965b62ab.png)

#### 📌Pengerjaan Script📌
1. Memasukkan _mandatory library python matploblib_ untuk memberikan efek visual pada grafik, _numpy_ untuk perhitungan numerik dan _sys_ untuk mengakses konfigurasi interpreter pada saat _runtime_. Memasukkan juga pendefinisian.
```
import matplotlib.pyplot as plt
import numpy as np
import sys
 
def percentage(part, whole):
        percentage = 100 * float(part)/float(whole)
        return str(round(percentage,2)) + "X"

```
2. Selanjutnya, memasukkan parameter perhitungan polutan yang akan digunakan.
```
#Memasukkan Parameter Awal
C = 1.51    #Kecepatan Aliran
ad = 1.51   #Koefisien Difusi
#Arah Arus (Berdasarkan Geographic Convention)
theta = 0  #Skenario I, II, III atau IV
#Parameter Lanjutan
q = 0.95    #Kriteria Kestabilan
x = 500     #Jumlah Grid Horizontal (x)
y = 500     #Jumlah Grid Vertikal (y)
dx = 5      
dy = 5
Tend = 105   #Lama Simulasi
#Tend = 1
dt = 0.5
#Polutan
px = 250   #Polutan pada grid x
py = 235   #Polutan pada grid y
Ic = 1051   #Jumlah Polutan
 
```
3. Kemudian, _script_ perhitungan dibuat untuk mengetahui persebaran polutan.
```
#Perhitungan U dan V ()
u = C * np.sin(theta*np.pi/180)
v = C * np.cos(theta*np.pi/180)
dt_count = 1/((abs(u)/(q*dx))+(abs(v)/(q*dy))+(2*ad/(q*dx*2))+(2*ad/(q*dy*2)))
 
Nx = int(x/dx)      #number of mesh in x direction
Ny = int(y/dy)      #number of mesh in y direction
Nt = int(Tend/dt)   #number of timesteps
#Perhitungan Titik Polutan di Buang
px1 = int(px/dx)
py1 = int(py/dy)
 
#Fungsi disederhanakan
lx = u*dt/dx
ly = v*dt/dy
ax = ad*dt/dx**2
ay = ad*dt/dy**2
cfl = (2*ax + 2*ay + abs(lx) + abs(ly))     #Syarat Kestabilan CFL
#Perhitungan CFL
if cfl >= q:
    print('CFL Violated, Please use dt :'+str(round(dt_count,4)))
    sys.exit()
#%%

```
4. Setelah itu, _script_ pembuatan grid dibuat sebagai alat bantu untuk menyusun atau mengatur hasil _running_ polutan.
```
#Pembuatan Grid
x_grid = np.linspace(0-dx, x+dx, Nx+2)      #Ghostnode pada boundary
y_grid = np.linspace(0-dx, y+dy, Ny+2)      #Ghostnode pada boundary
t = np.linspace(0, Tend, Nt+1)
x_mesh,y_mesh = np.meshgrid(x_grid,y_grid)
F = np.zeros((Nt+1, Ny+2, Nx+2))
 
```
5. Selanjutnya, iterasi dilakukan sampai semua syarat batas terpenuhi.
```
#Kondisi Awal(Initial Condition)
F[0,py1,px1] = Ic
#%%
#Iterasi
for n in range (0, Nt):
    for i in range (1,Ny+1):
        for j in range(1,Nx+1):
            F[n+1,i,j]=((F[n,i,j]*(1-abs(lx)-abs(ly)))  + \
                        (0.5*(F[n,i-1,j]*(ly+abs(ly)))) + \
                        (0.5*(F[n,i+1,j]*(abs(ly)-ly))) + \
                        (0.5*(F[n,i,j-1]*(lx+abs(lx)))) + \
                        (0.5*(F[n,i,j+1]*(abs(lx)-lx))) + \
                        (ay*(F[n,i+1,j]-2*(F[n,i,j])+F[n,i-1,j])) + \
                        (ax*(F[n,i,j+1]-2*(F[n,i,j])+F[n,i,j-1]))) #Diskritisasi
    #Syarat Batas (Dirichlet Boundary Condition)
    F[n+1,0,:] = 0 #BC Bawah
    F[n+1,:,0] = 0 #BC Kiri
    F[n+1,Ny+1,:] = 0 #BC Atas
    F[n+1,:,Nx+1] = 0 #BC Kanan
 
``` 
6. Langkah berikutnya membuat _script_ untuk _output_ gambar penyebaran polutan. _Script_ siap dijalankan.
```
    #Output Gambar
    plt.clf()
    plt.pcolor(x_mesh, y_mesh, F[n+1,:,:],cmap = 'jet',shading ='auto',edgecolors = 'k')
    cbar = plt.colorbar(orientation = 'vertical', shrink = 0.95, extend = 'both')
    cbar.set_label(label='Concentration', size = 8)
    #plt.clim(0,100)
    plt.title('Nama Lengkap_NIM \n t='+str(round(dt*(n+1),3))+', Initial Condition='+str(Ic),fontsize=10)
    plt.xlabel('x_grid',fontsize=9)
    plt.ylabel('y_grid',fontsize=9)
    plt.axis([0, x, 0, y])
    #plt.pause(0.01)
    plt.savefig(str(n+1)+'.jpg', dpi = 300)
    plt.pause(0.01)
    plt.close()
    print('running timestep ke:' +str(n+1) + ' dari:' +str(Nt) + '('+ percentage(n+1,Nt)+')')
    #print('Nilai CFL:' +str(cfl) + ' dengan arah:' +str(theta))
```
#### 📌Hasil Running📌
![Hasil Running](https://user-images.githubusercontent.com/105897134/169467814-4a96de24-4c9f-4309-b1ae-5ceef7ffa5d9.png)
