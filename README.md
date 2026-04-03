# Bài thực hành: Thiết lập và Khai thác GraphQL API với Bagisto Headless

**Họ tên:** Nguyễn Văn Danh  
**MSSV:** 23810310136
**Ngày thực hiện:** 03/04/2026  

## Ảnh minh chứng

### 1. Danh sách sản phẩm trong Admin


### 2. Query 3 - Lọc sản phẩm + Console log


### 3. Giao diện Frontend


## Trả lời câu hỏi

### Câu 1: So sánh lưu lượng dữ liệu REST API vs GraphQL

Sự khác biệt lớn nhất nằm ở hiện tượng Over-fetching (lấy dư dữ liệu):

REST API: Khi gọi một endpoint (ví dụ: /products/1), server trả về toàn bộ cấu trúc dữ liệu được định nghĩa sẵn. Nếu em chỉ cần "tên sản phẩm" nhưng API trả về cả mô tả, hình ảnh, đánh giá... thì dung lượng payload sẽ lớn, gây lãng phí băng thông và làm chậm tốc độ tải trang.

GraphQL: Cho phép em chỉ định chính xác các trường cần thiết (ví dụ: product { name }). Server chỉ trả về đúng những gì được yêu cầu. Điều này giúp tối ưu hóa payload, giảm thiểu kích thước gói tin truyền qua mạng, đặc biệt hiệu quả trên các thiết bị di động hoặc môi trường mạng yếu.

### Câu 2: Query hay Mutation để thay đổi giá sản phẩm?
Để thay đổi giá của một sản phẩm, em phải sử dụng Mutation.

Giải thích:

Query trong GraphQL được thiết kế cho các hoạt động đọc dữ liệu (tương đương GET trong REST) và không làm thay đổi trạng thái của server.

Mutation được sử dụng cho các hoạt động ghi hoặc thay đổi dữ liệu (tương đương POST, PUT, DELETE trong REST). Việc thay đổi giá là một hành động cập nhật cơ sở dữ liệu, do đó cần dùng Mutation để đảm bảo tính đúng đắn về mặt kiến trúc và giúp server nhận biết đây là một tác vụ có tính thay đổi (side-effect).






## Link video demo
[Link video YouTube hoặc file đính kèm]
