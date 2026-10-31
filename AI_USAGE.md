# AI Usage Log

Nhật ký sử dụng AI cho hai bài tập: **Buổi 1 (Chương 1)** – khảo sát và cải tiến thẻ sản phẩm; **Buổi 2 (Chương 2)** – HTML5 và CSS3.

## 1. Công cụ AI
Tên công cụ: Claude (Anthropic)

## 2. Mục đích sử dụng

### Buổi 1 (Chương 1)
- Phân tích giao diện và chức năng website Pet Mart theo 5 khu vực (Nhiệm vụ 2).
- Đề xuất phương án thiết kế thẻ sản phẩm (Nhiệm vụ 3, Bước 2).
- Tạo mã nguồn HTML/CSS ban đầu và ảnh SVG, giải thích cách chạy và các điểm cần kiểm tra (Nhiệm vụ 3, Bước 3).
- Giải thích các thành phần HTML/CSS để sinh viên hiểu và tự kiểm tra, chỉnh sửa.

### Buổi 2 (Chương 2)
- Tóm tắt các bước của đề và nhắc những chỗ cần chụp màn hình.
- Rà soát trang Buổi 1 và đo các vấn đề về cấu trúc, tương phản màu, hiệu ứng tương tác (Bước 1).
- Soạn khối HTML header, menu, đường dẫn, chân trang và logo SVG (Bước 2).
- Soạn các khối CSS (định dạng, Box Model, hover/focus) kèm giải thích từng chỗ sửa (Bước 3, 4, 7).
- Gợi ý các thí nghiệm Flexbox và CSS Grid trong DevTools (Bước 5, 6).
- Gợi ý cách sửa lỗi nhãn giảm giá (Bước 8).

## 3. Prompt đã sử dụng

### Buổi 1 (Chương 1)

#### Prompt 1 – Phân tích website (Nhiệm vụ 2)
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

#### Prompt 2 – Đề xuất giao diện (Nhiệm vụ 3, Bước 2)
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

#### Prompt 3 – Tạo mã nguồn (Nhiệm vụ 3, Bước 3)

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

### Buổi 2 (Chương 2)
Dưới đây là bốn prompt đã dùng

#### Prompt 4 – Nhờ rà soát trang vì còn đơn sơ (Bước 1)
Gửi kèm ảnh chụp trang, `index.html` và `style.css` của Buổi 1.

```
Hãy giúp tôi hoàn thành Bước 1 một cách đầu tư và nghiên cứu kỹ, để trang có thể phát triển lên chuyên nghiệp.
```

#### Prompt 5 – Làm giao diện giống một cửa hàng thật (Bước 2)

```
Trang đã có header nhưng chưa chuyên nghiệp và chưa giống một shop bán sản phẩm. Tôi muốn điều chỉnh để sắp xếp lại như một website chuyên nghiệp: có logo, tên cửa hàng, địa chỉ... 
```

#### Prompt 6 – Yêu cầu giải thích từng chỗ sửa (Bước 3–4)
Gửi kèm tệp `style.css` hiện tại.

```
Hướng dẫn sửa từ dưới lên: chỗ cũ là gì, thay bằng gì, để làm gì, để tôi hiểu việc mình đang làm.
```

#### Prompt 7 – Phản hồi kết quả thử một đề xuất (Bước 8)
Gửi kèm ảnh chụp trang ở 390 px sau khi thêm `margin-left: auto` cho `.tag`.

```
Tôi đã thêm dòng đó nhưng nhãn "Giảm 17%" vẫn bị xuống dòng.
```

## 4. Kết quả AI đề xuất

### Buổi 1 (Chương 1)

**Nhiệm vụ 2 – Phân tích website:** AI lập bảng phân tích 5 khu vực. AI đọc được nội dung chữ của trang chủ, trang danh mục và một trang chi tiết sản phẩm nên nêu được một số điểm như danh mục chưa thấy bộ lọc và sắp xếp, phân trang dài, trang chi tiết chỉ có một ảnh và không có nút "Mua ngay". AI không xem được hình ảnh, bị chặn ở trang giỏ hàng và không xem được trang kết quả tìm kiếm, nên ghi hai khu vực này là chưa kiểm chứng.

