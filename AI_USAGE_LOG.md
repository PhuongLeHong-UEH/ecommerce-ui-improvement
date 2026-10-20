# Nhật Ký Sử Dụng AI Trong Phát Triển Giao Diện

Dự án: Cải tiến giao diện thẻ sản phẩm thương mại điện tử
Đối tượng nghiên cứu: Tiki.vn
Mục đích: Lập nhật ký theo dõi việc áp dụng công cụ AI hỗ trợ phân tích và viết mã nguồn theo đúng yêu cầu môn học.

---

## 1. Quy Trình Sử Dụng AI

Quá trình thực hiện bài tập được chia làm 3 bước rõ ràng:
Step 1: Đưa ra câu hỏi cụ thể kèm bối cảnh yêu cầu phân tích giao diện và tối ưu UX.
Step 2: Đánh giá kết quả trả về từ AI, so sánh với giao diện thực tế của Tiki.vn để loại bỏ các thông tin không chính xác.
Step 3: Tiến hành chỉnh sửa và viết lại mã nguồn bằng tay để phù hợp với tài nguyên thực tế của dự án.

---

## 2. Chi Tiết Các Yêu Cầu Đã Gửi Cho AI

### Yêu cầu 1: Phân tích 5 khu vực giao diện Tiki
- Nội dung yêu cầu: Yêu cầu AI đóng vai trò người phân tích giao diện để lập bảng đánh giá 5 khu vực gồm Trang chủ, Danh mục, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng với các mục: Mục đích, Thành phần, Điểm thuận tiện, Vấn đề phát sinh và Đề xuất.
- Kết quả thu được: AI đưa ra cấu trúc bảng đầy đủ. Các điểm tồn tại về bộ lọc trên di động và vị trí khối thanh toán giỏ hàng phù hợp với thực tế.
- Xử lý của sinh viên: Kiểm chứng lại từng vị trí trên website Tiki.vn và giữ lại các nhận xét đúng thực tế để đưa vào báo cáo.

### Yêu cầu 2: Đề xuất giải pháp sửa lỗi thẻ sản phẩm
- Nội dung yêu cầu: Yêu cầu AI đề xuất phương án xử lý 3 lỗi gồm: hiển thị giá mờ, nút mua không nổi bật và thẻ sản phẩm cao thấp không đều.
- Kết quả thu được: AI đề xuất cách phân chia lại cấu trúc thẻ HTML và sử dụng thuộc tính Flexbox kết hợp cắt chữ tự động trong CSS.
- Xử lý của sinh viên: Tiếp nhận phương án kỹ thuật và yêu cầu AI chuyển sang bước tạo mã chi tiết.

### Yêu cầu 3: Tạo mã nguồn HTML và CSS
- Nội dung yêu cầu: Yêu cầu AI tạo mã nguồn tách riêng hai file `index.html` và `style.css`, sử dụng đúng danh sách tên ảnh local trong thư mục images.
- Kết quả thu được: AI xuất đoạn mã HTML chuẩn ngữ nghĩa và file CSS chứa đầy đủ cấu trúc khung và thuộc tính tự điều chỉnh màn hình.

---

## 3. Các Phần Sinh Viên Tự Điều Chỉnh Bằng Tay

| Thành phần mã | Mức độ điều chỉnh | Nội dung tự chỉnh sửa và lý do |
| :--- | :--- | :--- |
| Đường dẫn tệp ảnh (`src`) | Thay đổi hoàn toàn | Chỉnh sửa lại toàn bộ đường dẫn hình ảnh trong file HTML từ dạng liên kết mạng sang đường dẫn tệp tin nội bộ `images/ao_thun.jpg`, `images/giay.jpg`, `images/quan_tay.jpg`, `images/sandal.jpg` để đảm bảo bài tập chạy không cần kết nối mạng. |
| Nội dung chữ | Thay đổi hoàn toàn | Cập nhật lại tên các sản phẩm và mức giá tương ứng đúng với các mặt hàng thời trang trong thư mục hình ảnh thực tế. |
| Tùy chỉnh CSS (`style.css`) | Chỉnh sửa 30% | thêm thuộc tính `object-fit: cover` cho phần hình ảnh để tránh tình trạng ảnh bị co giãn lệch tỉ lệ, bổ sung chiều cao dòng cố định cho phần tên sản phẩm để đảm bảo không bị lỗi giao diện khi hiển thị trên các trình duyệt khác nhau. |

---

## 4. Kết Luận Khi Sử Dụng AI

Sử dụng AI giúp rút ngắn thời gian lập cấu trúc khung và đưa ra các gợi ý xử lý CSS hợp lý. Tuy nhiên, việc tự kiểm tra giao diện trên trình duyệt và tự tay sửa đổi mã nguồn là bắt buộc để đảm bảo tệp tin liên kết đúng cấu trúc thư mục local và hiển thị chính xác theo yêu cầu đề bài.

