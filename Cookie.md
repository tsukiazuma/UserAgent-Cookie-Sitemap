## Người thực hiện: Trần Ngọc Nam
## Ngày thực hiện: 11/5/2022

# Mục lục:
1. [Cookie là gì?](#1)
2. [Thuật ngữ](#2)
3. [Ứng dụng của cookie](#3)
4. [Những rủi ro mà Cookie mang lại](#4)
5. [Cookie và Quyền riêng tư](#5)
   1. [Quy định chung về bảo mật thông tin (GDPR) của Liên minh châu Âu](#6)
   2. [Hiển thị thông tin cookie](#7)

## Cookie là gì?<a name='1'></a>
- Cookie là một bộ nhắc nhỏ mà website lưu trữ ở trên máy tính của bạn có thể định danh cho bạn.
-  Cookie được dùng với mục đích:
   -  Lưu trữ phiên đăng nhập nhằm phục vụ cho mục đích xác thực với website, duy trì trạng thái đăng nhập.
   -  Dùng để ghi nhớ thông tin trạng thái, ghi nhớ hoạt động người dùng thực hiện trong quá trình truy cập và duyệt một trang web.
   -  Dùng để lưu lại các thông tin khác mà người dùng nhập hay điền vào trang web như tên, địa chỉ, email, v.v...
  
## Thuật ngữ:<a name='2'></a>
- Session cookie:
  - Chỉ tồn tại trong bộ nhớ tạm thời khi người dùng duyệt web.
  - Thông thường, trình duyệt sẽ xóa bỏ cookie khi người dùng ngưng phiên duyệt web.
  - Không có thời hạn có hiệu lực (yếu tố để phân biệt).
- Persistent cookie:
  - Hết hiệu lực sau một thời điểm nào đó hoặc sau một khoảng thời gian nào đó được ấn định trước.
  - Trong thời gian hiệu lực, thông tin mà persistent cookie lưu lại sẽ được gửi đến máy chủ của website mà người dùng truy cập mỗi khi họ duyệt trang đó, hoặc khi họ truy cập một nguồn tài nguyên thuộc website thông qua một website khác
- Secure cookie:
  - Chỉ có thể được gửi và nhận qua một kết nối được mã hoá (HTTPS).
  - Không được gửi và nhận qua một kết nối không mã hoá (HTTP).
- Http-only cookie: không được truy cập bởi các giao diện lập trình ứng dụng (API) phía người dùng (client-side APIs) như JavaScript.
- Same-site cookie: chỉ được gửi qua các yêu cầu xuất phát cùng một tên miền mục tiêu.
- Third-party cookie:
  - Thuộc một tên miền khác với tên miền trên thanh địa chỉ.
  - Thường gặp trong trường hợp một website hiển thị thông tin từ các website khác (banner quảng cáo từ website khác).
- Supercookie:
  - Xuất phát từ các tên miền ở tầng cao nhất (ví dụ như.com) hay các hậu tố công cộng (public suffix) như.co.uk.
  - Là một mối nguy hiểm tiềm tàng vì các supercookie có thể được dùng để nguỵ trang một yêu cầu không hợp pháp trông như một yêu cầu hợp pháp từ người dùng.
- Zombie cookie: là loại bị xoá đi.

## Ứng dụng của cookie:<a name='3'></a>
- Quản lý phiên chạy bằng cách ghi nhớ trạng thái của người dùng. Chúng làm cho web tiện lợi hơn, người dùng có thể truy cập vào web nhanh hơn không phải nhập lại các thông tin nhiều lần.
- Cá nhân hoá kinh nghiệm người dùng. Website dùng cookie để ghi nhớ các lựa chọn ưa thích mà người dùng thiết lập khi tương tác với website trước đó, ví dụ: màu sắc trang nền của website, ngôn ngữ mặc định.
- Theo dõi hoạt động.  Các trang web dùng cookie để ghi lại và phân tích thói quen duyệt web của người dùng.
  
## Những rủi ro mà Cookie mang lại:<a name='4'></a>
- Cookie ảnh hưởng tới sự riêng tư của người dùng.
- Cookie có thể làm tăng nguy cơ mất thông tin đăng nhập.

## Cookie và Quyền riêng tư:<a name='5'></a>

### Quy định chung về bảo mật thông tin (GDPR) của Liên minh châu Âu:<a name='6'></a>
- GDPR yêu cầu các công ty phải có sự chấp thuận của người dùng châu Âu về việc các website này dùng cookie để thu thập thông tin về hoạt động người dùng.

### Hiển thị thông tin cookie:<a name='7'></a>
- Thông báo về việc dùng cookie: Khi người dùng truy cập một trang web, một tin nhắn sẽ được hiển thị để thông báo cho người dùng về việc trang web đó có sử dụng cookie để thu thập thông tin duyệt web của người dùng.
- Chính sách cookie hoặc Chính sách riêng tư:
  - Thường chứa nhiều thông tin hơn về các cookie mà một trang web sử dụng và thường dưới dạng văn bản dài, hiển thị như một trang tin.
  - Các Chính sách cookie hoặc Chính sách riêng tư này cũng thường bao gồm các hướng dẫn để người dùng có thể chọn cho phép hay từ chối một hay nhiều loại cookie.
- Chức năng điều chỉnh cookie: Các trang web cũng có thể có chức năng điều chỉnh cookie để người dùng có thể lựa chọn cho phép hay từ chối loại cookie họ muốn.