**Nhiệm vụ 3, Bước 2 – Phương án thiết kế:**
- Tách giá theo từng loại ngay trên thẻ để mức giảm đi kèm đúng loại.
- Thẻ nhiều loại: Từ 10.000₫, danh sách từng loại, nút "Chọn tùy chọn". Thẻ một mức giá: giá hiện tại, giá gốc gạch ngang, nhãn % trên ảnh, nút "Thêm vào giỏ".
- HTML: ul/li cho lưới, article cho thẻ, img có alt, h3 cho tên, del cho giá gốc, button cho nút.
- CSS: một file riêng, biến màu, đặt tên lớp theo thành phần, Grid cho lưới, Flexbox trong thẻ.
- Hiển thị: điện thoại 1 cột, máy tính bảng 2 cột, máy tính 3 cột.
- Các điểm cần kiểm tra về khả năng sử dụng.

**Nhiệm vụ 3, Bước 3 – Mã nguồn:** AI tạo `index.html`, `css/style.css` và 6 ảnh SVG với 6 sản phẩm mẫu (2 thẻ nhiều loại, 4 thẻ một mức giá), kèm hướng dẫn cách chạy và các điểm cần kiểm tra.

### Buổi 2 (Chương 2)

**Prompt 4 – Rà soát (Bước 1):** AI đo trang và nêu ba vấn đề kèm số liệu: trang không có `nav` và không có liên kết `a` nào (thứ tự Tab chỉ đi qua 6 nút); 8 phần tử có tỷ lệ tương phản dưới 4,5:1 (nút chữ trắng trên `#e6321f` đạt 4,33:1, nhãn giảm giá `#d12a1a` trên `#fde8e5` đạt 4,39:1); chưa có hover và `transition`. AI đề xuất đổi màu đạt chuẩn WCAG AA và dẫn các mục liên quan trong giáo trình (HTML ngữ nghĩa, Box Model, Flexbox, Grid).

**Prompt 5 – Header và chân trang (Bước 2):** AI soạn khối HTML gồm thanh thông tin, logo và tên cửa hàng, ô tìm kiếm, giỏ hàng, menu `nav`, đường dẫn, chân trang 3 cột, logo SVG và gợi ý một số tên cửa hàng. Các liên kết dùng `href="#"` vì chưa có trang đích.

**Prompt 6 – Các khối CSS (Bước 3, 4, 7):** AI đưa các khối CSS cho header, menu, chân trang, đổi ba biến màu (`--primary` sang `#cc2a1a`, `--primary-dark` sang `#a82012`, `--sale` sang `#b92518`), chỉnh `padding`, viền, bo góc, cỡ chữ giá của thẻ, và thêm hover, `transition`, `:focus-visible`. Mỗi chỗ có phần "chỗ cũ, thay mới, để làm gì".

**Prompt 7 – Lỗi nhãn giảm giá (Bước 8):** Đề xuất đầu tiên của AI là `margin-left: auto` cho `.tag`. Sau phản hồi của sinh viên, AI đo bề rộng dòng và chỉ ra ở 980 px dòng rộng khoảng 269 px, hơi thiếu chỗ, còn ở 390 px chỉ rộng khoảng 208 px nên không thể vừa. AI đề xuất giảm `gap`, `padding` của `.options li` và `min-width` của `.options__name`.

## 5. Kiểm tra và điều chỉnh

### Buổi 1 (Chương 1)

**Nhiệm vụ 2 – Đối chiếu với website thật** (sinh viên tự khảo sát trước, sau đó đối chiếu từng nhận xét của AI):
- *Giữ lại các ý đúng:* menu chia sẵn cho chó và mèo; có breadcrumb; có phân trang (khoảng 110 trang); không có bộ lọc và sắp xếp; thẻ sản phẩm có khoảng giá và nhãn giảm giá; nhóm sản phẩm chia theo loại; trang chi tiết có chọn loại, số lượng, nút "Thêm vào giỏ hàng" và sản phẩm tương tự; chỉ có một ảnh sản phẩm; không có nút "Mua ngay"; bài tin tức cũ.
- *Điều chỉnh:* AI nói chưa thấy ô tìm kiếm hiển thị sẵn, nhưng trên website thật ô tìm kiếm nằm ở đầu trang. AI nói giá chỉ hiện dạng khoảng, nhưng thực tế giá đổi theo loại đã chọn. AI nói "Sản phẩm tương tự" lẫn đồ chó trong trang đồ mèo, nhưng thực tế gặp chiều ngược lại (trang đồ chó có gợi ý đồ mèo).
- *Loại bỏ vì không đúng với website thật:* gợi ý tự động và lịch sử khi tìm kiếm; mã giảm giá sản phẩm trong giỏ; nhận xét khối "theo giống" ở trang chủ không khớp nội dung (thực tế khối đã chia theo chó và mèo); số sản phẩm mỗi trang là 12 (thực tế tùy trang); nút "Thêm vào giỏ" của sản phẩm có biến thể dẫn sang trang khác (thực tế không chuyển trang).
- *Bổ sung của sinh viên:* kết quả tìm kiếm chia "Bài viết" và "Sản phẩm", bài viết hiện trước sản phẩm, nhiều bài chỉ có ảnh "NO THUMBNAIL"; sau khi thêm vào giỏ có khung giỏ nhỏ hiện ngay, trang giỏ chưa thấy phí vận chuyển; breadcrumb ở trang chi tiết có một dấu chấm trống; nhãn "-17%" ở mục sản phẩm tương tự đứng cạnh khoảng giá nên chưa rõ giảm cho loại nào; chưa thấy ghi chú về VAT.

