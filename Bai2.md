# Phân loại và sắp xếp Product Backlog theo MoSCoW

- Môn học: IT206 (Quản lý dự án với Agile/Scrum)
- Bài học: Session 06 - Thực hành: Acceptance Criteria, Prioritized Product Backlog
- Vai trò: Product Owner (PO)
- Dự án: Hệ thống mượn sách thư viện (độc giả đặt mượn online, nhận sách giấy tại quầy trong 48 giờ)
- Kế hoạch: Bản phát hành đầu tiên (Release 1, MVP) triển khai trong 3 Sprint (mỗi Sprint 2 tuần).

---

## 1. Phân loại 12 hạng mục theo MoSCoW

Nhóm Product Owner phân loại 12 hạng mục dựa trên câu hỏi kiểm tra của từng nhóm và mức độ phụ thuộc giữa các chức năng:

- Must have: Thiếu nó thì hệ thống không thể vận hành được luồng mượn sách online. Quy định tối đa 5 hạng mục; nhóm chọn 4 mục.
- Should have: Chức năng quan trọng, nhưng nếu chưa làm xong ở Release 1 thì vẫn có cách xử lý tạm thời (workaround) bằng quy trình thủ công tại quầy.
- Could have: Tính năng hỗ trợ trải nghiệm, nếu cắt bỏ ở đợt đầu thì ảnh hưởng rất nhỏ đến mục tiêu chính.
- Won't have (this time): Chưa làm trong 3 Sprint đầu, vẫn lưu trong Product Backlog để đánh giá ở các đợt phát hành tiếp theo.

### Bảng phân loại chi tiết:

| STT | Tên hạng mục | Nhóm MoSCoW | Lý do phân loại và quan hệ phụ thuộc |
| :---: | :--- | :---: | :--- |
| 10 | Thủ thư quản lý kho sách (thêm/sửa/xóa sách) | Must have | Cần có dữ liệu sách trong kho thì hệ thống mới có thông tin để tìm kiếm và cho mượn. Đây là chức năng nền tảng cho các mục sau. |
| 1 | Đăng nhập/đăng ký tài khoản độc giả | Must have | Cần định danh độc giả để ghi nhận ai đang giữ sách giấy của thư viện. Không thể cho mượn tài sản nặc danh. |
| 2 | Tìm kiếm sách theo tên/tác giả | Must have | Độc giả phải tìm được sách trên hệ thống thì mới chọn để đặt mượn được. Mục này phụ thuộc vào dữ liệu sách ở mục 10. |
| 3 | Mượn sách online (có giới hạn số sách mượn cùng lúc) | Must have | Tính năng mượn sách là mục đích chính của toàn bộ hệ thống. Phụ thuộc vào mục 10 (kho sách), mục 1 (tài khoản) và mục 2 (tìm kiếm). |
| 9 | Xem lịch sử mượn sách của bản thân | Should have | Giúp độc giả tra cứu các sách đang mượn và hạn trả. Nếu chưa có trên web, bạn đọc có thể xem phiếu hẹn giấy hoặc hỏi thủ thư tại quầy (có workaround). Phụ thuộc vào mục 3. |
| 4 | Gia hạn mượn sách online | Should have | Giúp bạn đọc gia hạn thuận tiện. Nếu chưa có, độc giả có thể mang sách đến quầy nhờ thủ thư gia hạn trực tiếp (có workaround). Phụ thuộc vào mục 3. |
| 8 | Thông báo email khi sắp đến hạn trả sách | Should have | Giúp giảm tình trạng trả sách trễ hạn. Độc giả vẫn có thể tự ghi nhớ ngày hẹn trả ghi trên phiếu lúc nhận sách (có workaround). |
| 5 | Đặt trước sách khi hết (kèm thông báo khi sách có sẵn) | Should have | Giúp giữ chỗ khi sách hết bản in. Khi chưa có tính năng này, thủ thư có thể ghi sổ tay danh sách chờ tại quầy (có workaround). Phụ thuộc vào mục 3. |
| 12 | Tích hợp đăng nhập bằng Google/Facebook | Could have | Tiện lợi cho người dùng nhưng không bắt buộc, vì hệ thống đã có tính năng đăng ký và đăng nhập chuẩn ở mục 1. |
| 6 | Đánh giá và bình luận sách sau khi đọc | Could have | Tăng tính kết nối bạn đọc nhưng không ảnh hưởng đến việc mượn và trả sách giấy ở đợt phát hành đầu. Phụ thuộc vào mục 3. |
| 7 | Gợi ý sách theo sở thích cá nhân (recommendation) | Won't have (this time) | Hệ thống mới chưa có dữ liệu lịch sử đọc của người dùng để phân tích gợi ý chính xác, nên để dành cho các đợt phát hành sau. |
| 11 | Chat trực tiếp với thủ thư | Won't have (this time) | Cần người trực chat thường xuyên và tốn thời gian xây dựng chức năng thời gian thực. Độc giả có thể gọi điện thoại, gửi email hoặc trao đổi trực tiếp tại quầy thư viện. |

