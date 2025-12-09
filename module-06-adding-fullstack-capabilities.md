# Module 6: Adding Full-Stack Capabilities - Sức mạnh của Backend

**Mục tiêu:** Hiểu cách thêm xác thực, cơ sở dữ liệu và tích hợp

**Thời gian ước tính:** 45-60 phút

---

## 🎯 Bạn sẽ học được gì trong module này

Vào cuối module này, bạn sẽ:
- Hiểu "full-stack" nghĩa là gì
- Biết cách kích hoạt Lovable Cloud
- Hiểu về Connectors (Bộ kết nối) và cách sử dụng chúng
- Học cách thêm xác thực người dùng
- Học cách thêm cơ sở dữ liệu
- Hiểu cách tích hợp API
- Biết các phương pháp bảo mật tốt nhất
- Có thể xây dựng các ứng dụng mạnh mẽ hơn

---

## 📖 Bài học 1: Full-Stack là gì?

### Frontend vs. Backend

- **Frontend:** Những gì người dùng nhìn thấy và tương tác (nút, văn bản, hình ảnh). Đây là những gì chúng ta đã xây dựng cho đến nay.
- **Backend:** "Bộ não" đằng sau hậu trường (lưu trữ dữ liệu, xử lý thanh toán, đăng nhập người dùng).
- **Full-Stack:** Kết hợp cả hai!

### Tại sao bạn cần Full-Stack?

Bạn cần các khả năng backend nếu bạn muốn:
- Người dùng đăng nhập và có tài khoản
- Lưu trữ dữ liệu (bài đăng blog, bình luận, hồ sơ)
- Xử lý thanh toán
- Gửi email
- Kết nối với các dịch vụ khác (Google Maps, AI, v.v.)

**Tin tốt:** Lovable làm cho việc thêm các tính năng backend trở nên dễ dàng như việc yêu cầu chúng!

---

## 📖 Bài học 2: Lovable Cloud - Backend tích hợp sẵn của bạn

### Lovable Cloud là gì?

**Lovable Cloud** là giải pháp backend tích hợp sẵn của Lovable. Nó cung cấp cho bạn mọi thứ bạn cần mà không cần thiết lập phức tạp.

### Nó bao gồm những gì?

- **Cơ sở dữ liệu:** Để lưu trữ dữ liệu của bạn
- **Xác thực:** Để đăng nhập người dùng
- **Lưu trữ:** Để tải lên tệp và hình ảnh
- **Edge Functions:** Để chạy mã backend an toàn

### Cách kích hoạt Lovable Cloud

1. Mở dự án của bạn
2. Nhấp vào biểu tượng **Cloud** (đám mây) trên thanh công cụ
3. Nhấp vào **"Enable Lovable Cloud"** (Kích hoạt Lovable Cloud)

Đó là tất cả! Bây giờ dự án của bạn đã có một backend đầy đủ sức mạnh.

### Khi nào nên sử dụng Lovable Cloud

- ✅ Hầu hết các dự án mới
- ✅ Khi bạn muốn thiết lập nhanh nhất
- ✅ Khi bạn cần xác thực và cơ sở dữ liệu tiêu chuẩn
- ✅ Khi bạn không muốn quản lý các máy chủ riêng biệt

---

## 📖 Bài học 3: Connectors - Kết nối với thế giới

### Connectors là gì?

**Connectors** (Bộ kết nối) giống như những cây cầu nối dự án Lovable của bạn với các dịch vụ bên ngoài. Chúng cho phép bạn sử dụng các công cụ mạnh mẽ mà không cần viết mã phức tạp.

### Các Connector phổ biến

- **Supabase:** Cơ sở dữ liệu và xác thực mạnh mẽ (nếu bạn cần nhiều hơn Lovable Cloud)
- **Stripe:** Xử lý thanh toán
- **Resend:** Gửi email
- **OpenAI:** Các tính năng AI
- **Google Maps:** Bản đồ và vị trí

### Cách Connectors hoạt động

1. **Cấu hình một lần** - Thiết lập connector trong cài đặt không gian làm việc của bạn
2. **Sử dụng mọi nơi** - Sử dụng nó trong bất kỳ dự án nào
3. **Lovable xử lý kết nối** - Bạn chỉ cần yêu cầu các tính năng
4. **An toàn** - Thông tin xác thực được lưu trữ an toàn

### Thiết lập một Connector

#### Bước 1: Lấy khóa API

Hầu hết các connector yêu cầu khóa API (giống như mật khẩu cho các dịch vụ):
1. Đăng ký dịch vụ (Supabase, Stripe, v.v.)
2. Lấy khóa API của bạn từ bảng điều khiển của họ
3. Giữ chúng an toàn (như mật khẩu)

#### Bước 2: Thêm vào Lovable

1. Đi tới **Settings** (Cài đặt) → **Integrations** (Tích hợp) → **Connectors**
2. Nhấp vào **"Add Connector"** (Thêm Connector)
3. Chọn dịch vụ (Supabase, Stripe, v.v.)
4. Nhập khóa API của bạn
5. Lưu

#### Bước 3: Sử dụng trong dự án của bạn

Sau khi cấu hình, chỉ cần yêu cầu:

```
Add Stripe checkout to this product page
(Thêm thanh toán Stripe vào trang sản phẩm này)
```

```
Use Supabase for user authentication
(Sử dụng Supabase để xác thực người dùng)
```

### Ví dụ thực tế: Kết nối dịch vụ

#### Ví dụ 1: Kết nối Supabase

