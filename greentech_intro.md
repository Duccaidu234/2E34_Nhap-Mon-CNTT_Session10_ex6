# 🌱 GreenTech - Giải pháp Nông nghiệp Xanh Thông minh

> *Dự án công nghệ hỗ trợ phát triển nông nghiệp bền vững, tối ưu hóa nguồn tài nguyên nước và dinh dưỡng cho cây trồng thông qua hệ thống cảm biến IoT.*

---

## 📌 Phân tích kỹ thuật & Quản lý dự án

### 1. So sánh Plain Text (Markdown) và Rich Text (.docx)

* **Bản chất lưu trữ:**
  * **Rich Text (`.docx`):** Là một tập tin nén nhị phân (ZIP archive chứa nhiều file XML và siêu dữ liệu). Khi làm việc nhóm trên Git, hệ thống không thể đọc từng dòng văn bản mà coi đây là file binary, dẫn đến việc không thể sử dụng tính năng **Git Diff** để xem chính xác ai đã sửa dòng nào.
  * **Plain Text (`.md`):** Là văn bản thô thuần túy. Mọi ký tự định dạng đều là các ký tự văn bản chuẩn. Điều này giúp Git dễ dàng theo dõi chi tiết từng dòng thay đổi (line-by-line) và xử lý merge code vô cùng nhanh chóng.

* **Khả năng chống hư hại dữ liệu (Corrupt Resilience):**
  * Trong trường hợp gặp lỗi đường truyền mạng khiến file bị mất 1 byte dữ liệu:
    * File `.docx` sẽ bị hỏng toàn bộ cấu trúc nén/XML và phần mềm không thể mở được (*File corrupt*).
    * File `.md` vẫn mở và đọc bình thường các phần còn lại vì nó chỉ chứa ký tự văn bản thuần.

---

## 🎯 Giới thiệu dự án

**GreenTech** là hệ sinh thái phần cứng kết hợp phần mềm mã nguồn mở, được thiết kế dành riêng cho các mô hình canh tác hiện đại. Hệ thống cho phép thu thập dữ liệu môi trường thời gian thực, tự động hóa quy trình chăm sóc và cung cấp giao diện quản trị trực quan cho người sử dụng.

---

## ✨ Các tính năng cốt lõi

* [x] **Giám sát thời gian thực:** Theo dõi các chỉ số nhiệt độ, độ ẩm không khí và độ ẩm đất 24/7.
* [x] **Tự động hóa thông minh:** Kích hoạt hệ thống tưới tiêu dựa trên ngưỡng dữ liệu phân tích từ cảm biến.
* [ ] **Đồng bộ hóa đám mây:** Lưu trữ nhật ký hoạt động và hiển thị biểu đồ thống kê trực quan.

---

## 🛠️ Công nghệ sử dụng

| Thành phần | Công nghệ / Nền tảng | Chức năng |
| :--- | :--- | :--- |
| **Vi điều khiển (SoC)** | ESP32 / Arduino | Thu thập dữ liệu & điều khiển thiết bị |
| **Cảm biến** | DHT22, Capacitive Soil Moisture | Đo thông số môi trường & độ ẩm đất |
| **Quản lý tài liệu** | Markdown (`.md`), Git & GitHub | Quản lý mã nguồn và tài liệu dự án |