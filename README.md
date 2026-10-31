# Pet Nhà Mình – E-commerce UI Improvement

Repository này lưu hai bài tập cá nhân liên tiếp của học phần *Phát triển ứng dụng WEB/TMĐT* (UEH), cùng phát triển một giao diện danh sách sản phẩm cho cửa hàng thú cưng mô phỏng.

- **Sinh viên:** Đoàn Thị Thu Ngọc

## 1. Tổng quan

| Bài tập | Nội dung chính | 
|---|---|
| Buổi 1 (Chương 1) | Khảo sát Pet Mart, phân tích vấn đề thẻ sản phẩm, xây dựng thẻ sản phẩm cải tiến bằng HTML5 và CSS3 | 
| Buổi 2 (Chương 2) | Củng cố HTML5 ngữ nghĩa, chuẩn hóa CSS, Box Model, Flexbox, CSS Grid, hover/focus, kiểm thử và tự sửa lỗi | 

Buổi 2 tiếp tục trên mã nguồn của Buổi 1, không tạo repository mới. Lịch sử thay đổi của từng buổi xem ở mục *Commits* trên GitHub.

## 2. Website tham khảo

- Tên website: Pet Mart
- URL: https://www.petmart.vn/
- Khu vực đã khảo sát: Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng.

Website chỉ dùng để tham khảo cách tổ chức giao diện. Mã nguồn và hình ảnh trong repository này do sinh viên và công cụ AI tạo ra, không sao chép mã nguồn hay hình ảnh của Pet Mart. Tên cửa hàng **Pet Nhà Mình**, địa chỉ, số điện thoại, email, tên và giá sản phẩm đều là **dữ liệu mẫu** phục vụ bài tập, không phải thông tin thật.

## 3. Giao diện hiện tại

| Thành phần | Mô tả | Thuộc buổi |
|---|---|---|
| Thanh thông tin, header | Ưu đãi giao hàng, hotline, logo và tên cửa hàng, ô tìm kiếm, giỏ hàng | Buổi 2 |
| Menu và đường dẫn | Menu chính 6 mục, đường dẫn (breadcrumb), liên kết "Bỏ qua menu" | Buổi 2 |
| Danh sách sản phẩm | 6 sản phẩm mẫu, hiển thị tên, giá, giá gốc gạch ngang, nhãn giảm giá | Buổi 1 |
| Thẻ nhiều loại | Hiển thị "Từ 10.000₫", liệt kê từng loại kèm giá, giá gốc và nhãn giảm giá đúng loại, nút "Chọn tùy chọn" | Buổi 1 |
| Thẻ một mức giá | Giá hiện tại, giá gốc, nhãn phần trăm giảm trên ảnh, nút "Thêm vào giỏ" | Buổi 1 |
| Bố cục theo màn hình | Điện thoại 1 cột (thẻ xếp ngang), máy tính bảng 2 cột, máy tính 3 cột | Buổi 1, hoàn thiện ở Buổi 2 |
| Chân trang | 3 cột: giới thiệu, hỗ trợ khách hàng, liên hệ | Buổi 2 |
| Tương tác | Khung focus khi dùng bàn phím (Buổi 1); hiệu ứng hover và `transition` (Buổi 2) | Buổi 1, 2 |

## 4. Công nghệ và cấu trúc thư mục

HTML5 và CSS3 (CSS Grid, Flexbox, media query, biến CSS). Không dùng backend, cơ sở dữ liệu hay thư viện bên ngoài.

```
ecommerce-ui-improvement/
├── index.html
├── css/
│   └── style.css
├── images/            (6 ảnh sản phẩm SVG + logo.svg)
├── README.md
└── AI_USAGE.md
```

## 5. Cách chạy

1. Tải mã nguồn: `git clone https://github.com/ngocdoan206/ecommerce-ui-improvement.git` (hoặc *Code → Download ZIP* rồi giải nén).
2. Mở thư mục bằng VS Code, nhấp đúp `index.html` để mở bằng trình duyệt.
3. Hoặc xem trực tiếp trên GitHub Pages: https://ngocdoan206.github.io/ecommerce-ui-improvement/

## 6. Buổi 1 – Khảo sát và cải tiến thẻ sản phẩm

**Khu vực cải tiến:** thẻ sản phẩm trong trang danh sách sản phẩm, tập trung vào cách hiển thị giá từng loại, giá gốc, giá khuyến mãi và mức giảm giá.

