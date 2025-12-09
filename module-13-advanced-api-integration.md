# Module 13: Tích hợp API Nâng cao

**Mục tiêu:** Làm chủ việc tích hợp các API bên ngoài vượt ra ngoài các trình kết nối cơ bản

**Thời gian ước tính:** 45-60 phút

**Điều kiện tiên quyết:** Hoàn thành Module 1-6 trước

---

## 🎯 Bạn Sẽ Học Được Gì Trong Module Này

Vào cuối module này, bạn sẽ:
- Hiểu sự khác biệt giữa gọi API phía máy chủ (server-side) và phía máy khách (client-side)
- Biết cách tích hợp các API công khai
- Học cách tích hợp an toàn các API riêng tư
- Hiểu cách xử lý dữ liệu bất đồng bộ
- Có khả năng hiển thị dữ liệu API một cách hiệu quả
- Biết cách xử lý lỗi API
- Xây dựng các tích hợp API thực tế

---

## 📖 Bài học 1: Gọi API Phía Máy chủ vs. Phía Máy khách

### Sự Khác biệt là gì?

**Gọi API Phía Máy khách (Client-Side):**
- Được thực hiện từ trình duyệt (frontend)
- Trình duyệt của người dùng thực hiện yêu cầu
- Khóa API có thể bị lộ (nếu là khóa công khai)
- Giới hạn ở các API công khai hoặc các API có bật CORS

**Gọi API Phía Máy chủ (Server-Side):**
- Được thực hiện từ máy chủ (backend)
- Máy chủ của bạn thực hiện yêu cầu
- Khóa API được giữ bí mật (trong trình quản lý bí mật)
- Có thể sử dụng bất kỳ API nào (công khai hoặc riêng tư)

### Khi nào Sử dụng Mỗi Loại

**Sử dụng Phía Máy khách Khi:**
- ✅ API công khai (không cần xác thực)
- ✅ API hỗ trợ CORS
- ✅ Lấy dữ liệu đơn giản
- ✅ Cần cập nhật thời gian thực

**Sử dụng Phía Máy chủ Khi:**
- ✅ API riêng tư (yêu cầu khóa bí mật)
- ✅ Dữ liệu nhạy cảm
- ✅ Cần giới hạn tốc độ (rate limiting)
- ✅ Cần chuyển đổi dữ liệu

### Cách Lovable Xử lý Việc Này

**Lovable tự động chọn:**
- **API Công khai** → Phía máy khách (trực tiếp từ trình duyệt)
- **API Riêng tư** → Phía máy chủ (thông qua Edge Functions)

**Bạn chỉ cần yêu cầu:**
```
Integrate the [API name] API
(Tích hợp API [tên API])
```

Lovable sẽ tìm ra cách tiếp cận tốt nhất!

**💡 Mẹo cho người mới bắt đầu:** Đừng lo lắng về các chi tiết kỹ thuật! Lovable xử lý nó. Chỉ cần biết rằng các khóa riêng tư được giữ an toàn.

---

## 📖 Bài học 2: Tích hợp API Công khai

### API Công khai là gì?

**API Công khai** không yêu cầu xác thực. Bất kỳ ai cũng có thể sử dụng chúng.

**Ví dụ:**
- Dữ liệu thời tiết
- Thông tin công cộng
- Dịch vụ miễn phí
- Dữ liệu mở

### Cách Tích hợp API Công khai

#### Ví dụ 1: API Thời tiết

**Tích hợp Đơn giản:**
```
Integrate the Open-Meteo weather API to show current weather for a city. 
API: https://api.open-meteo.com/v1/forecast
Display temperature, conditions, and a simple icon.
(Tích hợp API thời tiết Open-Meteo để hiển thị thời tiết hiện tại cho một thành phố.
API: https://api.open-meteo.com/v1/forecast
Hiển thị nhiệt độ, điều kiện và một biểu tượng đơn giản.)
```

