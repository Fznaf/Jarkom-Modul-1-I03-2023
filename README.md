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

We can directly go to packet no. 130, and check the detail panel. There we can find the header checksum, which is "0x18e5"

<img width="718" alt="Screenshot 2023-09-18 at 20 45 25" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/968d1f7e-a3e2-4cfa-aaa3-e3937aa68308">

![Screenshot 2023-09-18 at 20 53 26](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/24cbddc7-c4e2-41fd-878e-14c6a510d910)

# 5.

There are zip file provided with a password, the password might be available in the capture file, so we will check it first.

![Screenshot 2023-09-18 at 21 23 45](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/d1581ddd-19c0-4089-9017-b25ddf0edaa4)

The SMTP file isn't encrypted, so we can take a look at the content. One of them contains email with the password

<img width="691" alt="Screenshot 2023-09-18 at 21 24 22" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/fdefd32a-37f7-4c4c-b0c0-4ce1425ce3a0">

The password is encoded in Base64, decoding it yields "5implePas5word". After unlocking the zip file, we can connect to the netcat server and insert the answer to get the flag

<img width="718" alt="pasted image 0" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/e352675e-c806-43f6-ada3-32862cbfe98e">

# 6.

We're being told that "SOURCE ADDRESS 7812" is invalid. Source address here means the IP source and 7812 means we need to take a look at packet no. 7812. The clue a1 e5 u21 means that we need to convert the number into letter (1=a, 2=b, ..., 26=z).

<img width="566" alt="Screenshot 2023-09-22 at 19 23 45" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/2ac16153-a58a-46e7-9c85-c192a4c753b7">

Converting `104.18.14.101`, we get `JDRNJA` and we can get the flag

# 7.

To find packets that go to ip 184.87.193.88, we can use the filter "ip.dst == 184.87.193.88"

![Screenshot 2023-09-18 at 20 32 23](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/cd36a1ff-cf76-471f-a413-590545fce72b)

The number of packets displayed is 6, put it into the netcat and then we will get the flag.

<img width="620" alt="Screenshot 2023-09-18 at 20 58 37" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/bc5be9d5-376e-4412-8b4d-0ff7a18cdb98">

# 8.

The question asked us to make a query filter that will display all the packets that are going to port 80.
The query would be ```tcp.portdst == 80 || udp.portdst == 80```

Our team did not manage to answer this question on the practicum timeline because we forget to put "dst" on "dstport"

# 9.

To answer question number 9, similar to number 8, we  just need to make a query filter that will display only the packets that came from the address 10.51.40.1 but not going to address 10.39.55.34.

The query that will fulfill the requirement would be ```ip.src == 10.51.40.1 && ip.dst != 10.39.55.34```

Unfortunately we also didn't manage to solve this in practicum because the answer checks for literal string and our team missed the correct formatting.

# 10.

For number 10, we will first filter the package to only display the ones that has TELNET protocol using ```telnet```

![Screenshot 2023-09-18 at 20 33 52](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/8ef70170-aa0a-4447-97d7-ced5afd5c855)

Then, since TELNET is unencrypted, we can check for each packet to see the credentials. In this case, packet no. 81 contains the correct credentials, which is `dhafin:kesayangannyak0k0`

<img width="718" alt="Screenshot 2023-09-18 at 20 35 19" src="https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/57976bb0-90de-4cbd-9e12-fbe18d9ee5f2">

![Screenshot 2023-09-18 at 20 52 22](https://github.com/Fznaf/Jarkom-Modul-1-I03-2023/assets/59758342/e7a666c6-9769-477d-9030-2379c9e56623)

# Revision
- We couldn't solve problem 6

# Issues
- We know the query for no. 8 and 9, but we couldn't get the flag as the answer on the server may be different to ours
