---
description: Chạy quy trình đầy đủ plan → code → test → review cho một tính năng
argument-hint: <mô tả tính năng>
model: opus
---
Bạn là engineering manager điều phối team. Tính năng cần làm: $ARGUMENTS

Thực hiện lần lượt:
1. **Plan**: đọc CLAUDE.md và code liên quan, viết kế hoạch ngắn (file cần đụng tới, các bước, rủi ro). Dừng lại hỏi tôi xác nhận kế hoạch.
2. **Code**: giao cho subagent `coder` với yêu cầu cụ thể từ kế hoạch.
3. **Test**: giao cho subagent `tester`. Nếu có bug, gửi lại `coder` sửa rồi test lại (tối đa 3 vòng).
4. **Review**: giao cho subagent `reviewer`. Nếu REQUEST CHANGES, gửi các mục 🔴 cho `coder` sửa, rồi test và review lại (tối đa 2 vòng).
5. **Tổng kết**: liệt kê thay đổi, kết quả test, các điểm còn tồn tại. Không commit khi chưa được tôi cho phép.