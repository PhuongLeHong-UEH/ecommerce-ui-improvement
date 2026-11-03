# Nhật Ký Sử Dụng AI Trong Phát Triển Giao Diện (Buổi 2)
Môn học: Phát triển ứng dụng Web và Thương mại điện tử

Thực hiện: Lê Hồng Phương  
Mã sinh viên: 31241024012  
Lớp: EE0001  

Website nghiên cứu: Tiki  
Trang chạy thử nghiệm: https://tiki.vn  

Dự án: Cải tiến giao diện thẻ sản phẩm thương mại điện tử (Nâng cấp Buổi 2)  
Đối tượng nghiên cứu: Tiki.vn  
Mục đích: Lập nhật ký theo dõi việc áp dụng công cụ AI hỗ trợ phân tích, xây dựng Flexbox menu, hiệu ứng tương tác và tối ưu Responsive theo đúng yêu cầu bài tập cá nhân Buổi 2.

---

## 1. Quy Trình Sử Dụng AI

Quá trình thực hiện bài tập Buổi 2 được chia làm 3 bước rõ ràng:
- **Step 1:** Đưa ra câu hỏi cụ thể kèm mã nguồn hiện tại (`index.html`, `style.css`), yêu cầu AI đề xuất cách thêm thanh Menu điều hướng (`<nav>`), áp dụng Flexbox cho Header, bổ sung trạng thái tương tác (`:hover`, `:focus-visible`) và giải thích các thuộc tính CSS.
- **Step 2:** Đánh giá kết quả trả về từ AI, sử dụng DevTools (F12) kiểm tra tính chính xác của các đường kẻ Flexbox Overlay, thử nghiệm phím Tab để kiểm tra `:focus-visible` và coi trước ở các mốc màn hình 1366px, 768px, 390px.
- **Step 3:** Tiến hành tinh chỉnh mã nguồn bằng tay, điều chỉnh khoảng cách `gap`, bổ sung thuộc tính Responsive xếp dọc cho Header trên di động và hoàn thiện bảng kiểm thử.

---

## 2. Chi Tiết Các Yêu Cầu Đã Gửi Cho AI

### Yêu cầu 1: Tích hợp Menu điều hướng & Căn chỉnh Flexbox cho Header
- **Nội dung yêu cầu:** Yêu cầu AI hướng dẫn bổ sung thẻ `<nav class="nav-menu">` vào trong `<header>` và viết CSS sử dụng `display: flex`, `justify-content: space-between`, `align-items: center` để căn chỉnh tên cửa hàng bên trái, menu bên phải.
- **Kết quả thu me:** AI cung cấp đoạn mã HTML `<nav>` chuẩn ngữ nghĩa và mã CSS áp dụng Flexbox giúp bố cục Header dàn đều 2 bên mượt mà.
- **Xử lý của sinh viên:** Cập nhật mã vào dự án, mở DevTools bật nhãn `flex` để xác minh đường lưới Flexbox hiển thị đúng thực tế.

### Yêu cầu 2: Bổ sung hiệu ứng tương tác Hover & Focus-visible
- **Nội dung yêu cầu:** Yêu cầu AI đề xuất cách tạo hiệu ứng di chuột (`:hover`) đổi màu cho nút bấm/menu kèm `transition`, và bổ sung trạng thái `:focus-visible` hỗ trợ điều hướng bằng bàn phím (Accessibility).
- **Kết quả thu được:** AI đưa ra đoạn mã CSS `:hover` đổi màu nền và `:focus-visible` tạo đường viền nổi bật `outline: 3px solid #f59e0b`.
- **Xử lý của sinh viên:** Thử nghiệm dùng phím Tab trên bàn phím để kiểm tra tiêu điểm xuất hiện xung quanh tên sản phẩm và nút bấm trước khi đưa vào bài tập.

### Yêu cầu 3: Tối ưu Responsive cho thiết bị di động (390px)
- **Nội dung yêu cầu:** Yêu cầu AI hỗ trợ phát hiện và khắc phục lỗi xô lệch Header khi xem ở kích thước màn hình nhỏ 390px.
- **Kết quả thu được:** AI đề xuất sử dụng `@media (max-width: 576px)` kết hợp `flex-direction: column` để chuyển menu rớt xuống hàng dọc dưới tiêu đề.
- **Xử lý của sinh viên:** Kiểm tra trên Chrome DevTools ở mốc 390px, điều chỉnh lại `gap: 12px` cho thoáng mắt và ghi nhận đây là phần lỗi tự cải tiến độc lập.

