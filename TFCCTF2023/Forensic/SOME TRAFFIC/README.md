# **SOME TRAFFIC**
## **Challenge**
Our SOC analysts said that in the last few days, some of our employees started to upload a lot of photos on random sites. Check it out.

Flag Format: TFCCTF{...}.

Disclaimer (forensics+stegano)

What's the flag?
## **Writeup**
Đề bài cho chúng ta file sus.pcapng. Mở file bằng Wireshark, với gợi ý là forensics+stegano thì có thể suy đoán được là sẽ có một file ảnh trong traffic thuộc file .pcapng được cho. Export file từ .pcapng ta được 7 file như hình:
![image](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/498c4267-6c60-438a-9d14-a4cf1de80d0a)
Tạm bỏ qua 4 file định dạng .html, mở 3 file bằng HexEd thì nhận thấy đó là 3 file .png:
![image](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/ba29db46-077d-4316-9aee-0206032619fb)
Xoá bỏ phần thừa ở đầu và cuối file để lưu về 3 file .png hoàn chỉnh:
![image](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/4253c3b7-207b-492d-9d6d-580117dcc381)
Chạy file ảnh qua 1 loạt các tool như pngcheck, exiftool, binwalk, zsteg, ... tìm được flag sau khi chạy zsteg ở hình đầu tiên:
![image](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/297d0bce-fe92-4de5-a551-5ed7f11319b3)


Flag: `TFCCTF{H1dd3n_d4t4_1n_p1x3ls_i5n't_f4n_4nd_e4sy_to_f1nd!}`
