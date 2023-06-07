# Todos
Todos with Spring Framework, Mysql, Docker...

prj này sử dụng ControllerJPA trong trường hợp có bug khi chạy thì có backdoor là Controller sử dụng service với lambda exp.  

Vì là prj dành cho mục đích học tập nên trong prj này dùng db là mysql container với docker và có backdoor là h2database với data được insert trong data.sql.  
Vậy nên ta cần chạy lệnh sau với docker trước khi run prj:  
docker run --detach --env MYSQL_ROOT_PASSWORD=vickpassword --env MYSQL_USER=todos-user --env MYSQL_PASSWORD=vicktodos --env MYSQL_DATABASE=todos --name mysql --publish 3306:3306 mysql:8-oracle  
Câu lệnh này sẽ tạo một container MySQL với tên là mysql và cấu hình mật khẩu cho tài khoản root và tài khoản MySQL mới với tên todos-user. Container này sẽ có một database mới với tên là todos, được sử dụng để lưu trữ các dữ liệu liên quan đến một ứng dụng Todos. Container sẽ được kết nối với port 3306 trên máy tính hoặc server của bạn để có thể tiếp cận và quản lý các database.

Sau đó,  chúng ta có thể connect với navicat bằng username password trên để quản lí db hoặc dùng lệnh \connect todos-user@localhost:3306  
trên mysql shell.  

ĐẶC BIỆT LƯU Ý: vì prj dùng mysql container với docker nên mỗi lần chạy prj cần vào docker chạy database của prj.  
Hi vọng prj trên có thể làm nguồn tài liệu cho các bạn trong quá trình học tập Spring Framework.  
Trân trọng!   
Phạm Hồng Hiệu

