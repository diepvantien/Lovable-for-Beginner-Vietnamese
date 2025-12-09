# Module 10: Gỡ lỗi và Kiểm thử Ứng dụng của Bạn

**Mục tiêu:** Học cách tìm và sửa lỗi, và kiểm thử ứng dụng của bạn một cách kỹ lưỡng

**Thời gian ước tính:** 30-40 phút

---

## 🎯 Bạn Sẽ Học Được Gì Trong Module Này

Vào cuối module này, bạn sẽ:
- Hiểu cách đọc và diễn giải các thông báo lỗi
- Biết cách sử dụng Chat Mode để gỡ lỗi
- Thành thạo việc sử dụng Lịch sử (History) để hoàn tác các thay đổi
- Học cách chỉnh sửa tin nhắn để sửa chữa sai lầm
- Hiểu các chiến lược kiểm thử
- Có khả năng gỡ lỗi các vấn đề phổ biến
- Biết cách kiểm thử ứng dụng của bạn một cách kỹ lưỡng

---

## 📖 Bài học 1: Hiểu về Thông báo Lỗi

### Thông báo Lỗi là gì?

**Thông báo lỗi (Error messages)** là cách Lovable cho bạn biết có điều gì đó không ổn. Ban đầu chúng có vẻ đáng sợ, nhưng thực ra chúng là những manh mối hữu ích!

### Các Loại Lỗi Phổ Biến

#### 1. Lỗi Build (Build Errors)

**Chúng trông như thế nào:**
- Văn bản màu đỏ hoặc chỉ báo lỗi
- Các thông báo như "Failed to build" (Không thể build) hoặc "Error in code" (Lỗi trong mã)
- Số dòng hoặc tên tệp

**Ý nghĩa của chúng:**
- Có vấn đề gì đó trong mã của bạn
- Thường là lỗi cú pháp hoặc thiếu một phần nào đó

**Ví dụ:**
```
Error: Missing closing bracket in Header.jsx line 15
```

**Cần làm gì:**
1. Đọc kỹ thông báo lỗi
2. Ghi lại tên tệp và số dòng
3. Hỏi Chat Mode: "Lỗi này có nghĩa là gì và làm thế nào để sửa nó?"
4. Hoặc yêu cầu Agent Mode: "Sửa lỗi trong Header.jsx dòng 15"

#### 2. Lỗi Runtime (Runtime Errors)

**Chúng trông như thế nào:**
- Lỗi xảy ra khi ứng dụng của bạn đang chạy
- Thông báo trong console của trình duyệt
- Mọi thứ không hoạt động như mong đợi

**Ý nghĩa của chúng:**
- Ứng dụng của bạn đã build thành công, nhưng có gì đó bị hỏng khi sử dụng
- Thường là lỗi logic hoặc thiếu kết nối

**Ví dụ:**
```
Error: Cannot read property 'name' of undefined
```

**Cần làm gì:**
1. Kiểm tra hành động nào đã gây ra lỗi
2. Sử dụng Chat Mode để điều tra: "Tại sao lỗi này lại xảy ra?"
3. Sửa vấn đề cơ bản

#### 3. Lỗi Kết nối (Connection Errors)

**Chúng trông như thế nào:**
- Thông báo "Failed to connect" (Không thể kết nối)
- Lỗi API
- Vấn đề kết nối cơ sở dữ liệu

**Ý nghĩa của chúng:**
- Không thể tiếp cận dịch vụ (cơ sở dữ liệu, API, v.v.)
- Thường là vấn đề cấu hình

**Ví dụ:**
```
Error: Failed to connect to database
```

**Cần làm gì:**
1. Kiểm tra xem backend đã được bật chưa
2. Xác minh các khóa API đã được thiết lập chưa
3. Hỏi Chat Mode: "Tại sao tôi không thể kết nối với cơ sở dữ liệu?"

### Cách Đọc Thông báo Lỗi

**Bước 1: Đừng Hoảng Loạn!**
- Lỗi là bình thường
- Chúng là manh mối, không phải thất bại
- Mọi lập trình viên đều gặp lỗi

**Bước 2: Đọc Toàn bộ Thông báo**
- Thông báo lỗi thường cho bạn biết điều gì sai
- Tìm tên tệp và số dòng
- Ghi chú bất kỳ chi tiết cụ thể nào

**Bước 3: Hiểu Ngữ cảnh**
- Bạn đang làm gì khi nó xảy ra?
- Bạn đang xây dựng tính năng gì?
- Gần đây có thay đổi gì không?

**Bước 4: Sử dụng Chat Mode**
```
[Dán thông báo lỗi vào đây]

Bạn có thể giúp tôi hiểu lỗi này có nghĩa là gì và cách sửa nó không?
```

