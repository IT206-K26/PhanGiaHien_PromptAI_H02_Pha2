# BÀI LÀM PHA 2 

- **Họ tên: Phan Gia Hiển**
- **Lớp: K26-CNTT1**
- **Link repository Pha2: https://github.com/IT206-K26/PhanGiaHien_PromptAI_H02_Pha2**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini): Gemini**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé ra JSON

**KET QUA AI**

```text
[
{
"ma_goi": "SVT",
"ngay_su_kien": "2026-12-20",
"nguoi_lon": 2,
"tre_em": 1,
"loai_ve": "thuong",
"ghi_chu": null
},
{
"ma_goi": "FZ",
"ngay_su_kien": "2027-01-05",
"nguoi_lon": 3,
"tre_em": 0,
"loai_ve": "thuong",
"ghi_chu": "hỗ trợ xe lăn"
},
{
"ma_goi": "VIP",
"ngay_su_kien": null,
"nguoi_lon": 4,
"tre_em": 0,
"loai_ve": "vip",
"ghi_chu": "một người khiếm thị cần hỗ trợ tìm chỗ"
}
]
```

**Link trò chuyện: https://share.gemini.google/J3BgFimpCshD**

## 4.3. Báo giá vé bằng Chain-of-Thought

**KET QUA AI**

```text
Tiền người lớn:
Gói SVT có giá 1.200.000 đồng/người lớn.$5 \times 1.200.000 = 6.000.000$ đồng.Tiền trẻ em:2 trẻ em (8 tuổi và 10 tuổi, thuộc nhóm 5–11 tuổi, tính 70% giá người lớn): $2 \times (1.200.000 \times 70\%) = 2 \times 840.000 = 1.680.000$ đồng.1 bé 3 tuổi (dưới 5 tuổi, miễn phí): $0$ đồng.Tổng tiền trẻ em: $1.680.000 + 0 = 1.680.000$ đồng.Tiền vé:$6.000.000 + 1.680.000 = 7.680.000$ đồng.Giảm giá nhóm:
Nhóm có 5 người lớn (đạt mức từ 5 người lớn trở lên) nên được giảm 5% trên tiền vé:$7.680.000 \times 5\% = 384.000$ đồng.
Tiền vé sau giảm: $7.680.000 - 384.000 = 7.296.000$ đồng.Phụ thu:
1 người lớn chọn khu ghế ưu tiên (không được giảm giá):$1 \times 300.000 = 300.000$ đồng.Tổng tiền:$7.296.000 + 300.000 = 7.596.000$ đồng.[RESULT: 7.596.000 đồng]
```

**Link trò chuyện: https://share.gemini.google/J3BgFimpCshD**

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{"loai_su_co": "sai_khu_vuc", "so_khach": 2, "so_hiep_bi_anh_huong": 2, "tom_tat": "Khán giả bị xếp sang khu không mái che trong 2 hiệp đầu."}

tiền là 2.000.000 đồng (tương ứng 500.000 đồng/khách cho mỗi hiệp bị ảnh hưởng, áp dụng cho 2 khách trong 2 hiệp đầu).

Để chúng tôi có thể tiến hành hoàn tiền trong thời gian sớm nhất, Quý khán giả vui lòng phản hồi lại email này kèm theo thông tin tài khoản ngân hàng nhận tiền (số tài khoản, tên chủ tài khoản và tên ngân hàng).

Một lần nữa, chúng tôi thành thật xin lỗi vì trải nghiệm chưa trọn vẹn vừa qua và rất cảm ơn Quý khán giả đã ghi nhận sự nhiệt tình của đội ngũ nhân viên soát vé. Rất mong tiếp tục nhận được sự đồng hành của Quý khán giả trong các trận đấu sắp tới với chất lượng phục vụ tốt nhất.

Trân trọng,

Ban tổ chức Cúp Sao Vàng
```

**Link trò chuyện: https://share.gemini.google/J3BgFimpCshD**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 0/5 | - Trích dẫn: *"Vé Sân Vận Động bên em giá 1.000.000đ/người, xem rất đã luôn ạ."*<br>

<br>Lý do sai: Báo sai giá vé (giá chuẩn là 1.200.000 đồng/người lớn).<br>

<br>- Trích dẫn: *"Anh huỷ trước 3 ngày thì được hoàn tiền đầy đủ nha anh."*<br>

<br>Lý do sai: Báo sai chính sách huỷ (huỷ từ 3 đến 6 ngày chỉ hoàn 50%, hoàn 100% chỉ áp dụng khi huỷ trước sự kiện từ 7 ngày trở lên, dưới 3 ngày không hoàn tiền). | "Giá vé gói Sân Vận Động (SVT) là 1.200.000 đồng/người lớn. Về chính sách huỷ vé: huỷ trước sự kiện từ 7 ngày trở lên được hoàn 100%, từ 3 đến 6 ngày hoàn 50%, và dưới 3 ngày không hoàn tiền." |
| **Đầy đủ (30%)** | 1.5/3 | Có đề cập đến cả hai câu hỏi về giá và chính sách huỷ, nhưng chưa nêu đủ các mốc hoàn tiền và thiếu lời mời cung cấp thông tin đặt vé.<br>

<br>- Trích dẫn: *"Anh cần gì cứ nhắn em nhé!"*<br>

<br>Lý do sai: Câu kết chung chung, không mời khán giả cung cấp ngày trận đấu và số lượng vé để đặt. | "Nếu anh có nhu cầu đặt vé, anh vui lòng cung cấp ngày diễn ra trận đấu và số lượng vé để em hỗ trợ giữ chỗ ngay ạ." |
| **Giọng điệu (20%)** | 1/2 | Có lời chào lịch sự nhưng còn sử dụng từ ngữ suồng sã, thiếu tính chuyên nghiệp.<br>

<br>- Trích dẫn: *"xem rất đã luôn ạ"* và *"nha anh"*<br>

<br>Lý do sai: Dùng từ ngữ quá thân mật, không phù hợp với môi trường tư vấn khách hàng chuyên nghiệp. | Lược bỏ cụm *"xem rất đã luôn ạ"* và thay *"nha anh"* bằng *"ạ"* để giữ sự trang trọng, lịch sự. |

Tổng điểm: 2.5/10.
```

**Link trò chuyện: https://share.gemini.google/J3BgFimpCshD**
