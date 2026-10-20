# AI Usage Log

## 1. Công cụ AI
Tên công cụ: Claude (Anthropic)

## 2. Mục đích sử dụng
- Phân tích giao diện và chức năng website Pet Mart theo 5 khu vực (Nhiệm vụ 2).
- Đề xuất phương án thiết kế thẻ sản phẩm (Nhiệm vụ 3, Bước 2).
- Tạo mã nguồn HTML/CSS ban đầu và ảnh SVG, giải thích cách chạy và các điểm cần kiểm tra (Nhiệm vụ 3, Bước 3).
- Giải thích các thành phần HTML/CSS để sinh viên hiểu và tự kiểm tra, chỉnh sửa.

## 3. Prompt đã sử dụng

### Prompt 1 – Phân tích website (Nhiệm vụ 2)
Chạy ở một cuộc trò chuyện mới, chỉ cung cấp tên và URL website, không cung cấp kết quả khảo sát của sinh viên.

```
Bạn là chuyên gia phân tích giao diện và trải nghiệm người dùng của website thương mại điện tử.

Hãy phân tích website sau:
- Tên: Pet Mart
- URL: https://www.petmart.vn/

Yêu cầu: phân tích 5 khu vực sau của website: Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng.

Với MỖI khu vực, trình bày theo 4 mục:
1. Chức năng đang được cung cấp
2. Điểm hợp lý trong thiết kế
3. Điểm có thể cải thiện
4. Đề xuất cải tiến và lý do

Trình bày dưới dạng một bảng gồm 5 dòng (mỗi khu vực một dòng) và 4 cột tương ứng 4 mục trên, mỗi ô ghi ngắn gọn.

Lưu ý:
- Chỉ nêu những gì bạn thực sự thấy hoặc truy cập được trên website.
- Nếu không truy cập được website hoặc không chắc một chi tiết, hãy nói rõ là "không chắc" hoặc "chưa kiểm chứng", không tự suy đoán.
- Trả lời bằng tiếng Việt.
```

### Prompt 2 – Đề xuất giao diện (Nhiệm vụ 3, Bước 2)
Chạy trong cuộc trò chuyện hỗ trợ bài tập, nơi AI đã có sẵn nội dung khảo sát của sinh viên.

```
Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử bằng HTML5 và CSS3.

Tôi muốn cải tiến khu vực: thẻ sản phẩm trong trang danh sách sản phẩm. Vấn đề hiện tại: thẻ sản phẩm có nhiều loại chỉ hiển thị khoảng giá, nhãn giảm giá đứng cạnh khoảng giá nên khách không biết giảm cho loại nào; nút "Thêm vào giỏ" chưa rõ thêm loại nào.

Đối tượng sử dụng: khách hàng mua sắm trực tuyến tại Việt Nam.

Hãy đề xuất:
1. Bố cục giao diện.
2. Các thành phần HTML cần sử dụng.
3. Cách tổ chức CSS.
4. Cách hiển thị trên máy tính và điện thoại.
5. Những điểm cần kiểm tra về khả năng sử dụng.

Trước tiên, hãy giải thích phương án thiết kế.
Chưa tạo toàn bộ mã nguồn cho đến khi tôi yêu cầu.
```

### Prompt 3 – Tạo mã nguồn (Nhiệm vụ 3, Bước 3)

```
Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện thương mại điện tử bằng HTML5 và CSS3.

Yêu cầu:
- Giao diện có tiêu đề và khu vực sản phẩm.
- Có tối thiểu 4 sản phẩm mẫu.
- Mỗi sản phẩm có hình ảnh, tên, giá và nút thao tác.
- Bố cục phù hợp với màn hình máy tính và điện thoại.
- Mã HTML có cấu trúc rõ ràng.
- CSS được tách thành file riêng.
- Không sử dụng backend hoặc cơ sở dữ liệu.
- Không đưa thư viện hoặc thành phần không cần thiết vào dự án.

Yêu cầu thêm theo phương án đã chọn:
- Có cả thẻ nhiều loại (hiện "Từ [giá thấp nhất]", liệt kê từng loại với giá, giá gốc gạch ngang và nhãn giảm giá của đúng loại đó, nút "Chọn tùy chọn") và thẻ một mức giá (giá hiện tại, giá gốc gạch ngang, nhãn % trên ảnh, nút "Thêm vào giỏ").
- Tên file: index.html và css/style.css.
- Hình ảnh dùng file SVG tự tạo đơn giản trong thư mục images/, không dùng ảnh của website khác.
- Thêm chú thích ngắn trong CSS cho từng đoạn.

Giải thích cách chạy trang web và những phần tôi cần kiểm tra.
```

## 4. Kết quả AI đề xuất

**Nhiệm vụ 2 – Phân tích website:** AI lập bảng phân tích 5 khu vực. AI đọc được nội dung chữ của trang chủ, trang danh mục và một trang chi tiết sản phẩm nên nêu được một số điểm như danh mục chưa thấy bộ lọc và sắp xếp, phân trang dài, trang chi tiết chỉ có một ảnh và không có nút "Mua ngay". AI không xem được hình ảnh, bị chặn ở trang giỏ hàng và không xem được trang kết quả tìm kiếm, nên ghi hai khu vực này là chưa kiểm chứng.

**Nhiệm vụ 3, Bước 2 – Phương án thiết kế:**
- Tách giá theo từng loại ngay trên thẻ để mức giảm đi kèm đúng loại.
- Thẻ nhiều loại: Từ giá 10000d, danh sách từng loại, nút "Chọn tùy chọn". Thẻ một mức giá: giá hiện tại, giá gốc gạch ngang, nhãn % trên ảnh, nút "Thêm vào giỏ".
- HTML: ul/li cho lưới, article cho thẻ, img có alt, h3 cho tên, del cho giá gốc, button cho nút.
- CSS: một file riêng, biến màu, đặt tên lớp theo thành phần, Grid cho lưới, Flexbox trong thẻ.
- Hiển thị: điện thoại 1 cột, máy tính bảng 2 cột, máy tính 3 cột.
- Các điểm cần kiểm tra về khả năng sử dụng.

