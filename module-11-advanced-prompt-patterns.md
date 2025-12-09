# Module 11: Các Mẫu Prompt Nâng cao

**Mục tiêu:** Làm chủ các kỹ thuật nâng cao cho các ứng dụng phức tạp

**Thời gian ước tính:** 40-50 phút

**Điều kiện tiên quyết:** Hoàn thành Module 1-5 trước

---

## 🎯 Bạn Sẽ Học Được Gì Trong Module Này

Vào cuối module này, bạn sẽ:
- Hiểu các mẫu prompt nâng cao cho các luồng phức tạp
- Biết cách tạo nội dung động, dựa trên dữ liệu
- Học logic điều kiện trong các prompt
- Hiểu cách xử lý vòng lặp và lặp lại
- Có khả năng xây dựng các ứng dụng tinh vi hơn
- Biết các mẫu cho các tương tác người dùng phức tạp

---

## 📖 Bài học 1: Tạo Nội dung Động

### Nội dung Động là gì?

**Nội dung động (Dynamic content)** thay đổi dựa trên dữ liệu, đầu vào của người dùng hoặc các điều kiện. Thay vì các trang tĩnh, bạn tạo các trang thích ứng.

### Nội dung Động Cơ bản

**Ví dụ:**
```
Create a blog post page that displays:
- Post title (from database)
- Post content (from database)
- Author name (from database)
- Publication date (from database)
- Related posts (based on category)
(Tạo một trang bài viết blog hiển thị:
- Tiêu đề bài viết (từ cơ sở dữ liệu)
- Nội dung bài viết (từ cơ sở dữ liệu)
- Tên tác giả (từ cơ sở dữ liệu)
- Ngày xuất bản (từ cơ sở dữ liệu)
- Các bài viết liên quan (dựa trên danh mục))
```

**Điều này làm gì:** Tạo một mẫu điền dữ liệu khác nhau cho mỗi bài viết.

### Các Mẫu Động Nâng cao

#### Mẫu 1: Hiển thị Có điều kiện

**Ví dụ:**
```
On the product page, show different content based on product availability:
- If product is in stock: Show "Add to Cart" button and stock count
- If product is out of stock: Show "Notify Me" button and "Out of Stock" message
- If product is on sale: Show sale badge and discounted price
(Trên trang sản phẩm, hiển thị nội dung khác nhau dựa trên tình trạng sẵn có của sản phẩm:
- Nếu sản phẩm còn hàng: Hiển thị nút "Thêm vào giỏ hàng" và số lượng tồn kho
- Nếu sản phẩm hết hàng: Hiển thị nút "Thông báo cho tôi" và thông báo "Hết hàng"
- Nếu sản phẩm đang giảm giá: Hiển thị huy hiệu giảm giá và giá đã giảm)
```

#### Mẫu 2: Danh sách Dựa trên Dữ liệu

**Ví dụ:**
```
Create a task list that:
- Shows all tasks from the database
- Displays different information based on task status:
  - Pending tasks: Show in yellow with "Complete" button
  - Completed tasks: Show in green with strikethrough
  - Overdue tasks: Show in red with warning icon
- Updates automatically when tasks change
(Tạo một danh sách công việc:
- Hiển thị tất cả các công việc từ cơ sở dữ liệu
- Hiển thị thông tin khác nhau dựa trên trạng thái công việc:
  - Công việc đang chờ: Hiển thị màu vàng với nút "Hoàn thành"
  - Công việc đã hoàn thành: Hiển thị màu xanh lá cây với gạch ngang
  - Công việc quá hạn: Hiển thị màu đỏ với biểu tượng cảnh báo
- Cập nhật tự động khi công việc thay đổi)
```

#### Mẫu 3: Nội dung Dành riêng cho Người dùng

**Ví dụ:**
```
Create a dashboard that shows:
- Personalized greeting with user's name
- Content based on user's role:
  - Admin users: Show admin panel and all data
  - Regular users: Show only their own data
  - Guest users: Show limited preview
- Recommendations based on user's activity
(Tạo một bảng điều khiển hiển thị:
- Lời chào cá nhân hóa với tên người dùng
- Nội dung dựa trên vai trò của người dùng:
  - Người dùng quản trị: Hiển thị bảng quản trị và tất cả dữ liệu
  - Người dùng thường: Chỉ hiển thị dữ liệu của riêng họ
  - Người dùng khách: Hiển thị bản xem trước hạn chế
- Đề xuất dựa trên hoạt động của người dùng)
```

