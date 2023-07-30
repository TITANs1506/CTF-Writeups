# **MAYDAY!**
## **Challenge**
Embark on 'Dizzy', a carousel ride through cryptography! This warmup challenge spins you around the basics of ciphers and keys. Sharpen your mind, find the flag, and remember - in crypto, it's fun to get a little dizzy!

T4 l16 _36 510 _27 s26 _11 320 414 {6 }39 C2 T0 m28 317 y35 d31 F1 m22 g19 d38 z34 423 l15 329 c12 ;37 19 h13 _30 F5 t7 C3 325 z33 _21 h8 n18 132 k24
## **Writeup**
Vì không có định hướng về loại mã hóa này nên ta dùng công cụ [cipher-identifier](https://www.dcode.fr/cipher-identifier) để xem thử và được kết quả là mã hóa *Letter Positions*
Tuy nhiên công cụ chỉ hỗ trợ sắp xếp các chứ cái nên ta sẽ làm tay. Mã hóa này rất đơn giản nhưng cũng rất đau đầu như tên của bài CTF, mỗi phần sẽ có 1 cặp số thứ tự và text có thể trước hoặc sau như *T4* có nghĩa là T ở vị trí thứ 5. Ta sẽ phải sắp xếp từ 0 đến hết đoạn mã hóa và ra được flag:

Flag: `TFCCTF{th15_ch4ll3ng3_m4k3s_m3_d1zzy_;d}`
