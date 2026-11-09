# Bài 6: Ứng dụng AI trong khắc phục lỗi Git Permission Denied

Lỗi: `error: open(".git/FETCH_HEAD"): Permission denied`

## 1. Prompt 3 thành phần (Vai trò - Bối cảnh - Yêu cầu)

```
**Vai trò:** Bạn là một kỹ sư phần mềm giàu kinh nghiệm về Git, đang hướng dẫn một sinh viên mới học.

**Bối cảnh:** Mình đang push code lên GitHub thì Terminal báo lỗi
error: open(".git/FETCH_HEAD"): Permission denied.
Mình dùng Windows, đã thử chạy lại nhiều lần nhưng không được. Gần deadline nên cần sửa gấp.

**Yêu cầu:** Giải thích lỗi này nghĩa là gì bằng ngôn ngữ đơn giản,
liệt kê các nguyên nhân thường gặp và các bước sửa theo thứ tự từ an toàn đến mạnh tay.
Với mỗi lệnh phải nói rõ lệnh đó làm gì và có rủi ro gì không.
```

## 2. Giải thích lỗi (theo AI, sau khi mình đọc lại và hiểu)

- Lỗi nghĩa là Git **không được phép mở/ghi file** `.git/FETCH_HEAD`.
- Nguyên nhân thường gặp: thư mục `.git` thuộc quyền của người dùng khác hoặc admin, file bị đặt chỉ đọc (read-only), hoặc bị phần mềm khác (antivirus, OneDrive) khóa.

## 3. Thực hiện "Run as Administrator"

Các bước:

1. Đóng Terminal cũ.
2. Bấm Start, gõ `cmd` hoặc `PowerShell`, chuột phải chọn **Run as administrator**.
3. Dùng `cd` vào thư mục dự án.
4. Chạy lại `git push` (hoặc `git fetch`) xem còn lỗi không.

> <img width="1480" height="756" alt="img_v3_02179_3b95de30-d09a-4641-aaef-0d5b12ec4aix" src="https://github.com/user-attachments/assets/28a9c4ec-ed87-40f6-83b4-a88ca05deb78" />


## 4. Nếu vẫn không sửa được: tin nhắn nhờ giảng viên (Bug Reporting Framework)

```
Chào thầy Sang, em là Nguyễn Vũ Quốc Anh (MSSV: N26DTCN004).
Em đang gặp lỗi khi push code lên GitHub, em xin nhờ thầy hỗ trợ ạ.

**Context:** Windows 11, Git version 2.56.0 (bản 64-bit).
Em đang push bài tập lên GitHub, dự án nằm ở thư mục FECT_HEAD

**Expected:** Lệnh git push chạy thành công và code lên GitHub.

**Actual:** Terminal báo lỗi, không push được.

**Log:**
error: open(".git/FETCH_HEAD"): Permission denied

Em đã thử: chạy lại lệnh nhiều lần, chạy Terminal bằng quyền Administrator
nhưng vẫn lỗi. Em gửi kèm ảnh chụp màn hình ạ.
Em cảm ơn thầy/cô.
```
