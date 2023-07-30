# **BABY DUCKY NOTES**
## **Challenge**
Quack quack! Try and huack me!
## **Writeup**
Khi đọc source code phần *route.py* ta thấy 1 đoạn code có thể bị lỗi IDOR:
```
@web.route('/posts/view/<user>', methods=['GET'])
@auth_required
def posts_view(username, user):
    try:
        posts = db_get_user_posts(user, username == user)
    except:
        raise Exception(username)

    return render_template('posts.html', posts=posts)
```

Từ đoạn code ta có thể biết được rằng nhập bất cứ username nào vào url cũng trả về tất cả các bài post của user đó
Kết hợp 2 query trong phần *database.py* ta biết được tài khoản *admin* đang chứa flag:
```
query(con, f'''
INSERT INTO users (
    username,
    password
    ) VALUES (
        'admin',
        '{os.environ.get("ADMIN_PASSWD")}'  
    );
    ''')
```
```
INSERT INTO posts (
        user_id,
        title,
        content,
        hidden
        ) VALUES (
            1,
            'Here is a ducky flag!',
            '{os.environ.get("FLAG")}',
            0
        
    );
```
Tạo 1 tài khoản bất kì rồi sửa đường dẫn thành /posts/view/admin ta có được flag:

![image](https://github.com/TITANs1506/CTF-Writeups/assets/42516564/ee9dbc1c-95dc-4307-a5d1-7ab44f79a8b7)


Flag:`TFCCTF{Adm1n_l0St_h1s_m1nd!}`
