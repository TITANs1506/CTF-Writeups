# **who is it**
## **Challenge**
Someone just sent you an email claiming to be Google's co-founder Larry Page but you suspect a scam.
Can you help us identify whose mail server the email actually originated from?
Download the email file [here]. Flag: picoCTF{FirstnameLastname}
## **Writeup**
Mình đánh giá đây là 1 bài CTF khá khoai khi định dạng flag là tên người như thế này. Để tìm được nguồn gốc của server ta phải tìm được ip trong file trước:
```
strings email-export.eml | grep "ip"
        (version=TLS1_3 cipher=TLS_AES_256_GCM_SHA384 bits=256/256)
Received-SPF: pass (google.com: domain of lpage@onionmail.org designates 173.249.33.206 as permitted sender) client-ip=173.249.33.206;
Content-Type: multipart/mixed; boundary="--_NmP-426c22a2e0d8fc9a-Part_1"
Content-Type: multipart/alternative;
```
Thấy được 1 ip khả nghi mình thử vứt lên [WhatIsMyIP](https://www.whatismyip.com/ip-whois-lookup/) và tìm thử ở IP Whois Lookup và voila có vẻ người cần tìm đây rồi:

<img width="313" alt="image" src="https://user-images.githubusercontent.com/42516564/228849867-08d6990d-992f-4e7d-b432-8c491cccd711.png">

Flag:`picoCTF{WilhelmZwalina}`