---

## 3. Các Phần Sinh Viên Tự Điều Chỉnh Bằng Tay

| Thành phần mã | Mức độ điều chỉnh | Nội dung tự chỉnh sửa và lý do |
| :--- | :--- | :--- |
| **Cấu trúc Header (`<header>`)** | Bổ sung 100% | Tự tay chèn khối `<nav class="nav-menu">` chứa 3 liên kết *Trang chủ*, *Sản phẩm*, *Giới thiệu* để hoàn thiện chuẩn HTML5 ngữ nghĩa. |
| **Hiệu ứng `:focus-visible`** | Bổ sung 100% | Viết thêm các quy tắc CSS `:focus-visible` cho nút `.btn-add-cart` và thẻ tiêu đề sản phẩm để đáp ứng tiêu chuẩn Accessibility (hỗ trợ phím Tab). |
| **Tối ưu Responsive Header** | Điều chỉnh 40% | Viết đoạn mã `@media (max-width: 576px)` tùy chỉnh `flex-direction: column` và `align-items: flex-start` giúp menu không bị đè chữ hay tràn khung trên điện thoại 390px. |
| **Bảng kiểm thử & Báo cáo** | Tự thực hiện 100% | Lập bảng kiểm thử 7 tiêu chí (HTML, CSS Status 200, Image, Link, Responsive 390px, Hover/Focus, Sửa lỗi độc lập) và tự giải thích lý thuyết Box Model/Flexbox/Grid. |

---

## 4. Kết Quả AI Đề Xuất (Buổi 2)

- **Đề xuất Flexbox:** AI gợi ý giải pháp căn chỉnh Header 2 bên bằng `justify-content: space-between` và căn giữa theo trục dọc bằng `align-items: center`.
- **Đề xuất Accessibility:** AI hướng dẫn phân biệt `:hover` (tương tác chuột) và `:focus-visible` (tương tác bàn phím Tab), đề xuất sử dụng `outline-offset` để đường viền nổi bật không làm thay đổi kích thước phần tử.
- **Đề xuất Responsive:** AI gợi ý dùng Media Query để chuyển đổi linh hoạt giữa `flex-direction: row` (máy tính) và `flex-direction: column` (điện thoại).

---

## 5. Kiểm Tra Và Điều Chỉnh

### 5.1. Các điểm đã tiến hành kiểm tra
- **Kiểm tra DevTools Overlay:** Bật công cụ kiểm tra Flexbox/Grid trên Chrome DevTools (F12) để chụp ảnh minh chứng các trục căn chỉnh và khoảng cách `gap`.
- **Kiểm tra phím Tab (Keyboard Navigation):** Nhấn phím Tab liên tục trên trình duyệt để kiểm tra khung viền `:focus-visible` di chuyển qua từng liên kết và nút bấm.
- **Kiểm tra Responsive Multi-device:** Thay đổi kích thước trình duyệt DevTools ở các mốc 1366px (Desktop), 768px (Tablet) và 390px (Mobile) để xác minh bố cục không bị tràn.

### 5.2. Các điểm đã sửa đổi và không sử dụng
- **Điều chỉnh màu viền Focus:** Sửa màu `outline` mặc định của AI sang màu cam `#f59e0b` nổi bật để dễ quan sát hơn trên nền trắng.
- **Loại bỏ thuộc tính Flex thừa:** Loại bỏ các khai báo `flex-wrap` không cần thiết ở Header để giữ cho cấu trúc CSS đơn giản, dễ quản lý.

---

## 6. Phần Em Hiểu Và Có Thể Giải Thích

- **Vai trò của Class Selector & Box Model:** Giải thích rõ khái niệm `class` dùng để tái sử dụng style, sự khác biệt giữa `padding` (khoảng cách trong) và `margin` (khoảng cách ngoài đẩy phần tử).
- **Cơ chế Flexbox trong Header:** Giải thích được tác dụng của `display: flex` đặt ở phần tử cha (`.header-content`), thuộc tính `justify-content` điều khiển trục chính và `align-items` điều khiển trục phụ.
- **Sự khác biệt giữa CSS Grid và Flexbox:** Flexbox quản lý bố cục 1 chiều (hàng hoặc cột - áp dụng cho Header/Nút bấm), trong khi CSS Grid quản lý 2 chiều (hàng và cột - áp dụng chia 4 cột sản phẩm).
- **Ý nghĩa của `:hover` và `:focus-visible`:** `:hover` kích hoạt khi di chuột; `:focus-
