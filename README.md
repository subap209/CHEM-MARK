# Chấm bài Hóa THPT (PWA)

Ứng dụng chấm bài kiểm tra môn Hóa học theo cấu trúc đề THPT, cài được lên Android và iPhone, chạy khi không có mạng, có quét phiếu trả lời bằng camera.

## Các file
- `index.html`: toàn bộ ứng dụng (giao diện, chấm điểm, nhận dạng phiếu bằng camera)
- `manifest.webmanifest`, `icon-*.png`: để cài lên màn hình chính
- `sw.js`: lưu sẵn ứng dụng để dùng khi không có mạng

## Đưa lên mạng để mở trên điện thoại (chọn một cách)
**Cách 1: GitHub Pages (miễn phí, có sẵn mã nguồn để chỉnh sửa)**
1. Tạo kho mới trên github.com, tải toàn bộ các file trong thư mục này lên.
2. Vào Settings, Pages, chọn nhánh `main` và thư mục `/ (root)`, bấm Save.
3. Sau ít phút có đường link dạng `https://tenban.github.io/tenkho/`.

**Cách 2: Netlify Drop (nhanh nhất)**
1. Mở app.netlify.com/drop, kéo cả thư mục này vào.
2. Nhận ngay đường link HTTPS.

Bắt buộc dùng HTTPS (hai cách trên đều có) thì camera và chế độ ngoại tuyến mới hoạt động.

## Cài lên điện thoại
- **iPhone/iPad:** mở link bằng Safari, bấm Chia sẻ, chọn "Thêm vào Màn hình chính".
- **Android:** mở link bằng Chrome, bấm menu ba chấm, chọn "Cài đặt ứng dụng".

## Quy trình dùng
1. **Lớp học:** tạo lớp, dán danh sách (STT, mã HS, họ tên) hoặc chọn file CSV.
2. **Đề kiểm tra:** tạo đề, đặt cấu trúc (mặc định 18 + 4 + 6 câu), nhập đáp án từng mã đề.
3. **In phiếu trả lời:** trong màn hình đề, bấm "In phiếu trả lời". In A4, tỷ lệ 100%, đen trắng.
4. **Chấm bài:** chọn đề và học sinh, bấm "Quét phiếu bằng camera". Kiểm tra các ô nghi ngờ rồi lưu. Ứng dụng tự chuyển sang học sinh kế tiếp.
5. **Bảng điểm, Thống kê:** xem điểm cả lớp, câu khó, đáp án nhiễu; sao chép hoặc tải CSV để mở bằng Excel.
6. **Cài đặt:** sao lưu và khôi phục toàn bộ dữ liệu bằng file JSON.

## Quy tắc tính điểm mặc định
- Phần I: 18 câu, 0,25 điểm mỗi câu.
- Phần II: 4 câu, mỗi câu 4 ý. Đúng 1/2/3/4 ý được 0,1/0,25/0,5/1 điểm.
- Phần III: 6 câu, 0,25 điểm mỗi câu, có sai số cho phép và nhiều đáp án chấp nhận được (ngăn cách bằng dấu `;`).
Tất cả có thể đổi trong Cài đặt hoặc ngay trong từng đề.

## Mẹo chụp phiếu
- Thấy rõ cả 4 ô đen ở góc, ô to nhất ở góc trên bên trái.
- Đặt phiếu phẳng, đủ sáng, tránh bóng tay và chói đèn.
- Học sinh tô kín ô bằng bút chì đen hoặc bút mực đen.

## Lưu ý
- Dữ liệu lưu trong trình duyệt của từng máy, không tự đồng bộ giữa các máy. Hãy sao lưu định kỳ.
- Nếu camera trực tiếp không mở được, dùng nút "Chụp bằng app máy ảnh" (vẫn nhận dạng bình thường).
- Chưa có xuất file Excel (.xlsx) và PDF: hiện có sao chép bảng điểm dán vào Excel/Google Sheets và tải CSV.