**💡 Mẹo cho người mới bắt đầu:** Thông báo lỗi là bạn của bạn! Chúng cho bạn biết chính xác điều gì sai. Hãy học cách đọc chúng, và việc gỡ lỗi sẽ trở nên dễ dàng hơn nhiều.

---

## 📖 Bài học 2: Sử dụng Chat Mode để Gỡ lỗi

### Tại sao Chat Mode lại Hoàn hảo cho việc Gỡ lỗi

Chat Mode rất lý tưởng để gỡ lỗi vì:
- ✅ Nó điều tra mà không thực hiện thay đổi
- ✅ Nó giải thích điều gì sai
- ✅ Nó đề xuất các giải pháp
- ✅ Nó giúp bạn hiểu vấn đề

### Quy trình Gỡ lỗi với Chat Mode

#### Bước 1: Mô tả Vấn đề

**Hãy cụ thể:**
```
Form liên hệ không gửi đi được. Khi tôi nhấp vào gửi, không có gì xảy ra và tôi không thấy thông báo lỗi nào.
```

**Không hữu ích:**
```
Nó bị hỏng
```

#### Bước 2: Cung cấp Ngữ cảnh

**Bao gồm thông tin liên quan:**
```
Tôi vừa thêm một form liên hệ vào trang chủ. Nó có các trường tên, email và tin nhắn. Khi người dùng nhấp vào gửi, không có gì xảy ra. Việc xác thực form có vẻ hoạt động (hiển thị lỗi cho các trường trống), nhưng việc gửi đi thì không hoạt động.
```

#### Bước 3: Để Chat Mode Điều tra

Chat Mode sẽ:
- Xem xét mã của bạn
- Kiểm tra thiết lập form
- Xác định vấn đề
- Giải thích điều gì sai

#### Bước 4: Nhận Giải pháp

Chat Mode sẽ:
- Giải thích vấn đề
- Đề xuất cách sửa nó
- Cung cấp một kế hoạch
- Sau đó bạn có thể thực hiện nó

### Ví dụ về Cuộc hội thoại Gỡ lỗi

**Bạn (Chat Mode):**
```
Trang đăng nhập của tôi không hoạt động. Khi tôi nhập thông tin xác thực và nhấp vào đăng nhập, không có gì xảy ra. Bạn có thể giúp tôi gỡ lỗi này không?
```

**Chat Mode:**
- Điều tra mã đăng nhập
- Kiểm tra thiết lập xác thực
- Tìm kiếm các vấn đề

**Phản hồi của Chat Mode:**
```
Tôi đã tìm thấy vấn đề. Form đăng nhập không được kết nối với backend xác thực. Form gửi đi, nhưng không có trình xử lý nào để xử lý nó.

Đây là những gì cần phải sửa:
1. Kết nối form với dịch vụ xác thực
2. Thêm xử lý lỗi cho thông tin xác thực sai
3. Thêm trạng thái đang tải trong khi đăng nhập
4. Chuyển hướng sau khi đăng nhập thành công

Bạn có muốn tôi thực hiện sửa lỗi này không?
```

**Bạn:**
```
Vâng, hãy thực hiện sửa lỗi
```

**Chat Mode:**
- Cung cấp kế hoạch hoặc chuyển sang Agent Mode
- Sửa vấn đề

### Gỡ lỗi Nâng cao với Chat Mode

#### Gỡ lỗi các Vấn đề Phức tạp

**Ví dụ:**
```
Danh sách công việc của tôi không hiển thị các công việc. Tôi có thể thấy các công việc trong cơ sở dữ liệu, nhưng chúng không hiển thị trên trang. Bạn có thể điều tra tại sao không?
```

**Chat Mode sẽ:**
- Kiểm tra truy vấn cơ sở dữ liệu
- Kiểm tra component hiển thị
- Kiểm tra luồng dữ liệu
- Xác định vấn đề nằm ở đâu

#### Gỡ lỗi Vấn đề Hiệu suất

**Ví dụ:**
```
Trang của tôi tải rất chậm. Bạn có thể giúp tôi xác định nguyên nhân gây chậm không?
```

**Chat Mode sẽ:**
- Kiểm tra các hình ảnh lớn
- Tìm kiếm mã không hiệu quả
- Đề xuất tối ưu hóa

#### Gỡ lỗi Vấn đề Thiết kế

**Ví dụ:**
```
Trên thiết bị di động, menu điều hướng bị chồng lên nội dung. Bạn có thể giúp tôi sửa thiết kế responsive không?
```

**Chat Mode sẽ:**
- Kiểm tra CSS và bố cục
- Xác định các vấn đề responsive
- Đề xuất các bản sửa lỗi