**Nhiệm vụ 3, Bước 3 – Mã nguồn:** AI tạo `index.html`, `css/style.css` và 6 ảnh SVG với 6 sản phẩm mẫu (2 thẻ nhiều loại, 4 thẻ một mức giá), kèm hướng dẫn cách chạy và các điểm cần kiểm tra.

## 5. Kiểm tra và điều chỉnh

**Nhiệm vụ 2 – Đối chiếu với website thật** (sinh viên tự khảo sát trước, sau đó đối chiếu từng nhận xét của AI):
- *Giữ lại các ý đúng:* menu chia sẵn cho chó và mèo; có breadcrumb; có phân trang (khoảng 110 trang); không có bộ lọc và sắp xếp; thẻ sản phẩm có khoảng giá và nhãn giảm giá; nhóm sản phẩm chia theo loại; trang chi tiết có chọn loại, số lượng, nút "Thêm vào giỏ hàng" và sản phẩm tương tự; chỉ có một ảnh sản phẩm; không có nút "Mua ngay"; bài tin tức cũ.
- *Điều chỉnh:* AI nói chưa thấy ô tìm kiếm hiển thị sẵn, nhưng trên website thật ô tìm kiếm nằm ở đầu trang. AI nói giá chỉ hiện dạng khoảng, nhưng thực tế giá đổi theo loại đã chọn. AI nói "Sản phẩm tương tự" lẫn đồ chó trong trang đồ mèo, nhưng thực tế gặp chiều ngược lại (trang đồ chó có gợi ý đồ mèo).
- *Loại bỏ vì không đúng với website thật:* gợi ý tự động và lịch sử khi tìm kiếm; mã giảm giá sản phẩm trong giỏ; nhận xét khối "theo giống" ở trang chủ không khớp nội dung (thực tế khối đã chia theo chó và mèo); số sản phẩm mỗi trang là 12 (thực tế tùy trang); nút "Thêm vào giỏ" của sản phẩm có biến thể dẫn sang trang khác (thực tế không chuyển trang).
- *Bổ sung của sinh viên:* kết quả tìm kiếm chia "Bài viết" và "Sản phẩm", bài viết hiện trước sản phẩm, nhiều bài chỉ có ảnh "NO THUMBNAIL"; sau khi thêm vào giỏ có khung giỏ nhỏ hiện ngay, trang giỏ chưa thấy phí vận chuyển; breadcrumb ở trang chi tiết có một dấu chấm trống; nhãn "-17%" ở mục sản phẩm tương tự đứng cạnh khoảng giá nên chưa rõ giảm cho loại nào; chưa thấy ghi chú về VAT.

**Nhiệm vụ 3 – Kiểm tra mã nguồn:**
- Mở trang bằng Chrome, dùng DevTools kiểm tra ở 375px, 768px, 960px và 1280px: ảnh hiển thị đủ, bố cục đổi cột đúng (1, 2, 3 cột), không bị cuộn ngang.
- *Điểm sinh viên tự phát hiện và sửa:* khoảng trống lớn giữa tên và giá ở 768px và 1280px. Sinh viên dùng DevTools tìm ra nguyên nhân là `min-height: 2.6em` của `.card__title`, thử tắt thuộc tính, kiểm tra ở 960px (cỡ hẹp nhất của bố cục 3 cột) thấy tên vẫn một dòng và giá, nút các thẻ vẫn thẳng hàng, nên đã xóa dòng này trong `css/style.css`. Hạn chế đã biết: nếu sau này có tên sản phẩm dài xuống hai dòng, giá của các thẻ cạnh nhau có thể lệch.
- *Điều cần lưu ý:* giá và tên sản phẩm trong các thẻ mẫu chỉ là dữ liệu mẫu; ảnh sản phẩm là SVG tự tạo, không dùng ảnh của Pet Mart.

## 6. Phần tôi hiểu và có thể giải thích
- **`<ul>`, `<li>`, `<article>`:** danh sách sản phẩm là một `ul`, mỗi sản phẩm là một `li` chứa một `article` (một thẻ sản phẩm độc lập).
- **`<del>`:** đánh dấu nội dung bị thay thế (giá gốc), mặc định hiển thị gạch ngang.
- **`<button>`:** nút thao tác; có `type="button"` để không gửi form.
- **`display: grid` và `grid-template-columns`:** chia khu vực sản phẩm thành các cột; `repeat(3, 1fr)` là 3 cột bằng nhau.
- **`@media (min-width: ...)`:** khi màn hình đủ rộng thì áp dụng quy tắc bên trong, nhờ đó cùng một trang đổi cách hiển thị giữa điện thoại, máy tính bảng và máy tính.
- **`display: flex`, `flex-direction: column` và `margin-top: auto`:** xếp nội dung thẻ theo chiều dọc và đẩy nút xuống cuối thẻ để các nút thẳng hàng dù nội dung dài ngắn khác nhau.
- **`:root` và biến CSS (`--primary`, `--sale`...):** khai báo màu dùng chung, đổi một chỗ là đổi toàn trang.
- **`min-height` của `.card__title`:** đặt chiều cao tối thiểu cho tên sản phẩm. Dòng này tạo khoảng trống khi tên chỉ một dòng nên tôi đã bỏ; đánh đổi là nếu tên dài hai dòng thì giá các thẻ có thể lệch.
