# Lab 03 – Câu hỏi thảo luận

## 1. Merge base là gì?
- Là commit chung gần nhất của hai nhánh (điểm hai nhánh tách ra).
- Git merge kiểu "3 chiều": so sánh merge base với phía A và phía B.
  - Chỉ một phía sửa dòng đó -> Git tự lấy bản đã sửa.
  - Cả hai phía cùng sửa một dòng theo cách khác nhau -> xung đột.
- Ví dụ trong repo: `git merge-base 6568afa dbe52ad` -> 52038d4 (merge PR #11).
  Cả feature/vietnamese-messages và feature/show-added-title đều sửa dòng print
  trong Cart.add_dvd so với 52038d4 -> xung đột, giải quyết ở commit 45b8184.

## 2. Vì sao master và release/* phải dùng revert, không dùng reset?
- master, release/* là lịch sử đã chia sẻ (đã push, người khác/nhánh khác dựa vào).
- reset dời con trỏ nhánh, bỏ commit -> phải force push, lịch sử người khác bị lệch,
  có thể mất commit của người khác; branch protection cũng chặn force push.
- revert tạo commit mới đảo ngược thay đổi -> lịch sử chỉ ghi thêm, vẫn truy vết được
  "đã đưa vào gì, đã gỡ ra gì, vì sao" (vd: PR #14 revert PR #13).
- Với merge commit phải dùng `git revert -m 1 <sha>` để chọn cha thứ 1 (master) làm gốc.