**💡 Mẹo cho người mới bắt đầu:** Chat Mode giống như một đối tác gỡ lỗi. Hãy sử dụng nó thoải mái khi mọi thứ không hoạt động!

---

## 📖 Bài học 3: Sử dụng Lịch sử (History) để Hoàn tác Thay đổi

### Lịch sử là gì?

**Lịch sử (History)** là bản ghi của tất cả các thay đổi được thực hiện đối với dự án của bạn. Nó giống như một cỗ máy thời gian - bạn có thể quay lại bất kỳ phiên bản nào trước đó!

### Tại sao Lịch sử lại Quan trọng

- ✅ **Lưới an toàn** - Hoàn tác sai lầm dễ dàng
- ✅ **Thử nghiệm tự do** - Thử mọi thứ mà không sợ hãi
- ✅ **So sánh các phiên bản** - Xem những gì đã thay đổi
- ✅ **Khôi phục công việc** - Quay lại trạng thái hoạt động tốt

### Cách Truy cập Lịch sử

#### Bước 1: Tìm Lịch sử

1. Tìm **"History"** hoặc **"Version History"** trong dự án của bạn
2. Thường ở:
   - Menu trên cùng
   - Thanh bên
   - Cài đặt dự án
   - Hoặc hỏi Lovable: "Show me the project history" (Cho tôi xem lịch sử dự án)

#### Bước 2: Xem Lịch sử

Bạn sẽ thấy:
- **Dòng thời gian (Timeline)** - Các thay đổi được liệt kê theo trình tự thời gian
- **Mô tả** - Những gì đã thay đổi trong mỗi phiên bản
- **Dấu thời gian** - Khi nào các thay đổi được thực hiện
- **Xem trước** - Xem mỗi phiên bản trông như thế nào

#### Bước 3: Hiểu Dòng thời gian

**Gần đây nhất ở trên cùng:**
- Các thay đổi mới nhất trước
- Các thay đổi cũ hơn ở dưới
- Dễ dàng xem sự tiến triển

### Cách Hoàn tác về Phiên bản Trước

#### Phương pháp 1: Hoàn tác từ Lịch sử

1. **Mở Lịch sử**
2. **Tìm phiên bản** bạn muốn quay lại
3. **Xem trước nó** - Nhấp để xem nó trông như thế nào
4. **Nhấp "Revert"** hoặc "Restore"
5. **Xác nhận** - Bạn sẽ được yêu cầu xác nhận
6. **Dự án của bạn hoàn tác** - Quay lại phiên bản đó

#### Phương pháp 2: Yêu cầu Hoàn tác

```
Revert to the version before I added the navigation menu
(Hoàn tác về phiên bản trước khi tôi thêm menu điều hướng)
```

hoặc

```
Go back to yesterday's version
(Quay lại phiên bản ngày hôm qua)
```

#### Phương pháp 3: Hoàn tác Các thay đổi Cụ thể

```
Undo the last change I made
(Hoàn tác thay đổi cuối cùng tôi đã thực hiện)
```

hoặc

```
Remove the feature I just added
(Xóa tính năng tôi vừa thêm)
```

### Ví dụ Quy trình: Mắc lỗi → Hoàn tác → Lặp lại

**Kịch bản:** Bạn đang xây dựng trang chủ và thực hiện một thay đổi làm hỏng bố cục.

#### Bước 1: Thực hiện Thay đổi

Bạn yêu cầu:
```
Change the homepage layout to a three-column grid
(Thay đổi bố cục trang chủ thành lưới ba cột)
```

**Kết quả:** Bố cục bị hỏng - các cột bị lệch, nội dung chồng chéo.

#### Bước 2: Xác định Vấn đề

Bạn nhận thấy:
- Bố cục trông sai
- Nội dung bị chồng chéo
- Chế độ xem di động bị hỏng

#### Bước 3: Sử dụng Chat Mode để Hiểu

**Bạn (Chat Mode):**
```
The homepage layout I just changed looks broken. Can you help me understand what went wrong?
(Bố cục trang chủ tôi vừa thay đổi trông bị hỏng. Bạn có thể giúp tôi hiểu điều gì đã sai không?)
```

**Chat Mode:**
- Giải thích vấn đề
- Đề xuất bố cục cần điều chỉnh
- Khuyên nên hoàn tác và thử một cách tiếp cận khác

#### Bước 4: Hoàn tác Thay đổi

**Tùy chọn A: Sử dụng Lịch sử**
1. Đi tới Lịch sử
2. Tìm phiên bản trước khi thay đổi lưới
3. Nhấp "Revert"
4. Dự án quay lại trạng thái hoạt động tốt

