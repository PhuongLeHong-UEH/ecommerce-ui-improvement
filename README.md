# Báo Cáo Cải Tiến Giao Diện Thẻ Sản Phẩm Website Thương Mại Điện Tử

Môn học: Phát triển ứng dụng Web và Thương mại điện tử
Thực hiện: Lê Hồng Phương 
Mã sinh viên: 31241024012 
Lớp: EE0001
Website nghiên cứu: Tiki 
Trang chạy thử nghiệm: https://tiki.vn 

---

## 1. Tổng Quan Về Website Nghiên Cứu

Nền tảng khảo sát: Tiki (https://tiki.vn)
Lĩnh vực hoạt động: Thương mại điện tử đa ngành hàng (sách, thiết bị số, thời trang, đồ gia dụng).
Khách hàng mục tiêu: Người tiêu dùng mua sắm trực tuyến tại Việt Nam có nhu cầu về sản phẩm chính hãng và dịch vụ giao hàng nhanh.
Các chức năng chính: Tìm kiếm, lọc sản phẩm theo ngành hàng, xem thông tin chi tiết, thêm sản phẩm vào giỏ và thanh toán.

---

## 2. Bảng Khảo Sát 5 Khu Vực Giao Diện Trên Tiki

| Khu vực | Mục đích chức năng | Thành phần giao diện | Điểm thuận tiện cho người dùng | Vấn đề phát sinh thực tế | Đề xuất cải tiến |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1. Trang chủ | Điều hướng, giới thiệu chương trình ưu đãi và sản phẩm nổi bật. | Banner quảng cáo, biểu tượng ngành hàng, khối sản phẩm Flash Sale, danh sách gợi ý. | Hiển thị khuyến mãi trực quan, có nhãn phân biệt sản phẩm giao nhanh TikiNOW. | Mật độ banner và hình ảnh dày đặc gây rối mắt người dùng trên màn hình nhỏ. | Thu gọn khối quảng cáo phụ, gom các nhóm ngành hàng thành danh mục trượt đơn giản. |
| 2. Danh mục sản phẩm | Phân loại và lọc sản phẩm theo nhu cầu cụ thể của khách hàng. | Cây danh mục, bộ lọc theo giá/thương hiệu/đánh giá, thanh sắp xếp. | Tiêu chí lọc đa dạng, tích hợp bộ lọc dịch vụ giao hàng 2 giờ. | Bảng bộ lọc trên giao diện di động chiếm nhiều diện tích hiển thị. | Chuyển bộ lọc trên điện thoại sang dạng danh sách thẻ ngang thu gọn. |
| 3. Chi tiết sản phẩm | Cung cấp đầy đủ thông tin để người dùng quyết định mua hàng. | Bộ ảnh sản phẩm, thông tin giá, thông số kỹ thuật, đánh giá của người mua, nút mua hàng. | Nút đặt hàng bố trí ở vị trí dễ quan sát, hiển thị đánh giá thực tế kèm hình ảnh. | Phần mô tả nội dung kéo dài làm mất thời gian cuộn trang của người dùng. | Thêm thanh điều hướng cố định phía trên khi cuộn xuống xem thông số và đánh giá. |
| 4. Tìm kiếm | Hỗ trợ người dùng chủ động tìm kiếm sản phẩm theo từ khóa. | Thanh nhập từ khóa, danh sách gợi ý tự động, lịch sử tìm kiếm. | Trả về gợi ý nhanh, có hiển thị ảnh thu nhỏ và giá sản phẩm ngay trong danh sách gợi ý. | Kết quả tìm kiếm đôi khi không chính xác nếu người dùng nhập sai lỗi chính tả phức tạp. | Bổ sung cơ chế tự động sửa lỗi chính tả tiếng Việt và hỗ trợ tìm kiếm bằng hình ảnh. |
| 5. Giỏ hàng | Kiểm tra danh sách sản phẩm đã chọn, áp dụng mã giảm giá và tính tổng tiền. | Danh sách sản phẩm chia theo cửa hàng, ô nhập mã giảm giá, bảng tính tổng chi phí, nút thanh toán. | Phân loại rõ ràng từng nhà bán hàng, tự động cập nhật tổng tiền khi thay đổi số lượng. | Khối tóm tắt tiền bị đẩy xuống dưới cùng khi danh sách sản phẩm dài. | Cố định thanh tóm tắt chi phí và nút thanh toán ở cuối màn hình điện thoại. |

---

## 3. Phân Tích 3 Lỗi Giao Diện Thẻ Sản Phẩm Và Phương Án Xử Lý

### 3.1. Các lỗi phát hiện trên giao diện thực tế
1. Cấu trúc giá thiếu rõ ràng: Giá gốc và phần trăm giảm giá hiển thị mờ, mức độ tương phản thấp khiến người dùng khó nhận biết mức giảm.
2. Nút mua hàng không nổi bật: Thiếu nút thao tác trực tiếp trên thẻ hoặc nút có kích thước nhỏ, chưa tạo được điểm nhấn để người dùng thực hiện hành động.
3. Bố cục thẻ lệch nhau: Tên sản phẩm có độ dài ngắn khác nhau làm chiều cao các thẻ bị trập trùng, làm cho hàng nút bấm bị lệch không thẳng hàng.

### 3.2. Giải pháp kỹ thuật triển khai bằng HTML5 và CSS3
1. Xử lý hiển thị giá:
   - Dùng font chữ đậm và kích thước lớn cho giá bán chính thức.
   - Đặt giá gốc phía dưới có gạch ngang kèm nhãn phần trăm giảm giá ngay bên cạnh để tăng mức độ chú ý.
2. Thiết kế nút mua hàng:
   - Bổ sung nút "Thêm vào giỏ" rộng bằng chiều ngang thẻ sản phẩm.
   - Sử dụng màu nền có độ tương phản cao so với nền trắng của thẻ và thêm hiệu ứng đổi màu khi rê chuột.
3. Đồng bộ kích thước thẻ và xử lý tên sản phẩm:
   - Áp dụng CSS Grid cho khung chứa và Flexbox cho cấu trúc bên trong thẻ sản phẩm, đặt chiều cao cố định 100%.
   - Sử dụng thuộc tính `-webkit-line-clamp: 2` kết hợp chiều cao cố định cho phần tên sản phẩm để giới hạn tối đa 2 dòng. Nếu tên dài hơn sẽ tự động xuất hiện dấu ba chấm.
   - Đặt `margin-top: auto` cho nút mua hàng để đẩy nút xuống vị trí đáy thẻ, giúp toàn bộ hàng nút luôn nằm trên một đường thẳng.

---

## 4. Cấu Trúc Thư Mục Dự Án

ecommerce-ui-improvement/
├── index.html
├── css/
│   └── style.css
├── images/
│   ├── ao_thun.jpg
│   ├── giay.jpg
│   ├── quan_tay.jpg
│   └── sandal.jpg
├── README.md
└── AI_USAGE.md

---

## 5. Hướng Dẫn Chạy Vấn Đáp Và Kiểm Thử

### Cách chạy dự án:
1. Tải thư mục mã nguồn về máy tính.
2. Mở file `index.html` bằng trình duyệt web bất kỳ hoặc phần mềm VS Code.

### Các điểm cần kiểm tra khi đánh giá:
- Giá bán hiện tại có hiển thị rõ ràng hơn so với giá gốc và phần trăm giảm giá không.
- Thử thay đổi kích thước trình duyệt từ máy tính xuống di động để kiểm tra khả năng tự động chuyển từ 4 cột sang 2 cột.
- Kiểm tra các thẻ sản phẩm có tên ngắn và tên dài để xác nhận chiều cao toàn bộ các thẻ và vị trí nút bấm luôn thẳng hàng.

# 6. Cải Tiến Đã Thực Hiện 
## 6.1. Mô tả vấn đề ban đầu - Vấn đề 1: Phần hiển thị giá sản phẩm thiếu sự tương phản. Giá gốc, giá bán và nhãn phần trăm giảm giá nằm sát nhau với font chữ mờ, khiến người mua khó nhận biết mức độ ưu đãi. - Vấn đề 2: Nút thao tác mua hàng chưa nổi bật hoặc bị thiếu trên thẻ sản phẩm, chưa tạo được điểm nhấn để kích thích hành động của khách hàng. - Vấn đề 3: Các thẻ sản phẩm nằm cùng một hàng có chiều cao không đồng đều do độ dài tên sản phẩm khác nhau. Tên quá dài làm đẩy các phần tử bên dưới xuống, làm cho hàng nút bấm bị lệch không thẳng hàng. 

## 6.2. Thay đổi đã thực hiện - Thay đổi 1 (Tối ưu hiển thị giá): Tách biệt giá bán chính thức bằng font chữ to (18px), tô đậm và sử dụng màu đỏ tương phản cao. Đặt giá gốc gạch ngang phía dưới cùng nhãn phần trăm giảm giá dạng khung rõ ràng ngay bên cạnh. - Thay đổi 2 (Nổi bật nút bấm): Thêm nút "Thêm vào giỏ" nằm ngang bằng chiều rộng thẻ sản phẩm, dùng màu xanh nổi bật kèm biểu tượng giỏ hàng và hiệu ứng chuyển màu khi rê chuột. - Thay đổi 3 (Cân bằng bố cục): Đặt chiều cao cố định 100% cho toàn bộ thẻ bằng CSS Grid và Flexbox. Sử dụng thuộc tính cắt chữ tự động (-webkit-line-clamp: 2) để giới hạn tiêu đề tối đa 2 dòng. Đặt thuộc tính margin-top: auto cho nút mua hàng để đảm bảo tất cả các nút luôn căn thẳng hàng ngang ở đáy thẻ. 


--- # 7. Hỗ Trợ Từ AI 

## 7.1. Tóm tắt những phần AI hỗ trợ - Phân tích và lập bảng đánh giá trải nghiệm người dùng (UX/UI) trên 5 khu vực của website Tiki.vn. - Gợi ý phương án xử lý bố cục thẻ sản phẩm bằng các kỹ thuật CSS hiện đại (Flexbox, Grid, -webkit-line-clamp). - Sinh mã khung ban đầu cho file index.html và file style.css. 


## 7.2. Các phần tôi đã kiểm tra - Đối chiếu thực tế: Truy cập trực tiếp website Tiki.vn để xác minh các nhận xét của AI, loại bỏ các đánh giá thiếu căn cứ. - Sửa mã HTML: Thay đổi toàn bộ đường dẫn hình ảnh online sang thư mục tệp tin nội bộ (images/ao_thun.jpg, images/giay.jpg, images/quan_tay.jpg, images/sandal.jpg) và cập nhật tên sản phẩm, giá tiền đúng với hình ảnh thực tế. - Tinh chỉnh CSS: Bổ sung thuộc tính object-fit: cover giúp hình ảnh không bị co giãn méo tỉ lệ, thiết lập chiều cao dòng cố định cho phần tên sản phẩm để tránh lỗi hiển thị trên các trình duyệt khác nhau. - Kiểm thử giao diện: Mở trang web trên trình duyệt, nhấn F12 để kiểm tra độ cân bằng chiều cao của các thẻ sản phẩm và thu nhỏ màn hình để xác nhận tính năng tự động chuyển từ 4 cột sang 2 cột trên điện thoại chạy ổn định. 




