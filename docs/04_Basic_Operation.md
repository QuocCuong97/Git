# Các thao tác cơ bản
## **1) Clone**
- Clone remote repository dành cho bất kỳ máy tính nào :
    ```
    git clone https://github.com/QuocCuong97/demo.git
    ```
- Clone repository dành cho máy đã add SSH Key :
    ```
    git clone git@github.com:QuocCuong97/demo.git
    ```
    <img src=https://i.imgur.com/AWazdfi.png>
- Clone nội dung bên trong repository vào thư mục `/root/code/` cụ thể :
    ```
    git clone git@github.com:QuocCuong97/demo.git /root/code/
    ```
## **2) Add**
- Thử tạo 1 file trong thư mục repo :
    ```
    cd demo
    touch newfile.md
    ```
- Thực hiện **add** file lên Github :
    ```
    git add newfile.md
    ```
    hoặc add tất cả các file đã thêm vào :
    ```
    git add .
    ```
- Thực hiện kiểm tra : file `newfile.md` đang đợi **commit**
    ```
    git status
    ```

    <img src=https://i.imgur.com/N7yvyMj.png>

## **3) Commit**
- Giống như xét duyệt lại lần cuối các thay đổi trong local repository để đưa lên Github
    ```
    git commit newfile.md -m "Tao file moi"
    ```
    hoặc commit tất cả các file pending :
    ```
    git commit * -m "Tao file moi"
    ```
    - `-m` : Ghi lại comment cho 1 **commit**

        <img src=https://i.imgur.com/kZ3OpKa.png>
## **4) Push**
- Đẩy các file đã **commit** lên Github
    ```
    git push origin master
    ```

    <img src=https://i.imgur.com/Rw6ijWD.png>

## **5) Pull**
- Giả sử có 1 thay đổi nào đó được tạo trên Github , cần phải đồng bộ xuống Local để làm việc . Thao tác **pull** sẽ đối chiếu remote repo trên Github và Local repo sau đó thực hiện đồng bộ xuống máy Local .
    ```
    git pull
    ```
    <img src=https://i.imgur.com/ADvn3g8.png>

## **6) Log**
- Hiển thị chi tiết các log commit của repo :
    ```
    git log
    ```
    <img src=https://i.imgur.com/mDsgeZF.png>