**Tùy chọn B: Yêu cầu Hoàn tác**
```
Revert the last change - go back to before I changed the layout to three columns
(Hoàn tác thay đổi cuối cùng - quay lại trước khi tôi thay đổi bố cục thành ba cột)
```

#### Bước 5: Thử một Cách tiếp cận Khác

**Bạn:**
```
The three-column grid didn't work. Let me try a different approach. Create a two-column layout with the main content on the left and sidebar on the right, but make sure it's responsive.
(Lưới ba cột không hoạt động. Hãy để tôi thử một cách tiếp cận khác. Tạo bố cục hai cột với nội dung chính bên trái và thanh bên bên phải, nhưng hãy đảm bảo nó responsive.)
```

**Kết quả:** Bố cục tốt hơn và hoạt động!

#### Bước 6: Lặp lại và Cải thiện

**Bạn:**
```
The two-column layout works, but can you add more spacing and make the sidebar slightly narrower?
(Bố cục hai cột hoạt động, nhưng bạn có thể thêm khoảng cách và làm cho thanh bên hẹp hơn một chút không?)
```

**Kết quả:** Bố cục hoàn hảo!

**Những Gì Bạn Đã Học:**
- ✅ Đã mắc lỗi (điều đó không sao cả!)
- ✅ Đã xác định vấn đề
- ✅ Đã hoàn tác an toàn
- ✅ Đã thử một cách tiếp cận tốt hơn
- ✅ Đã lặp lại để hoàn thiện

**💡 Mẹo cho người mới bắt đầu:** Hoàn tác không phải là thất bại - đó là học hỏi! Mọi lập trình viên đều hoàn tác các thay đổi thường xuyên.

---

## 📖 Bài học 4: Chỉnh sửa Tin nhắn để Sửa chữa Sai lầm

### Chỉnh sửa Tin nhắn là gì?

**Chỉnh sửa tin nhắn** cho phép bạn sửa đổi hoặc xóa các tin nhắn trước đó để thay đổi những gì Lovable đã làm.

### Khi nào nên Chỉnh sửa Tin nhắn

Chỉnh sửa tin nhắn khi:
- ✅ Bạn đã yêu cầu điều gì đó mà bạn không muốn
- ✅ Bạn muốn tinh chỉnh một yêu cầu trước đó
- ✅ Bạn đã mắc lỗi trong prompt của mình
- ✅ Bạn muốn thử một cách tiếp cận khác

### Cách Chỉnh sửa Tin nhắn

#### Bước 1: Tìm Tin nhắn

1. **Xem lịch sử tin nhắn của bạn** - Thường hiển thị trong khu vực chat/nhập liệu
2. **Tìm tin nhắn** đã thực hiện thay đổi mà bạn muốn hoàn tác
3. **Tìm tùy chọn chỉnh sửa** - Thường là biểu tượng chỉnh sửa hoặc nút

#### Bước 2: Chỉnh sửa Tin nhắn

**Tùy chọn A: Sửa đổi Tin nhắn**
- Nhấp chỉnh sửa
- Thay đổi văn bản
- Lưu
- Lovable sẽ điều chỉnh dựa trên tin nhắn mới

**Tùy chọn B: Xóa Tin nhắn**
- Nhấp xóa
- Xóa tin nhắn
- Lovable sẽ hoàn tác thay đổi đó

#### Bước 3: Xem Kết quả

- Các thay đổi cập nhật tự động
- Dự án của bạn điều chỉnh
- Bạn có thể tiếp tục từ đó

### Ví dụ: Chỉnh sửa để Sửa lỗi

**Tin nhắn Gốc:**
```
Change all buttons to red
(Thay đổi tất cả các nút thành màu đỏ)
```

**Kết quả:** Tất cả các nút bây giờ đều màu đỏ, nhưng bạn nhận ra bạn chỉ muốn một nút màu đỏ.

**Sửa bằng cách Chỉnh sửa:**
1. **Tìm tin nhắn** "Change all buttons to red"
2. **Chỉnh sửa nó thành:**
   ```
   Change only the "Submit" button to red, keep all other buttons blue
   (Chỉ thay đổi nút "Gửi" thành màu đỏ, giữ tất cả các nút khác màu xanh)
   ```
3. **Lưu** - Lovable cập nhật tương ứng

### Ví dụ: Tinh chỉnh Yêu cầu

**Tin nhắn Gốc:**
```
Add a contact form
(Thêm một form liên hệ)
```

**Sau đó, bạn nhận ra bạn muốn nhiều hơn:**
1. **Tìm tin nhắn** "Add a contact form"
2. **Chỉnh sửa nó thành:**
   ```
   Add a contact form with name, email, phone, and message fields. Include validation and a success message.
   (Thêm một form liên hệ với các trường tên, email, điện thoại và tin nhắn. Bao gồm xác thực và thông báo thành công.)
   ```
