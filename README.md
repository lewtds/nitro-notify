# nitro-notify

Đây là một phần mềm rất bare-bone do mình viết trong thời gian ngắn để phục vụ
nhu cầu cá nhân là hiển thị những entry trong todo list thành notification.

## Yêu cầu

Đối với một máy tính dùng Ubuntu:

- python3
- python3-notify2

## Cách sử dụng

Nếu bạn có dùng Nitrotasks để quản lý danh sách các công việc cần làm thì bạn có
thể để ý khi bật sync bằng Dropbox hay Ubuntu One, Nitrotasks sẽ tạo một file `todo.txt`
trong thư mục sync của bạn (`~/Dropbox/Apps/Nitro/todo.txt` với Dropbox, còn Ubuntu One thì
mình không rõ). File này có cấu trúc rất đơn giản:

    Đục lỗ bàn học @next 
    Đọc hướng dẫn Python @next 
    THE PURLOINED LETTER @Reading List 
    Nghiên cứu build RPM @Learning List 
    Dịch Unix tut @today
    
gồm nhiều dòng chứa các mục cần làm và tag ở phía sau. Tag chúng ta quan tâm là
tag _@today_.

Khi sử dụng chương trình thì edit biến `data_path` trong file chạy để trỏ đến file
này và chạy như bình thường. Cứ 15 phút chương trình sẽ đọc lại file này, tách
các dòng có tag _@today_ và tạo notification lên màn hình.
