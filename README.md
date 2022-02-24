# HỆ THỐNG CẢNH BÁO TRỘM BẰNG GMAIL

- Sử dụng MSP430G2553 giao tiếp UART với ESP8266
- Sử dụng ESP8266 để gửi mail thông qua máy chủ SMTP
- Nguyên lý hoạt động:
  + Hệ thống gồm có 2 chế độ là bật cảnh báo và tắt cảnh báo. Mặc định
ban đầu khi vừa đc cấp nguồn thì hệ thống sẽ vào chế độ bật cảnh báo.
  + Nút nhấn P3 dùng để chuyển đổi giữa 2 chế độ.
  + Khi vào chế độ bật cảnh báo, LCD thông báo bật cảnh báo đồng thời
đèn LED sáng lên và ESP sẽ gửi một gmail đến mail cá nhân một
thông báo đã bật. Sau đó, LCD sẽ hiện nhiệt độ, độ ẩm của phòng cùng
với chữ “ON”. Khi cảm biến PIR phát hiện vật cản thì lập tức còi sẽ hú
trong 10s và gửi một mail thông báo có người đang đi vào. Sau đó
LCD sẽ vào lại giao diện hiển thị nhiệt độ, độ ẩm như lúc đầu.
  + Khi vào chế độ tắt cảnh báo, LCD thông báo tắt cảnh báo đồng thời
LED sẽ tắt và ESP sẽ gửi một mail thông báo đã tắt cảnh báo. Sau đó,
LCD sẽ hiển thị nhiệt độ, độ ẩm của phòng và chữ “OFF”. Khi ở chế
độ tắt cảnh báo, MCU không nhận dữ liệu từ cảm biến vật cản hồng
ngoại

Video demo:  https://youtu.be/hWzx3pw2aIo