3. **Lưu** - Lovable cải thiện form

**💡 Mẹo cho người mới bắt đầu:** Đừng ngại chỉnh sửa tin nhắn! Đó là một cách mạnh mẽ để tinh chỉnh và sửa chữa mọi thứ.

---

## 📖 Bài học 5: Chiến lược Kiểm thử

### Tại sao Kiểm thử lại Quan trọng

**Kiểm thử** đảm bảo ứng dụng của bạn:
- ✅ Hoạt động như mong đợi
- ✅ Không bị lỗi
- ✅ Cung cấp trải nghiệm người dùng tốt
- ✅ Sẵn sàng cho người dùng

### Khi nào nên Kiểm thử

**Kiểm thử:**
- ✅ Sau khi xây dựng một tính năng mới
- ✅ Sau khi thực hiện thay đổi
- ✅ Trước khi triển khai
- ✅ Khi có điều gì đó có vẻ sai
- ✅ Thường xuyên trong suốt quá trình phát triển

### Kiểm thử Cái gì

#### 1. Kiểm thử Chức năng (Functionality Testing)

**Nó có hoạt động không?**
- ✅ Tất cả các nút đều hoạt động
- ✅ Các form gửi đi chính xác
- ✅ Các liên kết điều hướng đúng
- ✅ Các tính năng hoạt động như dự định

**Cách kiểm thử:**
- Nhấp vào mọi thứ
- Điền vào tất cả các form
- Thử tất cả các tương tác
- Kiểm thử các trường hợp biên (edge cases)

#### 2. Kiểm thử Trực quan (Visual Testing)

**Nó trông có đúng không?**
- ✅ Bố cục chính xác
- ✅ Màu sắc đúng
- ✅ Khoảng cách tốt
- ✅ Văn bản dễ đọc

**Cách kiểm thử:**
- Xem trên các kích thước màn hình khác nhau
- Kiểm tra tất cả các trang
- Xác minh hình ảnh tải được
- Kiểm thử trên các trình duyệt khác nhau

#### 3. Kiểm thử Luồng Người dùng (User Flow Testing)

**Người dùng có thể hoàn thành các tác vụ không?**
- ✅ Đăng ký hoạt động
- ✅ Đăng nhập hoạt động
- ✅ Có thể tạo nội dung
- ✅ Có thể điều hướng dễ dàng

**Cách kiểm thử:**
- Đi qua các hành trình người dùng hoàn chỉnh
- Kiểm thử như một người dùng mới
- Kiểm thử như một người dùng đã đăng nhập
- Thử các đường dẫn khác nhau

#### 4. Kiểm thử Lỗi (Error Testing)

**Điều gì xảy ra khi mọi thứ đi sai hướng?**
- ✅ Thông báo lỗi hữu ích
- ✅ Các form xác thực chính xác
- ✅ Đầu vào không hợp lệ được xử lý
- ✅ Ứng dụng không bị crash

**Cách kiểm thử:**
- Gửi các form trống
- Nhập dữ liệu không hợp lệ
- Cố gắng làm hỏng mọi thứ
- Kiểm thử các kịch bản lỗi

### Danh sách Kiểm tra (Checklist) Kiểm thử

**Trước khi triển khai, hãy kiểm thử:**

**Chức năng:**
- [ ] Tất cả các nút đều hoạt động
- [ ] Tất cả các form đều gửi được
- [ ] Tất cả các liên kết đều hoạt động
- [ ] Điều hướng hoạt động
- [ ] Các tính năng hoạt động chính xác

**Trực quan:**
- [ ] Trông tốt trên máy tính để bàn
- [ ] Trông tốt trên di động
- [ ] Trông tốt trên máy tính bảng
- [ ] Màu sắc chính xác
- [ ] Văn bản dễ đọc

**Trải nghiệm Người dùng:**
- [ ] Dễ sử dụng
- [ ] Hướng dẫn rõ ràng
- [ ] Thông báo lỗi hữu ích
- [ ] Tải nhanh
- [ ] Tương tác mượt mà

**Bảo mật:**
- [ ] Xác thực hoạt động
- [ ] Người dùng chỉ có thể truy cập dữ liệu của họ
- [ ] Các form được bảo mật
- [ ] Không lộ dữ liệu nhạy cảm

**💡 Mẹo cho người mới bắt đầu:** Kiểm thử khi bạn xây dựng! Đừng đợi đến cuối cùng. Bắt lỗi sớm khi chúng dễ sửa hơn.

---