**Chi tiết hơn:**
```
Create a weather widget that:
- Uses Open-Meteo API (https://api.open-meteo.com/v1/forecast)
- Allows user to enter a city name
- Fetches current weather for that city
- Displays: temperature, conditions, humidity, wind speed
- Shows a weather icon based on conditions
- Updates when user searches for a new city
- Handles errors (city not found, API down)
(Tạo một widget thời tiết:
- Sử dụng API Open-Meteo (https://api.open-meteo.com/v1/forecast)
- Cho phép người dùng nhập tên thành phố
- Lấy thời tiết hiện tại cho thành phố đó
- Hiển thị: nhiệt độ, điều kiện, độ ẩm, tốc độ gió
- Hiển thị biểu tượng thời tiết dựa trên điều kiện
- Cập nhật khi người dùng tìm kiếm thành phố mới
- Xử lý lỗi (không tìm thấy thành phố, API ngừng hoạt động))
```

#### Ví dụ 2: API Tin tức

**Tích hợp:**
```
Integrate a news API to display recent articles:
- Fetch articles from https://newsapi.org/v2/top-headlines
- Display article title, description, image, and source
- Show 10 most recent articles
- Add "Load More" button for additional articles
- Handle API rate limits gracefully
(Tích hợp API tin tức để hiển thị các bài báo gần đây:
- Lấy bài báo từ https://newsapi.org/v2/top-headlines
- Hiển thị tiêu đề bài báo, mô tả, hình ảnh và nguồn
- Hiển thị 10 bài báo gần đây nhất
- Thêm nút "Tải thêm" cho các bài báo bổ sung
- Xử lý giới hạn tốc độ API một cách khéo léo)
```

#### Ví dụ 3: API Dữ liệu Ngẫu nhiên

**Tích hợp:**
```
Integrate the JSONPlaceholder API to create a demo data section:
- Fetch posts from https://jsonplaceholder.typicode.com/posts
- Display posts in a card layout
- Show post title and body
- Add pagination (10 posts per page)
(Tích hợp API JSONPlaceholder để tạo phần dữ liệu demo:
- Lấy bài viết từ https://jsonplaceholder.typicode.com/posts
- Hiển thị bài viết trong bố cục thẻ
- Hiển thị tiêu đề và nội dung bài viết
- Thêm phân trang (10 bài viết mỗi trang))
```

### Các Thực hành Tốt nhất cho API Công khai

1. **Xử lý Lỗi:**
   ```
   Add error handling for the API:
   - Show message if API is down
   - Handle invalid responses
   - Display user-friendly error messages
   (Thêm xử lý lỗi cho API:
   - Hiển thị thông báo nếu API ngừng hoạt động
   - Xử lý phản hồi không hợp lệ
   - Hiển thị thông báo lỗi thân thiện với người dùng)
   ```

2. **Thêm Trạng thái Đang tải:**
   ```
   Show loading indicator while fetching data from the API
   (Hiển thị chỉ báo đang tải trong khi lấy dữ liệu từ API)
   ```

3. **Lưu vào Bộ nhớ đệm Khi Thích hợp:**
   ```
   Cache API responses for 5 minutes to reduce API calls
   (Lưu phản hồi API vào bộ nhớ đệm trong 5 phút để giảm các cuộc gọi API)
   ```

**💡 Mẹo cho người mới bắt đầu:** API công khai rất tuyệt để học tập! Bắt đầu với những cái đơn giản, sau đó chuyển sang các tích hợp phức tạp hơn.

---

## 📖 Bài học 3: Tích hợp API Riêng tư An toàn

### API Riêng tư là gì?

**API Riêng tư** yêu cầu xác thực (khóa API, token, v.v.). Chúng chứa dữ liệu hoặc chức năng nhạy cảm.

**Ví dụ:**
- Xử lý thanh toán
- Dữ liệu người dùng
- Dịch vụ email
- Phân tích

### Cách Tích hợp API Riêng tư An toàn

