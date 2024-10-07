# my-notes-info
ini adalah note saya mengenai semua eror yang pernah saya alami

<h3>7 Oktober 2024</h3>
<h6>problem</h6>
```tikak bisa koneksi dengan adb secara wireless```
<h6>solved</h6>
```adb pair IPL:PORT``` (enter and add pairing code)
```adb connect IP:PORT```
```adb devices```

<h3>20 Agustus 2024</h3>

<h6>problem</h6>
```terjadi error ModuleNotFoundError: No module named 'flask_login'```
```kodisi lain dimana saat di jalankan langsung exit```
padahal sudah di install, solusinya jika menggunakan windows

<h6>solved</h6>

```Jalankan program lewat powershell dengan akses administrator```

<h3>26 Juni 2024</h3>

<h6>problem</h6>

```beberapa paket di termux tidak bisa diinstall```

<h6>solved</h6>

```pkg install tur-repo```lalu coba install kembali

<h3>17 Agustus 2024</h3>
<h6>problem</h6>

```flask db init```
```Error: No such command "db".```
<h6>solved</h6>

```pip install flask-migrate --upgrade```
```flask db init```
<br>
h3>24 October 2023</h3>
<h6>problem</h6>

```python 3.12 eror install openai library```
<h6>solved</h6>

```downgrade to python 3.10```
<br>

<h6>problem</h6>

```youtube adbock problem```
<h6>solved</h6>
<a href="https://www.tampermonkey.net/index.php?version=4.19.0&ext=iikm&updated=true">tampermonkey</a> download ekstension
<br>
<a href="https://github.com/TheRealJoelmatic/RemoveAdblockThing/releases/tag/v8">github</a> click  javacript file and  click install button
<br>
<h6>alternative</h6>
<a href="https://yewtu.be">YEWTU</a>


<h3>25 October 2023</h3>
<h6>problem</h6>

```gagal module 'PIL.Image' has no attribute 'ANTIALIAS'```

<h6>solved</h6>

```pip uninstall Pillow```
<br>
```pip install Pillow==9.5.0```
<br>
solusi lain
replace ```Image.ANTIALIAS``` with ```Image.Resampling.LANCZOS```
<br>

<h3>13 November 2023</h3>
<h6>problem</h6>

``` -_- ```

<h6>solved</h6>

```Eror```
<br>
```Eror```
<br>


<h3>27 Desember 2023</h3>
<h6>problem</h6>

```AttributeError: module 'httpcore' has no attribute 'SyncHTTPTransport```

<h6>solved</h6>

```pip install httpcore==0.15.0 httpx pymongo googletrans```
<br>


<h3>12 Januari 2024</h3>
<h6>problem</h6>
<h6>Windows 11 CMD git</h6>

``` (END) ```

<h6>solved</h6>

type```:q```
<br>


<h3>13 Januari 2024</h3>
<h6>problem</h6>
<h6>Install gh(github CLI)</h6>

``` make repository from Command Prompt ```

<h6>solved</h6>

```run windows cmd as administrator```
type```choco install gh```
<br>


<h3>16 Januari 2024</h3>
<h6>problem</h6>

``` AttributeError: 'NoneType' object has no attribute 'groups'```

<h6>solved</h6>

```Debian linux in VPS```
type```pip uninstall gdown```<br>
type```pip install gdown==4.6.1```
<br>
<h3>16 Januari 2024</h3>
<h6>problem</h6>

```2024/01/16 20:40:27 Fatal error: failed to mount FUSE fs: mount stopped before calling Init: mount failed: cgofuse: cannot find winfsp```

<h6>solved</h6>

```Windows 11```
type```choco install winfsp```
<br>
<h3>16 Januari 2024</h3>
<h6>problem</h6>

```login google VPS with windows 11```

<h6>solved</h6>

```VPS to Windows 11```
type```ssh -L 53682:localhost:53682 -C -N -l <your_user> <your_remote_server_ip>```
<br>
paste link google login from VPS to Windows 11
<br>

<br>
<h3>28 Januari 2024</h3>
<h6>problem</h6>

```Install package linux in background (GOOGLE COLAB)```

<h6>solved</h6>

type```!pip install nohup```
type```!nohup pip install selenium &```
<br>

