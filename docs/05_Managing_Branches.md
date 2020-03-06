# Làm việc với các Branches
<img src=https://i.imgur.com/ddUGg4q.png>


- Trong quá trình phát triển một sản phẩm, luôn có một nhánh chính (**branch**) gọi là `master`(nhánh gốc) được tạo ra mặc định khi tạo mới repo. Các nhánh con khác được người lập trình tạo nên dùng để phát triển tính năng riêng biệt hoặc để test sản phẩm .
## **1) Tạo một nhánh mới**
- Sử dụng lệnh `git branch` để tạo nhánh mới có tên là `develop` :
    ```
    git branch develop
    ```
## **2) Chuyển nhánh từ `master` sang nhánh mới để làm việc**
- Sử dụng lệnh `git checkout` để chuyển nhánh :
    ```
    git checkout develop
    ```
    <img src=https://i.imgur.com/mQ8FfrG.png>
## **3) Tạo và chuyển nhánh đồng thời**
- Sử dụng option `-b` của lệnh `git checkout` để tạo nhánh mới và đồng thời chuyển sang làm việc ở nhánh đó :
    ```
    git checkout -b developer
    ```
    <img src=https://i.imgur.com/MUfmrg1.png>
## **4) Liệt kê các nhánh đang có**
- Sử dụng lệnh `git branch` để hiển thị các nhánh đang có ở máy local :
    ```
    git branch
    ```
    <img src=https://i.imgur.com/0OSIIRw.png>

- Sử dụng thêm option `-a` để hiển thị toàn bộ các nhánh đang có ở máy local và remote :
    ```
    git branch -a
    ```
    <img src=https://i.imgur.com/D7fHr92.png>

> Dấu `*` biểu thị nhánh đang active 
## **5) Xóa nhánh**
- Sử dụng option `-D` của lệnh `git branch` để xóa một nhánh (inactive) :
    ```
    git branch -D developer
    ```
    <img src=https://i.imgur.com/3PGWFMz.png>
## **6) Đổi tên nhánh**
- Sử dụng option `-m` của lệnh `git branch` để đổi tên một nhánh ( **VD:** từ `developer` sang `develop` ) :
    ```
    git branch -m developer develop
    ```
    <img src=https://i.imgur.com/AN7KMIF.png>
## **7) Push các commit của nhánh lên GitHub**
- Thực hiện kiểm tra nội dung file `newfile.md` được pull về từ master :
    ```
    cat newfile.md
    ádsdasds
    ```
- Khi đang ở nhánh `develop` , đổi nội dung file thành "`File duoc chinh sua boi develop`" .
- Thực hiện `add`, `commit` :
    ```
    git add .
    git commit -m "Chinh sua file"
    ```
    <img src=https://i.imgur.com/aWicJgy.png>
- Thực hiện `push` theo cấu trúc lệnh `git push origin [tên_nhánh]` :
    ```
    git push origin develop
    ```
    <img src=https://i.imgur.com/1ON0V9z.png>

- Sau bước này , trên repo GitHub sẽ xuất hiện nhánh mới vừa tạo :

    <img src=https://i.imgur.com/gfPbVDR.png>

- File `newfile.md` trên nhánh `master` không bị thay đổi , tuy nhiên đã bị thay đổi trong nhánh `develop` :

    <img src=https://i.imgur.com/rTAiBQB.png>

    <img src=https://i.imgur.com/AtAwNEd.png>

## **8) Merge các thay đổi của các nhánh**
- Ta sẽ thực hiện `merge` ( trộn ) nội dung của nhánh `develop` vào nhánh `master` .
- Trước khi `merge` , có thể kiểm tra đối chiếu giữa nội dung repo merge và repo cần merge theo công thức "`git diff [nhánh cần merge] [nhánh đối chiếu]`" :
    ```
    git diff master develop
    ```
    <img src=https://i.imgur.com/eDXAiRV.png>

- Sau khi kiểm tra , chuyển nhánh làm việc về nhánh cần merge và tiến hành merge bằng lệnh `git merge` :
    ```
    git checkout master
    git merge develop
    ```
    <img src=https://i.imgur.com/VH6d6fV.png>

- Thực hiện `push` một lần nữa để đồn bộ nhánh `master` lên repo GitHub :
    ```
    git push origin master
    ```
    <img src=https://i.imgur.com/YgahRI7.png>

    => Kết quả :
    
    <img src=https://i.imgur.com/ZCcs6RU.png>
