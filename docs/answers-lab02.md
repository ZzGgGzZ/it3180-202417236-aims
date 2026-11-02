# Lab 02 – Câu hỏi thảo luận

> Ghi chú: làm một mình nên không bật Require approvals. Bước "Request changes → Approve"
> được thay bằng comment review trên dòng code (PR #4) + Resolve conversation.

## 1. Vì sao phải đồng bộ master trước khi tạo PR?
- Nhánh tạo từ master cũ chưa có thay đổi mới (vd: print_cart).
- Đồng bộ để phát hiện xung đột ngay trên nhánh mình, kiểm thử đúng code sẽ được
  tích hợp ("thứ được duyệt = thứ được tích hợp"), reviewer thấy diff sạch.

## 2. Khi nào KHÔNG được rebase?
- Khi commit đã push và người khác có thể đang dựa trên nó (master, release/*).
- Rebase tạo SHA mới -> lịch sử người khác bị lệch, phải force push.
- Chỉ rebase nhánh riêng chưa chia sẻ.

## 3. feature/* khác topic/* ra sao?
- feature/*: thêm chức năng cho phần mềm (print_cart, search_by_title).
- topic/*: thay đổi theo chủ đề, không phải tính năng: tài liệu, cấu hình, template.