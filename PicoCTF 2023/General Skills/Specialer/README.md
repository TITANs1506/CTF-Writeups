# **Specialer**
## **Challenge**
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.
## **Writeup**
Sau một hồi vật lộn thử tất cả các lệnh thì mình thấy có 2 lệnh duy nhất dùng được là *echo* và *cd*. Sau một hồi tìm kiếm trên mạng cách xem file bằng echo mình đã có 1 lệnh hết sức ảo ma:  `echo "$(<example.txt)"`
Cuối cùng ta có: `ls` có thể thay thế bằng `echo *`, `cat` có thể thay thế bằng `echo "$(<example.txt)"` và `cd`
3 lệnh này đã quá đủ để bạn tìm ra flag rồi :v

```
$ echo *
abra ala sim
$ cd ala/
$ echo *
kazam.txt mode.txt
$ echo "$(<kazam.txt)"
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_838b49d1}
```

Flag:`picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_838b49d1}`
