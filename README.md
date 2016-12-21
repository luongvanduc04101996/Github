### Github  
Github là một dịch vụ lưu trữ dựa trên web cho các dự án phát triển phần mềm trong đó sử dụng các hệ thống kiểm soát phiên bản Git. Github cung cấp phiên bản trả phí cho các kho tư nhân, doanh nghiệp hoặc có thể miễn phí cho dự 
án mã nguồn mở. Github đang trở nên ngày càng phổ biến và thiết yếu hơn đối với các doanh nghiệp - như là một sơ yếu lý lịch cho các nhà tuyển dụng.
Github chủ yếu được dùng để chứa mã, nhưng cũng thường được dùng với nhiều tài liệu hay với mục đích khác như theo dõi vấn đề và tính năng yêu cầu, tài liệu wiki, github cũng hỗ trợ cho bạn tạo các trang web nhỏ có thể được lưu từ kho công cộng trên github. Định dạng là https://username.github.io  
### Clone  
Để clone một repo về ta có thể chọn **Clone or Download** và nhấn Download Zip hoặc copy đường dẫn (bạn có thể chọn clone sử dụng SSH hoặc HTTP) và thực hiện với lệnh sau:  
```**git clone**[đường dẫn vừa copy thư mục chứa repo trên local]```  
### Add  
**git add [tên_file]**: dùng để add file chỉ định  
__git add *__: dùng để add tất cả  
**git add --all**: dùng để add tất cả  
### Remove  
```  
Để remove một thư mục hay một file nào đó bạn có thể xóa ở máy local sau đó add và commit lại là xong
Nếu muốn xóa repo bạn vào repo đó trên server và chọn Delete this repository ở phần Setting. Đọc warning và chọn yes...  
```  
### Commit  
__git commit *__: dùng để commit tất cả
**git commit [tên_file] -m [thêm chú thích]**: dùng để thêm chú thích cho commit của mình  
### Push  
Sau khi commit thì tất cả đã lưu vào máy cục bộ và giờ thì chúng ta sẽ push lên server với lệnh  
```git push -u origin master:```  
### Pull  
Hành động pull là hành động được thực hiện khi server có những thay đổi mà máy cục bộ vẫn chưa và giờ muốn cập nhật những thay đổi này. Ta dùng lệnh
**git pull**: *lưu ý vào đúng repo cần pull*  
### Remote  
Việc remote được hiện khi bạn muốn add một máy chủ từ xa nào đó. Để thực hiện remote bạn làm như sau:  
```
git remote add origin [link repo]
Để liệt kê các remote mà bạn đã add thì có thể dùng lệnh
git remote -v  
```  
### Fork  
Tại một thời điểm ta muốn phân phối hay sử dụng một project hay repo của ai đó để bắt đầu và điều này nghĩa là ta sẽ Fork một repo về. Sau khi Fork về thì repo đó sẽ tồn tại trên github của chúng ta. Chúng ta có thể clone nó về máy local để bắt đầu sử dụng.
Sau khi một repo được được clone, nó sẽ có một remote origin trỏ đến repo mà chúng ta đã Fork về chứ không phải là repo gốc. Để theo dõi repo gốc mà chúng ta đã Fork, chúng ta cần add một remote khác có tên là upstream:  
```
git remote add upstream [link repo gốc]
git fetch upstream
```  
### Watch  
Để thực hiện bạn chọn Watch trên repo mà bạn muốn và khi đó bạn sẽ nhận được thông báo cho các yêu cầu mới hay vấn đề gì xảy ra với repo đó.  
### Fetch  
Lệnh này sẽ truy cập vào dự án từ xa nào đó và cập nhật dữ liệu mà bạn chưa có trên repo đó. Sau khi Fetch xong bạn có thể tham chiếu đến toàn bộ các nhánh của dự án đó.
Để thực hiện bạn sử dụng:  
```
git fetch tên remote
Bạn có thể git fetch upstream như repo mà ta đã firk phía trên
```  
###Các thiết lập ban đầu  
```
Bạn cần thiết tập tên và email của mình để khi commit lên server sẽ nhận biết được ai đang commit lên1 repo (vì có thể nhiều người tham gia)
__git config --global user.name "tên/username của bạn"__
__git config --global user.email "email của bạn"__
Lựa chọn trình soạn thảo mặc định (có thể không cần) như nano, vi, emacs,...
__git config --global core.editor nano__
Bạn có thể xem lại các thiết lập của mình
__git config --list__
```  
###SSH  
```
Gõ 
ssh -keygen -t rsa  
ssh -agent -s  
ssh -add ~/.ssh/id_rsa  
cat .ssh//id_rsa.pub  

```  
Sau đó bạn dùng cat hay bất cứ lệnh nào hay cách nào để copy đoạn mã trong file id_rsa.pub và truy cập đường dẫnhttps://github.com/settings/ssh và chọn New SSH key để thêm key vào (bạn nhớ là đăng nhập vào tài khoản github trước).  
Quay lại với terminal bạn có thể kiểm tra bằng cách đánh ssh git@github.com Nếu xuất hiện Hi username! You've successfully authenticated... thì chúc mừng bạn đã được liên kết với tài khoản github.  
###Catching your Github password  
Nếu bạn clone repo sử dụng HTTP thì có thể sử dụng 1 helper để lưu user/pass tài khoản github để tiện việc commit những thay đổi (sẽ không cần đánh user/pass lại)  
Nếu bạn clone repo của github sử dụng SSH thì bạn sẽ xác thực bằng key SSH thay vì tên người dùng.  
Để sử dụng helper bạn dùng lệnh sau:  
```git config --global credential.helper cache  
git config --global credential.helper 'cache --timeout=1800'```
__Lưu ý__: nếu bạn không thiết lập thời gian cho helper thì mặc định sẽ là 15 phút
###