**💡 Mẹo cho người mới bắt đầu:** Bắt đầu đơn giản, sau đó thêm các điều kiện. Xây dựng phiên bản cơ bản trước, sau đó thêm logic điều kiện.

---

## 📖 Bài học 2: Logic Điều kiện trong Prompt

### Logic Điều kiện là gì?

**Logic điều kiện** có nghĩa là "nếu điều này, thì điều kia" - hiển thị nội dung hoặc hành vi khác nhau dựa trên các điều kiện.

### Các Mẫu Điều kiện Cơ bản

#### Mẫu 1: Nếu-Thì Đơn giản (Simple If-Then)

**Ví dụ:**
```
Create a user profile page that:
- If user is logged in: Show full profile with edit button
- If user is not logged in: Show limited preview with "Sign up to see more" message
(Tạo một trang hồ sơ người dùng:
- Nếu người dùng đã đăng nhập: Hiển thị hồ sơ đầy đủ với nút chỉnh sửa
- Nếu người dùng chưa đăng nhập: Hiển thị bản xem trước hạn chế với thông báo "Đăng ký để xem thêm")
```

#### Mẫu 2: Nhiều Điều kiện

**Ví dụ:**
```
Create a product card component that displays differently based on:
- Product availability (in stock, out of stock, pre-order)
- Product type (physical, digital, subscription)
- User's purchase history (new, previously purchased, in cart)
Show appropriate buttons and information for each combination
(Tạo một component thẻ sản phẩm hiển thị khác nhau dựa trên:
- Tình trạng sẵn có của sản phẩm (còn hàng, hết hàng, đặt trước)
- Loại sản phẩm (vật lý, kỹ thuật số, đăng ký)
- Lịch sử mua hàng của người dùng (mới, đã mua trước đó, trong giỏ hàng)
Hiển thị các nút và thông tin phù hợp cho từng kết hợp)
```

#### Mẫu 3: Kiểu dáng Có điều kiện

**Ví dụ:**
```
Style the task list items based on priority:
- High priority tasks: Red background, bold text, urgent icon
- Medium priority tasks: Yellow background, normal text
- Low priority tasks: Gray background, lighter text
- Completed tasks: Green checkmark, strikethrough, grayed out
(Tạo kiểu cho các mục danh sách công việc dựa trên mức độ ưu tiên:
- Công việc ưu tiên cao: Nền đỏ, chữ đậm, biểu tượng khẩn cấp
- Công việc ưu tiên trung bình: Nền vàng, chữ thường
- Công việc ưu tiên thấp: Nền xám, chữ nhạt hơn
- Công việc đã hoàn thành: Dấu tích xanh, gạch ngang, làm mờ)
```

### Các Mẫu Điều kiện Nâng cao

#### Mẫu 4: Điều kiện Lồng nhau

**Ví dụ:**
```
Create a notification system that shows different messages based on:
- User type (admin, member, guest)
  - If admin: Show all notifications including system alerts
  - If member: Show user-specific notifications
  - If guest: Show only public announcements
- Notification type (message, alert, update)
  - Messages: Show sender and preview
  - Alerts: Show with warning icon
  - Updates: Show with info icon
- Read status (read, unread)
  - Unread: Bold and highlighted
  - Read: Normal styling
(Tạo một hệ thống thông báo hiển thị các tin nhắn khác nhau dựa trên:
- Loại người dùng (quản trị viên, thành viên, khách)
  - Nếu là quản trị viên: Hiển thị tất cả thông báo bao gồm cảnh báo hệ thống
  - Nếu là thành viên: Hiển thị thông báo dành riêng cho người dùng
  - Nếu là khách: Chỉ hiển thị thông báo công khai
- Loại thông báo (tin nhắn, cảnh báo, cập nhật)
  - Tin nhắn: Hiển thị người gửi và xem trước
  - Cảnh báo: Hiển thị với biểu tượng cảnh báo
  - Cập nhật: Hiển thị với biểu tượng thông tin
- Trạng thái đọc (đã đọc, chưa đọc)
  - Chưa đọc: Đậm và nổi bật
  - Đã đọc: Kiểu dáng bình thường)
```

#### Mẫu 5: Tính năng Có điều kiện

