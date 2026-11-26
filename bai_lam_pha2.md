# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 09
- **Họ tên:*Lê Gia Bảo*
- **Lớp:*HCM-KS26-CNTT2*
- **Link repository Pha2:*https://github.com/lgbtrick/HCM-KS26-CNTT2_PromptAI_H02/blob/main/bai_lam_pha2.md*
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):*Gemini*

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt chỗ workshop ra JSON

**KET QUA AI**

```text
[
{
"ma_lop": "NANTAY",
"ngay_hoc": "2026-12-13",
"nguoi_lon": 2,
"tre_em": 1,
"ca_hoc": "chieu",
"ghi_chu": null
},
{
"ma_lop": "BANXOAY",
"ngay_hoc": "2027-01-10",
"nguoi_lon": 3,
"tre_em": 0,
"ca_hoc": null,
"ghi_chu": "1 người bị đau cổ tay"
},
{
"ma_lop": "VEGOM",
"ngay_hoc": null,
"nguoi_lon": 4,
"tre_em": 0,
"ca_hoc": "sang",
"ghi_chu": "1 bạn đi xe lăn"
}
]
```

**Link trò chuyện:*https://share.gemini.google/KdtR4RK6ECIP*

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
Dưới đây là bảng tính chi tiết báo giá cho nhóm của bạn tại Đất Việt Workshop cho lớp **BANXOAY** (Đơn giá người lớn: 550.000 đồng):

**Bước 1: Tiền người lớn.**

* Nhóm có 5 người lớn.
* Phép tính: $5 \times 550.000 = 2.750.000\text{ đồng}$

**Bước 2: Tiền trẻ em (xem xét trẻ theo độ tuổi).**

* Trẻ 8 tuổi và trẻ 12 tuổi nằm trong độ tuổi từ 6 đến 12 tuổi, tính 70% giá người lớn: $550.000 \times 70\% = 385.000\text{ đồng/trẻ}$.
* Bé 4 tuổi (dưới 6 tuổi đi kèm, không làm sản phẩm): miễn phí ($0\text{ đồng}$).
* Phép tính tổng tiền trẻ em: $(2 \times 385.000) + 0 = 770.000\text{ đồng}$

**Bước 3: Tiền học = tiền người lớn + tiền trẻ em.**

* Phép tính: $2.750.000 + 770.000 = 3.520.000\text{ đồng}$

**Bước 4: Giảm giá nhóm (Kiểm tra điều kiện tính số tiền giảm và tiền học sau giảm).**

* Kiểm tra điều kiện: Nhóm có 5 người lớn (đạt điều kiện từ 5 người lớn trở lên) nên được giảm 5% trên tiền học.
* Phép tính số tiền được giảm: $3.520.000 \times 5\% = 176.000\text{ đồng}$
* Phép tính tiền học sau giảm: $3.520.000 - 176.000 = 3.344.000\text{ đồng}$

**Bước 5: Phí nung và giao.**

* Nhóm cần nung và giao 4 sản phẩm với đơn giá 80.000 đồng/sản phẩm (không áp dụng giảm giá).
* Phép tính: $4 \times 80.000 = 320.000\text{ đồng}$

**Bước 6: Tổng tiền = tiền học sau giảm + phí nung và giao.**

* Phép tính: $3.344.000 + 320.000 = 3.664.000\text{ đồng}$

**Tổng cộng chi phí cho yêu cầu của nhóm bạn là: 3.664.000 đồng.**
```

**Link trò chuyện:*https://share.gemini.google/xIBOSGlNZYoZ*

### b) Kiểm tra kết quả AI

Đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
"loai_su_co": "khac",
"so_khach": 0,
"so_san_pham_bi_hong": null,
"tom_tat": "Không có nội dung email khiếu nại được cung cấp để phân tích."
}
```

**Link trò chuyện:*https://share.gemini.google/NllHCyQ36gfY*

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 0 / 5.0 | - **Câu lỗi 1:** *"Lớp vẽ gốm bên em 200k thôi nè, vui lắm luôn."*<br>

<br>- **Lý do sai:** Báo sai giá chuẩn của lớp VEGOM (250.000 đồng/người lớn).<br>

<br>- **Câu lỗi 2:** *"Chị đổi trước 1 ngày thì free nha chị."*<br>

<br>- **Lý do sai:** Báo sai chính sách đổi lịch. Đổi trước 1 ngày (24 giờ) thuộc khung từ 12 đến dưới 48 giờ, mất phí 30.000 đồng/người chứ không được miễn phí. | - **Sửa lỗi 1:** *"Lớp vẽ gốm (VEGOM) bên em có giá 250.000 đồng/người lớn ạ."*<br>

<br>- **Sửa lỗi 2:** *"Nếu chị đổi lịch trước giờ học 1 ngày (24 giờ), phí đổi lịch là 30.000 đồng/người ạ (miễn phí khi đổi trước từ 48 giờ trở lên)."* |
| **Đầy đủ (30%)** | 2.0 / 3.0 | - **Câu lỗi:** *"Có gì chị nhắn em nha!"*<br>

<br>- **Lý do sai:** Bài làm đã trả lời được 2 câu hỏi của khách (dù sai thông tin) nhưng thiếu lời mời khách cung cấp thông tin ngày học, ca học và số lượng người tham gia để hỗ trợ đặt chỗ. | - **Sửa lỗi:** *"Nếu chị muốn đăng ký, chị cho em xin thông tin về ngày học, ca học và số lượng người tham gia để bên em hỗ trợ giữ chỗ cho mình nhé!"* |
| **Giọng điệu (20%)** | 0.5 / 2.0 | - **Câu lỗi 1:** *"Hi chị ơi! Lớp vẽ gốm bên em 200k thôi nè, vui lắm luôn."*<br>

<br>- **Lý do sai:** Dùng từ ngữ suồng sã, thiếu chuyên nghiệp (*"Hi"*, *"thôi nè"*, *"vui lắm luôn"*).<br>

<br>- **Câu lỗi 2:** *"Chị đổi trước 1 ngày thì free nha chị."*<br>

<br>- **Lý do sai:** Dùng tiếng lóng/tiếng Anh pha trộn và trợ từ khẩu ngữ thiếu trang trọng (*"free nha chị"*). | - **Sửa lỗi 1:** *"Chào chị ạ! Lớp vẽ gốm bên em có mức phí là 250.000 đồng/người lớn ạ."*<br>

<br>- **Sửa lỗi 2:** *"Trường hợp chị đổi lịch trước giờ học 1 ngày thì phí đổi là 30.000 đồng/người ạ."* |
| **Tổng điểm** | **2.5 / 10** |  |  |
```

**Link trò chuyện:*https://share.gemini.google/ksIwnsO1Zd52*