Nhóm Must have gồm 4 hạng mục, nằm trong giới hạn không quá 5 mục theo quy định.

---

## 2. Thứ tự ưu tiên trong Product Backlog

Product Backlog được sắp xếp tuần tự từ 1 đến 12 theo nhóm MoSCoW và thứ tự phụ thuộc kỹ thuật:

| Thứ tự | Mã PBI | Tên hạng mục | Nhóm MoSCoW | Phụ thuộc vào | Dự kiến thực hiện |
| :---: | :---: | :--- | :---: | :---: | :---: |
| 1 | PBI-10 | Thủ thư quản lý kho sách (thêm/sửa/xóa sách) | Must have | Không | Sprint 1 |
| 2 | PBI-01 | Đăng nhập/đăng ký tài khoản độc giả | Must have | Không | Sprint 1 |
| 3 | PBI-02 | Tìm kiếm sách theo tên/tác giả | Must have | PBI-10 | Sprint 1 và 2 |
| 4 | PBI-03 | Mượn sách online (có giới hạn số sách mượn cùng lúc) | Must have | PBI-10, PBI-01, PBI-02 | Sprint 2 |
| 5 | PBI-09 | Xem lịch sử mượn sách của bản thân | Should have | PBI-01, PBI-03 | Sprint 2 |
| 6 | PBI-04 | Gia hạn mượn sách online | Should have | PBI-03, PBI-09 | Sprint 3 |
| 7 | PBI-08 | Thông báo email khi sắp đến hạn trả sách | Should have | PBI-01, PBI-03 | Sprint 3 |
| 8 | PBI-05 | Đặt trước sách khi hết (kèm thông báo khi sách có sẵn) | Should have | PBI-03 | Sprint 3 |
| 9 | PBI-12 | Tích hợp đăng nhập bằng Google/Facebook | Could have | PBI-01 | Sprint 3 (nếu còn thời gian) |
| 10 | PBI-06 | Đánh giá và bình luận sách sau khi đọc | Could have | PBI-01, PBI-03 | Xem xét cho Release 2 |
| 11 | PBI-07 | Gợi ý sách theo sở thích cá nhân (recommendation) | Won't have | PBI-03, PBI-09 | Xem xét cho Release sau |
| 12 | PBI-11 | Chat trực tiếp với thủ thư | Won't have | PBI-01 | Xem xét cho Release sau |

### Giải thích quan hệ phụ thuộc:
1. Nhóm Must have đi theo luồng logic: trước tiên thủ thư phải tạo kho sách (PBI-10) và có tài khoản bạn đọc (PBI-01), độc giả tìm được sách (PBI-02) rồi mới thực hiện thao tác mượn sách (PBI-03).
2. Nhóm Should have chỉ làm được khi đã có chức năng mượn sách: muốn xem lịch sử (PBI-09), gia hạn (PBI-04) hay đặt trước (PBI-05) thì hệ thống phải có dữ liệu mượn từ PBI-03. Vì vậy PBI-03 đứng trước toàn bộ nhóm này.
3. Các mục Won't have vẫn được giữ lại ở cuối backlog để tiện theo dõi kế hoạch sau này mà không làm xáo trộn phạm vi 3 Sprint đầu.

---

## 3. Tự phản biện các hạng mục có thể gây tranh luận

1. Tích hợp đăng nhập Google/Facebook (mục 12): Bên truyền thông hoặc giao diện có thể muốn xếp vào Should have vì bạn đọc trẻ quen dùng tài khoản mạng xã hội để đăng nhập cho nhanh. Dù vậy, với thư viện, tài khoản độc giả cần đối soát với thẻ thư viện hoặc mã sinh viên để quản lý việc trả sách giấy, nên đăng nhập hệ thống tiêu chuẩn ở mục 1 là đủ cho bản đầu tiên.
2. Chat trực tiếp với thủ thư (mục 11): Có ý kiến cho rằng cần đưa vào Should have để hỗ trợ bạn đọc khi hệ thống mới đưa vào sử dụng. Tuy nhiên, tính năng này đòi hỏi phân công nhân sự trực thường xuyên và mất nhiều công xây dựng phần mềm chat; độc giả vẫn có thể liên hệ nhanh qua số điện thoại hoặc quầy thư viện nên chưa cần thiết đưa vào 3 Sprint đầu.
3. Gợi ý sách theo sở thích (mục 7): Một số người muốn đưa lên Could have để khuyến khích sinh viên đọc sách. Thực tế là ở bản phát hành đầu tiên, hệ thống chưa có dữ liệu mượn sách của người dùng nên thuật toán chưa thể hoạt động hiệu quả. Giữ mục này ở nhóm Won't have để làm sau khi đã có dữ liệu là lựa chọn hợp lý hơn.
