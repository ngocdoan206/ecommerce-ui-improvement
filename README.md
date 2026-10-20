# E-commerce UI Improvement

## 1. Giới thiệu
Bài tập Chương 1 môn Phát triển ứng dụng WEB/TMĐT. Sinh viên khảo sát website thương mại điện tử Pet Mart, tìm ra vấn đề ở thẻ sản phẩm và xây dựng phiên bản thẻ sản phẩm cải tiến bằng HTML5 và CSS3.

Khu vực giao diện được cải tiến: **thẻ sản phẩm trong trang danh sách sản phẩm**, tập trung vào cách hiển thị giá từng loại, giá gốc, giá khuyến mãi và mức giảm giá.

## 2. Website tham khảo
- Tên website: Pet Mart
- URL: https://www.petmart.vn/
- Khu vực đã khảo sát: Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng.

Website chỉ dùng để tham khảo cách tổ chức giao diện. Mã nguồn và hình ảnh trong repository này do sinh viên và công cụ AI tạo ra, không sao chép mã nguồn hay hình ảnh của Pet Mart.

## 3. Chức năng
- Hiển thị danh sách sản phẩm (6 sản phẩm mẫu).
- Hiển thị tên và giá sản phẩm.
- Thẻ sản phẩm có nhiều loại: hiển thị Từ 10000d, liệt kê từng loại kèm giá, giá gốc gạch ngang và nhãn giảm giá của đúng loại, nút "Chọn tùy chọn".
- Thẻ sản phẩm một mức giá: hiển thị giá hiện tại, giá gốc gạch ngang, nhãn phần trăm giảm trên ảnh, nút "Thêm vào giỏ".
- Bố cục hỗ trợ nhiều kích thước màn hình: điện thoại 1 cột (thẻ xếp ngang), máy tính bảng 2 cột, máy tính 3 cột.
- Nút có viền khi chọn bằng bàn phím, ảnh có chữ thay thế (alt).

## 4. Công nghệ
- HTML5
- CSS3 (CSS Grid, Flexbox, media query, biến CSS)
- Không sử dụng backend, cơ sở dữ liệu hoặc thư viện bên ngoài.

Cấu trúc thư mục:
- `index.html`: trang web
- `css/style.css`: toàn bộ CSS
- `images/`: ảnh sản phẩm dạng SVG tự tạo
- `README.md`: tài liệu này
- `AI_USAGE.md`: nhật ký sử dụng AI

## 5. Cách chạy
Mở file `index.html` bằng trình duyệt.

Hoặc xem trực tiếp trên GitHub Pages: https://ngocdoan206.github.io/ecommerce-ui-improvement/

## 6. Cải tiến đã thực hiện
**Vấn đề ban đầu:** qua khảo sát Pet Mart, thẻ sản phẩm có nhiều loại (ví dụ 1 túi hoặc 6 túi) chỉ hiển thị một khoảng giá, và nhãn giảm giá "-17%" đứng cạnh khoảng giá đó. Khách khó biết mức giảm áp dụng cho loại nào và phải vào trang chi tiết mới thấy giá từng loại.

**Thay đổi đã thực hiện:**
- Tách giá theo từng loại ngay trên thẻ; mỗi loại có giá gốc và nhãn giảm giá riêng.
- Thẻ nhiều loại dùng nút "Chọn tùy chọn", thẻ một mức giá dùng nút "Thêm vào giỏ" để nút nói đúng hành động sẽ xảy ra.
- Dùng CSS Grid và media query để bố cục thay đổi theo màn hình, thẻ xếp ngang trên điện thoại để xem được nhiều sản phẩm hơn.
- Dùng margin-top: auto cho nút để các nút luôn thẳng hàng ở cuối thẻ.

**Điểm sinh viên tự phát hiện và chỉnh sửa:** khi kiểm tra ở 768px và 1280px, sinh viên thấy giữa tên sản phẩm và giá có một khoảng trống lớn. Nguyên nhân là thuộc tính `min-height: 2.6em` của `.card__title`, được đặt để dành chỗ cho tên hai dòng. Sinh viên thử tắt thuộc tính này trong Chrome DevTools và kiểm tra ở nhiều cỡ màn hình, kể cả 960px (cỡ hẹp nhất của bố cục 3 cột). Kết quả: tất cả tên sản phẩm vẫn nằm trên một dòng, giá và nút của các thẻ vẫn thẳng hàng, nên đã xóa dòng này trong `css/style.css`. Hạn chế đã biết: nếu sau này có sản phẩm tên dài xuống hai dòng, giá của các thẻ cạnh nhau có thể lệch nhau.

**Lưu ý:** giá và tên sản phẩm trong trang là dữ liệu mẫu phục vụ bài tập, không phải giá hiện tại của Pet Mart.

## 7. Hỗ trợ từ AI
Sinh viên sử dụng Claude (Anthropic) để:
- Phân tích website Pet Mart ở Nhiệm vụ 2.
- Đề xuất phương án thiết kế thẻ sản phẩm.
- Tạo mã nguồn HTML/CSS ban đầu và ảnh SVG.

Những phần sinh viên tự thực hiện:
- Tự khảo sát 5 khu vực của Pet Mart và ghi nhận trước khi dùng AI.
- Đối chiếu kết quả AI với website thật, giữ các ý đúng, loại các ý chưa có bằng chứng và bổ sung nhận xét riêng.
- Chọn phương án thiết kế.
- Mở trang trên trình duyệt, kiểm tra ở 375px, 768px, 960px và 1280px bằng Chrome DevTools.
- Tự phát hiện và chỉnh sửa khoảng trống giữa tên và giá (mục 6).

Chi tiết xem tại [AI_USAGE.md](AI_USAGE.md).