**Nhiệm vụ 3 – Kiểm tra mã nguồn:**
- Mở trang bằng Chrome, dùng DevTools kiểm tra ở 375px, 768px, 960px và 1280px: ảnh hiển thị đủ, bố cục đổi cột đúng (1, 2, 3 cột), không bị cuộn ngang.
- *Điểm sinh viên tự phát hiện và sửa:* khoảng trống lớn giữa tên và giá ở 768px và 1280px. Sinh viên dùng DevTools tìm ra nguyên nhân là `min-height: 2.6em` của `.card__title`, thử tắt thuộc tính, kiểm tra ở 960px (cỡ hẹp nhất của bố cục 3 cột) thấy tên vẫn một dòng và giá, nút các thẻ vẫn thẳng hàng, nên đã xóa dòng này trong `css/style.css`. Hạn chế đã biết: nếu sau này có tên sản phẩm dài xuống hai dòng, giá của các thẻ cạnh nhau có thể lệch.
- *Điều cần lưu ý:* giá và tên sản phẩm trong các thẻ mẫu chỉ là dữ liệu mẫu; ảnh sản phẩm là SVG tự tạo, không dùng ảnh của Pet Mart.

### Buổi 2 (Chương 2)

**Bước 1 – Rà soát:** không đưa kết quả của AI vào bảng ngay mà tự tái hiện từng vấn đề trên trình duyệt (không có menu và liên kết, tỷ lệ tương phản, không phản hồi khi rê chuột) và chụp ảnh minh chứng.

**Bước 2 – HTML:**
- Tự chọn tên cửa hàng "Pet Nhà Mình" trong các tên được gợi ý; giữ địa chỉ, hotline, email ở dạng dữ liệu mẫu.
- Dùng `href="#"` thay vì liên kết tới tệp chưa có để tránh lỗi 404; mỗi thẻ sản phẩm chỉ có một liên kết (nằm trong `h3`).
- Kiểm tra bằng phím Tab và Nu Html Checker. Lần đầu nhập nhầm đường dẫn tệp thay vì nội dung nên công cụ báo hai lỗi sai; sau khi tải tệp `index.html` lên, kết quả là không lỗi, không cảnh báo.

**Bước 3–4 – CSS và Box Model:** tự áp dụng từng chỗ sửa bằng cách tìm trong `style.css`, tải lại và kiểm tra ở 1366 px và 390 px. Xem Box Model của thẻ trong DevTools (margin 0, border 1 px, padding 16 px).

**Bước 5–6 – Flexbox và Grid:** tự thử đổi giá trị `justify-content`, `align-items`, `gap`, `grid-template-columns`, `object-fit` trong DevTools và ghi lại quan sát. Khi tìm `repeat` từng chọn nhầm phần tử chân trang thay vì danh sách sản phẩm, sau đó chọn lại đúng `ul.product-grid`.

**Bước 7 – Hover/focus:** kiểm tra bằng chuột và phím Tab; chụp trạng thái hover của thẻ và trạng thái focus (khung xanh) của nút.

**Bước 8 – Điểm sinh viên kiểm tra và tự sửa:** ở 980 px, nhãn "Giảm 17%" rớt xuống dòng riêng và nằm sát trái. Đề xuất đầu của AI (`margin-left: auto`) được thử nghiệm và chỉ chuyển nhãn sang sát phải, nhãn vẫn xuống dòng, nên sinh viên báo lại. Sau khi AI đo bề rộng dòng, sinh viên áp dụng việc giảm `gap` (8 px xuống 6 px), `padding` (`4px 8px` xuống `4px 6px`) và `min-width` (3,2em xuống 2,6em), rồi kiểm tra lại ở 980 px (nhãn cùng dòng) và 390 px (nhãn vẫn xuống dòng, nằm sát phải). Giữ nguyên hành vi ở 390 px vì dòng chỉ rộng khoảng 208 px, không đủ chỗ. Hạn chế đã biết: nếu sau này giá hoặc tên gói dài hơn, nhãn có thể lại xuống dòng ở 980 px.

