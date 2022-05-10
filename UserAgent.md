## Người thực hiện: Trần Ngọc Nam
## Ngày thực hiện: 9/5/2022

# Mục lục:
1. [Khái niệm](#1)
2. [Dùng trong HTTP](#2)
   1. [Định dạng cho trình duyệt web do con người vận hành](#3)
   2. [Định dạng cho các tác nhân tự động (bot)](#4)
   3. [Giả mạo tác nhân người dùng](#5)
   4. [Phát hiện tác nhân người dùng](#6)
   5. [Ký hiệu độ mạnh mã hóa](#7)
   6. [Ngừng sử dụng tiêu đề tác nhân người dùng](#8) 

## Khái niệm:<a name='1'></a>
- Trong máy tính, tác nhân người dùng là các phần mềm, hoạt động thay mặt cho người dùng, phần mềm này "truy xuất, hiển thị và tạo điều kiện cho người dùng cuối tương tác với nội dung Web". Do đó, tác nhân người dùng là một loại tác nhân phần mềm đặc biệt.
- Ví dụ như trình duyệt web và trình đọc email. Thông thường, tác nhân người dùng hoạt động như một máy khách trong hệ thống máy khách-máy chủ. Trong một số ngữ cảnh, chẳng hạn như trong Giao thức khởi đầu phiên (SIP), thuật ngữ tác nhân người dùng đề cập đến cả hai điểm cuối của một phiên giao tiếp.
- Khi tác nhân phần mềm hoạt động trong một giao thức mạng, nó thường xác định chính nó, loại ứng dụng, hệ điều hành, kiểu thiết bị, nhà cung cấp phần mềm hoặc bản sửa đổi phần mềm, bằng cách gửi một chuỗi nhận dạng đặc trưng cho đồng nghiệp điều hành của nó.

## Dùng trong HTTP:<a name='2'></a>
- Trong HTTP, chuỗi User-Agent thường được sử dụng để thương lượng nội dung, trong đó máy chủ gốc chọn nội dung hoặc thông số hoạt động phù hợp cho phản hồi.
- Chuỗi User-Agent là một trong những tiêu chí mà trình thu thập dữ liệu Web có thể bị loại trừ khỏi việc truy cập vào các phần nhất định của trang web bằng Tiêu chuẩn loại trừ rô bốt (tệp robots.txt).
- Như với nhiều tiêu đề yêu cầu HTTP khác, thông tin trong "User-Agent" góp phần vào thông tin mà máy khách gửi đến máy chủ, vì chuỗi này có thể khác nhau giữa các người dùng.
  
### Định dạng cho trình duyệt web do con người vận hành:<a name='3'></a>
- Định dạng của chuỗi User-Agent trong HTTP là danh sách các mã thông báo sản phẩm (từ khóa) với các nhận xét tùy chọn.
- Các phần của chuỗi này như sau:
  - Tên và phiên bản sản phẩm (WikiBrowser / 1.0)
  - Công cụ bố trí và phiên bản (Gecko / 1.0)
- Ví dụ: <code>Mozilla/5.0 (iPad; U; CPU OS 3_2_1 like Mac OS X; en-us) AppleWebKit/531.21.10 (KHTML, like Gecko) Mobile/7B405</code>.
  - Mozilla / 5.0: Trước đây được sử dụng để chỉ khả năng tương thích với công cụ kết xuất Mozilla.
  - (iPad; U; CPU OS 3_2_1 như Mac OS X; en-us): Chi tiết về hệ thống mà trình duyệt đang chạy.
  - AppleWebKit / 531.21.10: Nền tảng mà trình duyệt sử dụng.
  - (KHTML, như Gecko): Thông tin chi tiết về nền tảng trình duyệt.
  - Mobile / 7B405: Điều này được trình duyệt sử dụng để chỉ ra các cải tiến cụ thể có sẵn trực tiếp trong trình duyệt hoặc thông qua các bên thứ ba.
- Trước khi chuyển sang cơ sở mã Chromium, Opera là trình duyệt web được sử dụng rộng rãi nhất không có chuỗi User-Agent bằng "Mozilla". Ngày 15/7/2013, Chuỗi User-Agent của Opera bắt đầu bằng "Mozilla / 5.0" và để tránh gặp phải các quy tắc máy chủ kế thừa, không còn bao gồm từ "Opera" (thay vào đó sử dụng chuỗi "OPR" để biểu thị Opera phiên bản).

### Định dạng cho các tác nhân tự động (bot):<a name='4'></a>
- Các công cụ thu thập dữ liệu web tự động có thể sử dụng một biểu mẫu đơn giản, trong đó một lĩnh vực quan trọng là thông tin liên lạc trong trường hợp có vấn đề. Theo quy ước, từ "bot" được bao gồm trong tên của tác nhân.
- Ví dụ: <code>Googlebot/2.1 (+http://www.google.com/bot.html)</code>
- Các tác nhân tự động phải tuân theo các quy tắc trong một tệp đặc biệt có tên "robots.txt".
  
### Giả mạo tác nhân người dùng:<a name='5'></a>
- Các trình duyệt khác nhau có tính năng che giấu hoặc giả mạo nhận dạng của chúng để buộc một số nội dung phía máy chủ nhất định.
- Ví dụ: trình duyệt Android tự nhận mình là Safari (trong số những thứ khác) để hỗ trợ khả năng tương thích.
- Các chương trình máy khách HTTP khác, như trình quản lý tải xuống và trình duyệt ngoại tuyến, thường có khả năng thay đổi chuỗi User-Agent.
- Kết quả của việc giả mạo User-Agent dùng có thể là số liệu thống kê thu thập được về việc sử dụng trình duyệt Web là không chính xác.

### Phát hiện tác nhân người dùng:<a name='6'></a>
- Phát hiện tác nhân người dùng là thực hành các trang web hiển thị nội dung khác nhau hoặc điều chỉnh khi xem với một số tác nhân người dùng nhất định. Phát hiện tác nhân người dùng được coi là hoạt động kém hiệu quả, vì nó khuyến khích thiết kế dành riêng cho trình duyệt và phạt các trình duyệt mới với nhận dạng tác nhân người dùng không được công nhận. Thay vào đó, W3C khuyên bạn nên tạo đánh dấu HTML tiêu chuẩn, cho phép hiển thị chính xác trong càng nhiều trình duyệt càng tốt và kiểm tra các tính năng trình duyệt cụ thể thay vì các phiên bản hoặc thương hiệu trình duyệt cụ thể.
- Các trang web dành cho hiển thị bằng điện thoại di động thường dựa vào phát hiện tác nhân người dùng, vì các trình duyệt di động thường khác nhau rất nhiều.

### Ký hiệu độ mạnh mã hóa:<a name='7'></a>
- Các trình duyệt web được tạo ra ở Hoa Kỳ, chẳng hạn như Netscape Navigator và Internet Explorer, trước đây đã sử dụng các chữ cái U, I và N để chỉ định cường độ mã hóa trong chuỗi tác nhân người dùng.
- Năm 1996, Hoa Kỳ cho phép mã hóa với các khóa dài hơn 40 bit, các nhà cung cấp đã vận chuyển các phiên bản trình duyệt khác nhau với các thế mạnh mã hóa khác nhau.
- "U" là viết tắt của "USA" (đối với phiên bản có mã hóa 128 bit).
- "I" là viết tắt của "International" - trình duyệt có mã hóa 40 bit và có thể được sử dụng ở bất cứ đâu trên thế giới.
- Và "N" là viết tắt (trên thực tế) cho "None" (không có mã hóa).
- Sau khi dỡ bỏ các hạn chế xuất khẩu, hầu hết các nhà cung cấp đều hỗ trợ mã hóa 256 bit.

### Ngừng sử dụng tiêu đề tác nhân người dùng:<a name='8'></a>
- Năm 2020, Google đã thông báo loại bỏ hỗ trợ cho chuỗi User-Agent trong trình duyệt Google Chrome.
- Google tuyên bố rằng một tính năng mới gọi là Client Hints sẽ thay thế chức năng của chuỗi User-Agent.