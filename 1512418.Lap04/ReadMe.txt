Trần Duy Phương
1512418
mail: tranduyphuong20100@gmail.com
các chức năng đã làm:
1. Tạo ra TreeView bên trái, ListView bên phải. 
2. Xét TreeView
- Tạo node root là This PC
- Lấy danh sách các ổ đĩa trong máy bằng hàm GetLogicalDriveStrings, thêm các ổ đĩa vào node root, tạo sẵn thuộc tính cChildren = true để báo hiệu có các node con. Gán giá trị của ổ đĩa ví dụ C:\ vào PARAM (tag) để lấy lên xài lại.
Bắt sự kiện Expanding, lấy ra đường dẫn dấu ở PARAM để biết mình phải xư lí thư mục nào, duyệt nội dung thư mục bằng FindFirstFile & FindNextFile, chỉ lấy các thư mục để thêm vào làm node con.
3. Xét ListView
- Hiển thị toàn bộ thư mục và tập tin tương ứng với một đường dẫn 
- Bấm đôi vào một thư mục sẽ thấy toàn bộ thư mục con và tập tin.
- Tạo ra ListView có 4 cột: Tên, Loại, Thời gian chỉnh sửa, Dung lượng. Với thư mục set text cho 2 cột Tên và Loại. 
Với tập tin cần hiển thị tối thiểu là 3 cột: Tên, Thời gian chỉnh sửa, Dung lượng.
- set cứng luôn icon folder tự chọn, bấm đôi một tập tin sẽ chạy app tương ứng

- luồng sự kiện chính:
+ Chạy chương trình lên, hiển thị node This PC trên TreeView bên trái ở trạng thái collapse (thu gọn).
 Bấm vào sẽ xổ xuống các node con là danh sách ổ đĩa.
+ khi bấm đúp chuột vào list view thì nó vào thư mục đó, nếu là file sẽ mở file tương ứng
+ khi bấm vào thì phía trên sẽ hiển thị đường dẫn đến thư mục tại ô LINK
+ khi bấm vào 1 thư mục thì phía trên sẽ có dung lượng, tên loại,... xuất hiện


- link tới github:
https://github.com/Duy-Phuong/code.git
- link tới bitbucket:
https://tranduyphuong@bitbucket.org/tranduyphuong/windev.git

- link video demo hướng dẫn upload lên youtube:
https://www.youtube.com/watch?v=XhNzL2WXmgk&list=PLjvYb5WK-sh5dFly0mqw3HInw6_fZoHtn