**Vấn đề ban đầu:** qua khảo sát Pet Mart, thẻ sản phẩm có nhiều loại (ví dụ 1 túi hoặc 6 túi) chỉ hiển thị một khoảng giá, và nhãn giảm giá "-17%" đứng cạnh khoảng giá đó. Khách khó biết mức giảm áp dụng cho loại nào và phải vào trang chi tiết mới thấy giá từng loại.

**Thay đổi đã thực hiện:**
- Tách giá theo từng loại ngay trên thẻ; mỗi loại có giá gốc và nhãn giảm giá riêng.
- Thẻ nhiều loại dùng nút "Chọn tùy chọn", thẻ một mức giá dùng nút "Thêm vào giỏ" để nút nói đúng hành động sẽ xảy ra.
- Dùng CSS Grid và media query để bố cục thay đổi theo màn hình, thẻ xếp ngang trên điện thoại để xem được nhiều sản phẩm hơn.
- Dùng `margin-top: auto` cho nút để các nút luôn thẳng hàng ở cuối thẻ.

**Điểm sinh viên tự phát hiện và chỉnh sửa:** khi kiểm tra ở 768px và 1280px, sinh viên thấy giữa tên sản phẩm và giá có một khoảng trống lớn. Nguyên nhân là thuộc tính `min-height: 2.6em` của `.card__title`, được đặt để dành chỗ cho tên hai dòng. Sinh viên thử tắt thuộc tính này trong Chrome DevTools và kiểm tra ở nhiều cỡ màn hình, kể cả 960px (cỡ hẹp nhất của bố cục 3 cột). Kết quả: tất cả tên sản phẩm vẫn nằm trên một dòng, giá và nút của các thẻ vẫn thẳng hàng, nên đã xóa dòng này trong `css/style.css`. Hạn chế đã biết: nếu sau này có sản phẩm tên dài xuống hai dòng, giá của các thẻ cạnh nhau có thể lệch nhau.

## 7. Buổi 2 – HTML5 và CSS3

### 7.1. Vấn đề phát hiện ở đầu buổi

Khi rà soát lại sản phẩm Buổi 1, trang còn ba vấn đề:

| Vấn đề | Hướng cải thiện | Kết quả mong muốn |
|---|---|---|
| Chưa có menu điều hướng, tên sản phẩm không phải liên kết | Thêm header có `nav`; đặt tên sản phẩm thành thẻ `a` | Có đường đi giữa các khu vực, HTML đúng ngữ nghĩa |
| Nút chính và nhãn giảm giá có tỷ lệ tương phản dưới 4,5:1 (4,33:1 và 4,39:1) | Đổi màu theo hướng tối hơn | Chữ dễ đọc, đạt WCAG AA |
| Thẻ không phản hồi khi rê chuột | Thêm `:hover`, `transition`, `:focus-visible` | Nhận biết thẻ và nút có thể tương tác |

### 7.2. Kỹ thuật đã thực hành

| Nội dung | Đã áp dụng |
|---|---|
| HTML5 ngữ nghĩa | `header`, `nav` (menu chính và đường dẫn), `main`, `section`, `article`, `footer`, `address`; thứ bậc tiêu đề h1 → h2 → h3 |
| Liên kết, hình ảnh, danh sách | `a`, `img` có `alt`, `ul`/`ol`/`li`; mỗi thẻ sản phẩm có một liên kết |
| CSS bên ngoài | `css/style.css` liên kết bằng `<link>`; màu khai báo bằng biến CSS |
| Selector | Element (`a`, `img`), class (`.card`, `.price`), descendant (`.card__title a`, `.options li`) |
| Box Model | `margin`, `padding`, `border`, `border-radius`, `box-sizing: border-box` |
| Flexbox | Thanh thông tin, hàng logo – tìm kiếm – giỏ hàng, menu |
| CSS Grid | Danh sách sản phẩm 1 / 2 / 3 cột (mốc 600 px và 960 px), chân trang 3 cột |
| Hover và focus | `:hover`, `:focus-visible`, `:focus-within`, `transition`, `prefers-reduced-motion` |

### 7.3. Thay đổi so với Buổi 1

- **Cấu trúc:** thêm header (thanh thông tin, logo, ô tìm kiếm, giỏ hàng, menu), đường dẫn và chân trang 3 cột; tên sản phẩm trở thành liên kết (`href="#"` vì chưa có trang chi tiết).
- **Màu sắc:** `--primary` từ `#e6321f` sang `#cc2a1a`, `--primary-dark` sang `#a82012`, `--sale` từ `#d12a1a` sang `#b92518`. Tỷ lệ tương phản tăng lên khoảng 5,3:1.
- **Thẻ sản phẩm:** `padding` 10 → 12 px (và 12 → 16 px từ 600 px), viền `#d5dbe8`, bo góc 14 → 16 px, giá 1,125 → 1,25 rem, tên sản phẩm đậm hơn.
- **Tương tác:** thẻ nhấc lên và có bóng khi rê chuột, nút và menu đổi màu mượt, khung focus xanh khi dùng phím Tab.

