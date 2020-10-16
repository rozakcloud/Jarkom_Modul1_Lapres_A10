# Lapres Modul 1 Jarkom Kelompok 10

## A. Display Filter
1. http.host == "testing.mekanis.me"
Follow tcp stream packet tersebut, dan akan terlihat bahwa web servernya adalah nginx
Web server dari http://testing.mekanis.me/ adalah nginx

![1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/1.jpg)

2.http contains "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"

![2_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/2-1.jpg)
![2_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/2-2.jpg)
![2_3](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/2-3.jpg)

3.http.host contains "ppid.dpr.go.id" && http.request.method ==POST
Username = 10pemuda
Password = guncangdunia
![3_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/3-1.jpg)
![3_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/3-2.jpg)

4. http.authbasic
untuk mencari web-web yang menggunakan basic authentication
![4_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/4-1.jpg)
![4_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/4-2.jpg)

5. Http contains “aku.pengen.pw”
Buka Authorization, akan terlihat Credentialnya
Username: kakakgamtenk
Password: hartatahtabermuda
![5](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/5.jpg)

6. ftp-data.command contains "Answer.zip"
Follow TCP Stream packetnya dan save dengan bentuk raw dengan ekstensi .zip
buka file zipnya dan masukkan password dengan cara
ftp-data.command contains "zipkey"
dan akan ketemu passnya di info packetnya

7. Frame contains “Yes.pdf”
Lalu klik kanan packet dan pilih Folow -> Follow  TCP Stream
Lalu ganti “ASCII” “Show and save data as” dengan “Raw”
Lalu save file dengan nama Yes.zip
Buka file Yes.zip yang berisi Yes.pdf, dan buka pdfnya
![7](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/7.jpg)
![7_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/7-2.jpg)

8. ftp contains "Microsoft"
ip.host == 198.246.117.106 && ftp.request.command == RETR
yang di download adalah readme

9. ftp.request.command == USER or tp.request.command == PASS
Username : dhana
Password : dhana123

![9_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/9.jpg)
![9_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/9-2.jpg)

10. Ctrl+F dan cari hex value dari “25 50 44 46”
“25 50 44 46” merupakan hex value dari %PDF
Lalu tekan Follow -> TCP Stream
Lalu ganti “ASCII” “Show and save data as” dengan “Raw”
Simpan dengan ekstensi .pdf
![10_1](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/10-1.jpg)
![10_2](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/10-2.jpg)
![10_3](https://github.com/rozakcloud/Jarkom_Modul1_Lapres_A10/blob/main/img/10-3.jpg)

## B. Capture Filter
11. port 21

12. src port 80

13. dst port 443

14. ip.src == 192.168.100.5

IP kita sendiri dapat dilihat melalui CMD dan menulis keyword ‘ipconfig’ .Setelah itu berhasil mendapat ip yang terdapat di ipv4 Address -> 192.168.100.5

15. ip.dst == 103.94.190.11 && http.request.method == GET
