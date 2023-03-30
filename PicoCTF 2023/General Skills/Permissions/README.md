# **Permissions**
## **Challenge**
Can you read files in the root file?
## **Writeup**
Biết mình là *picoplayer* qua nên sau một hồi mò mẫm mình tìm được mục metadata.json:
```
picoplayer@challenge:/home$ cd /challenge/
picoplayer@challenge:/challenge$ ls
metadata.json
picoplayer@challenge:/challenge$ cat metadata.json 
{"flag": "picoCTF{uS1ng_v1m_3dit0r_55878b51}", "username": "picoplayer", "password": "pEN9KN1qYm"}
```

Flag: `picoCTF{uS1ng_v1m_3dit0r_55878b51}`
