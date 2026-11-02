# Lab 01 – Câu hỏi thảo luận

## 1. Vì sao dùng git mv?
- Git không lưu thao tác "đổi tên"; nó tự suy ra khi file mới giống file cũ.
- `git mv` = di chuyển + stage cả xóa lẫn thêm trong 1 bước, không quên phía nào.
- Commit chỉ di chuyển, không sửa nội dung -> giống 100% -> GitHub hiện "renamed",
  `git log --follow` vẫn truy được lịch sử.

## 2. release/lab01 có phải baseline không?
- Có: là trạng thái đã thống nhất để nộp, chỉ được đổi qua quy trình (hotfix + PR).
- Nhưng nhánh có thể di chuyển; định danh bất biến chính xác là commit SHA / tag
  (Lab 04 sẽ gắn tag v0.1.0).

## 3. Vì sao không commit thẳng master dù làm một mình?
- Giữ master luôn chạy được.
- PR ghi lại lý do, nội dung, cách kiểm thử -> truy vết được, khớp với sprint.
- Có bước tự review (Files changed), sau này gắn CI; revert cả thay đổi dễ.
- Tập thói quen cho làm việc nhóm.