#### Bước 1: Lấy Khóa API của Bạn

1. Đăng ký dịch vụ
2. Lấy khóa API từ bảng điều khiển của họ
3. **Giữ bí mật!** (Giống như mật khẩu)

#### Bước 2: Lưu trữ trong Trình quản lý Bí mật (Secrets Manager)

**QUAN TRỌNG:** Không bao giờ đặt khóa API trong prompt hoặc mã!

**✅ Cách Đúng:**
1. Đi tới **Cloud** → **Secrets**
2. Thêm khóa API của bạn
3. Đặt tên cho nó (ví dụ: "WEATHER_API_KEY")
4. Lưu

**❌ Cách Sai:**
```
Use API key: abc123xyz456
```
**KHÔNG BAO GIỜ LÀM ĐIỀU NÀY!**

#### Bước 3: Tham chiếu trong Prompt của Bạn

**Sau khi lưu trữ trong secrets:**
```
Integrate the OpenWeatherMap API using the key stored in secrets (WEATHER_API_KEY).
Create a weather widget that fetches current weather for a city.
Base URL: https://api.openweathermap.org/data/2.5
Endpoint: /weather?q={city}&appid={API_KEY}
(Tích hợp API OpenWeatherMap sử dụng khóa được lưu trữ trong secrets (WEATHER_API_KEY).
Tạo một widget thời tiết lấy thời tiết hiện tại cho một thành phố.
URL cơ sở: https://api.openweathermap.org/data/2.5
Endpoint: /weather?q={city}&appid={API_KEY})
```

**Lovable sẽ:**
- Sử dụng khóa từ secrets
- Tạo Edge Function (phía máy chủ)
- Giữ khóa an toàn
- Xử lý cuộc gọi API

### Ví dụ: Tích hợp API An toàn

**Quy trình Hoàn chỉnh:**

1. **Thêm Khóa API vào Secrets:**
   - Đi tới Cloud → Secrets
   - Thêm: `OPENWEATHER_API_KEY` = `your_key_here`
   - Lưu

2. **Tích hợp API:**
   ```
   Integrate OpenWeatherMap API securely:
   - Use the API key from secrets (OPENWEATHER_API_KEY)
   - Create server-side function to fetch weather
   - Endpoint: GET /weather?q={city}&appid={API_KEY}
   - Create frontend widget that calls this function
   - Display: temperature, conditions, icon
   - Handle errors securely
   (Tích hợp API OpenWeatherMap an toàn:
   - Sử dụng khóa API từ secrets (OPENWEATHER_API_KEY)
   - Tạo hàm phía máy chủ để lấy thời tiết
   - Endpoint: GET /weather?q={city}&appid={API_KEY}
   - Tạo widget frontend gọi hàm này
   - Hiển thị: nhiệt độ, điều kiện, biểu tượng
   - Xử lý lỗi an toàn)
   ```

3. **Lovable Tạo:**
   - Edge Function (phía máy chủ, an toàn)
   - Component frontend (gọi hàm)
   - Xử lý lỗi
   - Tất cả các khóa đều ở trong secrets!

**💡 Mẹo cho người mới bắt đầu:** Luôn sử dụng trình quản lý bí mật cho các API riêng tư. Đó là cách an toàn!

---

## 📖 Bài học 4: Xử lý Dữ liệu Bất đồng bộ

### Bất đồng bộ là gì?

**Bất đồng bộ (Asynchronous)** có nghĩa là mọi thứ xảy ra vào những thời điểm khác nhau, không phải tất cả cùng một lúc.

**Ví dụ:**
- Người dùng nhấp vào nút
- Ứng dụng yêu cầu dữ liệu từ API
- Người dùng vẫn có thể tương tác (không bị đóng băng)
- Dữ liệu đến sau
- Ứng dụng cập nhật với dữ liệu

### Cách Xử lý Bất đồng bộ trong Prompt

#### Mẫu 1: Trạng thái Đang tải