### 7.4. Điểm sinh viên tự sửa lỗi

Khi kiểm tra ở 980 px (bố cục 3 cột), nhãn "Giảm 17%" trong dòng "6 túi" bị rớt xuống dòng riêng và nằm sát trái. Nguyên nhân là dòng này rộng khoảng 269 px, không đủ chỗ cho tên gói, giá, giá cũ và nhãn trên một dòng, nên `flex-wrap` đẩy nhãn xuống. Cách sửa: giảm `gap` của `.options li` từ 8 px xuống 6 px, giảm `padding` từ `4px 8px` xuống `4px 6px`, giảm `min-width` của `.options__name` từ 3,2em xuống 2,6em, và thêm `margin-left: auto` cho `.tag` để nhãn nằm sát phải khi vẫn phải xuống dòng. Kết quả: ở 980 px và 1366 px nhãn nằm cùng dòng; ở 390 px dòng chỉ rộng khoảng 208 px nên nhãn vẫn xuống dòng, đây là hành vi chủ ý.

### 7.5. Kiểm thử

Kiểm tra bằng Chrome DevTools ở 1366 px, 768 px và 390 px; kiểm tra HTML bằng Nu Html Checker.

| Nội dung kiểm tra | Kết quả | Ghi chú |
|---|---|---|
| Trang HTML mở được | Đạt | Nu Html Checker không báo lỗi hay cảnh báo |
| CSS được áp dụng | Đạt | `css/style.css` liên kết đúng |
| Hình ảnh hiển thị đúng | Đạt | Không bị méo ở 3 kích thước |
| Liên kết hoạt động | Đạt một phần | Dùng `href="#"` vì chưa có trang đích |
| Bố cục không tràn nghiêm trọng | Đạt | Không có thanh cuộn ngang của cả trang |
| Hover/focus hoạt động | Đạt | Kiểm tra bằng chuột và phím Tab |
| Đã tự sửa ít nhất một vấn đề | Đạt | Mục 7.4 |

## 8. Hỗ trợ từ AI

Công cụ: Claude (Anthropic).

**Buổi 1:** phân tích website Pet Mart ở Nhiệm vụ 2, đề xuất phương án thiết kế thẻ sản phẩm, tạo mã HTML/CSS ban đầu và ảnh SVG.

**Buổi 2:** rà soát và đo trang, soạn khối HTML header/chân trang và logo SVG, soạn các khối CSS (định dạng, hover/focus), gợi ý thí nghiệm Flexbox, Grid và cách sửa lỗi nhãn giảm giá.

**Phần sinh viên tự thực hiện (cả hai buổi):**
- Tự khảo sát 5 khu vực của Pet Mart và ghi nhận trước khi dùng AI.
- Đối chiếu kết quả AI với website thật, giữ các ý đúng, loại các ý chưa có bằng chứng.
- Chọn phương án thiết kế, chọn tên cửa hàng, áp dụng từng thay đổi vào mã.
- Chạy trang và kiểm tra bằng Chrome DevTools, phím Tab và Nu Html Checker ở nhiều kích thước màn hình.
- Tự phát hiện và chỉnh sửa lỗi ở mỗi buổi (mục 6 và mục 7.4).

Chi tiết các prompt và phần kiểm tra, điều chỉnh xem tại [AI_USAGE.md](AI_USAGE.md).

## 9. Liên kết

- Repository: https://github.com/ngocdoan206/ecommerce-ui-improvement
- Website (GitHub Pages): https://ngocdoan206.github.io/ecommerce-ui-improvement/

## 10. Hạn chế và hướng phát triển

Các liên kết hiện dùng `href="#"`; ô tìm kiếm và giỏ hàng mới chỉ là giao diện; dữ liệu cửa hàng và sản phẩm là dữ liệu mẫu. Nếu sản phẩm có tên dài xuống hai dòng, giá của các thẻ cạnh nhau có thể lệch nhau. Ở Buổi 3, trang sẽ được bổ sung JavaScript để tìm kiếm, lọc theo danh mục, sắp xếp theo giá và thêm sản phẩm vào giỏ hàng.