**Bước 1: Lấy thông tin xác thực Supabase**
1. Đăng ký tại [supabase.com](https://supabase.com)
2. Tạo một dự án mới
3. Đi tới **Settings** → **API**
4. Sao chép:
   - **Project URL** (ví dụ: `https://yourproject.supabase.co`)
   - **Anon/Public Key** (an toàn để sử dụng ở frontend)
   - **Service Role Key** (giữ bí mật - chỉ dành cho backend)

**Bước 2: Thêm vào Lovable**
1. Đi tới **Settings** → **Integrations** → **Connectors**
2. Nhấp vào **"Add Connector"**
3. Chọn **"Supabase"**
4. Nhập Project URL và khóa API của bạn
5. Lưu

**Bước 3: Sử dụng Supabase trong dự án của bạn**

**Cho Xác thực:**
```
Use Supabase for user authentication. Create sign up and login pages that connect to Supabase Auth.
(Sử dụng Supabase để xác thực người dùng. Tạo các trang đăng ký và đăng nhập kết nối với Supabase Auth.)
```

**Cho Cơ sở dữ liệu:**
```
Set up Supabase database for storing blog posts. Create a table called 'posts' with fields: id, title, content, author_id, created_at.
(Thiết lập cơ sở dữ liệu Supabase để lưu trữ các bài đăng blog. Tạo một bảng gọi là 'posts' với các trường: id, title, content, author_id, created_at.)
```

**Cho Lưu trữ:**
```
Use Supabase Storage for uploading user profile pictures. Add an upload component to the profile page.
(Sử dụng Supabase Storage để tải lên ảnh hồ sơ người dùng. Thêm thành phần tải lên vào trang hồ sơ.)
```

#### Ví dụ 2: Kết nối Stripe

**Bước 1: Lấy khóa Stripe**
1. Đăng ký tại [stripe.com](https://stripe.com)
2. Đi tới **Developers** → **API keys**
3. Sao chép:
   - **Publishable Key** (bắt đầu bằng `pk_` - an toàn cho frontend)
   - **Secret Key** (bắt đầu bằng `sk_` - giữ bí mật!)

**⚠️ QUAN TRỌNG:** Không bao giờ chia sẻ Secret Key của bạn! Nó giống như một mật khẩu.

**Bước 2: Thêm vào Lovable**
1. Đi tới **Settings** → **Integrations** → **Connectors**
2. Nhấp vào **"Add Connector"**
3. Chọn **"Stripe"**
4. Nhập **Publishable Key** và **Secret Key** của bạn
5. Lưu

**Bước 3: Sử dụng Stripe trong dự án của bạn**

**Cho Thanh toán một lần:**
```
Add Stripe payment to this product page. When user clicks "Buy Now", show Stripe checkout for $29.99.
(Thêm thanh toán Stripe vào trang sản phẩm này. Khi người dùng nhấp vào "Mua ngay", hiển thị thanh toán Stripe với giá $29.99.)
```

**Cho Đăng ký:**
```
Add Stripe subscription to this page. Create a monthly subscription plan for $9.99/month with Stripe Checkout.
(Thêm đăng ký Stripe vào trang này. Tạo gói đăng ký hàng tháng với giá $9.99/tháng với Stripe Checkout.)
```

**Cho Biểu mẫu thanh toán:**
```
Create a payment form using Stripe Elements. Include card number, expiry, and CVC fields. Process payment when form is submitted.
(Tạo biểu mẫu thanh toán sử dụng Stripe Elements. Bao gồm các trường số thẻ, ngày hết hạn và CVC. Xử lý thanh toán khi biểu mẫu được gửi.)
```

**💡 Mẹo cho người mới:** Bắt đầu với Lovable Cloud. Chỉ thêm các connector khi bạn cần các tính năng cụ thể mà chúng cung cấp.

---

## 📖 Bài học 4: MCP Servers - Cung cấp ngữ cảnh

### MCP Servers là gì?

**MCP Servers** (Model Context Protocol) cung cấp cho Lovable quyền truy cập vào các công cụ và dữ liệu hiện có của bạn. Chúng giúp Lovable hiểu ngữ cảnh của bạn tốt hơn.

### MCP Servers làm gì

MCP Servers:
- Kết nối với các công cụ hiện có của bạn (Linear, Notion, v.v.)
- Cung cấp ngữ cảnh trong quá trình tạo ứng dụng
- Giúp Lovable hiểu quy trình làm việc của bạn
- Chỉ được sử dụng trong khi xây dựng (không có trong ứng dụng cuối cùng)

### Các MCP Server phổ biến

#### Linear - Quản lý dự án

**Nó làm gì:**
- Nhập các vấn đề và thông số kỹ thuật
- Hiểu các yêu cầu dự án của bạn
- Xây dựng các tính năng dựa trên vé (ticket) của bạn

**Khi nào nên sử dụng:**
- Bạn sử dụng Linear để quản lý dự án
- Bạn muốn xây dựng từ các vé của mình
- Bạn có thông số kỹ thuật chi tiết trong Linear

#### Notion - Tài liệu

**Nó làm gì:**
- Đọc các trang Notion của bạn
- Sử dụng tài liệu của bạn làm ngữ cảnh
- Xây dựng dựa trên ghi chú của bạn

**Khi nào nên sử dụng:**
- Bạn ghi chép tài liệu trong Notion
- Bạn muốn xây dựng từ tài liệu của mình
- Bạn có các yêu cầu trong Notion

#### Atlassian (Jira/Confluence)

**Nó làm gì:**
- Truy cập vé Jira
- Đọc tài liệu Confluence
- Xây dựng từ thông số kỹ thuật của bạn

**Khi nào nên sử dụng:**
- Nhóm của bạn sử dụng các công cụ Atlassian
- Bạn có thông số kỹ thuật trong Jira/Confluence
- Bạn muốn xây dựng từ vé

### Cách MCP Servers hoạt động

1. **Cấu hình máy chủ** - Kết nối nó với công cụ của bạn
2. **Lovable sử dụng nó trong khi xây dựng** - Cung cấp ngữ cảnh
3. **Không bao gồm trong ứng dụng cuối cùng** - Chỉ được sử dụng trong quá trình phát triển
4. **Giúp xây dựng ứng dụng tốt hơn** - Lovable hiểu nhu cầu của bạn

**💡 Mẹo cho người mới:** MCP Servers là nâng cao. Bạn có thể bỏ qua chúng bây giờ và thêm chúng sau nếu cần.

---

## 📖 Bài học 5: Tích hợp bất kỳ API nào

### API là gì?

**API** (Application Programming Interface) là cách các dịch vụ khác nhau nói chuyện với nhau. Hãy nghĩ về nó giống như một thực đơn tại nhà hàng - nó cho bạn biết bạn có thể gọi món gì.

### Tại sao tích hợp API?

API cho phép bạn:
- Sử dụng dữ liệu từ các dịch vụ khác
- Thêm các tính năng bạn không tự xây dựng
- Kết nối với các công cụ bên ngoài
- Mở rộng khả năng của ứng dụng

### Các loại API

#### API Công khai (Không cần xác thực)

Những API này không yêu cầu mật khẩu/khóa:

**Ví dụ:**
- Dữ liệu thời tiết
- Thông tin công cộng
- Dịch vụ miễn phí

**Cách sử dụng:**
```
Integrate the weather API: https://api.weather.com/forecast
(Tích hợp API thời tiết: https://api.weather.com/forecast)
```

Lovable phát hiện không cần xác thực và thêm nó trực tiếp!

#### API Riêng tư (Yêu cầu xác thực)

Những API này cần khóa API (giống như mật khẩu):

**Ví dụ:**
- Xử lý thanh toán
- Dữ liệu người dùng
- Dịch vụ riêng tư

**Cách sử dụng:**
1. **Yêu cầu Lovable tích hợp:**
   ```
   Integrate the OpenWeatherMap API for weather data.
   Base URL: https://api.openweathermap.org/data/2.5
   Auth: API key passed as appid parameter
   (Tích hợp API OpenWeatherMap cho dữ liệu thời tiết.
   URL cơ sở: https://api.openweathermap.org/data/2.5
   Xác thực: Khóa API được truyền dưới dạng tham số appid)
   ```
2. **Kích hoạt Lovable Cloud** (nếu chưa kích hoạt)
3. **Thêm khóa API của bạn:**
   - Đi tới **Cloud** → **Secrets**
   - Thêm khóa API của bạn
   - Lưu nó an toàn
4. **Lovable tạo tích hợp** - Sử dụng Edge Functions để giữ an toàn cho các khóa

### Hiểu về Khóa API Công khai vs. Riêng tư

**Khóa API Công khai:**
- ✅ An toàn để sử dụng trong mã frontend
- ✅ Có thể hiển thị trong trình duyệt
- ✅ Quyền hạn hạn chế
- ✅ Ví dụ: Stripe Publishable Key (bắt đầu bằng `pk_`), Supabase Anon Key
- ⚠️ Vẫn nên được giữ an toàn hợp lý

**Khóa API Riêng tư/Bí mật:**
- ❌ **KHÔNG BAO GIỜ** để lộ trong mã frontend
- ❌ **KHÔNG BAO GIỜ** đặt trong câu lệnh hoặc mã
- ❌ **PHẢI** được lưu trữ trong trình quản lý bí mật (secrets manager)
- ✅ Quyền truy cập đầy đủ vào tài khoản
- ✅ Ví dụ: Stripe Secret Key (bắt đầu bằng `sk_`), Supabase Service Role Key

**⚠️ QUY TẮC QUAN TRỌNG:** Khóa riêng tư PHẢI LUÔN được lưu trữ trong Trình quản lý bí mật của Lovable, không bao giờ trong mã hoặc câu lệnh của bạn!

**Cách Lovable bảo vệ khóa:**
- Khóa được lưu trữ trong **Cloud → Secrets**
- Chỉ truy cập thông qua **Edge Functions** (phía máy chủ)
- Không bao giờ để lộ cho frontend
- Được mã hóa và an toàn

### Các API phổ biến bạn có thể sử dụng

- **Weather APIs** - Hiển thị dữ liệu thời tiết
- **Maps APIs** - Hiển thị vị trí
- **Social Media APIs** - Chia sẻ lên các nền tảng xã hội
- **Payment APIs** - Xử lý thanh toán
- **Email APIs** - Gửi email
- **Analytics APIs** - Theo dõi việc sử dụng

**💡 Mẹo cho người mới:** Bắt đầu với các API công khai đơn giản để học. Sau đó chuyển sang các API có xác thực khi cần.

---

## 📖 Bài học 6: Các phương pháp bảo mật tốt nhất

### Tại sao bảo mật lại quan trọng

**Bảo mật** bảo vệ ứng dụng và người dùng của bạn khỏi:
- Truy cập trái phép
- Vi phạm dữ liệu
- Gian lận thanh toán
- Các cuộc tấn công độc hại

**Xây dựng ứng dụng an toàn là điều cần thiết!** Ngay cả người mới bắt đầu cũng cần hiểu những điều cơ bản về bảo mật.

### Cách Lovable xử lý bảo mật

**Tin tốt:** Lovable tự động xử lý nhiều mối lo ngại về bảo mật! Nhưng bạn vẫn cần tuân theo các phương pháp tốt nhất.

#### Các tính năng bảo mật tự động

Lovable tự động:
- ✅ **Băm mật khẩu** - Mật khẩu không bao giờ được lưu trữ dưới dạng văn bản thuần túy
- ✅ **Bảo vệ khóa API** - Khóa được lưu trữ an toàn trong trình quản lý bí mật
- ✅ **Sử dụng HTTPS** - Tất cả các kết nối đều được mã hóa
- ✅ **Xác thực đầu vào** - Ngăn chặn các cuộc tấn công phổ biến
- ✅ **Quản lý phiên** - Phiên người dùng an toàn

**Bạn không cần phải viết mã cho những thứ này!** Lovable làm điều đó cho bạn.

### Các phương pháp bảo mật tốt nhất

#### 1. Bảo vệ khóa API

**❌ KHÔNG BAO GIỜ làm điều này:**
```
Add my Stripe key: sk_live_1234567890
```

**❌ KHÔNG BAO GIỜ đặt khóa trong câu lệnh:**
```
Use API key abc123xyz in the code
```

**✅ LUÔN LUÔN làm điều này:**
1. **Lưu trữ khóa trong Secrets Manager:**
   - Đi tới **Cloud** → **Secrets**
   - Thêm khóa của bạn
   - Đặt tên cho nó (ví dụ: "STRIPE_SECRET_KEY")
   - Lưu

2. **Tham chiếu khóa theo tên:**
   ```
   Use the Stripe connector I've configured in settings
   (Sử dụng connector Stripe tôi đã cấu hình trong cài đặt)
   ```

3. **Lovable truy cập khóa an toàn:**
   - Khóa ở trong trình quản lý bí mật
   - Chỉ truy cập phía máy chủ
   - Không bao giờ để lộ cho frontend

**Ví dụ - Cách đúng:**
```
1. Add Stripe Secret Key to Cloud → Secrets (name it STRIPE_SECRET_KEY)
2. Then ask: "Add Stripe payment processing using the configured Stripe connector"
(1. Thêm Stripe Secret Key vào Cloud → Secrets (đặt tên là STRIPE_SECRET_KEY)
2. Sau đó yêu cầu: "Thêm xử lý thanh toán Stripe sử dụng connector Stripe đã cấu hình")
```

#### 2. Bảo mật mật khẩu

**Cách Lovable xử lý mật khẩu:**

- ✅ **Tự động băm** - Mật khẩu được băm (mã hóa) trước khi lưu trữ
- ✅ **Không bao giờ lưu trữ văn bản thuần túy** - Bạn không thể nhìn thấy mật khẩu thực tế
- ✅ **So sánh an toàn** - Mật khẩu được xác minh an toàn
- ✅ **Tích hợp các phương pháp tốt nhất** - Không cần tự viết mã này

**Những gì bạn nên làm:**
- ✅ Yêu cầu mật khẩu mạnh (Lovable có thể thực thi điều này)
- ✅ Sử dụng các trường xác nhận mật khẩu
- ✅ Thêm chức năng đặt lại mật khẩu
- ✅ Không bao giờ ghi nhật ký hoặc hiển thị mật khẩu

**Ví dụ câu lệnh:**
```
Add password requirements: minimum 8 characters, must include uppercase, lowercase, and number
(Thêm yêu cầu mật khẩu: tối thiểu 8 ký tự, phải bao gồm chữ hoa, chữ thường và số)
```

#### 3. Giới hạn tốc độ (Rate Limiting)

**Giới hạn tốc độ là gì?**

Giới hạn tốc độ ngăn chặn lạm dụng bằng cách giới hạn số lượng yêu cầu mà người dùng có thể thực hiện.

**Tại sao nó quan trọng:**
- Ngăn chặn thư rác
- Ngăn chặn các cuộc tấn công brute force
- Bảo vệ tài nguyên của bạn
- Giữ chi phí thấp

**Cách Lovable xử lý nó:**

Lovable Cloud bao gồm giới hạn tốc độ tự động:
- ✅ Giới hạn nỗ lực đăng nhập
- ✅ Ngăn chặn lạm dụng API
- ✅ Bảo vệ chống lại các cuộc tấn công
- ✅ Giới hạn có thể cấu hình

**Những gì bạn có thể làm:**
```
Add rate limiting to the contact form: maximum 5 submissions per hour per user
(Thêm giới hạn tốc độ vào biểu mẫu liên hệ: tối đa 5 lần gửi mỗi giờ cho mỗi người dùng)
```

#### 4. Xác thực đầu vào

**Xác thực đầu vào là gì?**

Kiểm tra xem đầu vào của người dùng có an toàn và chính xác không trước khi sử dụng nó.

**Tại sao nó quan trọng:**
- Ngăn chặn tiêm mã độc hại
- Đảm bảo dữ liệu đúng định dạng
- Bảo vệ cơ sở dữ liệu của bạn
- Cải thiện trải nghiệm người dùng

**Cách Lovable xử lý nó:**

Lovable tự động:
- ✅ Xác thực đầu vào biểu mẫu
- ✅ Làm sạch dữ liệu người dùng
- ✅ Ngăn chặn SQL injection
- ✅ Chặn mã độc hại

**Những gì bạn nên làm:**
- ✅ Chỉ định yêu cầu xác thực trong câu lệnh
- ✅ Kiểm tra biểu mẫu với dữ liệu không hợp lệ
- ✅ Thêm thông báo lỗi hữu ích

**Ví dụ:**
```
Create a contact form with validation:
- Email must be valid email format
- Name must be at least 2 characters
- Message must be between 10 and 1000 characters
- Show clear error messages for invalid inputs
(Tạo biểu mẫu liên hệ với xác thực:
- Email phải đúng định dạng email
- Tên phải có ít nhất 2 ký tự
- Tin nhắn phải từ 10 đến 1000 ký tự
- Hiển thị thông báo lỗi rõ ràng cho đầu vào không hợp lệ)
```

#### 5. Bảo mật xác thực người dùng

**Các phương pháp tốt nhất:**

**✅ Nên:**
- Sử dụng yêu cầu mật khẩu mạnh
- Triển khai thời gian chờ phiên
- Thêm "Ghi nhớ tôi" một cách an toàn
- Sử dụng HTTPS (tự động với Lovable)
- Đăng xuất người dùng sau khi không hoạt động

**❌ Không nên:**
- Lưu trữ mật khẩu dưới dạng văn bản thuần túy (Lovable ngăn chặn điều này)
- Hiển thị lỗi mật khẩu tiết lộ email có tồn tại hay không
- Cho phép nỗ lực đăng nhập không giới hạn
- Lưu trữ dữ liệu nhạy cảm ở frontend

**Ví dụ câu lệnh:**
```
Add session timeout: log users out after 30 minutes of inactivity
(Thêm thời gian chờ phiên: đăng xuất người dùng sau 30 phút không hoạt động)
```

```
Add login attempt limiting: lock account after 5 failed attempts
(Thêm giới hạn nỗ lực đăng nhập: khóa tài khoản sau 5 lần thử thất bại)
```

#### 6. Bảo vệ dữ liệu

**Những gì cần bảo vệ:**
- Thông tin cá nhân người dùng
- Dữ liệu thanh toán
- Khóa API và bí mật
- Mã thông báo xác thực

**Cách bảo vệ:**

**✅ Sử dụng Biến môi trường:**
- Lưu trữ cấu hình nhạy cảm trong secrets
- Không bao giờ mã hóa cứng dữ liệu nhạy cảm
- Sử dụng các khóa khác nhau cho phát triển/sản xuất

**✅ Mã hóa dữ liệu nhạy cảm:**
- Lovable mã hóa dữ liệu khi truyền tải (HTTPS)
- Mã hóa cơ sở dữ liệu được xử lý tự động
- Lưu trữ tệp an toàn

**✅ Giới hạn truy cập dữ liệu:**
```
Make sure users can only see and edit their own data, not other users' data
(Đảm bảo người dùng chỉ có thể xem và chỉnh sửa dữ liệu của chính họ, không phải dữ liệu của người dùng khác)
```

#### 7. Bảo mật API

**Cho API Công khai:**
- ✅ Thường an toàn để sử dụng trực tiếp
- ✅ Không cần xác thực
- ✅ Chức năng hạn chế
- ⚠️ Vẫn xác thực phản hồi

**Cho API Riêng tư:**
- ✅ **LUÔN LUÔN** sử dụng trình quản lý bí mật
- ✅ **KHÔNG BAO GIỜ** đặt khóa trong mã
- ✅ Sử dụng Edge Functions (Lovable làm điều này)
- ✅ Xác thực tất cả các phản hồi API

**Ví dụ - Tích hợp API an toàn:**
```
1. Add OpenWeatherMap API key to Cloud → Secrets (name it WEATHER_API_KEY)
2. Then: "Integrate OpenWeatherMap API using the key in secrets. Create a weather widget that fetches current weather for a city."
(1. Thêm khóa API OpenWeatherMap vào Cloud → Secrets (đặt tên là WEATHER_API_KEY)
2. Sau đó: "Tích hợp API OpenWeatherMap sử dụng khóa trong secrets. Tạo tiện ích thời tiết lấy thời tiết hiện tại cho một thành phố.")
```

### Danh sách kiểm tra bảo mật

Trước khi triển khai ứng dụng của bạn, hãy kiểm tra:

- [ ] Tất cả các khóa API đều nằm trong trình quản lý bí mật (không phải trong mã)
- [ ] Mật khẩu có các yêu cầu được thực thi
- [ ] Dữ liệu người dùng được bảo vệ (người dùng không thể truy cập dữ liệu của người khác)
- [ ] Các biểu mẫu có xác thực
- [ ] Giới hạn tốc độ được bật (nếu cần)
- [ ] Thông báo lỗi không tiết lộ thông tin nhạy cảm
- [ ] HTTPS được bật (tự động với Lovable)
- [ ] Xác thực hoạt động chính xác
- [ ] Không có dữ liệu nhạy cảm trong mã frontend

### Những sai lầm bảo mật phổ biến cần tránh

**❌ Sai lầm 1: Đặt khóa API trong câu lệnh**
```
Add Stripe with key sk_live_12345
```
**✅ Sửa:** Lưu trữ trong secrets, tham chiếu theo tên

**❌ Sai lầm 2: Không xác thực đầu vào**
```
Create a form (no validation mentioned)
```
**✅ Sửa:** Luôn chỉ định yêu cầu xác thực

**❌ Sai lầm 3: Để lộ dữ liệu người dùng**
```
Show all users' data to everyone
```
**✅ Sửa:** Hạn chế truy cập dữ liệu cho chủ sở hữu

**❌ Sai lầm 4: Mật khẩu yếu**
```
Allow any password
```
**✅ Sửa:** Yêu cầu mật khẩu mạnh

**❌ Sai lầm 5: Không giới hạn tốc độ**
```
Allow unlimited form submissions
```
**✅ Sửa:** Thêm giới hạn tốc độ cho các biểu mẫu công khai

### Nhận trợ giúp về bảo mật

Nếu bạn không chắc chắn về bảo mật:

1. **Hỏi Chế độ Chat:**
   ```
   I'm adding payment processing. What security measures should I have in place?
   (Tôi đang thêm xử lý thanh toán. Tôi nên áp dụng các biện pháp bảo mật nào?)
   ```

2. **Kiểm tra Tài liệu:**
   - Tài liệu bảo mật Lovable
   - Hướng dẫn bảo mật cụ thể của dịch vụ (Stripe, Supabase, v.v.)

3. **Kiểm tra kỹ lưỡng:**
   - Cố gắng phá vỡ ứng dụng của chính bạn
   - Kiểm tra với đầu vào không hợp lệ
   - Kiểm tra xử lý lỗi

**💡 Mẹo cho người mới:** Đừng lo lắng về việc tự triển khai mã bảo mật! Lovable xử lý hầu hết. Chỉ cần tuân theo các phương pháp tốt nhất trong cách bạn sử dụng nó.

---

## 🛠️ Thực hành thực tế: Thêm xác thực

Hãy thêm xác thực người dùng vào một dự án!

### Thực hành: Thêm xác thực người dùng

#### Bước 1: Kích hoạt Backend

Yêu cầu Lovable:
```
Enable Lovable Cloud for this project
(Kích hoạt Lovable Cloud cho dự án này)
```

Hoặc nếu sử dụng Supabase:
```
Connect Supabase for authentication and database
(Kết nối Supabase cho xác thực và cơ sở dữ liệu)
```

#### Bước 2: Thêm xác thực

Yêu cầu Lovable:
```
Add user authentication with:
- Sign up page with email and password
- Login page
- Logout functionality
- Protected routes (pages only logged-in users can see)
(Thêm xác thực người dùng với:
- Trang đăng ký với email và mật khẩu
- Trang đăng nhập
- Chức năng đăng xuất
- Các tuyến được bảo vệ (các trang chỉ người dùng đã đăng nhập mới có thể xem))
```

#### Bước 3: Kiểm tra nó

1. **Thử đăng ký:**
   - Đi tới trang đăng ký
   - Nhập email và mật khẩu
   - Gửi
   - Bạn sẽ được đăng nhập!

2. **Thử đăng xuất:**
   - Nhấp đăng xuất
   - Bạn sẽ được đăng xuất

3. **Thử đăng nhập:**
   - Đi tới trang đăng nhập
   - Nhập thông tin xác thực của bạn
   - Bạn sẽ được đăng nhập!

#### Bước 4: Tùy chỉnh nó

Yêu cầu cải tiến:
```
Make the login page match my brand colors
Add "Remember me" checkbox to login
Add password reset functionality
(Làm cho trang đăng nhập phù hợp với màu sắc thương hiệu của tôi
Thêm hộp kiểm "Ghi nhớ tôi" vào đăng nhập
Thêm chức năng đặt lại mật khẩu)
```

**🎉 Chúc mừng!** Bạn vừa thêm xác thực vào ứng dụng của mình!

---

## 🛠️ Thực hành thực tế: Thêm cơ sở dữ liệu

Hãy thêm cơ sở dữ liệu để lưu trữ dữ liệu!

### Thực hành: Thêm cơ sở dữ liệu cho bài đăng Blog

#### Bước 1: Kích hoạt cơ sở dữ liệu

Nếu sử dụng Lovable Cloud:
```
Add a database to store blog posts
(Thêm cơ sở dữ liệu để lưu trữ các bài đăng blog)
```

Nếu sử dụng Supabase:
```
Set up Supabase database for blog posts
(Thiết lập cơ sở dữ liệu Supabase cho các bài đăng blog)
```

#### Bước 2: Xác định cấu trúc dữ liệu của bạn

Yêu cầu Lovable:
```
Create a database table for blog posts with:
- Title (text)
- Content (text)
- Author (text)
- Date published (date)
- Featured image (image URL)
(Tạo bảng cơ sở dữ liệu cho các bài đăng blog với:
- Tiêu đề (văn bản)
- Nội dung (văn bản)
- Tác giả (văn bản)
- Ngày xuất bản (ngày)
- Hình ảnh nổi bật (URL hình ảnh))
```

#### Bước 3: Tạo các trang để sử dụng cơ sở dữ liệu

Yêu cầu Lovable:
```
Create a blog listing page that shows all posts from the database
(Tạo trang danh sách blog hiển thị tất cả các bài đăng từ cơ sở dữ liệu)
```

```
Create a blog post detail page that shows a single post
(Tạo trang chi tiết bài đăng blog hiển thị một bài đăng đơn lẻ)
```

```
Create an admin page to add new blog posts to the database
(Tạo trang quản trị để thêm các bài đăng blog mới vào cơ sở dữ liệu)
```

#### Bước 4: Kiểm tra nó

1. **Thêm bài đăng:**
   - Đi tới trang quản trị
   - Điền vào biểu mẫu
   - Gửi
   - Bài đăng sẽ được lưu!

2. **Xem bài đăng:**
   - Đi tới trang danh sách blog
   - Xem các bài đăng của bạn!

3. **Xem bài đăng đơn lẻ:**
   - Nhấp vào một bài đăng
   - Xem bài đăng đầy đủ!

**🎉 Chúc mừng!** Bạn vừa thêm cơ sở dữ liệu vào ứng dụng của mình!

---

## 🛠️ Dự án nhỏ: Thêm thanh toán đăng ký Stripe

Hãy xây dựng một trang đăng ký hoàn chỉnh với Stripe! Điều này minh họa việc sử dụng connector trong thực tế.

### Mục tiêu dự án

Tạo một trang đăng ký nơi người dùng có thể:
- Xem các gói đăng ký
- Đăng ký gói hàng tháng
- Xử lý thanh toán an toàn với Stripe
- Xem trạng thái đăng ký

### Bước 1: Thiết lập tài khoản Stripe

**Trước khi bắt đầu:**
1. Đăng ký tại [stripe.com](https://stripe.com) (miễn phí để bắt đầu)
2. Đi tới **Developers** → **API keys**
3. Lấy **khóa thử nghiệm** (test keys) của bạn (để phát triển):
   - **Publishable Key** (bắt đầu bằng `pk_test_`)
   - **Secret Key** (bắt đầu bằng `sk_test_`)

**💡 Lưu ý:** Sử dụng khóa thử nghiệm để phát triển. Chuyển sang khóa trực tiếp (live keys) khi sẵn sàng cho sản xuất.

### Bước 2: Cấu hình Stripe trong Lovable

1. **Đi tới Settings** → **Integrations** → **Connectors**
2. **Nhấp "Add Connector"**
3. **Chọn "Stripe"**
4. **Nhập khóa của bạn:**
   - Publishable Key: `pk_test_...` (khóa thử nghiệm của bạn)
   - Secret Key: `sk_test_...` (khóa thử nghiệm của bạn)
5. **Lưu**

**⚠️ Nhắc nhở bảo mật:** Khóa được lưu trữ an toàn trong trình quản lý bí mật của Lovable, không phải trong mã của bạn!

### Bước 3: Tạo trang các gói đăng ký

Yêu cầu Lovable:
```
Create a subscription plans page with:
- Header: "Choose Your Plan"
- Three subscription tiers:
  1. Basic - $9.99/month - "Perfect for individuals"
  2. Pro - $19.99/month - "Best for professionals"
  3. Enterprise - $49.99/month - "For teams and businesses"
- Each plan should have a "Subscribe" button
- Use a clean, modern card layout
- Make it responsive for mobile
(Tạo trang các gói đăng ký với:
- Tiêu đề: "Chọn gói của bạn"
- Ba cấp độ đăng ký:
  1. Cơ bản - $9.99/tháng - "Hoàn hảo cho cá nhân"
  2. Chuyên nghiệp - $19.99/tháng - "Tốt nhất cho chuyên gia"
  3. Doanh nghiệp - $49.99/tháng - "Dành cho nhóm và doanh nghiệp"
- Mỗi gói nên có nút "Đăng ký"
- Sử dụng bố cục thẻ hiện đại, sạch sẽ
- Làm cho nó đáp ứng cho di động)
```

### Bước 4: Thêm Stripe Checkout

Yêu cầu Lovable:
```
Add Stripe Checkout to the subscription page. When a user clicks "Subscribe" on a plan:
- Open Stripe Checkout for that plan's price
- Use the Stripe connector I've configured
- After successful payment, redirect to a success page
- Store the subscription in the database with user ID and plan type
(Thêm Stripe Checkout vào trang đăng ký. Khi người dùng nhấp vào "Đăng ký" trên một gói:
- Mở Stripe Checkout cho giá của gói đó
- Sử dụng connector Stripe tôi đã cấu hình
- Sau khi thanh toán thành công, chuyển hướng đến trang thành công
- Lưu trữ đăng ký trong cơ sở dữ liệu với ID người dùng và loại gói)
```

### Bước 5: Tạo trang thành công

Yêu cầu Lovable:
```
Create a subscription success page that:
- Shows a success message
- Displays the plan the user subscribed to
- Has a "Go to Dashboard" button
- Looks professional and celebratory
(Tạo trang đăng ký thành công:
- Hiển thị thông báo thành công
- Hiển thị gói người dùng đã đăng ký
- Có nút "Đi tới Bảng điều khiển"
- Trông chuyên nghiệp và mang tính chúc mừng)
```

### Bước 6: Thêm quản lý đăng ký

Yêu cầu Lovable:
```
Create a "My Subscription" page that:
- Shows the user's current subscription plan
- Displays subscription status (active, canceled, etc.)
- Shows next billing date
- Has a "Manage Subscription" button that links to Stripe customer portal
- Only accessible to logged-in users
(Tạo trang "Đăng ký của tôi":
- Hiển thị gói đăng ký hiện tại của người dùng
- Hiển thị trạng thái đăng ký (hoạt động, đã hủy, v.v.)
- Hiển thị ngày thanh toán tiếp theo
- Có nút "Quản lý đăng ký" liên kết đến cổng thông tin khách hàng Stripe
- Chỉ có thể truy cập đối với người dùng đã đăng nhập)
```

### Bước 7: Bảo mật việc triển khai

Yêu cầu Lovable:
```
Make sure the subscription implementation is secure:
- All payment processing happens server-side
- Stripe keys are only accessed through secrets manager
- User can only see their own subscription
- Add proper error handling for failed payments
(Đảm bảo việc triển khai đăng ký được bảo mật:
- Tất cả xử lý thanh toán diễn ra phía máy chủ
- Khóa Stripe chỉ được truy cập thông qua trình quản lý bí mật
- Người dùng chỉ có thể xem đăng ký của chính họ
- Thêm xử lý lỗi thích hợp cho các khoản thanh toán thất bại)
```

### Bước 8: Kiểm tra luồng

**Các bước kiểm tra:**

1. **Kiểm tra Đăng ký:**
   - Đi tới trang đăng ký
   - Nhấp "Đăng ký" trên một gói
   - Sử dụng thẻ thử nghiệm Stripe: `4242 4242 4242 4242`
   - Sử dụng bất kỳ ngày hết hạn nào trong tương lai (ví dụ: 12/25)
   - Sử dụng bất kỳ CVC 3 chữ số nào
   - Hoàn tất thanh toán
   - Sẽ chuyển hướng đến trang thành công

2. **Kiểm tra Trang đăng ký:**
   - Đi tới "Đăng ký của tôi"
   - Sẽ hiển thị gói hoạt động của bạn
   - Sẽ hiển thị ngày thanh toán tiếp theo

3. **Kiểm tra Bảo mật:**
   - Thử truy cập đăng ký của người dùng khác (sẽ thất bại)
   - Kiểm tra xem khóa có trong mã frontend không
   - Xác minh xử lý thanh toán được bảo mật

### Bước 9: Thêm sự hoàn thiện

Yêu cầu Lovable:
```
Improve the subscription experience:
- Add loading states during payment processing
- Show clear error messages if payment fails
- Add confirmation before subscribing
- Improve the design and user experience
- Add email confirmation after successful subscription
(Cải thiện trải nghiệm đăng ký:
- Thêm trạng thái đang tải trong quá trình xử lý thanh toán
- Hiển thị thông báo lỗi rõ ràng nếu thanh toán thất bại
- Thêm xác nhận trước khi đăng ký
- Cải thiện thiết kế và trải nghiệm người dùng
- Thêm xác nhận email sau khi đăng ký thành công)
```

### Những gì bạn đã học

Dự án nhỏ này đã dạy bạn:
- ✅ Cách cấu hình connector Stripe
- ✅ Cách sử dụng connector trong câu lệnh
- ✅ Cách xử lý thanh toán an toàn
- ✅ Cách lưu trữ dữ liệu đăng ký
- ✅ Các phương pháp bảo mật tốt nhất cho thanh toán
- ✅ Tích hợp thanh toán trong thế giới thực

### Các vấn đề phổ biến và giải pháp

**Vấn đề: "Stripe không hoạt động"**
- Kiểm tra xem khóa có trong cài đặt Connectors không
- Xác minh bạn đang sử dụng khóa thử nghiệm để kiểm tra
- Đảm bảo Lovable Cloud được kích hoạt

**Vấn đề: "Thanh toán không xử lý"**
- Kiểm tra bảng điều khiển Stripe để tìm lỗi
- Xác minh khóa là chính xác
- Kiểm tra với thẻ thử nghiệm Stripe

**Vấn đề: "Đăng ký không lưu"**
- Kiểm tra cơ sở dữ liệu đã được thiết lập chưa
- Xác minh xác thực người dùng đang hoạt động
- Kiểm tra xem dữ liệu đăng ký có đang được lưu trữ không

**💡 Mẹo chuyên nghiệp:** Luôn kiểm tra với chế độ thử nghiệm Stripe trước! Sử dụng thẻ thử nghiệm và khóa thử nghiệm trước khi đi vào hoạt động.

---

## 🎯 Thử thách Module 6

**Xây dựng kỹ năng backend của bạn với các thử thách lũy tiến này!**

### Thử thách 1: Tính năng cơ sở dữ liệu cơ bản (Người mới bắt đầu)

**Nhiệm vụ của bạn:** Xây dựng hệ thống bình luận cho blog sử dụng Lovable Cloud.

**Yêu cầu:**
- Tạo bảng cơ sở dữ liệu cho bình luận
- Bình luận nên có: tên tác giả, văn bản bình luận, ngày tháng và ID bài đăng
- Tạo biểu mẫu để thêm bình luận
- Hiển thị bình luận bên dưới bài đăng blog
- Chỉ hiển thị bình luận cho bài đăng hiện tại

**💡 Gợi ý:**
- Kích hoạt Lovable Cloud trước
- Xác định cấu trúc cơ sở dữ liệu của bạn rõ ràng
- Liên kết bình luận với bài đăng bằng ID bài đăng
- Kiểm tra thêm và xem bình luận

**Kiểm tra giải pháp của bạn:** Xem [Giải pháp thử thách](supplement-challenge-solutions.md#module-6-challenge-1)

---

### Thử thách 2: Mở rộng với Thông báo Email (Trung cấp)

**Nhiệm vụ của bạn:** Mở rộng hệ thống bình luận từ Thử thách 1 bằng cách thêm thông báo email sử dụng connector Resend.

**Yêu cầu:**
- Khi ai đó thêm bình luận, gửi email cho tác giả bài đăng blog
- Email nên bao gồm: tên người bình luận, văn bản bình luận, liên kết đến bài đăng
- Cấu hình connector Resend đúng cách
- Lưu trữ email trong trình quản lý bí mật (không phải trong mã!)

**💡 Gợi ý:**
- Thiết lập tài khoản Resend và lấy khóa API
- Thêm connector Resend trong cài đặt Lovable
- Lưu trữ khóa API trong trình quản lý bí mật
- Sử dụng Resend để gửi email khi bình luận được tạo

**Kiểm tra giải pháp của bạn:** Xem [Giải pháp thử thách](supplement-challenge-solutions.md#module-6-challenge-2)

---

### Thử thách 3: Bảo mật dữ liệu người dùng (Nâng cao)

**Nhiệm vụ của bạn:** Xây dựng hệ thống hồ sơ người dùng với bảo mật thích hợp.

**Yêu cầu:**
- Người dùng có thể tạo hồ sơ với: tên, tiểu sử, hình đại diện
- Người dùng chỉ có thể xem và chỉnh sửa hồ sơ của chính họ
- Thêm xác thực (đăng ký/đăng nhập)
- Bảo vệ trang hồ sơ (chỉ chủ sở hữu mới có thể truy cập)
- Lưu trữ dữ liệu hồ sơ an toàn

**💡 Gợi ý:**
- Kích hoạt xác thực trước
- Liên kết hồ sơ với ID người dùng
- Thêm kiểm tra ủy quyền
- Kiểm tra xem người dùng không thể truy cập hồ sơ của người khác

**Kiểm tra giải pháp của bạn:** Xem [Giải pháp thử thách](supplement-challenge-solutions.md#module-6-challenge-3)

---

### Thử thách 4: Tính năng hoàn chỉnh với Tích hợp API (Chuyên gia)

**Nhiệm vụ của bạn:** Xây dựng tính năng "Liên hệ với chúng tôi" mà:
- Có biểu mẫu liên hệ (tên, email, tin nhắn)
- Lưu trữ các lần gửi trong cơ sở dữ liệu
- Gửi thông báo email sử dụng Resend
- Tích hợp với API bản đồ để hiển thị vị trí của bạn
- Có giới hạn tốc độ (tối đa 3 lần gửi mỗi giờ)

**💡 Gợi ý:**
- Sử dụng Lovable Cloud cho cơ sở dữ liệu
- Cấu hình connector Resend
- Sử dụng API bản đồ công khai (như Google Maps)
- Thêm giới hạn tốc độ để ngăn chặn thư rác
- Kiểm tra luồng hoàn chỉnh

**Kiểm tra giải pháp của bạn:** Xem [Giải pháp thử thách](supplement-challenge-solutions.md#module-6-challenge-4)

---

**💡 Mẹo chuyên nghiệp:** Bắt đầu với Thử thách 1, kiểm tra kỹ lưỡng, sau đó chuyển sang thử thách tiếp theo. Mỗi thử thách xây dựng dựa trên thử thách trước đó!

---

## ✅ Danh sách kiểm tra Module 6

Trước khi chuyển sang Module 7, hãy đảm bảo bạn có thể:

- [ ] Giải thích "full-stack" nghĩa là gì
- [ ] Kích hoạt Lovable Cloud
- [ ] Hiểu connector là gì
- [ ] Biết khi nào nên sử dụng các tùy chọn backend khác nhau
- [ ] Thêm xác thực vào dự án
- [ ] Thêm cơ sở dữ liệu vào dự án
- [ ] Hiểu cách tích hợp API
- [ ] Lưu trữ khóa API an toàn trong trình quản lý bí mật
- [ ] Hiểu sự khác biệt giữa khóa API công khai và riêng tư
- [ ] Tuân theo các phương pháp bảo mật tốt nhất
- [ ] Cấu hình và sử dụng connector (Stripe, Supabase)
- [ ] Hiểu cách Lovable tự động xử lý bảo mật

---

## 🤔 Các câu hỏi thường gặp (FAQ)

### Hỏi: Tôi có cần biết cách thiết lập cơ sở dữ liệu không?
**Đáp:** Không! Lovable xử lý nó cho bạn. Chỉ cần mô tả dữ liệu bạn muốn lưu trữ.

### Hỏi: Tôi nên sử dụng backend nào?
**Đáp:** Bắt đầu với Lovable Cloud - đó là cách dễ nhất. Thêm connector nếu bạn cần các tính năng cụ thể.

### Hỏi: Khóa API có an toàn không?
**Đáp:** Có! Lovable lưu trữ chúng an toàn và sử dụng Edge Functions để bảo vệ chúng.

### Hỏi: Tôi có cần trả tiền cho các dịch vụ này không?
**Đáp:** Nhiều dịch vụ có gói miễn phí để bắt đầu. Kiểm tra giá của từng dịch vụ.

### Hỏi: Tôi có thể sử dụng nhiều backend không?
**Đáp:** Thông thường bạn chọn một backend chính, nhưng bạn có thể sử dụng connector cho các tính năng cụ thể.

### Hỏi: Nếu tôi không cần backend thì sao?
**Đáp:** Không sao cả! Các trang web đơn giản không phải lúc nào cũng cần backend. Thêm một cái khi bạn cần tài khoản người dùng hoặc lưu trữ dữ liệu.

### Hỏi: Tôi nên lưu trữ khóa API của mình ở đâu?
**Đáp:** LUÔN LUÔN trong Trình quản lý bí mật của Lovable (Cloud → Secrets). KHÔNG BAO GIỜ trong mã hoặc câu lệnh của bạn. Lovable xử lý bảo mật cho bạn.

### Hỏi: Sự khác biệt giữa khóa API công khai và riêng tư là gì?
**Đáp:** Khóa công khai (như Stripe Publishable Key) an toàn cho frontend. Khóa riêng tư (như Stripe Secret Key) phải ở trong trình quản lý bí mật và không bao giờ được để lộ.

### Hỏi: Lovable có xử lý bảo mật mật khẩu không?
**Đáp:** Có! Lovable tự động băm mật khẩu, vì vậy chúng không bao giờ được lưu trữ dưới dạng văn bản thuần túy. Bạn không cần tự viết mã này.

### Hỏi: Làm sao tôi biết ứng dụng của mình có an toàn không?
**Đáp:** Sử dụng danh sách kiểm tra bảo mật trong module này. Lovable xử lý hầu hết bảo mật tự động, nhưng bạn nên tuân theo các phương pháp tốt nhất như lưu trữ khóa trong secrets.

### Hỏi: Tôi có thể đặt khóa Stripe trực tiếp trong câu lệnh không?
**Đáp:** KHÔNG! Không bao giờ đặt khóa riêng tư trong câu lệnh. Lưu trữ chúng trong Secrets Manager, sau đó tham chiếu connector trong câu lệnh của bạn.

### Hỏi: Nếu tôi vô tình để lộ khóa API thì sao?
**Đáp:** Thu hồi ngay lập tức trong bảng điều khiển của dịch vụ và tạo một cái mới. Sau đó cập nhật nó trong trình quản lý bí mật của Lovable.

---

## 🎯 Tiếp theo là gì?

Làm việc tuyệt vời! Bây giờ bạn đã hiểu cách thêm các tính năng backend mạnh mẽ vào ứng dụng của mình. Bạn có thể:
- Sử dụng Lovable Cloud cho backend tích hợp sẵn
- Thêm connector cho các dịch vụ bên ngoài
- Tích hợp API an toàn
- Thêm xác thực
- Thêm cơ sở dữ liệu
- Tuân theo các phương pháp bảo mật tốt nhất
- Xây dựng tích hợp thanh toán

**Sẵn sàng cho Module 7?** Trong module tiếp theo, chúng ta sẽ tìm hiểu về Chế độ Code - xem và chỉnh sửa mã trực tiếp (tùy chọn cho người mới bắt đầu, nhưng hữu ích để biết)!

---

## 💡 Mẹo chuyên nghiệp cho người mới bắt đầu

1. **Bắt đầu với Lovable Cloud** - Đó là cách dễ nhất để thêm các tính năng backend

2. **Thêm tính năng dần dần** - Đừng cố gắng thêm mọi thứ cùng một lúc

3. **Kiểm tra khi bạn thực hiện** - Đảm bảo mọi thứ hoạt động trước khi thêm nhiều hơn

4. **Sử dụng connector khi cần thiết** - Chúng thêm các tính năng mạnh mẽ một cách dễ dàng

5. **Giữ an toàn cho khóa API** - LUÔN lưu trữ trong trình quản lý bí mật, KHÔNG BAO GIỜ trong mã hoặc câu lệnh

6. **Bắt đầu đơn giản** - Xác thực và cơ sở dữ liệu cơ bản trước, sau đó thêm độ phức tạp

7. **Tuân theo các thực hành bảo mật** - Lovable xử lý hầu hết bảo mật, nhưng bạn cần sử dụng nó đúng cách

8. **Kiểm tra với khóa thử nghiệm trước** - Luôn sử dụng chế độ thử nghiệm (khóa thử nghiệm Stripe, v.v.) trước khi đi vào hoạt động

9. **Hiểu khóa công khai vs. riêng tư** - Biết khóa nào an toàn cho frontend và khóa nào phải giữ bí mật

---

*Module 6 Hoàn thành! 🎉*
