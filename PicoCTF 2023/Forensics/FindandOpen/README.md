# **FindandOpen**
## **Challenge**
Someone might have hidden the password in the trace file.
Find the [key](https://github.com/TITANs1506/CTF-Writeups/blob/main/PicoCTF%202023/Forensics/FindandOpen/dump.pcap) to unlock this [file](https://github.com/TITANs1506/CTF-Writeups/blob/main/PicoCTF%202023/Forensics/FindandOpen/flag.zip). This tracefile might be good to analyze.
## **Writeup**
Dạo quanh 1 vòng file pcap ta có thể thấy các gợi ý của pico trên các packet Ethernet II. Xem kĩ từng packet ta có thể thấy 1 packet khả nghi với dấu = ở cuối có vẻ là Base64:
<img width="810" alt="image" src="https://user-images.githubusercontent.com/42516564/228873468-9a0ca0fd-ea87-4de1-bcd0-12b10b1c578d.png">

Thử encode bằng [CyberChef](https://gchq.github.io/CyberChef/) ta có thể thấy 1 phần của flag: `This is the secret: picoCTF{R34DING_LOKd_`
Dùng phần flag này làm password từ đó ta mở được file zip và tìm được flag hoàn chỉnh

Flag: `picoCTF{R34DING_LOKd_fil56_succ3ss_494c4f32}`
