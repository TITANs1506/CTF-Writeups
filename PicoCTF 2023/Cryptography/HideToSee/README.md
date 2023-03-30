# **HideToSee**
## **Challenge**
How about some hide and seek heh?
Look at this image [here](https://github.com/TITANs1506/CTF-Writeups/blob/main/PicoCTF%202023/Cryptography/HideToSee/atbash.jpg).

![image](https://user-images.githubusercontent.com/42516564/228805410-9c93d2c8-fcfa-4760-bfb8-10f8817014a5.png)


## **Writeup**
Đầu tiên khi đề bài cho ta một bức ảnh việc đầu tiên ta phải nghĩ đến là chắc chắn có thông điệp gì đó giấu trong bức ảnh đó. Mình đã dùng công cụ [stegseek](https://github.com/RickdeJager/stegseek) để kiểm tra.

```
$ stegseek --crack -sf atbash.jpg -wl rockyou.txt
StegSeek 0.6 - https://github.com/RickdeJager/StegSeek

[i] Found passphrase: ""
[i] Original filename: "encrypted.txt".
[i] Extracting to "atbash.jpg.out".
```

Ta thấy công cụ đã extract ra một file mới là **atbash.jpg.out** với flag bị encode.

```
krxlXGU{zgyzhs_xizxp_92533667}
```
Như hình ảnh đã gợi ý là phương pháp mã hóa Atbash Cipher nên mình đã lên [CyberChef](https://gchq.github.io/CyberChef/) để encode flag.

Flag: `picoCTF{atbash_crack_92533667}`