**Ví dụ:**
```
When fetching data from the API:
- Show loading spinner while fetching
- Display "Loading..." message
- Hide loading when data arrives
- Show data or error message
(Khi lấy dữ liệu từ API:
- Hiển thị vòng quay đang tải trong khi lấy
- Hiển thị thông báo "Đang tải..."
- Ẩn đang tải khi dữ liệu đến
- Hiển thị dữ liệu hoặc thông báo lỗi)
```

#### Mẫu 2: Xử lý Lỗi

**Ví dụ:**
```
Handle API errors gracefully:
- If API is down: Show "Service temporarily unavailable"
- If city not found: Show "City not found, please try another"
- If rate limited: Show "Too many requests, please wait"
- Always show user-friendly messages
(Xử lý lỗi API một cách khéo léo:
- Nếu API ngừng hoạt động: Hiển thị "Dịch vụ tạm thời không khả dụng"
- Nếu không tìm thấy thành phố: Hiển thị "Không tìm thấy thành phố, vui lòng thử lại"
- Nếu bị giới hạn tốc độ: Hiển thị "Quá nhiều yêu cầu, vui lòng đợi"
- Luôn hiển thị thông báo thân thiện với người dùng)
```

#### Mẫu 3: Logic Thử lại

**Ví dụ:**
```
If API call fails:
- Retry once after 2 seconds
- If still fails, show error message
- Allow user to manually retry
- Log errors for debugging
(Nếu cuộc gọi API thất bại:
- Thử lại một lần sau 2 giây
- Nếu vẫn thất bại, hiển thị thông báo lỗi
- Cho phép người dùng thử lại thủ công
- Ghi lại lỗi để gỡ lỗi)
```

### Ví dụ Thực tế: Widget Thời tiết

**Xử lý Bất đồng bộ Hoàn chỉnh:**
```
Create a weather widget with:
- Input field for city name
- "Get Weather" button
- When clicked:
  - Show loading spinner
  - Fetch weather from API (async)
  - Display weather when data arrives
  - Show error if API fails
  - Allow user to search again
- Handle all states: loading, success, error
(Tạo một widget thời tiết với:
- Trường nhập tên thành phố
- Nút "Lấy Thời tiết"
- Khi nhấp:
  - Hiển thị vòng quay đang tải
  - Lấy thời tiết từ API (bất đồng bộ)
  - Hiển thị thời tiết khi dữ liệu đến
  - Hiển thị lỗi nếu API thất bại
  - Cho phép người dùng tìm kiếm lại
- Xử lý tất cả các trạng thái: đang tải, thành công, lỗi)
```

**💡 Mẹo cho người mới bắt đầu:** Luôn yêu cầu trạng thái đang tải và xử lý lỗi. Nó làm cho ứng dụng của bạn cảm thấy chuyên nghiệp!

---

## 📖 Bài học 5: Hiển thị Dữ liệu API

### Các Thực hành Tốt nhất để Hiển thị Dữ liệu API

#### Mẫu 1: Định dạng Dữ liệu Đẹp mắt

**Ví dụ:**
```
Display the weather data in a user-friendly format:
- Temperature: Show in large, readable font with °C or °F
- Conditions: Show as text and icon
- Date/Time: Format as "Today, 3:00 PM"
- Make it visually appealing with cards or widgets
(Hiển thị dữ liệu thời tiết ở định dạng thân thiện với người dùng:
- Nhiệt độ: Hiển thị bằng phông chữ lớn, dễ đọc với °C hoặc °F
- Điều kiện: Hiển thị dưới dạng văn bản và biểu tượng
- Ngày/Giờ: Định dạng là "Hôm nay, 3:00 CH"
- Làm cho nó hấp dẫn trực quan với các thẻ hoặc widget)
```

#### Mẫu 2: Xử lý Trạng thái Trống

