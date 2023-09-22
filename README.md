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
First, we need to filter only HTTP response since this is a web server. We can use "http" as the filter

![Screenshot 2023-09-18 at 20 26 31](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/680d7696-9405-4a0d-abf8-2b0e0f4261ae)

Then, we need to look at the response from the server. In the screenshot, we can see 200 OK response. Looking deeper, we can find the name of the server "gunicorn"

<img width="707" alt="Screenshot 2023-09-18 at 20 27 30" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/4fdb398f-a401-4b38-b3d2-d7f5ddd59346">

![Screenshot 2023-09-18 at 20 52 38](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/9638fbe3-9fcf-4ef5-ac46-f860b91ef5a8)

# 3.

a. To find the number of packets with destination 239.255.255.250 and port 3702, we can use the filter "ip.dst == 239.255.255.250 and udp.port == 3702". We can see there's 21 packets

![Screenshot 2023-09-18 at 20 30 13](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/53afb33f-0476-4453-9a6c-05188282fb42)

b. Port 3702 is a port for the UDP protocol

![Screenshot 2023-09-18 at 20 57 39](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/173708cb-97a5-4a91-853d-2aed0412dca4)


# 4.

# 5.

# 6.

# 7.

# 8.

# 9.

# 10.