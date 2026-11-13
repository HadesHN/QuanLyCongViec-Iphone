# Sổ công việc — GitHub Pages / iPhone

Đây là ứng dụng web có thể thêm lên màn hình chính iPhone, không phải APK hoặc IPA. Bộ chứa toàn bộ tài nguyên v5, không cần npm hay bước build.

## Cách đơn giản: tải tệp lên GitHub

1. Tạo repository mới, ví dụ `so-cong-viec`; dùng nhánh `main`. Để triển khai miễn phí theo cách thông thường có thể dùng repository public.
2. Giải nén bộ này. Trong repository chọn Add file → Upload files. Tải **các tệp bên trong** thư mục lên gốc repository, để `index.html` nằm ngay ở gốc; không tải nguyên tệp ZIP.
3. Commit changes. Mở Settings → Pages → Build and deployment → Source: **Deploy from a branch**; Branch: **main**, Folder: **/(root)** → Save.
4. Chờ GitHub Pages triển khai, lấy địa chỉ ở Settings → Pages. Dạng địa chỉ: `https://TEN-TAI-KHOAN.github.io/so-cong-viec/` (thay bằng tài khoản và tên repository thật).

## Cách dùng workflow có sẵn

Nếu đẩy toàn bộ thư mục bằng Git (gồm `.github/workflows/pages.yml`), chọn Settings → Pages → Source: **GitHub Actions**, sau đó push lên `main` hoặc chạy workflow Publish So Cong Viec trong tab Actions. Nếu nhánh mặc định tên khác, đổi `branches` trong workflow. Không cần dùng đồng thời hai cách triển khai.

Khi chỉ tải bằng giao diện web, thư mục ẩn `.github` có thể không được tải lên; cách Deploy from a branch vẫn chạy được vì không cần workflow.

## Cài lên iPhone

1. Mở địa chỉ HTTPS đã triển khai bằng **Safari**.
2. Bấm Chia sẻ → **Thêm vào Màn hình chính** (Add to Home Screen) → Thêm.
3. Mở biểu tượng Sổ công việc mới trên màn hình chính; thử thêm một văn bản.
4. Mở thành công lần đầu và chờ tài nguyên lưu đệm trước khi thử ngắt mạng.

## Dữ liệu và nhắc việc

- Dữ liệu công việc và nội dung tệp được lưu cục bộ trong trình duyệt/ứng dụng web của thiết bị, không tự gửi lên GitHub và không đồng bộ với máy tính/APK.
- Dùng Sao lưu Excel → chuyển tệp → Khôi phục để chuyển dữ liệu. Kiểm tra kho đang dùng vì Safari và bản đã thêm màn hình chính có thể có kho riêng.
- Khi lưu Excel trên iPhone, làm theo hộp thoại tải xuống/chia sẻ của iOS; kiểm tra trong ứng dụng Tệp. Có thể cần chọn Lưu vào Tệp.
- Không đưa bản sao lưu, tệp đính kèm nghiệp vụ hay dữ liệu cá nhân vào repository. Repository và website có thể công khai; PIN chỉ khóa giao diện, không hạn chế người truy cập website hoặc mã hóa bản sao.
- Nhắc ngay trong giao diện hoạt động khi ứng dụng mở. Quyền/thông báo hệ thống phụ thuộc iOS và môi trường chạy; bộ này **chưa có Web Push**, không nhắc khi đã đóng ứng dụng. Nếu nút Bật thông báo không được hỗ trợ, vẫn theo dõi qua tab Cần chú ý.
- Giữ nguyên tên repository/địa chỉ khi cập nhật để tiếp tục truy cập dữ liệu. Sao lưu trước khi xóa dữ liệu Safari, gỡ biểu tượng hoặc đổi địa chỉ.

## Cập nhật

Sao lưu, thay toàn bộ các tệp mã web, commit và chờ triển khai. Đóng/mở lại ứng dụng để nhận phiên bản mới. Không chọn xóa dữ liệu website nếu chưa có bản sao. Cấu trúc dùng đường dẫn tương đối nên hỗ trợ cả website ở thư mục repository.

Bộ đã kiểm tra cấu trúc, đường dẫn tương đối và cú pháp JavaScript; chưa đăng lên tài khoản GitHub của anh và chưa kiểm tra trên iPhone thật.

Hướng dẫn chính thức: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