## 📖 Bài học 6: Các Kịch bản Gỡ lỗi Phổ biến

### Kịch bản 1: Tính năng Không Hoạt động

**Vấn đề:** Bạn đã thêm một tính năng, nhưng nó không hoạt động.

**Các bước Gỡ lỗi:**

1. **Kiểm tra xem nó đã được xây dựng chưa:**
   - Mã có ở đó không?
   - Các tệp đã được tạo chưa?
   - Sử dụng Chat Mode: "Did the feature get added correctly?" (Tính năng đã được thêm chính xác chưa?)

2. **Kiểm tra lỗi:**
   - Tìm kiếm thông báo lỗi
   - Kiểm tra console trình duyệt
   - Hỏi Chat Mode: "Are there any errors in this feature?" (Có lỗi nào trong tính năng này không?)

3. **Kiểm thử tính năng:**
   - Thử sử dụng nó
   - Xem điều gì xảy ra
   - Ghi lại bất kỳ thông báo lỗi nào

4. **Sửa vấn đề:**
   - Sử dụng Chat Mode để hiểu vấn đề
   - Sử dụng Agent Mode để sửa nó
   - Kiểm thử lại

### Kịch bản 2: Có gì đó Bị hỏng Sau khi Thay đổi

**Vấn đề:** Mọi thứ đã hoạt động, bạn thực hiện một thay đổi, bây giờ có gì đó bị hỏng.

**Các bước Gỡ lỗi:**

1. **Xác định những gì đã thay đổi:**
   - Kiểm tra Lịch sử
   - Xem những gì bạn đã sửa đổi
   - Sử dụng Chat Mode: "What did I change that might have broken this?" (Tôi đã thay đổi gì mà có thể làm hỏng cái này?)

2. **Hoàn tác nếu cần:**
   - Quay lại phiên bản hoạt động
   - Hoặc chỉ hoàn tác thay đổi có vấn đề

3. **Thử một cách tiếp cận khác:**
   - Thực hiện thay đổi theo cách khác
   - Chia nhỏ nó thành các bước nhỏ hơn
   - Kiểm thử khi bạn làm

### Kịch bản 3: Dữ liệu Không Lưu

**Vấn đề:** Người dùng có thể gửi form, nhưng dữ liệu không được lưu.

**Các bước Gỡ lỗi:**

1. **Kiểm tra backend:**
   - Lovable Cloud đã được bật chưa?
   - Cơ sở dữ liệu đã được thiết lập chưa?
   - Hỏi Chat Mode: "Is the database configured correctly?" (Cơ sở dữ liệu có được cấu hình chính xác không?)

2. **Kiểm tra kết nối form:**
   - Form có được kết nối với backend không?
   - Các trường có được ánh xạ chính xác không?
   - Sử dụng Chat Mode: "Is the contact form saving to the database?" (Form liên hệ có đang lưu vào cơ sở dữ liệu không?)

3. **Kiểm tra cơ sở dữ liệu:**
   - Bạn có thể thấy dữ liệu trong cơ sở dữ liệu không?
   - Các trường có chính xác không?
   - Kiểm thử thủ công

4. **Sửa kết nối:**
   - Kết nối lại form với cơ sở dữ liệu
   - Xác minh ánh xạ trường
   - Kiểm thử lại

### Kịch bản 4: Thiết kế Trông Sai

**Vấn đề:** Thiết kế không khớp với những gì bạn muốn.

**Các bước Gỡ lỗi:**

1. **Kiểm tra những gì đã được xây dựng:**
   - So sánh với yêu cầu của bạn
   - Xem những gì khác biệt
   - Sử dụng Chat Mode: "Why doesn't this match my design request?" (Tại sao cái này không khớp với yêu cầu thiết kế của tôi?)

2. **Xác định các vấn đề cụ thể:**
   - Màu sắc sai?
   - Bố cục sai?
   - Khoảng cách sai?
   - Hãy cụ thể

3. **Sửa dần dần:**
   - Sửa từng vấn đề một
   - Kiểm thử sau mỗi lần sửa
   - Lặp lại cho đến khi hoàn hảo

### Kịch bản 5: Vấn đề Hiệu suất

**Vấn đề:** Ứng dụng chậm hoặc lag.

**Các bước Gỡ lỗi:**

1. **Xác định vấn đề:**
   - Cái gì chậm? (tải, tương tác, v.v.)
   - Khi nào nó xảy ra?
   - Sử dụng Chat Mode: "Why is my app running slowly?" (Tại sao ứng dụng của tôi chạy chậm?)

2. **Kiểm tra các vấn đề phổ biến:**
   - Hình ảnh lớn?
   - Quá nhiều yêu cầu?
   - Mã không hiệu quả?
   - Chat Mode có thể xác định những điều này

