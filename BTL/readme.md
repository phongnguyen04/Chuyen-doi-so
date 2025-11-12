✨ Trình sửa lỗi chính tả AI - Sử dụng Gemini Vision
Một đồ án/bài tập cho môn học Chuyển đổi số

Đây là một ứng dụng desktop (viết bằng Python và CustomTkinter) sử dụng sức mạnh của Google Gemini API (model gemini-2.5-flash) để thực hiện việc kiểm tra và sửa lỗi chính tả, ngữ pháp cho người dùng.

Ứng dụng này là một minh chứng thực tế cho việc áp dụng các công nghệ mới (Generative AI) vào các quy trình truyền thống (soát lỗi văn bản) để tăng hiệu suất và độ chính xác.

🖼️ Giao diện ứng dụng
(Bạn hãy chụp ảnh màn hình ứng dụng của mình (phiên bản đã chỉnh sửa đẹp) và thay thế vào đây. Bạn có thể kéo thả ảnh vào Github hoặc dùng một dịch vụ host ảnh)

🚀 Liên kết với môn học "Chuyển đổi số"
Dự án này không chỉ là một công cụ tiện ích, mà còn là một ví dụ điển hình về Chuyển đổi số (Digital Transformation) trong bối cảnh xử lý thông tin và ngôn ngữ:

Số hóa (Digitization):

Chức năng: "Tải Ảnh" (OCR - Nhận dạng ký tự quang học).

Minh chứng: Ứng dụng có khả năng "đọc" dữ liệu từ dạng analog (chữ viết tay, chữ in trên ảnh) và chuyển đổi nó thành dữ liệu digital (văn bản text). Đây là bước đầu tiên và cốt lõi của mọi quy trình chuyển đổi số: biến thông tin phi cấu trúc thành dữ liệu có thể xử lý được.

Tự động hóa Quy trình (Process Automation):

Quy trình cũ: Người dùng phải tự đọc, tự tìm lỗi, và sửa lỗi thủ công. Quá trình này tốn thời gian, dễ sai sót và đòi hỏi sự tập trung cao độ.

Quy trình mới: Ứng dụng tự động hóa hoàn toàn các bước: "Đọc -> Phân tích -> Tìm lỗi -> Đề xuất sửa lỗi". Người dùng chỉ cần một cú nhấp chuột (click "Kiểm tra & Sửa lỗi") để hoàn tất một công việc vốn mất hàng giờ.

Tích hợp Công nghệ mới (AI Integration):

Thay vì dùng các bộ quy tắc (rule-based) kiểm tra chính tả truyền thống (chỉ phát hiện lỗi sai từ), dự án này tích hợp Generative AI (Gemini).

Điều này cho phép ứng dụng hiểu được ngữ cảnh (context) của câu, từ đó có thể sửa cả lỗi ngữ pháp, lỗi dùng từ và viết lại câu cho tự nhiên hơn, điều mà các công cụ cũ không thể làm được.

Tối ưu hóa Trải nghiệm (User Experience):

Chuyển đổi số lấy người dùng làm trung tâm. Thay vì một script dòng lệnh phức tạp, ứng dụng cung cấp một giao diện GUI (với CustomTkinter) sạch sẽ, thân thiện.

Các tính năng như "Nhập/Xuất DOCX", "Lưu lịch sử" (dùng json), và "Copy" cho thấy sự tập trung vào việc xây dựng một quy trình làm việc hoàn chỉnh và thuận tiện cho người dùng cuối.

🌟 Tính năng chính
✅ Kiểm tra từ Văn bản: Nhập trực tiếp văn bản cần sửa lỗi.

📷 Kiểm tra từ Hình ảnh: Tải lên ảnh chụp (văn bản, viết tay) để AI tự động đọc và sửa lỗi (OCR).

📄 Nhập liệu DOCX: Tải trực tiếp nội dung từ file .docx vào ứng dụng.

💾 Xuất file DOCX: Lưu kết quả đã sửa lỗi ra một file .docx mới.

📋 Copy kết quả: Sao chép nhanh văn bản đã sửa vào clipboard.

📜 Lịch sử chỉnh sửa: Tự động lưu lại lịch sử các lần sửa (dữ liệu lưu trong history.json) và cho phép xem lại, xóa.

🎨 Giao diện hiện đại: Sử dụng customtkinter với giao diện sáng, sạch sẽ, chuyên nghiệp.

🛠️ Công nghệ sử dụng
Ngôn ngữ: Python 3.x

Giao diện (GUI): customtkinter

Lõi AI: google-generativeai (Sử dụng Gemini 2.5 Flash)

Xử lý ảnh: Pillow (PIL) (Để tải ảnh, tạo preview và nạp icon)

Xử lý file: python-docx (Để đọc/ghi file Word), json (Để đọc/ghi lịch sử)

Quản lý API Key: python-dotenv

⚙️ Cài đặt & Chạy ứng dụng
1. Chuẩn bị Môi trường
Bạn cần cài đặt Python 3.7+.

(Khuyến khích) Tạo một môi trường ảo (virtual environment):

Bash

python -m venv venv
source venv/bin/activate  # Trên macOS/Linux
.\venv\Scripts\activate   # Trên Windows
2. Cài đặt thư viện
Tạo một file tên là requirements.txt với nội dung sau:

customtkinter
google-generativeai
pillow
python-docx
python-dotenv
Sau đó, chạy lệnh:

Bash

pip install -r requirements.txt
3. Cài đặt API Key
Truy cập Google AI Studio (Makersuite) để lấy API Key của bạn.

Tạo một file tên là .env trong cùng thư mục với file app.py (file code chính của bạn).

Thêm nội dung sau vào file .env:

GOOGLE_API_KEY="YOUR_API_KEY_HERE"
(Thay YOUR_API_KEY_HERE bằng key bạn vừa lấy)

4. Chạy ứng dụng
Bash

python app.py
(Thay app.py bằng tên file Python chính của bạn)

💡 Hướng phát triển (Nếu có thời gian)
So sánh "Diff": Hiển thị văn bản gốc và văn bản đã sửa cạnh nhau, bôi đỏ/xanh các từ đã bị thay đổi.

Xử lý hàng loạt: Cho phép chọn một thư mục chứa nhiều ảnh/file DOCX để sửa lỗi cùng lúc.

Đóng gói (Packaging): Dùng PyInstaller để đóng gói thành một file .exe duy nhất cho người dùng cuối.