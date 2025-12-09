# Module 14: Kiểm soát Phiên bản với GitHub

**Mục tiêu:** Học cách sử dụng GitHub với Lovable để kiểm soát phiên bản và cộng tác

**Thời gian ước tính:** 30-40 phút

**Điều kiện tiên quyết:** Hoàn thành Module 1-4 trước

---

## 🎯 Bạn Sẽ Học Được Gì Trong Module Này

Vào cuối module này, bạn sẽ:
- Hiểu kiểm soát phiên bản là gì và tại sao nó quan trọng
- Biết cách kết nối Lovable với GitHub
- Hiểu về commit, nhánh (branch) và pull request
- Học cách cộng tác với người khác
- Biết cách quản lý lịch sử mã của bạn
- Có khả năng sử dụng GitHub để sao lưu và làm hồ sơ năng lực (portfolio)

---

## 📖 Bài học 1: Hiểu về Kiểm soát Phiên bản

### Kiểm soát Phiên bản là gì?

**Kiểm soát phiên bản (Version control)** giống như một cỗ máy thời gian cho mã của bạn. Nó:
- ✅ Lưu mọi phiên bản của dự án của bạn
- ✅ Cho phép bạn quay lại bất kỳ thời điểm nào
- ✅ Theo dõi tất cả các thay đổi
- ✅ Cho phép cộng tác
- ✅ Cung cấp bản sao lưu

### Tại sao Sử dụng Kiểm soát Phiên bản?

**Lợi ích:**
- **Sao lưu** - Mã của bạn được an toàn
- **Lịch sử** - Xem dự án của bạn đã phát triển như thế nào
- **Cộng tác** - Làm việc với người khác
- **Thử nghiệm** - Thử mọi thứ mà không sợ hãi
- **Hồ sơ năng lực** - Thể hiện công việc của bạn
- **Khôi phục** - Lấy lại công việc đã mất

### Cơ bản về GitHub

**GitHub** là một nền tảng để kiểm soát phiên bản. Hãy nghĩ về nó như:
- Google Drive cho mã
- Cỗ máy thời gian cho các dự án
- Nền tảng cộng tác
- Nơi trưng bày hồ sơ năng lực

**💡 Mẹo cho người mới bắt đầu:** Bạn không cần phải hiểu tất cả các chi tiết kỹ thuật! Lovable làm cho nó dễ dàng.

---

## 📖 Bài học 2: Kết nối Lovable với GitHub

### Cách Kết nối

#### Bước 1: Có Tài khoản GitHub