**Ví dụ:**
```
Add features to the dashboard based on subscription level:
- Free users: Basic features only
- Pro users: Add advanced analytics and export
- Enterprise users: Add team collaboration and API access
Show upgrade prompts for features locked to higher tiers
(Thêm các tính năng vào bảng điều khiển dựa trên cấp độ đăng ký:
- Người dùng miễn phí: Chỉ các tính năng cơ bản
- Người dùng Pro: Thêm phân tích nâng cao và xuất dữ liệu
- Người dùng Doanh nghiệp: Thêm cộng tác nhóm và truy cập API
Hiển thị lời nhắc nâng cấp cho các tính năng bị khóa ở các cấp cao hơn)
```

**💡 Mẹo cho người mới bắt đầu:** Chia các điều kiện phức tạp thành các phần nhỏ hơn. Xây dựng từng điều kiện một, kiểm thử nó, sau đó thêm điều kiện tiếp theo.

---

## 📖 Bài học 3: Vòng lặp và Lặp lại

### Vòng lặp là gì?

**Vòng lặp (Loops)** lặp lại các hành động cho nhiều mục. Giống như nói "làm điều này cho mỗi mục trong danh sách".

### Các Mẫu Vòng lặp Cơ bản

#### Mẫu 1: Hiển thị Danh sách Mục

**Ví dụ:**
```
Create a blog listing page that:
- Fetches all blog posts from the database
- For each post, display:
  - Post title (as clickable link)
  - Featured image
  - Excerpt (first 150 characters)
  - Author name
  - Publication date
  - Read more button
- Show 10 posts per page with pagination
(Tạo một trang danh sách blog:
- Lấy tất cả các bài viết blog từ cơ sở dữ liệu
- Đối với mỗi bài viết, hiển thị:
  - Tiêu đề bài viết (dưới dạng liên kết có thể nhấp)
  - Hình ảnh nổi bật
  - Đoạn trích (150 ký tự đầu tiên)
  - Tên tác giả
  - Ngày xuất bản
  - Nút đọc thêm
- Hiển thị 10 bài viết mỗi trang với phân trang)
```

#### Mẫu 2: Tạo Nhiều Component

**Ví dụ:**
```
Create a services page that displays:
- For each service in the database, create a service card showing:
  - Service name
  - Description
  - Price
  - "Learn More" button
- Arrange cards in a responsive grid (3 columns on desktop, 1 on mobile)
(Tạo một trang dịch vụ hiển thị:
- Đối với mỗi dịch vụ trong cơ sở dữ liệu, tạo một thẻ dịch vụ hiển thị:
  - Tên dịch vụ
  - Mô tả
  - Giá
  - Nút "Tìm hiểu thêm"
- Sắp xếp các thẻ trong lưới responsive (3 cột trên máy tính để bàn, 1 trên di động))
```

#### Mẫu 3: Form Động

**Ví dụ:**
```
Create a dynamic survey form that:
- Loads questions from the database
- For each question, displays:
  - Question text
  - Appropriate input type (text, multiple choice, rating, etc.)
  - Required/optional indicator
- Validates and submits all answers together
(Tạo một form khảo sát động:
- Tải các câu hỏi từ cơ sở dữ liệu
- Đối với mỗi câu hỏi, hiển thị:
  - Văn bản câu hỏi
  - Loại đầu vào phù hợp (văn bản, trắc nghiệm, đánh giá, v.v.)
  - Chỉ báo bắt buộc/tùy chọn
- Xác thực và gửi tất cả các câu trả lời cùng nhau)
```

### Các Mẫu Vòng lặp Nâng cao

#### Mẫu 4: Vòng lặp Lồng nhau

**Ví dụ:**
```
Create a category page that shows:
- For each category:
  - Category name and description
  - For each product in that category:
    - Product card with image, name, price
  - "View All" link for the category
- Organize categories in sections
(Tạo một trang danh mục hiển thị:
- Đối với mỗi danh mục:
  - Tên và mô tả danh mục
  - Đối với mỗi sản phẩm trong danh mục đó:
    - Thẻ sản phẩm với hình ảnh, tên, giá
  - Liên kết "Xem tất cả" cho danh mục
- Tổ chức các danh mục thành các phần)
```

#### Mẫu 5: Vòng lặp Có điều kiện