## 6. Phần tôi hiểu và có thể giải thích

### Buổi 1 (Chương 1)
- **`<ul>`, `<li>`, `<article>`:** danh sách sản phẩm là một `ul`, mỗi sản phẩm là một `li` chứa một `article` (một thẻ sản phẩm độc lập).
- **`<del>`:** đánh dấu nội dung bị thay thế (giá gốc), mặc định hiển thị gạch ngang.
- **`<button>`:** nút thao tác; có `type="button"` để không gửi form.
- **`display: grid` và `grid-template-columns`:** chia khu vực sản phẩm thành các cột; `repeat(3, 1fr)` là 3 cột bằng nhau.
- **`@media (min-width: ...)`:** khi màn hình đủ rộng thì áp dụng quy tắc bên trong, nhờ đó cùng một trang đổi cách hiển thị giữa điện thoại, máy tính bảng và máy tính.
- **`display: flex`, `flex-direction: column` và `margin-top: auto`:** xếp nội dung thẻ theo chiều dọc và đẩy nút xuống cuối thẻ để các nút thẳng hàng dù nội dung dài ngắn khác nhau.
- **`:root` và biến CSS (`--primary`, `--sale`...):** khai báo màu dùng chung, đổi một chỗ là đổi toàn trang.
- **`min-height` của `.card__title`:** đặt chiều cao tối thiểu cho tên sản phẩm. Dòng này tạo khoảng trống khi tên chỉ một dòng nên tôi đã bỏ; đánh đổi là nếu tên dài hai dòng thì giá các thẻ có thể lệch.

### Buổi 2 (Chương 2)
- **`<nav>` và `aria-label`:** đánh dấu vùng điều hướng. Trang có hai `nav` (menu chính và đường dẫn) nên mỗi cái có `aria-label` riêng để trình đọc màn hình phân biệt.
- **`<article>` khác `<div>`:** `article` là một đơn vị nội dung độc lập có ý nghĩa (một sản phẩm), còn `div` chỉ là khối trung tính không mang ý nghĩa.
- **`alt` của ảnh:** giúp người dùng trình đọc màn hình biết ảnh thể hiện gì và hiển thị thay cho ảnh khi ảnh lỗi. Logo dùng `alt=""` vì tên cửa hàng đã có chữ bên cạnh.
- **Margin và padding:** padding là khoảng đệm bên trong viền (`.card` có `padding: 16px`), margin là khoảng cách bên ngoài viền (`.price` có `margin: 4px 0 2px`). Khoảng cách giữa các thẻ do `gap` của lưới đảm nhiệm nên `.card` không cần margin.
- **`box-sizing: border-box`:** chiều rộng đã gồm cả padding và border nên thêm đệm hoặc viền không làm phần tử phình ra.
- **`justify-content`, `align-items`, `gap`, `flex-wrap`:** `justify-content` căn theo trục chính (ngang khi xếp hàng), `align-items` theo trục phụ (dọc), `gap` tạo khoảng cách giữa các phần tử, `flex-wrap` cho phép phần tử xuống dòng khi hết chỗ.
- **Grid khác Flexbox:** Flexbox sắp xếp theo một chiều, Grid chia theo hai chiều (hàng và cột). Nếu xóa `display: grid` khỏi danh sách sản phẩm thì các thẻ xếp thành một cột dọc và mất khoảng cách vì `gap` không còn tác dụng.
- **`:hover` khác `:focus-visible`:** hover do chuột đi qua, focus-visible hiện khung khi dùng bàn phím (phím Tab); không nên bỏ khung focus vì người dùng bàn phím sẽ không biết mình đang ở đâu.
- **`transition`:** làm thuộc tính (màu, bóng, vị trí) chuyển dần trong 0,2 giây thay vì đổi đột ngột.
- **Tỷ lệ tương phản 4,5:1:** mức tối thiểu của WCAG AA cho chữ thường, giúp người có thị lực kém đọc được; nút cũ chỉ đạt 4,33:1 nên đã đổi sang màu tối hơn.
- **`margin-left: auto` trong Flexbox:** đẩy phần tử sang mép phải của hàng. Dùng cho giỏ hàng ở header và nhãn giảm giá, nhưng không ngăn phần tử xuống dòng khi hết chỗ.
