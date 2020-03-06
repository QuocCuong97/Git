# Cài đặt Git
## **1) Cài đặt `git`**
- Sử dụng lệnh sau để cài đặt :
    ```
    sudo apt-get install git   ( Ubuntu )
    yum install -y git         ( CentOS )
    ```
## **2) Cá nhân hóa môi trường `git`**
- Cài đặt username :
    ```
    git config --global user.name "QuocCuong97"
    ```
- Cài đặt email của user :
    ```
    git config --global user.email "cuongnq24101997@gmail.com"
    ```
- Cài đặt trình soạn thảo chính cho `git` :
    ```
    git config --global core.editor vim
    ```
- Highlight màu chữ trong `git` :
    ```
    git config --global color.ui true
    git config --global color.status auto
    git config --global color.branch auto
    ```
- Xem lại các cài đặt :
    ```
    git config --list
    ```
    ```
    user.name=QuocCuong97
    user.email=cuongnq24101997@gmail.com
    color.ui=true
    color.status=auto
    color.branch=auto
    core.editor=vim
    ```
## **3) Liên kết mã hóa SSH**
- Tạo **private key** :
    ```
    ssh-keygen -t rsa
    ```
    <img src=https://i.imgur.com/NOic8Hb.png>
    
    > **Chú ý :** Ghi nhớ passphrase nếu có tạo
    - Kết quả sau khi tạo key :
        ```
        ls /root/.ssh
        ```
        <img src=https://i.imgur.com/kk0kdIn.png>

- Copy public key
    ```
    cat /root/.ssh/id_rsa.pub
    ```
    <img src=https://i.imgur.com/IwCDvPB.png>

- Truy cập URL : https://github.com/settings/keys , chọn `New SSH key` :

    <img src=https://i.imgur.com/GfHXvRN.png>

- Paste **public key** vào rồi chọn `Add SSH key` :

    <img src=https://i.imgur.com/7s74YBs.png>

- Xác thực lại mật khẩu của **Github** :

    <img src=https://i.imgur.com/tIr0wcf.png>

- Liên kết thành công , có thể **commit** lên **Github** tại máy local mà không cần nhập `username` và `password` .

    <img src=https://i.imgur.com/QuAmMiZ.png>