**Ví dụ:**
```
Create a task dashboard that:
- For each task category (Work, Personal, Shopping):
  - Show category header
  - For each task in that category:
    - If task is not completed: Show full task card
    - If task is completed: Show collapsed/minimized card
  - Show category statistics (total, completed, pending)
(Tạo một bảng điều khiển công việc:
- Đối với mỗi danh mục công việc (Công việc, Cá nhân, Mua sắm):
  - Hiển thị tiêu đề danh mục
  - Đối với mỗi công việc trong danh mục đó:
    - Nếu công việc chưa hoàn thành: Hiển thị thẻ công việc đầy đủ
    - Nếu công việc đã hoàn thành: Hiển thị thẻ thu gọn/tối thiểu hóa
  - Hiển thị thống kê danh mục (tổng số, đã hoàn thành, đang chờ))
```

**💡 Mẹo cho người mới bắt đầu:** Vòng lặp rất mạnh mẽ! Sử dụng chúng bất cứ khi nào bạn cần hiển thị nhiều mục tương tự.

---

## 📖 Bài học 4: Luồng Người dùng Phức tạp

### Luồng Người dùng là gì?

**Luồng người dùng (User flows)** là các đường dẫn người dùng đi qua ứng dụng của bạn để hoàn thành các tác vụ. Các luồng phức tạp có nhiều bước và quyết định.

### Các Mẫu Luồng Nhiều Bước

#### Mẫu 1: Wizard/Luồng Onboarding

**Ví dụ:**
```
Create a multi-step onboarding wizard:
- Step 1: Welcome and account setup
- Step 2: Profile information (name, bio, preferences)
- Step 3: Choose interests/categories
- Step 4: Set preferences and notifications
- Step 5: Confirmation and completion
Each step should:
- Save progress (so users can go back)
- Show progress indicator
- Have "Next" and "Back" buttons
- Validate before proceeding
(Tạo một trình hướng dẫn onboarding nhiều bước:
- Bước 1: Chào mừng và thiết lập tài khoản
- Bước 2: Thông tin hồ sơ (tên, tiểu sử, sở thích)
- Bước 3: Chọn sở thích/danh mục
- Bước 4: Thiết lập tùy chọn và thông báo
- Bước 5: Xác nhận và hoàn thành
Mỗi bước nên:
- Lưu tiến trình (để người dùng có thể quay lại)
- Hiển thị chỉ báo tiến trình
- Có các nút "Tiếp theo" và "Quay lại"
- Xác thực trước khi tiếp tục)
```

#### Mẫu 2: Luồng Thanh toán

**Ví dụ:**
```
Create a checkout process with steps:
- Step 1: Review cart items
- Step 2: Shipping information
- Step 3: Payment method
- Step 4: Order confirmation
- Each step validates before allowing next step
- Show progress: "Step 2 of 4"
- Allow going back to previous steps
- Save information as user progresses
(Tạo một quy trình thanh toán với các bước:
- Bước 1: Xem lại các mục trong giỏ hàng
- Bước 2: Thông tin vận chuyển
- Bước 3: Phương thức thanh toán
- Bước 4: Xác nhận đơn hàng
- Mỗi bước xác thực trước khi cho phép bước tiếp theo
- Hiển thị tiến trình: "Bước 2 trên 4"
- Cho phép quay lại các bước trước
- Lưu thông tin khi người dùng tiến hành)
```

#### Mẫu 3: Quy trình Phê duyệt

**Ví dụ:**
```
Create a content approval system:
- Author creates content → Status: "Draft"
- Author submits for review → Status: "Pending Review"
- Reviewer approves → Status: "Approved" → Published
- Reviewer rejects → Status: "Rejected" → Returned to author with comments
- Show different views based on status and user role
(Tạo một hệ thống phê duyệt nội dung:
- Tác giả tạo nội dung → Trạng thái: "Bản nháp"
- Tác giả gửi để xem xét → Trạng thái: "Đang chờ xem xét"
- Người xem xét phê duyệt → Trạng thái: "Đã phê duyệt" → Đã xuất bản
- Người xem xét từ chối → Trạng thái: "Đã từ chối" → Trả lại cho tác giả với nhận xét
- Hiển thị các chế độ xem khác nhau dựa trên trạng thái và vai trò người dùng)
```

### Các Mẫu Quản lý Trạng thái

#### Mẫu 4: Quản lý Trạng thái Form

