# 

# **DỰ ÁN GREEN-TECH SMART FARM**

## **1\. Giới thiệu dự án**

Green-Tech Smart Farm là dự án ứng dụng công nghệ vào nông nghiệp thông minh. Hệ thống sử dụng các cảm biến để thu thập dữ liệu về nhiệt độ, độ ẩm không khí và độ ẩm đất, từ đó hỗ trợ theo dõi và quản lý môi trường trồng trọt.

Nhóm sử dụng mô hình **Hybrid Workflow**, kết hợp làm việc trên máy tính cá nhân và lưu trữ tài liệu trên nền tảng đám mây. Cách làm này giúp các thành viên dễ dàng cập nhật mã nguồn, chia sẻ báo cáo và phối hợp thực hiện công việc.

## **2\. Cấu trúc thư mục dự án**

```
Green-Tech/
├── README.md
├── docs/
│   ├── BaoCao_DuAn.docx
│   └── TaiLieu_KyThuat.pdf
├── sensors/
│   ├── temperature_sensor/
│   ├── humidity_sensor/
│   └── soil_moisture_sensor/
├── scripts/
│   └── test_sensor.py
├── reports/
│   └── BaoCao_NhaDauTu.pdf
├── config/
│   └── .env.example
└── .gitignore
```

**Chức năng của các thư mục:**

* `docs/`: Lưu báo cáo dự án và tài liệu kỹ thuật.  
* `sensors/`: Chứa mã nguồn của các loại cảm biến.  
* `scripts/`: Chứa các chương trình kiểm tra và hỗ trợ vận hành.  
* `reports/`: Lưu báo cáo dành cho nhà đầu tư.  
* `config/`: Chứa file cấu hình mẫu, không chứa mật khẩu thật.  
* `.gitignore`: Quy định các file không được đưa lên kho mã nguồn.

## **3\. Quy trình làm việc Hybrid Workflow**

Nhóm kết hợp làm việc trên máy tính cá nhân với nền tảng lưu trữ đám mây để thuận tiện cho việc cập nhật và chia sẻ dữ liệu.

### **3.1. Quy trình thực hiện**

1. Thành viên tải tài liệu hoặc mã nguồn cần thiết về máy tính cá nhân.  
2. Thực hiện chỉnh sửa và kiểm tra mã nguồn trên máy.  
3. Lưu thay đổi và chờ hệ thống Cloud Auto Sync đồng bộ.  
4. Kiểm tra trạng thái đồng bộ để đảm bảo file mới nhất đã được cập nhật.  
5. Sử dụng Version History để xem hoặc khôi phục phiên bản cũ khi cần.  
6. Với mã nguồn, nhóm sử dụng Git để theo dõi các thay đổi quan trọng.

### **3.2. Nguyên tắc sử dụng**

* Không chỉnh sửa nhiều bản sao của cùng một file mà không thống nhất phiên bản.  
* Đặt tên file rõ ràng, có số phiên bản khi cần thiết.  
* Không tắt đồng bộ khi đang cập nhật tài liệu quan trọng.  
* Không xem Cloud Auto Sync là phương án sao lưu duy nhất.  
* Không đưa mật khẩu hoặc thông tin đăng nhập vào kho mã nguồn.

## **4\. Quy tắc phân quyền chia sẻ tài liệu**

Nhóm áp dụng nguyên tắc **chỉ cấp quyền cần thiết cho từng người**, nhằm tránh rò rỉ dữ liệu và hạn chế chỉnh sửa ngoài ý muốn.

| Đối tượng | Tài liệu được chia sẻ | Quyền truy cập | Mục đích |
| ----- | ----- | ----- | ----- |
| Nhóm phát triển (Dev) | Thư mục `sensors/` và mã nguồn liên quan | Editor | Chỉnh sửa, kiểm tra và cập nhật mã nguồn |
| Nhà đầu tư | `BaoCao_NhaDauTu.pdf` | Viewer | Chỉ xem báo cáo, không chỉnh sửa |
| Đối tác thiết bị | `TaiLieu_KyThuat.pdf` | Commenter | Đọc tài liệu và góp ý |
| Trưởng nhóm | Các tài liệu cần quản lý | Editor | Điều phối và kiểm tra tiến độ |
| Người được giao quản lý thông tin cấu hình | Thông tin cấu hình nhạy cảm | Chỉ cấp quyền cần thiết | Bảo vệ thông tin truy cập hệ thống |