3. **Tối ưu hóa:**
   - Sửa các vấn đề đã xác định
   - Kiểm thử hiệu suất
   - Lặp lại

**💡 Mẹo cho người mới bắt đầu:** Hầu hết các vấn đề đều có quy luật. Khi bạn gỡ lỗi nhiều hơn, bạn sẽ nhận ra các vấn đề phổ biến nhanh hơn.

---

## 🛠️ Thực hành: Quy trình Gỡ lỗi Hoàn chỉnh

Hãy thực hành quy trình gỡ lỗi hoàn chỉnh!

### Thực hành: Gỡ lỗi một Tính năng Bị hỏng

**Kịch bản:** Bạn có một form liên hệ không hoạt động.

#### Bước 1: Xác định Vấn đề

1. **Thử sử dụng form:**
   - Điền vào nó
   - Gửi nó
   - Xem điều gì xảy ra (hoặc không xảy ra)

2. **Ghi lại các triệu chứng:**
   - Không có gì xảy ra?
   - Hiển thị lỗi?
   - Gửi nhưng không lưu?

#### Bước 2: Điều tra với Chat Mode

**Hỏi Chat Mode:**
```
My contact form isn't working. When I submit it, nothing happens. Can you investigate what's wrong?
(Form liên hệ của tôi không hoạt động. Khi tôi gửi nó, không có gì xảy ra. Bạn có thể điều tra xem có gì sai không?)
```

**Chat Mode sẽ:**
- Kiểm tra mã form
- Kiểm tra kết nối backend
- Xác định vấn đề
- Giải thích điều gì sai

#### Bước 3: Hiểu Vấn đề

**Đọc giải thích của Chat Mode:**
- Nguyên nhân gốc rễ là gì?
- Tại sao nó không hoạt động?
- Cần sửa gì?

#### Bước 4: Sửa Vấn đề

**Tùy chọn A: Sử dụng Agent Mode**
```
Fix the contact form based on what Chat Mode found. Connect it to the backend and make it save submissions.
(Sửa form liên hệ dựa trên những gì Chat Mode tìm thấy. Kết nối nó với backend và làm cho nó lưu các bài gửi.)
```

**Tùy chọn B: Sử dụng Kế hoạch của Chat Mode**
- Nhấp "Implement the plan" (Thực hiện kế hoạch)
- Để Agent Mode sửa nó

#### Bước 5: Kiểm thử Bản sửa lỗi

1. **Thử lại form:**
   - Điền vào nó
   - Gửi nó
   - Kiểm tra xem nó có hoạt động không

2. **Xác minh dữ liệu được lưu:**
   - Kiểm tra cơ sở dữ liệu
   - Xác nhận bài gửi đã được lưu trữ

3. **Kiểm thử xử lý lỗi:**
   - Gửi form trống
   - Gửi dữ liệu không hợp lệ
   - Xem lỗi có được xử lý không

#### Bước 6: Nếu Vẫn Bị hỏng

1. **Quay lại Chat Mode:**
   ```
   The form still isn't working. Can you check again?
   (Form vẫn không hoạt động. Bạn có thể kiểm tra lại không?)
   ```

2. **Hoặc hoàn tác và thử cách khác:**
   - Đi tới Lịch sử
   - Hoàn tác về trước khi có form
   - Thử một cách tiếp cận khác

**Những Gì Bạn Đã Học:**
- ✅ Cách xác định vấn đề
- ✅ Cách sử dụng Chat Mode để gỡ lỗi
- ✅ Cách sửa các vấn đề
- ✅ Cách kiểm thử các bản sửa lỗi
- ✅ Cách lặp lại nếu cần

---

## 🛠️ Thực hành: Hoàn tác và Lặp lại

Hãy thực hành quy trình hoàn tác!

### Thực hành: Mắc lỗi, Hoàn tác và Sửa

#### Bước 1: Tạo một "Lỗi" Cố ý

**Hỏi Lovable:**
```
Change all the text on the homepage to bright pink and make the font size 8px
(Thay đổi tất cả văn bản trên trang chủ thành màu hồng sáng và đặt kích thước phông chữ là 8px)
```

**Kết quả:** Trang chủ bây giờ không thể đọc được (văn bản màu hồng, phông chữ nhỏ xíu)

#### Bước 2: Xác định Vấn đề

- Văn bản quá nhỏ để đọc
- Màu hồng khó đọc
- Thiết kế bị hỏng

#### Bước 3: Hoàn tác Sử dụng Lịch sử

1. **Đi tới Lịch sử**
2. **Tìm phiên bản** trước khi bạn thay đổi văn bản
3. **Nhấp "Revert"**
4. **Xác nhận**
5. **Trang chủ được khôi phục!**