Nếu bạn chưa có:
1. Truy cập [github.com](https://github.com)
2. Nhấp **"Sign up"** (Đăng ký)
3. Tạo tài khoản miễn phí
4. Xác minh email của bạn

#### Bước 2: Kết nối trong Lovable

1. **Trong dự án Lovable của bạn**, đi tới **Settings** (Cài đặt)
2. **Tìm phần "GitHub"** hoặc **"Version Control"**
3. **Nhấp "Connect to GitHub"** (Kết nối với GitHub)
4. **Ủy quyền cho Lovable** - Nhấp "Authorize" hoặc "Allow"
5. **Chọn cài đặt kho lưu trữ (repository):**
   - Tạo kho lưu trữ mới
   - Hoặc sử dụng kho lưu trữ hiện có
   - Chọn công khai (public) hoặc riêng tư (private)
   - Lưu

#### Bước 3: Mã của Bạn Đồng bộ

Sau khi kết nối:
- **Mã đồng bộ tự động** - Các thay đổi được lưu vào GitHub
- **Bạn có thể xem nó trên GitHub** - Truy cập github.com để xem
- **Người khác có thể xem nó** - Nếu công khai, mọi người có thể xem công việc của bạn

**💡 Mẹo cho người mới bắt đầu:** Bắt đầu với kho lưu trữ riêng tư nếu bạn đang học. Đặt thành công khai sau nếu bạn muốn trưng bày nó.

---

## 📖 Bài học 3: Hiểu về Commit

### Commit là gì?

Một **commit** giống như lưu một bản chụp nhanh (snapshot) của dự án của bạn tại một thời điểm cụ thể.

**Hãy nghĩ về nó như:**
- Lưu một tài liệu
- Chụp một bức ảnh
- Tạo một điểm kiểm tra (checkpoint)

### Cách Commit Hoạt động trong Lovable

**Lovable tự động:**
- ✅ Tạo commit khi bạn thực hiện thay đổi
- ✅ Thêm thông báo mô tả
- ✅ Lưu vào GitHub
- ✅ Giữ lịch sử được tổ chức

**Bạn cũng có thể:**
- Tạo commit thủ công
- Thêm thông báo commit tùy chỉnh
- Kiểm soát khi nào commit xảy ra

### Thông báo Commit

**Thông báo commit tốt:**
- Mô tả những gì đã thay đổi
- Rõ ràng và cụ thể
- Giúp bạn hiểu lịch sử

**Ví dụ:**
- "Add user authentication" (Thêm xác thực người dùng)
- "Fix contact form submission" (Sửa lỗi gửi form liên hệ)
- "Update homepage design" (Cập nhật thiết kế trang chủ)
- "Add task filtering feature" (Thêm tính năng lọc công việc)

**💡 Mẹo cho người mới bắt đầu:** Lovable tạo các thông báo commit tốt một cách tự động. Bạn có thể tùy chỉnh chúng nếu muốn.

---

## 📖 Bài học 4: Nhánh (Branches)

### Nhánh là gì?

**Nhánh (Branches)** giống như các dòng thời gian song song. Bạn có thể làm việc trên các tính năng khác nhau mà không ảnh hưởng đến dự án chính.

**Hãy nghĩ về nó như:**
- Nhánh chính (Main branch) = Cuốn sách đã xuất bản
- Nhánh tính năng (Feature branch) = Bản nháp chương
- Bạn chỉnh sửa bản nháp, sau đó hợp nhất nó vào cuốn sách

### Khi nào Sử dụng Nhánh

**Sử dụng nhánh để:**
- ✅ Thử các tính năng mới
- ✅ Thử nghiệm
- ✅ Làm việc trên các thay đổi lớn
- ✅ Cộng tác với người khác

### Cách Tạo Nhánh

**Trong Lovable:**
```
Create a new branch called "feature-new-design" to work on redesigning the homepage
(Tạo một nhánh mới tên là "feature-new-design" để làm việc về thiết kế lại trang chủ)
```

**Hoặc trong GitHub:**
1. Đi tới kho lưu trữ của bạn
2. Nhấp vào menu thả xuống nhánh "main"
3. Nhập tên nhánh mới
4. Tạo nhánh

### Hợp nhất Nhánh

**Khi bạn hoàn thành:**
```
Merge the "feature-new-design" branch into main
(Hợp nhất nhánh "feature-new-design" vào main)
```

**Hoặc trong GitHub:**
1. Đi tới kho lưu trữ của bạn
2. Tạo Pull Request
3. Xem xét các thay đổi
4. Hợp nhất (Merge)

**💡 Mẹo cho người mới bắt đầu:** Bắt đầu chỉ với nhánh main. Sử dụng các nhánh khi bạn cảm thấy thoải mái hoặc làm việc trên các tính năng lớn.

---

## 📖 Bài học 5: Pull Requests

### Pull Request là gì?

Một **Pull Request (PR)** là một cách để:
- Xem xét các thay đổi trước khi hợp nhất
- Thảo luận về các thay đổi với người khác
- Nhận phản hồi
- Hợp nhất các nhánh một cách an toàn

### Cách Pull Request Hoạt động

1. **Thực hiện thay đổi** trong một nhánh
2. **Tạo Pull Request** - Đề xuất hợp nhất vào main
3. **Xem xét thay đổi** - Xem những gì khác biệt
4. **Thảo luận** - Bình luận và nhận phản hồi
5. **Hợp nhất** - Kết hợp vào nhánh main

### Tạo Pull Request

**Trong GitHub:**
1. Đi tới kho lưu trữ của bạn
2. Nhấp tab "Pull Requests"
3. Nhấp "New Pull Request"
4. Chọn các nhánh để so sánh
5. Thêm mô tả
6. Tạo PR

**💡 Mẹo cho người mới bắt đầu:** Pull Request rất tuyệt để cộng tác. Ngay cả khi làm một mình, chúng giúp bạn xem lại các thay đổi của chính mình!

---

## 📖 Bài học 6: Cộng tác với GitHub

### Làm việc với Người khác

**GitHub cho phép:**
- Nhiều người làm việc trên cùng một dự án
- Xem xét mã của nhau
- Thảo luận về các thay đổi
- Hợp nhất công việc với nhau

### Quy trình Cộng tác

1. **Clone kho lưu trữ** - Lấy một bản sao
2. **Tạo nhánh** - Làm việc trên tính năng
3. **Thực hiện thay đổi** - Xây dựng tính năng của bạn
4. **Commit thay đổi** - Lưu công việc của bạn
5. **Push lên GitHub** - Tải lên các thay đổi của bạn
6. **Tạo Pull Request** - Đề xuất hợp nhất
7. **Xem xét và hợp nhất** - Kết hợp vào main

### Sử dụng GitHub cho Hồ sơ năng lực

**Trưng bày công việc của bạn:**
- Đặt kho lưu trữ thành công khai
- Thêm tệp README
- Bao gồm ảnh chụp màn hình
- Tài liệu hóa các dự án của bạn
- Chia sẻ với nhà tuyển dụng/khách hàng

**💡 Mẹo cho người mới bắt đầu:** GitHub giống như một hồ sơ năng lực cho các nhà phát triển. Hãy giữ những công việc tốt nhất của bạn ở chế độ công khai!

---

## 🛠️ Thực hành

### Thực hành 1: Kết nối và Commit Đầu tiên

**Nhiệm vụ:** Kết nối một dự án với GitHub và thực hiện commit đầu tiên của bạn.

**Các bước:**
1. **Kết nối với GitHub** (như mô tả ở trên)
2. **Thực hiện một thay đổi nhỏ** cho dự án của bạn
3. **Kiểm tra GitHub** - Xem thay đổi của bạn ở đó
4. **Xem lịch sử commit** - Xem commit

### Thực hành 2: Tạo một Nhánh

**Nhiệm vụ:** Tạo một nhánh và thực hiện thay đổi.

**Các bước:**
1. **Tạo một nhánh:**
   ```
   Create a new branch called "experiment-new-feature"
   (Tạo một nhánh mới tên là "experiment-new-feature")
   ```
2. **Thực hiện thay đổi** trong nhánh đó
3. **Kiểm tra GitHub** - Xem nhánh
4. **Chuyển lại về main** - Xem nó không thay đổi

### Thực hành 3: Hợp nhất một Nhánh

**Nhiệm vụ:** Hợp nhất nhánh thử nghiệm của bạn.

**Các bước:**
1. **Đi tới GitHub**
2. **Tạo Pull Request** từ nhánh của bạn
3. **Xem xét thay đổi**
4. **Hợp nhất** vào main
5. **Xem thay đổi** trong nhánh main

---

## ✅ Danh sách Kiểm tra Module 14

Trước khi hoàn thành khóa học, hãy đảm bảo bạn có thể:

- [ ] Hiểu kiểm soát phiên bản là gì
- [ ] Kết nối Lovable với GitHub
- [ ] Hiểu commit và thông báo commit
- [ ] Tạo và sử dụng nhánh
- [ ] Tạo và hợp nhất pull request
- [ ] Sử dụng GitHub để sao lưu
- [ ] Hiểu cộng tác cơ bản

---

## 🤔 Các Câu Hỏi Thường Gặp (FAQ)

### Q: Tôi có cần GitHub không?
**A:** Nó là tùy chọn nhưng được khuyến nghị! Tuyệt vời để sao lưu và học tập.

### Q: GitHub có miễn phí không?
**A:** Có! Tài khoản miễn phí có kho lưu trữ công khai không giới hạn và một số kho lưu trữ riêng tư.

### Q: Tôi có thể sử dụng GitHub mà không cần biết Git không?
**A:** Có! Lovable xử lý hầu hết việc đó. Bạn có thể sử dụng giao diện web của GitHub cho phần còn lại.

### Q: Sự khác biệt giữa Git và GitHub là gì?
**A:** Git là công cụ, GitHub là nền tảng. Lovable sử dụng Git và kết nối với GitHub.

### Q: Tôi nên đặt repo của mình là công khai hay riêng tư?
**A:** Riêng tư cho các dự án cá nhân, công khai cho các phần hồ sơ năng lực bạn muốn trưng bày.

---

## 🎯 Tiếp theo là gì?

Làm tốt lắm! Bây giờ bạn đã hiểu kiểm soát phiên bản với GitHub. Sử dụng nó để sao lưu công việc của bạn và xây dựng hồ sơ năng lực của bạn.

**Tiếp tục với:**
- Module 15: Triển khai lên Đám mây Tùy chỉnh
- Hoặc áp dụng các kỹ năng này để quản lý các dự án của bạn!

---

*Module 14 Hoàn thành! 🎉*
