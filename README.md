# Jarkom-Modul-1-I03-2023
Lapres Praktikum Jarkom Modul 1 2023

Group members:
- Fauzan Ahmad Faisal (5025211067)
- Muhammad Ghifari Taqiuddin (5025211063)

Questions: https://docs.google.com/document/d/11D9IyOtBzf-MwVAiXIDZ0jQ92lO4lbOQZlospKTKIcc/edit

# 1.

There are several types of request in the FTP protocol, for example `RETR` (when downloading a file from the server) and `STOR` (when user uploads file to the server). We must search for the occurences of STOR request in the capture file. First, filter so that only FTP protocol are being displayed, using the "ftp" filter

![Screenshot 2023-09-18 at 19 13 18](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/8f18fab2-3502-4a5e-8ac4-9457a65fedb3)

a. We can see 1 STOR request there, and looking deeper, the raw sequence number (SEQ) is 258040667

<img width="499" alt="Screenshot 2023-09-18 at 19 15 51" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/3e81d7a4-932e-4293-a511-20cbfcb4434b">

b. The raw acknowledge number (ACK) from the screenshot above is 1044861039

c. The response of the previous request is right after it, and checking the sequence number, we get 1044861039

<img width="501" alt="Screenshot 2023-09-18 at 19 18 53" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/c75f6924-7829-45c1-86a5-b2090a76115a">

d. And for ACK number, we get 258040696

![Screenshot 2023-09-18 at 20 56 19](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/e336b36d-2e7a-412e-beb8-fae36d56587e)

# 2.
# 3.
# 4.
# 5.
# 6.
# 7.
# 8.
# 9.
# 10.