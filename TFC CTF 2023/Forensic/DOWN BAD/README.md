# **DOWN BAD**
## **Challenge**
The flag is right there!

## **Writeup**
Đề bài cho chúng ta file là downbad.png. Bản thân file này đang bị lỗi nên sử dụng pngcheck để kiểm tra:
![Screenshot 2023-07-31 164240](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/44592510-b2e8-43c4-9acb-561965ab887a)

Mở file bằng HexEd thấy được CRC checksum của hình giống như mô tả trong expected của pngcheck:
![image](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/09305de9-3491-45d5-9553-b39f14028add)

Sửa CRC checksum cho giống như kết quả được ghi trong pngcheck rồi tải về thu được ảnh:
![Screenshot 2023-07-31 164301](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/441677f6-9485-440c-b1a5-a2a241949f71)

![image](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/417920cb-6a11-4520-aeb7-847e43a07589)

Thử sửa ảnh thành hình vuông cùng tính lại CRC checksum thu về được ảnh có flag:
![Screenshot 2023-07-31 164455](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/9aae08cc-8486-4e52-8a86-28ca22502068)

![image](https://github.com/TITANs1506/CTF-Writeups/assets/108376735/51ea70cf-6ca1-4c96-80e5-cec692a2380d)


Flag: `TFCCTF{28ae25c96850245ffdd70a880158f9f3}`
