# KeToanGo

Chương trình giúp kế toán lấy hoá đơn điện tử về máy tính, thay vì tải từng hoá đơn bằng tay.

- **Tải từ cổng thuế:** đăng nhập [hoadondientu.gdt.gov.vn](https://hoadondientu.gdt.gov.vn) bằng mã số thuế của doanh nghiệp, chọn khoảng ngày, chương trình tải về toàn bộ hoá đơn **mua vào**, **bán ra** hoặc cả hai.
- **Lấy từ email:** lấy các file PDF hoá đơn mà nhà cung cấp gửi tới hộp thư Gmail.

## Tải về

Vào mục [Releases](https://github.com/nguyenhoangkhan/ke-toan-gon/releases/latest), tải file `KeToanGo.exe` rồi bấm đúp để chạy. Không cần cài đặt.

Yêu cầu: máy Windows có trình duyệt Microsoft Edge hoặc Google Chrome (Windows 10, 11 đều có sẵn Edge). Giao diện mở trong một cửa sổ riêng của trình duyệt.

Khi có bản mới, chương trình tự báo. Bạn bấm **Cập nhật ngay** là xong. Chương trình chỉ cài bản có chữ ký số của tác giả.

## Chương trình làm được gì

### Tải từ cổng thuế

- Tải file **XML** gốc của từng hoá đơn trong khoảng ngày đã chọn, gồm cả hoá đơn khởi tạo từ máy tính tiền.
- Lập **bảng kê Excel**, đánh dấu những hoá đơn cần chú ý theo kết quả kiểm tra của cổng thuế và liệt kê riêng những hoá đơn chưa tải được.
- Tải thêm bản **PDF** của hoá đơn từ trang tra cứu của phần mềm hoá đơn bên bán (tuỳ chọn):

  | Phần mềm hoá đơn bên bán                                                     | Lấy PDF                                           |
  | ---------------------------------------------------------------------------- | ------------------------------------------------- |
  | MISA meInvoice                                                               | Tự động                                           |
  | Softdreams EasyInvoice, Thái Sơn EInvoice, Viettel S-Invoice, Gas Petrolimex | Bạn gõ mã xác nhận, chương trình làm phần còn lại |
  | HT Invoice, HILO Invoice                                                     | Chương trình mở sẵn trang tra cứu để bạn tự tải   |
  | FAST, VNPT Invoice, BKAV eHoaDon                                             | Chưa hỗ trợ                                       |

Kết quả nằm trong thư mục bạn chọn (mặc định là `HoaDonDienTu` trong thư mục cá nhân), chia theo mã số thuế:

```
BangKe_MuaVao_<từ ngày>-<đến ngày>.xlsx
XML_MuaVao\   file XML của từng hoá đơn
PDF_MuaVao\   file PDF (nếu chọn tải PDF)
```

Hoá đơn bán ra nằm trong các thư mục và bảng kê có chữ `BanRa`.

### Lấy từ email

- Đăng nhập Gmail bằng **mật khẩu ứng dụng** 16 ký tự. Gmail không cho dùng mật khẩu thường ở đây. Cách tạo xem tại [trợ giúp của Google](https://support.google.com/accounts/answer/185833).
- Lọc theo khoảng ngày nhận, có thể chỉ lấy thư của một số người gửi hoặc tên miền.
- Hộp thư chỉ được **đọc**: chương trình không đánh dấu đã đọc, không xoá, không di chuyển email nào.
- File PDF lưu theo `HoaDonTuEmail\<ngày nhận>\<người gửi>\`, kèm bảng kê Excel. Chạy lại nhiều lần cũng không tải trùng.

## Dữ liệu của bạn

- Chương trình chạy ngay trên máy của bạn. Hoá đơn, bảng kê và nhật ký **không được gửi cho tác giả hay bất kỳ ai**.
- Chương trình chỉ kết nối tới cổng hoá đơn điện tử của cơ quan thuế, máy chủ Gmail (khi lấy từ email), trang tra cứu của phần mềm hoá đơn bên bán (khi tải PDF) và nơi đặt bản cập nhật.
- Mật khẩu cổng thuế và mật khẩu ứng dụng Gmail **không được lưu lại**. Chương trình chỉ nhớ mã số thuế, địa chỉ email, danh sách người gửi, thư mục lưu và phiên đăng nhập cổng thuế để lần sau đỡ nhập lại. Vì vậy không nên dùng chương trình trên tài khoản máy tính dùng chung với người khác.

## Lưu ý

- File **XML** mới là hoá đơn có giá trị pháp lý. Bảng kê Excel và file PDF chỉ để tra cứu, đối chiếu.
- Chương trình không bảo đảm tải đủ và đúng mọi hoá đơn: cổng thuế có thể cập nhật chậm, đường truyền có thể lỗi, các trang tra cứu có thể thay đổi. Hãy đối chiếu với cổng thuế và sổ sách trước khi kê khai, hạch toán.
- KeToanGo không phải sản phẩm của cơ quan thuế, của Google hay của các đơn vị phần mềm hoá đơn.
- Chương trình được cung cấp theo hiện trạng. Điều khoản sử dụng đầy đủ nằm ngay trong chương trình.