#### Bước 4: Thử một Cách tiếp cận Tốt hơn

**Bây giờ hỏi:**
```
Improve the homepage typography: increase heading sizes slightly, improve line spacing for readability, and use a more readable font. Keep the existing color scheme.
(Cải thiện kiểu chữ trang chủ: tăng kích thước tiêu đề một chút, cải thiện khoảng cách dòng để dễ đọc và sử dụng phông chữ dễ đọc hơn. Giữ nguyên bảng màu hiện có.)
```

**Kết quả:** Tốt hơn nhiều! Dễ đọc và được cải thiện.

**Những Gì Bạn Đã Học:**
- ✅ Cách sử dụng Lịch sử
- ✅ Cách hoàn tác các thay đổi
- ✅ Cách thử các cách tiếp cận tốt hơn
- ✅ Rằng sai lầm là bình thường - bạn luôn có thể sửa chúng!

---

## ✅ Danh sách Kiểm tra Module 10

Trước khi chuyển sang Module 9 (hoặc hoàn thành khóa học), hãy đảm bảo bạn có thể:

- [ ] Đọc và hiểu các thông báo lỗi
- [ ] Sử dụng Chat Mode để gỡ lỗi các vấn đề
- [ ] Sử dụng Lịch sử để hoàn tác các thay đổi
- [ ] Chỉnh sửa tin nhắn để sửa chữa sai lầm
- [ ] Kiểm thử ứng dụng của bạn một cách kỹ lưỡng
- [ ] Gỡ lỗi các vấn đề phổ biến
- [ ] Tuân theo quy trình gỡ lỗi
- [ ] Hoàn tác và lặp lại một cách tự tin

---

## 🤔 Các Câu Hỏi Thường Gặp (FAQ)

### Q: Nếu tôi không thể hiểu thông báo lỗi thì sao?
**A:** Sử dụng Chat Mode! Dán lỗi vào và hỏi: "Can you explain what this error means?" (Bạn có thể giải thích lỗi này có nghĩa là gì không?)

### Q: Tôi có thể hoàn tác bao xa?
**A:** Bạn có thể hoàn tác về bất kỳ phiên bản nào trước đó trong Lịch sử của mình. Không có giới hạn!

### Q: Việc hoàn tác có xóa công việc của tôi không?
**A:** Hoàn tác sẽ quay lại phiên bản trước đó, nhưng bạn luôn có thể đi tiếp một lần nữa. Công việc của bạn không bị mất vĩnh viễn.

### Q: Tôi có nên kiểm thử sau mỗi thay đổi không?
**A:** Đó là một thói quen tốt! Kiểm thử thường xuyên để bắt lỗi sớm.

### Q: Nếu Chat Mode không thể tìm thấy vấn đề thì sao?
**A:** Hãy thử cụ thể hơn, hoặc chia vấn đề thành các phần nhỏ hơn. Đôi khi bạn cần điều tra từng bước một.

### Q: Tôi có thể hoàn tác chỉ một tính năng không?
**A:** Có! Bạn có thể hoàn tác về một phiên bản cụ thể, hoặc yêu cầu Lovable xóa chỉ tính năng đó.

---

## 🎯 Tiếp theo là gì?

Làm tốt lắm! Bây giờ bạn đã biết cách:
- Gỡ lỗi các vấn đề hiệu quả
- Sử dụng Chat Mode để khắc phục sự cố
- Hoàn tác các thay đổi an toàn
- Kiểm thử các ứng dụng của bạn
- Sửa các vấn đề một cách tự tin

**Sẵn sàng cho Module 9?** Trong module cuối cùng, bạn sẽ xây dựng một dự án thực tế hoàn chỉnh, áp dụng mọi thứ bạn đã học bao gồm gỡ lỗi và kiểm thử!

---

## 💡 Mẹo Chuyên nghiệp cho Người mới bắt đầu

1. **Đừng sợ lỗi** - Chúng là cơ hội học tập!

2. **Sử dụng Chat Mode thoải mái** - Đó là đối tác gỡ lỗi của bạn

3. **Kiểm thử khi bạn xây dựng** - Bắt lỗi sớm

4. **Hoàn tác tự do** - Đó không phải là thất bại, đó là học hỏi

5. **Đọc thông báo lỗi** - Chúng cho bạn biết điều gì sai

6. **Ghi lại những gì hoạt động** - Ghi chú các cách tiếp cận thành công

7. **Kiên nhẫn** - Gỡ lỗi tốn thời gian, nhưng bạn sẽ giỏi hơn

---

*Module 10 Hoàn thành! 🎉*