### **4.1. Ý nghĩa các quyền**

* **Viewer:** Chỉ xem nội dung.  
* **Commenter:** Xem và để lại nhận xét.  
* **Editor:** Chỉnh sửa nội dung và thực hiện các thao tác được nền tảng cho phép.

Các tài liệu nên được chia sẻ ở chế độ **Restricted**, tức chỉ những người được cấp quyền mới có thể truy cập. Không sử dụng chế độ `Anyone with the link` cho tài liệu chứa thông tin nhạy cảm.

## **5\. Bảo vệ file `.env`**

File `.env` có thể chứa mật khẩu, khóa truy cập hoặc thông tin kết nối hệ thống. Vì vậy, nhóm cần thực hiện các quy tắc bảo mật sau:

1. Không đưa file `.env` chứa mật khẩu thật vào thư mục chia sẻ công khai.  
2. Không tải file `.env` thật lên GitHub hoặc kho mã nguồn dùng chung.  
3. Thêm `.env` vào file `.gitignore` để tránh đưa nhầm file vào kho mã nguồn.  
4. Chỉ cấp quyền truy cập thông tin cấu hình cho người thực sự cần sử dụng.  
5. Sử dụng file `.env.example` để hướng dẫn cấu hình mà không chứa mật khẩu thật.  
6. Không gửi mật khẩu trực tiếp trong nhóm chat.  
7. Nếu phát hiện mật khẩu bị lộ, cần thay đổi mật khẩu hoặc khóa truy cập ngay.

**Lưu ý:** Không chia sẻ file `.env` thật cho nhà đầu tư hoặc đối tác nếu họ không có nhiệm vụ cần sử dụng thông tin đó.

## **6\. Cấu trúc Channel và quy tắc giao tiếp**

Để tránh tin nhắn bị phân tán, nhóm thống nhất sử dụng các Channel theo từng mục đích.

| Channel | Mục đích sử dụng |
| ----- | ----- |
| `#thong-bao` | Thông báo quan trọng và cập nhật chung |
| `#dev-sensors` | Trao đổi về mã nguồn và kỹ thuật cảm biến |
| `#bao-loi-sensor` | Báo cáo lỗi, tìm nguyên nhân và đề xuất cách sửa |
| `#task-deadline` | Giao việc, cập nhật tiến độ và nhắc hạn hoàn thành |
| `#doi-tac` | Trao đổi các nội dung liên quan đến đối tác thiết bị |
| `#giai-tri` | Giao lưu và trao đổi ngoài công việc |

### **Quy tắc giao tiếp**

* Gửi tin nhắn đúng Channel để mọi người dễ tìm kiếm.  
* Khi giao việc, phải ghi rõ người phụ trách và thời hạn.  
* Khi được tag tên, thành viên cần phản hồi xác nhận thay vì chỉ thả biểu tượng cảm xúc hoặc xem tin nhắn.  
* Sử dụng Thread để thảo luận chi tiết về một lỗi, tránh làm trôi các thông báo khác.  
* Khi hoàn thành công việc, cần cập nhật trạng thái để cả nhóm nắm được tiến độ.

## **7\. Chuyển thảo luận lỗi thành nhiệm vụ cụ thể**

Khi phát hiện lỗi cảm biến, nhóm không chỉ thảo luận trong chat mà cần chuyển vấn đề thành một nhiệm vụ có người phụ trách, thời hạn và tiêu chí hoàn thành.

**Ví dụ nhiệm vụ: Khắc phục lỗi cảm biến độ ẩm đất**

| Nội dung | Chi tiết |
| ----- | ----- |
| Tên nhiệm vụ | Khắc phục lỗi cảm biến độ ẩm đất |
| Mô tả | Kiểm tra nguyên nhân cảm biến gửi dữ liệu không ổn định |
| Người phụ trách | Thành viên được nhóm phân công |
| Mức độ ưu tiên | Cao |
| Thời hạn | 17 giờ ngày hôm sau |
| Trạng thái ban đầu | To do |
| Tiêu chí hoàn thành | Cảm biến gửi dữ liệu ổn định, dữ liệu hiển thị chính xác trên hệ thống và đã được kiểm tra |

