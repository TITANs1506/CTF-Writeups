# **hideme**
## **Challenge**
Every file gets a flag.
The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://github.com/TITANs1506/CTF-Writeups/blob/main/PicoCTF%202023/Forensics/hideme/flag.png).
## **Writeup**
Mình đã dùng *binwalk* để extract ra các file ẩn:
```
binwalk -e flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2876, uncompressed size: 3029, name: secret/flag.png
42915         0xA7A3          End of Zip archive, footer length: 22

```

Thử vào folder mới được extract ta thấy 1 folder *secret* trong đó có chứa ảnh flag:

![image](https://user-images.githubusercontent.com/42516564/228841806-1b9686c3-e80a-43ee-aeaa-d6e3bfd67daa.png)

Flag:`picoCTF{Hiddinng_An-imag3_within_@n_ima9e_d55982e8}`
