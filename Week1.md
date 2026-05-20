# Báo cáo Tuần 1 – Nghiên cứu về Use Case

## 1. Use Case (Ca sử dụng) là gì?

Tuần 1, em đã tìm hiểu được khái niệm **Use Case** trong phân tích và thiết kế hệ thống. Use case định nghĩa một chuỗi các tương tác giữa một hoặc nhiều **tác nhân (actors)** bên ngoài với hệ thống.

Em hiểu rằng use case được dùng để mô tả các **yêu cầu chức năng** của hệ thống dưới góc nhìn **"hộp đen" (black box)** – nghĩa là chỉ quan tâm đến hệ thống làm *gì* (đầu vào từ người dùng và phản hồi của hệ thống), chứ không quan tâm đến cấu trúc bên trong nó hoạt động như thế nào.

Ngoài ra, em cũng nắm được rằng mỗi chuỗi xuyên suốt một use case được gọi là một **kịch bản (scenario)**. Một use case thường bao gồm:
- **Main sequence (Chuỗi chính):** dùng cho tình huống bình thường.
- **Alternative sequences (Chuỗi thay thế):** dùng để xử lý lỗi hoặc các tình huống ít xảy ra.

---

## 2. Các thành phần cấu tạo nên Use Case

### Tác nhân (Actor)

Em đã tìm hiểu được về khái niệm **Actor** – đại diện cho một vai trò tương tác với hệ thống từ bên ngoài. Actor có thể là:
- **Con người (human actor)**
- **Hệ thống bên ngoài (external system)**
- **Thiết bị đầu vào/đầu ra (I/O device)**
- **Bộ đếm thời gian (timer)**

Em cũng phân biệt được hai loại actor:

| Loại Actor | Mô tả |
|---|---|
| **Primary Actor (Tác nhân chính)** | Người/thực thể cung cấp đầu vào đầu tiên để khởi tạo use case |
| **Secondary Actor (Tác nhân phụ)** | Người/thực thể tham gia vào use case nhưng không phải người khởi tạo |

---

## 3. Cách vẽ và Tài liệu hóa Use Case

### 3.1. Quy tắc đặt tên và thiết kế

Em đã học được một số quy tắc quan trọng khi đặt tên use case:
- Tên use case phải luôn bắt đầu bằng **động từ + tân ngữ**.
  - Ví dụ: *"Withdraw Funds"* (Rút tiền), *"Browse Catalog"* (Xem danh mục)
- Cần tránh **functional decomposition** – tức là không chia nhỏ hệ thống thành các chức năng quá vụn vặt. Một use case phải mô tả một chuỗi sự kiện mang lại **giá trị hữu ích cụ thể** cho tác nhân.

### 3.2. Vẽ Biểu đồ Use Case (Use Case Diagram)

Em đã nắm được các ký hiệu cơ bản để vẽ biểu đồ use case:

| Thành phần | Ký hiệu |
|---|---|
| Tác nhân (Actor) | Hình người que (stick figure) |
| Hệ thống | Hình chữ nhật bao quanh bên ngoài |
| Use case | Hình bầu dục (oval) bên trong hình chữ nhật |
| Đường giao tiếp | Đường thẳng nối từ actor đến use case |

### 3.3. Viết Đặc tả Use Case (Use Case Specification)

Em cũng tìm hiểu được cách viết đặc tả chi tiết cho mỗi use case, bao gồm các mục sau:

| Mục | Nội dung |
|---|---|
| **Name & Summary** | Tên và tóm tắt mục đích của use case |
| **Preconditions** | Điều kiện bắt buộc phải đúng trước khi use case bắt đầu |
| **Main sequence** | Các bước tương tác chuẩn giữa actor và hệ thống (đánh số thứ tự) |
| **Alternative sequences / Exceptions** | Các kịch bản phụ, lỗi rẽ nhánh từ chuỗi chính |
| **Postcondition** | Trạng thái của hệ thống sau khi use case hoàn thành thành công |

