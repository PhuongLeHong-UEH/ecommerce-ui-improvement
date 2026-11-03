# BÁO CÁO BÀI TẬP CÁ NHÂN - BUỔI 2
**Môn học:** Phát triển ứng dụng Thương mại điện tử  
**Sinh viên thực hiện:** Lê Hồng Phương  - 31241024012  - EE0001 

---

## 1. Giới thiệu bài tập
Bài tập cá nhân Buổi 2 tiếp tục phát triển giao diện website thương mại điện tử từ Buổi 1. Mục tiêu của bài tập là tinh chỉnh mã nguồn HTML5/CSS3 chuẩn ngữ nghĩa, thực hành tổ chức bố cục với Box Model, Flexbox, CSS Grid và bổ sung các hiệu ứng tương tác (hover, focus-visible) tăng cường khả năng truy cập (Accessibility).

---

## 2. Website tham khảo và khu vực đã cải tiến
* **Website tham khảo:** Website Tiki ở buổi 1.
* **Khu vực đã cải tiến:** 
  * Tối ưu hóa **Header** tích hợp menu điều hướng (`<nav>`).
  * Cải tiến khu vực **Danh sách thẻ sản phẩm** (Product Grid) hiển thị thông tin giá bán, giá cũ, phần trăm giảm giá và nút bấm mua hàng.

---

## 3. Những kỹ thuật HTML5/CSS3 đã thực hành
* **HTML5 Semantic:** Sử dụng chuẩn các thẻ ngữ nghĩa `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`.
* **CSS Selector & Box Model:** 
  * Áp dụng Class Selector (`.product-card`, `.btn-add-cart`, `.nav-menu`) để định dạng tái sử dụng mã.
  * Tối ưu `margin`, `padding`, `border`, `border-radius` cho khung thẻ và khoảng cách nội dung.
* **Flexbox Layout:**
  * Dùng `display: flex`, `justify-content: space-between`, `align-items: center` để căn chỉnh Header và Menu nằm ngang.
  * Dùng Flexbox xếp dọc nội dung bên trong `.product-card` và căn giữa icon/chữ trong nút bấm `.btn-add-cart`.
* **CSS Grid Layout:** Áp dụng `display: grid` kết hợp `grid-template-columns: repeat(auto-fill, minmax(240px, 1fr))` và `gap: 16px` để tự động chia cột sản phẩm co giãn mượt mà.
* **Hiệu ứng & Accessibility:**
  * Thêm `:hover` tạo chuyển đổi hiệu ứng mềm mại (`transition: transform, background-color`).
  * Bổ sung `:focus-visible` giúp hiển thị đường viền viền nổi bật khi điều hướng giao diện bằng phím Tab.

---

## 4. Hướng dẫn chạy website
1. Tải repository hoặc giải nén thư mục dự án về máy tính.
2. Mở trực tiếp tệp `index.html` bằng các trình duyệt web phổ biến (Google Chrome, Microsoft Edge, Mozilla Firefox).
3. (Hoặc) Sử dụng tiện ích mở rộng **Live Server** trên Visual Studio Code để xem xem trước trực tiếp.

---

## 5. Những thay đổi đã thực hiện
* Bổ sung cấu trúc thẻ `<nav class="nav-menu">` chứa các liên kết điều hướng (*Trang chủ*, *Sản phẩm*, *Giới thiệu*) vào trong `<header>`.
* Cập nhật quy tắc Flexbox cho Header, hỗ trợ phản hồi responsive tự động xếp dọc (`flex-direction: column`) khi co màn hình xuống kích thước thiết bị di động (390px).
* Thiết lập hệ thống biến CSS (CSS Variables) ở `:root` để quản lý màu sắc đồng bộ (`--primary-color`, `--price-color`).
* Bổ sung trạng thái `:focus-visible` cho nút bấm và đường liên kết nhằm nâng cao trải nghiệm truy cập bằng bàn phím.

---

## 6. Công cụ AI đã sử dụng và cách tôi kiểm tra kết quả
* **Công cụ AI hỗ trợ:** ChatGPT / Claude / Gemini (sử dụng hỗ trợ tra cứu thuộc tính CSS và tối ưu Responsive).
* **Quy trình kiểm tra kết quả:**
  1. Sử dụng **Chrome DevTools (F12)** kiểm tra cấu trúc DOM (Elements) và kiểm tra tệp CSS (Network trả về Status 200).
  2. Bật công cụ **Flexbox Overlay / Grid Overlay** trên DevTools để xác minh các đường trục căn chỉnh và khoảng cách `gap`.
  3. Kiểm tra tính năng Responsive trên các mốc kích thước tiêu chuẩn: Desktop (1366px), Tablet (768px/960px) và Mobile (390px).
  4. Sử dụng phím **Tab** trên bàn phím để nghiệm thu hiệu ứng `:focus-visible`.

---

## 7. Đường dẫn repository và website
* **GitHub Repository:** https://github.com/PhuongLeHong-UEH/ecommerce-ui-improvement
* **Website Demo (nếu có):** https://phuonglehong-ueh.github.io/ecommerce-ui-improvement/ 


