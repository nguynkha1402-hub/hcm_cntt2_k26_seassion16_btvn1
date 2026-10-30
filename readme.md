## Giải quyết bẫy
-Sập nguồn: Hệ thống dùng cơ chế Lưu nguyên tử, đảm bảo file 3D không bị hỏng hay mất cấu trúc khi mất điện giữa chừng.

-Mất mạng: File được đưa vào Hàng đợi đồng bộ (Sync Queue). Ứng dụng ưu tiên lưu xuống ổ cứng Local để Designer làm tiếp, và sẽ tự động đẩy lên Cloud ngay khi có Internet trở lại mà không bị đứt đoạn.

## Sơ đồ luồng dữ liệu & Xử lý xung đột

-Luồng dữ liệu: Designer ấn Ctrl + S ➔ Ghi vào Local SSD ➔ Cloud Client phát hiện thay đổi ➔ Đồng bộ ngầm lên Server.

-Xung đột & Khôi phục: Khi ổ cứng bị "Bad Sector" làm hỏng file đồng bộ lên, hoặc có người ghi đè nhầm, hệ thống không làm mất dữ liệu cũ. Nhóm chỉ cần lên nền tảng Cloud, mở Version History của file đó, chọn mốc thời gian trước khi lỗi và ấn Restore để kéo lại bản vẽ ổn định.

## Quy trình 3 bước thiết lập chuẩn cho Designer

-Cài đặt Cloud Client: Cài Google Drive hoặc OneDrive bản Desktop, thiết lập chế độ Mirror Files (lưu song song dữ liệu vật lý ở Local và bản sao ở Cloud).

-Chuyển đổi Workspace: Đưa toàn bộ file dự án vào thư mục đồng bộ này (VD: C:\Google Drive\BaoTangPTIT). Tuyệt đối không lưu rải rác ở Desktop hay ổ đĩa khác.

-Thay đổi thói quen chia sẻ: Bỏ việc nén file gửi Zalo. Mọi thành viên chỉ sử dụng Share Link từ Cloud. Designer chỉ cần làm việc và ấn Ctrl + S bình thường, hệ thống tự động backup và quản lý các phiên bản.