> **Ghi chú em rút ra được:**
> - Các yêu cầu phi chức năng (bảo mật, hiệu suất...) có thể được bổ sung vào một phần riêng trong đặc tả.
> - Nếu hệ thống quá lớn, có thể nhóm các use case liên quan thành **Use case package**.
> - Có thể dùng **Activity Diagram (Biểu đồ hoạt động)** để mô hình hóa chính xác luồng điều khiển và các bước rẽ nhánh của một use case.

---

## 4. Các mối quan hệ (Relationships) trong Use Case

Em đã tìm hiểu được hai mối quan hệ quan trọng trong biểu đồ use case:

### `<<include>>` – Bao gồm

Em hiểu rằng quan hệ `<<include>>` dùng để **trích xuất** một chuỗi tương tác lặp đi lặp lại ở nhiều use case thành một phần chung (inclusion use case). Các use case gốc sẽ "gọi" phần chung này để **tái sử dụng**, tương tự như một hàm thư viện trong lập trình.

### `<<extend>>` – Mở rộng

Quan hệ `<<extend>>` được dùng khi một use case gốc quá phức tạp. Em hiểu rằng có thể tách một nhánh chức năng **thay thế, tùy chọn hoặc có điều kiện** thành một use case riêng. Use case mở rộng này chỉ được chèn vào use case gốc tại các **extension points** nếu một điều kiện cụ thể được thỏa mãn.

---

## 5. Công cụ em đã tìm hiểu để vẽ và phân tích Use Case

Trong tuần này, em cũng đã tìm hiểu một số công cụ hỗ trợ vẽ và phân tích use case:

| Công cụ | Loại | Link |
|---|---|---|
| **Draw.io** | Vẽ kéo thả trực quan | [draw.io](https://www.draw.io/) |
| **Figma** | Vẽ kéo thả trực quan | [figma.com](https://www.figma.com/) |
| **PlantUML** | Viết code sinh biểu đồ | [plantuml.com](https://www.plantuml.com/) |
| **ChatGPT / Copilot** | Hỗ trợ GenAI | — |

### Workflow kết hợp GenAI + PlantUML mà em đã thử

Em đã thực hành quy trình sau:
1. Đưa mô tả dự án cho **ChatGPT** → yêu cầu AI xác định các Actor, Use Case chính và viết bảng đặc tả chi tiết.
2. Yêu cầu ChatGPT sinh ra đoạn **code PlantUML**.
3. Copy đoạn code đó dán vào web PlantUML → tự động tạo ra sơ đồ Use Case ngay lập tức.

---

## 6. Overleaf – Viết tài liệu LaTeX online

Ngoài ra, em cũng đã tìm hiểu về **Overleaf** – một nền tảng viết tài liệu **LaTeX online** trên trình duyệt, thường dùng để làm báo cáo, luận văn, paper khoa học, tài liệu kỹ thuật.

> Nói đơn giản: Overleaf giống như **"Google Docs cho LaTeX"**.

### Em đã sử dụng Overleaf để làm gì trong tuần này?

Em đã sử dụng Overleaf để viết **bài báo khoa học** – tận dụng khả năng định dạng chuyên nghiệp của LaTeX mà không cần cài đặt bất kỳ phần mềm nào trên máy tính.

### Các ưu điểm nổi bật mà em nhận thấy

| Tính năng | Mô tả |
|---|---|
| **Online, không cần cài đặt** | Chạy hoàn toàn trên trình duyệt |
| **Cộng tác thời gian thực** | Nhiều người cùng chỉnh sửa như Google Docs |
| **Template phong phú** | Hàng nghìn template cho paper, luận văn, CV... |
| **Compile tự động** | Xem kết quả PDF ngay khi chỉnh sửa |
| **Hỗ trợ BibTeX** | Quản lý tài liệu tham khảo dễ dàng |

### Link truy cập

[https://www.overleaf.com/](https://www.overleaf.com/)
