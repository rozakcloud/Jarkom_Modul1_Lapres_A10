# Lapres Modul 1 Jarkom Kelompok A10
# A. Display Filter
## 1. Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
### http.host == "testing.mekanis.me"
### Follow tcp stream packet tersebut, dan akan terlihat bahwa web servernya adalah nginx
### Web server dari http://testing.mekanis.me/ adalah nginx

![1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/1.jpg)

### 2. Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!
### http contains "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"

![2_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/2-1.jpg)
![2_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/2-2.jpg)
![2_3](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/2-3.jpg)

### 3. Cari username dan password ketika login di "ppid.dpr.go.id"!
### http.host contains "ppid.dpr.go.id" && http.request.method ==POST
### Username = 10pemuda
### Password = guncangdunia
![3_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/3-1.jpg)
![3_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/3-2.jpg)

### 4. Temukan paket dari web-web yang menggunakan basic authentication method!
### http.authbasic
### untuk mencari web-web yang menggunakan basic authentication
![4](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/4.jpg)

### 5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!
### masuk ke website "aku.pengen.pw" dan isi sesuai perintah
![5_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/5-2.jpg)
### Buka Authorization, akan terlihat Credentialnya
### Username: kakakgamtenk
### Password: hartatahtabermuda
![5](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/5.jpg)

### 6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).
### ftp-data.command contains "Answer.zip"
### Follow TCP Stream packetnya dan save dengan bentuk raw dengan ekstensi .zip
### buka file zipnya dan masukkan password dengan cara
### ftp-data.command contains "zipkey" dan akan ketemu passnya di info packetnya
![6_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/6-1.jpg)
![6_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/6-2.jpg)
![6_3](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/6-3.jpg)

### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf" 
### frame contains “Yes.pdf”
### Lalu klik kanan packet dan pilih Folow -> Follow  TCP Stream
### Lalu ganti “ASCII” “Show and save data as” dengan “Raw”
### Lalu save file dengan nama Yes.zip
### Buka file Yes.zip yang berisi Yes.pdf, dan buka pdfnya
![7](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/7.jpg)
![7_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/7-2.jpg)

### 8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service! 
### ftp contains "Microsoft", lalu akan kelihatan bahwa IP dari Microsoft tersebut adalah 198.246.117.106
### ip.host == 198.246.117.106 && ftp.request.command == RETR
### objek yang di download adalah readme
![8](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/8.jpg)

### 9. Cari username dan password ketika login FTP pada localhost!
### ftp.request.command == USER or tp.request.command == PASS
### Username : dhana
### Password : dhana123

![9_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/9.jpg)
![9_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/9-2.jpg)

### 10. Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46" 
### Ctrl+F dan cari hex value dari “25 50 44 46”
### Lalu pada packet tersebut tekan Follow -> TCP Stream
### Lalu ganti “ASCII” “Show and save data as” dengan “Raw”
### Simpan dengan ekstensi .pdf
![10_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/10-1.jpg)
![10_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/10-2.jpg)
![10_3](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/10-3.jpg)

## B. Capture Filter
### 11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
#### masukkan pada Capture Filter "port 21", akan terlihat semua packet yang berasal atau menuju port 21
![11](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/11.jpg)

### 12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
### masukkan pada Capture Filter "src port 80", akan muncul semua packet yang berasal dari port 80
![12](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/12.jpg)

### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
### masukkan pada Capture Filter "dst port 443", akan muncul semua packet yang menuju ke port 443
![13](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/13.jpg)

### 14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
### IP kita sendiri dapat dilihat melalui CMD dan menulis keyword ‘ipconfig’ .Setelah itu berhasil mendapat IP yang terdapat di ipv4 Address -> 192.168.0.17
### setelah kita tahu IP kita, masukkan pada Capture Filter "src 192.168.0.17"

![14](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/14.jpg)

### 15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
### masukkan pada Capture Filter "dst monta.if.its.ac.id", akan muncul semua packet yang berdestinasi monta.if.its.ac.id
![15](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/15.jpg)
