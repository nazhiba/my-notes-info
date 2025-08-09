# my-notes-info
ini adalah note saya mengenai semua eror yang pernah saya alami

## August 9, 2025
### Problem
When I use Duolingo on Linux with the Microsoft Edge browser, there is no sound.

### Solved
In the Microsoft Edge browser, navigate to `edge://settings/?search=audio` and select **Block** under the setting `Control if audio and video play automatically on sites`.

## 25 July 2025
**Problem**  
Docker containers on Server 1 were experiencing high memory consumption, causing performance degradation and potential system instability. The server was running Docker version 27.5.1, while Server 2 was running the newer version 28.1.1+1 with significantly better memory management and resource optimization.

**Solved**  
The Docker Engine was upgraded from version 27.5.1 to 28.1.1+1 on Server 1 to match Server 2's configuration. The upgrade process involved:

1. Adding the official Docker repository GPG key
2. Configuring the Docker apt repository for Ubuntu 22.04
3. Installing the specific Docker version using:
   ```bash
   VERSION_STRING=5:28.1.1-1~ubuntu.22.04~jammy
   sudo apt-get install docker-ce=$VERSION_STRING docker-ce-cli=$VERSION_STRING containerd.io docker-buildx-plugin docker-compose-plugin
   ```

This upgrade provided improved memory management, better resource utilization, and enhanced stability for containerized applications. The memory consumption issue was resolved, and both servers now run identical Docker versions for consistency across the infrastructure.

<h3>17 July 2025</h3>
<h6>Problem</h6>
Some files that are already tracked in the repository (such as configuration or profile files) need to be modified locally to store session data or credentials. However, these local changes must not be committed back to the repository. Using `.gitignore` does not solve this issue, as it is only effective for files that have never been tracked by Git.

<h6>Solved</h6>
The solution is to use a Git command to mark already-tracked files so that their local changes are ignored. The command used is:

`git update-index --assume-unchanged <file-name>`

This instructs Git to no longer monitor changes to these files in the local working directory. As a result, the local version of the file containing sensitive data can persist without the risk of being committed.

To revert this and have Git track changes to the file again, use the command:

`git update-index --no-assume-unchanged <file-name>`

<h3>14 July 2025</h3>
<h6>Problem</h6>
The application experienced periodic crashes (<code>caught signal: 11</code>) after running for extended periods, indicating a memory leak or instability within the Puppeteer-controlled browser instance. The session refresh mechanism, intended to keep the session alive, introduced further complications: it would either destroy the session entirely (forcing a re-login) or redirect to an incorrect page after the refresh.
<h6>Solved</h6>
The session refresh logic in main.js was reworked to improve long-term stability. A periodic process now navigates the active browser page to about:blank, which effectively clears its resources and prevents memory leaks without destroying the underlying user session. Following this cleanup, the session is re-validated, and the page is then programmatically directed to its intended URL. This approach ensures the application remains stable and always maintains the correct navigational context after each refresh cycle.

<h3>14 July 2025</h3>
<h6>Problem</h6>
When building a Docker image from a Windows host, shell scripts copied into the container fail to execute, often with a "No such file or directory" error. This is caused by a mismatch in line-ending formats between Windows (CRLF) and the container's Linux environment (LF), which renders the scripts unreadable by the Linux shell.
<h6>Solved</h6>
The Dockerfile was modified to automatically convert script line endings during the image build process. A RUN command utilizing sed was added to strip the carriage return characters (\r) from the affected shell scripts immediately after they are copied into the image. This ensures the scripts use the correct Unix-style (LF) line endings and become executable within the container, fixing the issue permanently without requiring manual file conversion

<h3>23 May 2025</h3>
<h6>Problem</h6>

When running `whatsapp-web.js` in a Docker container, it gets stuck at `whatsapp-bot-app | Mencoba menginisialisasi client WhatsApp...`.

<h6>Solved</h6>

I'm using Windows 11 and ran `make down; make build; make up`.

Here's the Makefile I used. I'm not exactly sure why this sequence fixed the issue:)

```
build:
	docker compose build

up:
	docker compose up -d --build --force-recreate

down:
	docker compose down
```

<h3>18 Mei 2025</h3>
<h6>problem</h6>

```Laptop couldn't connect to the main Wi-Fi again.```

<h6>solved</h6>

```turn off wifi windows```

```turn on wifi windows```

<h3>26 April 2025</h3>
<h6>problem</h6>

```Laptop couldn't connect to the main Wi-Fi after booting, showing "Can't connect to this network". However, it worked fine when using mobile hotspot.```

<h6>solved</h6>

```Logged into Tenda router settings and changed the following:```

```Wireless Channel: Auto → 6```

```Channel Width: Auto → 20MHz```

```After saving and restarting the router, the laptop connected automatically without issues.```


<h3>11 Desember 2024</h3>
<h6>problem</h6>
```install go deb untuk windows```

- [download](https://github.com/golang/dep/releases)

- rename ke ```deb.exe```

- refrensi [github](https://github.com/golang/dep/issues/2086#issuecomment-455903281)


<h3>7 Oktober 2024</h3>
<h6>problem</h6>

```tidak bisa koneksi dengan adb secara wireless```
<h6>solved</h6>

```adb pair IPL:PORT``` (enter and add pairing code)

```adb connect IP:PORT```

```adb devices```

<h3>27 Agustus 2024</h3>

```python
# Membuat aplikasi Desktop dan terjadi masalah dimana 
from pydub import AudioSegment
ffmpeg = resource_path("ffmpeg\\bin\\ffmpeg.exe")
AudioSegment.converter = ffmpeg
#dst. tidak berfungsi

# dirubah dengan
from pydub import AudioSegment
import os
ffmpeg = "ffmpeg\\bin"
os.environ["PATH"] = ffmpeg + os.pathsep + os.environ["PATH"]
# ini akan menambahkan path ke environment variabel Windows
```

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


 
