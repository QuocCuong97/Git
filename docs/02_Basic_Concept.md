# Các khái niệm trong Git
### **Working Directory** và **Staging Area**
- **Working directory** là nơi các file được tạo ra và xử lý bởi người dùng .
- **Git** sẽ không track từng file mỗi khi nó bị thay đổi . Khi thực hiện hành động `commit` , **Git** sẽ tìm kiếm các file ở trong **staging area** . Chỉ các file trong**staging area** được `commit` chứ không phải hoàn toàn các file bị thay đổi sẽ được `commit` .
- Luồng làm việc của **Git** :
    
    <img src=https://i.imgur.com/mvSkphr.png>