**Ví dụ:**
```
When no data is available:
- Show friendly message: "No weather data available"
- Provide instructions: "Enter a city name to get weather"
- Don't show errors, show helpful guidance
(Khi không có dữ liệu:
- Hiển thị thông báo thân thiện: "Không có dữ liệu thời tiết"
- Cung cấp hướng dẫn: "Nhập tên thành phố để lấy thời tiết"
- Đừng hiển thị lỗi, hãy hiển thị hướng dẫn hữu ích)
```

#### Mẫu 3: Cập nhật Dữ liệu

**Ví dụ:**
```
Make the weather data update:
- Refresh button to get latest data
- Auto-refresh every 5 minutes
- Show "Last updated" timestamp
- Indicate when data is fresh vs. stale
(Làm cho dữ liệu thời tiết cập nhật:
- Nút làm mới để lấy dữ liệu mới nhất
- Tự động làm mới mỗi 5 phút
- Hiển thị dấu thời gian "Cập nhật lần cuối"
- Chỉ ra khi dữ liệu mới so với cũ)
```

### Ví dụ: Tích hợp API Hoàn chỉnh

**Bảng điều khiển Thời tiết:**
```
Create a weather dashboard that:
- Fetches weather from OpenWeatherMap API (key in secrets)
- Shows current weather for user's location
- Displays: temperature, conditions, humidity, wind
- Shows 5-day forecast
- Updates every hour
- Handles errors gracefully
- Shows loading states
- Responsive design for mobile
(Tạo một bảng điều khiển thời tiết:
- Lấy thời tiết từ API OpenWeatherMap (khóa trong secrets)
- Hiển thị thời tiết hiện tại cho vị trí của người dùng
- Hiển thị: nhiệt độ, điều kiện, độ ẩm, gió
- Hiển thị dự báo 5 ngày
- Cập nhật mỗi giờ
- Xử lý lỗi một cách khéo léo
- Hiển thị trạng thái đang tải
- Thiết kế responsive cho di động)
```

---

## 🛠️ Thực hành: Xây dựng Ứng dụng Thời tiết

Hãy xây dựng một ứng dụng thời tiết hoàn chỉnh!

### Bước 1: Thiết lập API