**Ví dụ:**
```
Create a complex form that:
- Saves progress automatically as user types
- Shows which fields are completed
- Validates fields in real-time
- Shows error messages immediately
- Allows saving as draft
- Prevents data loss if user navigates away
(Tạo một form phức tạp:
- Lưu tiến trình tự động khi người dùng nhập
- Hiển thị các trường nào đã hoàn thành
- Xác thực các trường trong thời gian thực
- Hiển thị thông báo lỗi ngay lập tức
- Cho phép lưu dưới dạng bản nháp
- Ngăn mất dữ liệu nếu người dùng điều hướng đi nơi khác)
```

#### Mẫu 5: Đa chọn với Phụ thuộc

**Ví dụ:**
```
Create a product configuration form where:
- User selects product type → Shows relevant options
- User selects size → Updates available colors
- User selects color → Updates available materials
- Each selection updates what's available next
- Shows running total price
- Validates that all required selections are made
(Tạo một form cấu hình sản phẩm nơi:
- Người dùng chọn loại sản phẩm → Hiển thị các tùy chọn liên quan
- Người dùng chọn kích thước → Cập nhật các màu có sẵn
- Người dùng chọn màu → Cập nhật các vật liệu có sẵn
- Mỗi lựa chọn cập nhật những gì có sẵn tiếp theo
- Hiển thị tổng giá đang chạy
- Xác thực rằng tất cả các lựa chọn bắt buộc đã được thực hiện)
```

**💡 Mẹo cho người mới bắt đầu:** Chia các luồng phức tạp thành các bước rõ ràng. Kiểm thử từng bước trước khi xây dựng bước tiếp theo.

---

## 📖 Bài học 5: Cấu trúc Prompt Nâng cao

### Mẫu 1: Tạo Dựa trên Mẫu (Template-Based Generation)

**Ví dụ:**
```
Create email templates for different scenarios:
- Welcome email (when user signs up)
- Password reset email
- Order confirmation email
- Newsletter email
Each template should:
- Use user's name dynamically
- Include relevant information
- Match brand styling
- Be responsive for email clients
(Tạo các mẫu email cho các kịch bản khác nhau:
- Email chào mừng (khi người dùng đăng ký)
- Email đặt lại mật khẩu
- Email xác nhận đơn hàng
- Email bản tin
Mỗi mẫu nên:
- Sử dụng tên người dùng một cách linh hoạt
- Bao gồm thông tin liên quan
- Phù hợp với phong cách thương hiệu
- Responsive cho các ứng dụng email)
```

### Mẫu 2: Kết hợp Component (Component Composition)

**Ví dụ:**
```
Build a dashboard using reusable components:
- Header component (used on all pages)
- Stats card component (reused for different metrics)
- Chart component (used for different data visualizations)
- Action button component (consistent across app)
Each component should be flexible and reusable
(Xây dựng một bảng điều khiển sử dụng các component tái sử dụng:
- Component Header (được sử dụng trên tất cả các trang)
- Component thẻ thống kê (được tái sử dụng cho các chỉ số khác nhau)
- Component biểu đồ (được sử dụng cho các trực quan hóa dữ liệu khác nhau)
- Component nút hành động (nhất quán trên toàn ứng dụng)
Mỗi component nên linh hoạt và có thể tái sử dụng)
```

### Mẫu 3: Chuyển đổi Dữ liệu (Data Transformation)

**Ví dụ:**
```
Create a data display that:
- Fetches raw data from API
- Transforms it: formats dates, calculates totals, groups by category
- Displays in user-friendly format:
  - Charts for numerical data
  - Tables for structured data
  - Cards for individual items
- Updates when data changes
(Tạo một màn hình hiển thị dữ liệu:
- Lấy dữ liệu thô từ API
- Chuyển đổi nó: định dạng ngày tháng, tính tổng, nhóm theo danh mục
- Hiển thị ở định dạng thân thiện với người dùng:
  - Biểu đồ cho dữ liệu số
  - Bảng cho dữ liệu có cấu trúc
  - Thẻ cho các mục riêng lẻ
- Cập nhật khi dữ liệu thay đổi)
```

### Mẫu 4: Các Mẫu Hướng Sự kiện (Event-Driven Patterns)

**Ví dụ:**
```
Create an interactive app where:
- User actions trigger updates:
  - Clicking "Like" updates like count immediately
  - Adding to cart updates cart icon badge
  - Submitting form shows success message
- Multiple components update based on same action
- Changes reflect immediately without page refresh
(Tạo một ứng dụng tương tác nơi:
- Hành động của người dùng kích hoạt cập nhật:
  - Nhấp vào "Thích" cập nhật số lượt thích ngay lập tức
  - Thêm vào giỏ hàng cập nhật huy hiệu biểu tượng giỏ hàng
  - Gửi form hiển thị thông báo thành công
- Nhiều component cập nhật dựa trên cùng một hành động
- Các thay đổi phản ánh ngay lập tức mà không cần tải lại trang)
```