<br>
<h3>9 Februari 2024</h3>
<h6>problem</h6>

```Kotlin cloud```

<h6>solved</h6>
<a href="https://play.kotlinlang.org">KOTLIN CLOUD</a>
<br>

<br>
<h3>21 Februari 2024</h3>
<h6>problem</h6>
<p>saat ingin menggunakan venv biasanya kita perlu melakukan activate di terminal, dengan adanya python intrepeter kita tidak perlu lagi melakukannya lewat terminal dan bisa langsung lewat Vscode</p>

```Python intrepeter```

<h6>solved</h6>
```

<br>
<br>
<h3>24 Maret 2024</h3>
<h6>problem</h6>

```
npx tailwindcss init
'_Jumpstart_Your_Dev_Career\client\node_modules\.bin\' is not recognized as an internal or external command,
operable program or batch file.
node:internal/modules/cjs/loader:1080
  throw err;
  ^

Error: Cannot find module 'D:\Nadzib\Documents\proyek_threejs\tailwindcss\lib\cli.js'
    at Module._resolveFilename (node:internal/modules/cjs/loader:1077:15)
    at Module._load (node:internal/modules/cjs/loader:922:27)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:81:12)
    at node:internal/main/run_main_module:23:47 {
  code: 'MODULE_NOT_FOUND',
  requireStack: []
}

Node.js v18.17.1
```

<h6>solved</h6>
```Hilangkan tanda & dan simbol lainnya termasuk ' '(spasi) untuk folder threejs-nya```

<br>
<h3>7 April 2024</h3>
<h6>problem</h6>

```
sudo nmap -sS 10.129.57.162
Starting Nmap 7.94 ( https://nmap.org ) at 2024-04-07 20:00 WIB
Nmap scan report for 10.129.57.162
Host is up (0.29s latency).
All 1000 scanned ports on 10.129.57.162 are in ignored states.
Not shown: 1000 closed tcp ports (reset)

Nmap done: 1 IP address (1 host up) scanned in 19.74 seconds
```

<h6>solved</h6>
```Masih Eror:🛐```

<br>



<h3>9 April 2024</h3>
<h6>problem</h6>

Saya ingin menghubungkan 2 jaringan openVPN dari Hackthebox dan TryhackMe. untuk itu saya memerlukan 2 port, dikarenakan port 1 sudah ada maka sekarang saya perlu membuat port yang ke-dua 

<h6>solved</h6>

open Terminal

> ```ip a```

> ```gajadi udh bisa otomatis wkwk💀🗿```

 #### Update 10 April 2024

- Lakukan konfigurasi sebagai berikut untuk membuatnya menjadi otomatis =

> ```nano ~/.bashrc``` ini adalah file yang selalu dieksekusi ketika user masuk di LINUX  

- scroll ke bawah dan tambahkan ini

> ```sudo openvpn /mnt/d/download/openvpn1.ovpn &```

> ```sudo openvpn /mnt/d/download/openvpn2.ovpn &``` Fungsi & disini agar scrip dijalankan di background, anda bisa mencobanya dengan dengan menghilangkan & untuk melihat perbedaannya

- tekan CTRL+X lalu Y

- ketikkan ```source ~/.bashrc```

- jika sudah ada tulisan ```sucessfully``` maka sudah selesai anda dapat tekan tombol Enter(ini adalah letak perbedaan jika anda menggunakan & dan tidak) 
<br>




<h3>9 Mei 2024</h3>

<h6>problem</h6>

Melihat proses selenium yang berada di Docker

<h6>solved</h6>

> <a href="https://docs.docker.com/engine/install/ubuntu/#installation-methods">Buka link untuk menginstall Docker</a>

> <a href="https://www.realvnc.com/en/connect/download/viewer/">Buka link untuk menginstall VNC Viwer</a>

> ```docker run -d -p 4444:4444 -p 5900:5900 --shm-size="2g" selenium/standalone-firefox:4.20.0-20240505``` 

> Buka VNC Viewer
> Buka IP localhost(```127.0.0.1```):tambahkan port sesuai yang kita tambahkan disini ```-p 5900:5900```  disini kita menggunakan port 5900 jadi tambahkan port ```:5900```

 [IP]:[PORT] = ```127.0.0.1:5900```


 
