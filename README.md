### Github  
Github là một dịch vụ lưu trữ dựa trên web cho các dự án phát triển phần mềm trong đó sử dụng các hệ thống kiểm soát phiên bản Git. Github cung cấp phiên bản trả phí cho các kho tư nhân, doanh nghiệp hoặc có thể miễn phí cho dự 
án mã nguồn mở. Github đang trở nên ngày càng phổ biến và thiết yếu hơn đối với các doanh nghiệp - như là một sơ yếu lý lịch cho các nhà tuyển dụng.
Github chủ yếu được dùng để chứa mã, nhưng cũng thường được dùng với nhiều tài liệu hay với mục đích khác như theo dõi vấn đề và tính năng yêu cầu, tài liệu wiki, github cũng hỗ trợ cho bạn tạo các trang web nhỏ có thể được lưu từ kho công cộng trên github. Định dạng là https://username.github.io  
### Clone  
Để clone một repo về ta có thể chọn **Clone or Download** và nhấn Download Zip hoặc copy đường dẫn (bạn có thể chọn clone sử dụng SSH hoặc HTTP) và thực hiện với lệnh sau:  
```**git clone**[đường dẫn vừa copy thư mục chứa repo trên local]```  
### Add  
**git add [tên_file]**: dùng để add file chỉ định  
**git add * **: dùng để add tất cả  
**git add --all**: dùng để add tất cả  
### Remove  
```  
Để remove một thư mục hay một file nào đó bạn có thể xóa ở máy local sau đó add và commit lại là xong
Nếu muốn xóa repo bạn vào repo đó trên server và chọn Delete this repository ở phần Setting. Đọc warning và chọn yes...  
```  
### Commit  
**git commit * **: dùng để commit tất cả
**git commit [tên_file] -m [thêm chú thích]**: dùng để thêm chú thích cho commit của mình  
### Push  
Sau khi commit thì tất cả đã lưu vào máy cục bộ và giờ thì chúng ta sẽ push lên server với lệnh  
```git push -u origin master:```  
###