---

## 🛠️ Thực hành

### Thực hành 1: Hiển thị Sản phẩm Động

**Thử thách:** Tạo một danh sách sản phẩm hiển thị thông tin khác nhau dựa trên trạng thái sản phẩm.

**Yêu cầu:**
- Hiển thị sản phẩm từ cơ sở dữ liệu
- Hiển thị huy hiệu "Còn hàng" cho các sản phẩm có sẵn
- Hiển thị huy hiệu "Giảm giá" cho các sản phẩm được giảm giá
- Hiển thị huy hiệu "Mới" cho các sản phẩm mới được thêm vào
- Kiểu dáng khác nhau cho mỗi trạng thái
- Sản phẩm có thể có nhiều huy hiệu

**💡 Gợi ý:** Sử dụng logic điều kiện trong prompt của bạn để xử lý các trạng thái khác nhau.

### Thực hành 2: Form Nhiều Bước

**Thử thách:** Tạo một form đăng ký với 3 bước.

**Yêu cầu:**
- Bước 1: Thông tin cơ bản (tên, email)
- Bước 2: Sở thích (sở thích, bản tin)
- Bước 3: Xác nhận
- Chỉ báo tiến trình
- Có thể quay lại các bước trước
- Xác thực từng bước

**💡 Gợi ý:** Xây dựng từng bước một, sau đó kết nối chúng.

### Thực hành 3: Bảng điều khiển Có điều kiện

**Thử thách:** Tạo một bảng điều khiển thay đổi dựa trên vai trò người dùng.

**Yêu cầu:**
- Người dùng quản trị thấy: Tất cả người dùng, thống kê hệ thống, công cụ quản trị
- Người dùng thường thấy: Dữ liệu của riêng họ, thống kê cá nhân
- Người dùng khách thấy: Bản xem trước hạn chế, lời nhắc đăng ký
- Cùng một trang, nội dung khác nhau

**💡 Gợi ý:** Sử dụng logic điều kiện để hiển thị/ẩn các phần dựa trên vai trò người dùng.

---

## ✅ Danh sách Kiểm tra Module 11

Trước khi chuyển sang module tiếp theo, hãy đảm bảo bạn có thể:

- [ ] Tạo nội dung động thay đổi dựa trên dữ liệu
- [ ] Sử dụng logic điều kiện trong các prompt
- [ ] Tạo các vòng lặp để hiển thị nhiều mục
- [ ] Xây dựng các luồng người dùng nhiều bước
- [ ] Xử lý quản lý trạng thái phức tạp
- [ ] Sử dụng các mẫu prompt nâng cao một cách hiệu quả

---

## 🤔 Các Câu Hỏi Thường Gặp (FAQ)

### Q: Các prompt có thể phức tạp đến mức nào?
**A:** Rất phức tạp! Nhưng hãy bắt đầu đơn giản và xây dựng dần lên. Chia các yêu cầu phức tạp thành các phần nhỏ hơn.

### Q: Tôi có nên sử dụng các mẫu này cho các dự án đơn giản không?
**A:** Không phải lúc nào cũng vậy. Sử dụng các prompt đơn giản cho các dự án đơn giản. Sử dụng các mẫu nâng cao khi bạn cần sự phức tạp.

### Q: Nếu logic điều kiện của tôi không hoạt động thì sao?
**A:** Hãy chia nhỏ nó ra. Kiểm thử từng điều kiện riêng biệt, sau đó kết hợp chúng.

### Q: Tôi có thể kết hợp nhiều mẫu không?
**A:** Có! Các ứng dụng nâng cao thường sử dụng nhiều mẫu cùng nhau.

---

## 🎯 Tiếp theo là gì?

Làm tốt lắm! Bây giờ bạn đã hiểu các mẫu prompt nâng cao. Những kỹ thuật này giúp bạn xây dựng các ứng dụng tinh vi hơn.

**Tiếp tục học với:**
- Module 12: Hiệu suất và Tối ưu hóa
- Module 13: Tích hợp API Nâng cao
- Hoặc quay lại Module 9 để xây dựng dự án capstone của bạn!

---

*Module 11 Hoàn thành! 🎉*