Sau khi hoàn thành, người phụ trách cập nhật trạng thái nhiệm vụ và thông báo kết quả cho nhóm. Nếu gặp khó khăn, thành viên cần báo sớm để được hỗ trợ.

## **8\. Quy trình Transfer Ownership khi kết thúc dự án**

Khi dự án kết thúc, nhóm cần chuyển quyền sở hữu tài liệu và tài nguyên cho người tiếp nhận phù hợp để đảm bảo dự án tiếp tục được quản lý.

### **Các bước thực hiện**

1. Kiểm tra toàn bộ thư mục, báo cáo, mã nguồn và tài liệu của dự án.  
2. Xác định người sẽ tiếp nhận quyền sở hữu.  
3. Kiểm tra tài khoản của người nhận và quyền truy cập hiện tại.  
4. Thực hiện Transfer Ownership nếu nền tảng hỗ trợ loại tài liệu hoặc tài nguyên đó.  
5. Nếu không hỗ trợ chuyển trực tiếp, sử dụng quy trình bàn giao phù hợp của nền tảng hoặc tổ chức.  
6. Kiểm tra lại quyền truy cập sau khi bàn giao.  
7. Thu hồi quyền của những người không còn tham gia dự án nếu cần thiết.  
8. Bàn giao thông tin cấu hình nhạy cảm qua phương thức an toàn, không ghi mật khẩu trực tiếp trong README.

Việc chuyển quyền sở hữu cần được thực hiện cẩn thận để tránh mất quyền truy cập hoặc làm gián đoạn hoạt động của dự án.

## **9\. Quy trình khôi phục khi xóa nhầm thư mục `sensors/`**

Nếu một thành viên vô tình xóa thư mục `sensors/`, nhóm cần xử lý nhanh để hạn chế mất dữ liệu.

### **Các bước khôi phục**

**Bước 1: Dừng các thao tác chỉnh sửa không cần thiết**

Thông báo cho nhóm biết sự cố và tạm dừng các thay đổi có thể làm tình hình phức tạp hơn.

**Bước 2: Kiểm tra Thùng rác của nền tảng đám mây**

Tìm thư mục `sensors/` trong Trash hoặc Recycle Bin. Nếu tìm thấy, chọn Restore để khôi phục.

**Bước 3: Kiểm tra Version History hoặc bản sao lưu**

Nếu không tìm thấy trong Thùng rác, kiểm tra lịch sử phiên bản, bản sao lưu hoặc kho Git để lấy lại mã nguồn.

**Bước 4: Kiểm tra lại dữ liệu**

Sau khi khôi phục, xác nhận các file cảm biến đã đầy đủ và chạy thử chương trình để đảm bảo hệ thống hoạt động bình thường.

**Bước 5: Thông báo kết quả**

Cập nhật tình trạng khôi phục cho các thành viên và ghi nhận nguyên nhân để tránh lặp lại sự cố.

### **Biện pháp phòng tránh**

* Sử dụng Git để quản lý lịch sử thay đổi mã nguồn.  
* Bật Cloud Auto Sync và thường xuyên kiểm tra trạng thái đồng bộ.  
* Có bản sao lưu độc lập cho các dữ liệu quan trọng.  
* Chỉ cấp quyền chỉnh sửa hoặc xóa cho người thực sự cần thiết.  
* Định kỳ kiểm tra khả năng khôi phục dữ liệu.

**Lưu ý:** Nếu thao tác xóa đã được đồng bộ lên các thiết bị khác, bản sao trên những thiết bị đó cũng có thể bị ảnh hưởng. Vì vậy, cần kiểm tra Thùng rác, lịch sử phiên bản và bản sao lưu thay vì mặc định rằng file vẫn còn trên máy khác.

## **10\. Kết luận**

Việc áp dụng Hybrid Workflow, phân quyền chia sẻ hợp lý và tổ chức giao tiếp theo Channel giúp dự án Green-Tech Smart Farm làm việc hiệu quả hơn. Đồng thời, việc bảo vệ file `.env`, chuyển quyền sở hữu đúng quy trình và xây dựng phương án khôi phục dữ liệu giúp hạn chế rủi ro bảo mật cũng như mất mát tài liệu.

Nhóm cần duy trì các quy tắc này trong suốt quá trình thực hiện dự án để đảm bảo dữ liệu được quản lý an toàn, công việc minh bạch và các thành viên phối hợp tốt với nhau.

