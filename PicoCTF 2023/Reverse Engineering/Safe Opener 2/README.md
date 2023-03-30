# **Safe Opener 2**
## **Challenge**
What can you do with this file?
I forgot the key to my safe but this [file](https://github.com/TITANs1506/CTF-Writeups/blob/main/PicoCTF%202023/Reverse%20Engineering/Safe%20Opener%202/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

## **Writeup**
Lại một bài cách cổ điển nhất CTF chiến được =))

```
strings SafeOpener.class | grep "picoCTF"
,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_5bfbd6f1}
```

Flag:`picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_5bfbd6f1}`
