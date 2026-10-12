# Thực hành Lab A6 - Lập trình thiết bị di động

**Họ và tên:** Bùi Quang Duy
**MSSV:** 231A290127

## Mô tả dự án
Đây là mã nguồn bài thực hành Lab A6: Ứng dụng "Đăng ký học phần" sử dụng Java và XML. 
Dự án bao gồm 2 màn hình (Form đăng ký và Màn hình tóm tắt thông tin xác nhận), tích hợp đầy đủ các nhóm control cơ bản như: `EditText`, `Spinner`, `RadioGroup`, `CheckBox`, `MaterialSwitch`, và `ToggleButton`. 
App đã xử lý bắt lỗi dữ liệu hợp lệ (validate) cho toàn bộ form trước khi đóng gói gửi sang màn hình xác nhận thông qua `Intent`.

## Các bài nâng cao đã hoàn thành
Dự án này đã hoàn thành **2 bài nâng cao** theo đúng yêu cầu của tài liệu hướng dẫn thực hành:

### 1. Bài NC2: Đếm số buổi đã chọn
- **Mô tả:** Đếm tổng số buổi học được sinh viên chọn (Sáng, Chiều, Tối) và hiển thị kết quả trực tiếp ngay phía dưới nhóm CheckBox.
- **Cách xử lý:** Khởi tạo và sử dụng chung một bộ lắng nghe sự kiện `OnCheckedChangeListener` cho cả 3 đối tượng CheckBox. Mỗi khi trạng thái tick có sự thay đổi, hệ thống sẽ tự động tính toán lại số lượng và cập nhật hiển thị lên giao diện thông qua `TextView`.

### 2. Bài NC3: Tích hợp chế độ tối (Dark Mode)
- **Mô tả:** Thêm một công tắc (`MaterialSwitch`) để người dùng có thể đổi giao diện nền màn hình sang chế độ tối ngay lập tức mà không cần khởi động lại ứng dụng.
- **Cách xử lý:** Bắt sự kiện bật/tắt của Switch. Khi Switch được bật, ứng dụng sẽ gọi lệnh `AppCompatDelegate.setDefaultNightMode(AppCompatDelegate.MODE_NIGHT_YES)` để kích hoạt theme tối. Khi người dùng tắt, truyền tham số `MODE_NIGHT_NO` để lập tức quay trở lại theme sáng ban đầu.