1. **Lấy Khóa API:**
   - Đăng ký tại [openweathermap.org](https://openweathermap.org) (có gói miễn phí)
   - Lấy khóa API của bạn

2. **Lưu trữ trong Secrets:**
   - Đi tới Cloud → Secrets
   - Thêm: `OPENWEATHER_API_KEY` = `your_key`
   - Lưu

### Bước 2: Tạo Widget Thời tiết

Hỏi Lovable:
```
Create a weather widget that:
- Has an input field for city name
- "Get Weather" button
- Fetches weather from OpenWeatherMap API using key from secrets
- Shows: temperature, conditions, humidity, wind speed
- Displays weather icon
- Shows loading state while fetching
- Handles errors (city not found, API down)
- Looks modern and clean
(Tạo một widget thời tiết:
- Có trường nhập tên thành phố
- Nút "Lấy Thời tiết"
- Lấy thời tiết từ API OpenWeatherMap sử dụng khóa từ secrets
- Hiển thị: nhiệt độ, điều kiện, độ ẩm, tốc độ gió
- Hiển thị biểu tượng thời tiết
- Hiển thị trạng thái đang tải trong khi lấy
- Xử lý lỗi (không tìm thấy thành phố, API ngừng hoạt động)
- Trông hiện đại và sạch sẽ)
```

### Bước 3: Thêm Dự báo

Hỏi Lovable:
```
Add a 5-day weather forecast below the current weather:
- Show daily high/low temperatures
- Show conditions for each day
- Display in a horizontal scrollable list
- Make it visually appealing
(Thêm dự báo thời tiết 5 ngày bên dưới thời tiết hiện tại:
- Hiển thị nhiệt độ cao/thấp hàng ngày
- Hiển thị điều kiện cho mỗi ngày
- Hiển thị trong danh sách cuộn ngang
- Làm cho nó hấp dẫn trực quan)
```

### Bước 4: Thêm Tính năng

Hỏi Lovable:
```
Enhance the weather app:
- Add "Use My Location" button (gets weather for current location)
- Add favorite cities (save 3 favorite cities)
- Add unit toggle (Celsius/Fahrenheit)
- Improve error messages
- Add refresh functionality
(Cải thiện ứng dụng thời tiết:
- Thêm nút "Sử dụng Vị trí của Tôi" (lấy thời tiết cho vị trí hiện tại)
- Thêm các thành phố yêu thích (lưu 3 thành phố yêu thích)
- Thêm chuyển đổi đơn vị (Độ C/Độ F)
- Cải thiện thông báo lỗi
- Thêm chức năng làm mới)
```

### Bước 5: Kiểm thử và Gỡ lỗi

1. **Kiểm thử với các thành phố hợp lệ:**
   - Nhập "London"
   - Nhập "New York"
   - Xác minh dữ liệu hiển thị

2. **Kiểm thử xử lý lỗi:**
   - Nhập thành phố không hợp lệ
   - Xem thông báo lỗi
   - Xác minh nó thân thiện với người dùng

3. **Kiểm thử trên di động:**
   - Kiểm tra thiết kế responsive
   - Kiểm thử tất cả các tính năng

**🎉 Chúc mừng!** Bạn đã xây dựng một tích hợp API hoàn chỉnh!

---

## ✅ Danh sách Kiểm tra Module 13

Trước khi hoàn thành khóa học, hãy đảm bảo bạn có thể:

- [ ] Hiểu gọi API phía máy chủ vs. phía máy khách
- [ ] Tích hợp các API công khai
- [ ] Tích hợp an toàn các API riêng tư
- [ ] Lưu trữ khóa API trong trình quản lý bí mật
- [ ] Xử lý dữ liệu bất đồng bộ
- [ ] Hiển thị dữ liệu API hiệu quả
- [ ] Xử lý lỗi API
- [ ] Xây dựng các tích hợp API hoàn chỉnh

---

## 🤔 Các Câu Hỏi Thường Gặp (FAQ)

### Q: Làm thế nào để tôi biết một API là công khai hay riêng tư?
**A:** Kiểm tra tài liệu API. Nếu nó yêu cầu khóa API cho tất cả các yêu cầu, nó là riêng tư. Nếu một số endpoint hoạt động mà không cần khóa, chúng là công khai.

### Q: Tôi có thể sử dụng nhiều API trong một ứng dụng không?
**A:** Có! Bạn có thể tích hợp bao nhiêu API tùy ý. Chỉ cần lưu trữ mỗi khóa trong secrets.

### Q: Nếu một API yêu cầu OAuth thì sao?
**A:** Điều đó phức tạp hơn. Hỏi Chat Mode: "How do I integrate an API that requires OAuth authentication?" (Làm thế nào để tôi tích hợp một API yêu cầu xác thực OAuth?)

### Q: Làm thế nào để tôi xử lý giới hạn tốc độ API?
**A:** Yêu cầu Lovable thực hiện giới hạn tốc độ và lưu vào bộ nhớ đệm. Cũng kiểm tra tài liệu của API để biết giới hạn.

### Q: Tôi có thể kiểm thử API trước khi tích hợp không?
**A:** Có! Nhiều API có các endpoint kiểm thử hoặc chế độ sandbox. Kiểm thử với chúng trước.

---

## 🎯 Tiếp theo là gì?

Tuyệt vời! Bây giờ bạn đã hiểu về tích hợp API nâng cao. Bạn có thể xây dựng các ứng dụng kết nối với các dịch vụ bên ngoài một cách an toàn và hiệu quả.

**Tiếp tục với:**
- Module 14: Kiểm soát Phiên bản với GitHub
- Hoặc áp dụng các kỹ năng này vào dự án capstone của bạn!

---

*Module 13 Hoàn thành! 🎉*
