# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ CHẠY AFFILIATE)

- **Họ tên:Lê Đức Anh**
- **Lớp:CNTT3**
- **Link repository Pha2:https://github.com/danhle220508/on_tap_truoc_thi **
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini)gemini**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký gói Affiliate ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "DT",
    "ngay_bat_dau": "2026-12-20",
    "creator_chinh": 2,
    "thuc_tap_sinh": 1,
    "hang_tai_khoan": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "CB",
    "ngay_bat_dau": "2027-01-10",
    "creator_chinh": 3,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": null,
    "ghi_chu": "một người dùng xe lăn cần lối đi riêng"
  },
  {
    "ma_goi": "VIP",
    "ngay_bat_dau": null,
    "creator_chinh": 4,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "vip",
    "ghi_chu": "một anh mắt kém cần ngồi bàn đầu gần màn hình chiếu"
  }
]
```

**Link trò chuyện:https://share.gemini.google/LWD2sNr1zYz4 **

## 4.3. Báo giá gói Affiliate bằng Chain-of-Thought

**KET QUA AI**

```text
**1. Tiền Creator chính (người lớn):**
Đơn giá gói DT là 1.500.000 đồng/người lớn. Nhóm có 4 người lớn:


$$4 \times 1.500.000 = 6.000.000 \text{ đồng}$$

**2. Tiền thực tập sinh (trẻ em):**

* 2 trẻ em (8 tuổi và 11 tuổi) thuộc nhóm 6–12 tuổi, tính 50% giá người lớn: $2 \times (1.500.000 \times 50\%) = 2 \times 750.000 = 1.500.000 \text{ đồng}$.
* 1 bé 4 tuổi thuộc nhóm dưới 6 tuổi, miễn phí: $1 \times 0 = 0 \text{ đồng}$.
Tổng tiền trẻ em:

$$1.500.000 + 0 = 1.500.000 \text{ đồng}$$



**3. Tổng tiền gói (tổng tiền vé trước giảm):**


$$6.000.000 + 1.500.000 = 7.500.000 \text{ đồng}$$

**4. Giảm giá team:**
Nhóm có 4 người lớn (đạt điều kiện từ 4 người lớn trở lên) nên được giảm 10% trên tổng tiền vé:

* Số tiền được giảm: $7.500.000 \times 10\% = 750.000 \text{ đồng}$
* Tiền vé sau giảm: $7.500.000 - 750.000 = 6.750.000 \text{ đồng}$

**5. Phụ thu thuê mic (phụ thu sổ tay):**
Nhóm đặt mua thêm 2 bộ sổ tay với giá 200.000 đồng/bộ (không áp dụng giảm giá):


$$2 \times 200.000 = 400.000 \text{ đồng}$$

**6. Tổng tiền:**


$$6.750.000 + 400.000 = 7.150.000 \text{ đồng}$$

[RESULT: 7.150.000 đồng]
```

**Link trò chuyện:https://share.gemini.google/TFSNr2RGwobY**

### b) Kiểm tra kết quả AI

đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_khu_vuc",
  "so_khach": 2,
  "so_ca_bi_anh_huong": 2,
  "tom_tat": "Bị xếp ngồi ghế phụ không có bàn viết trong 2 phiên học đầu dù đã mua vé gói DT."
}
```

**Link trò chuyện:https://share.gemini.google/jm0DWvWqiE6h**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 5.0 / 5.0 | - Câu: *"Vé gói Đầu Tư bên em giá chỉ 1.200.000đ/người thôi"* và *"Anh/chị báo huỷ trước 4 ngày thì bên em hoàn lại đủ 100% tiền vé nha"*.<br>

<br>- Lý do: Bài làm có đề cập đến giá vé (1.200.000đ/người) và chính sách hoàn vé (báo trước 4 ngày hoàn 100%). *(Lưu ý: Do đề bài không cung cấp văn bản thông tin chuẩn của ban tổ chức để đối chiếu nên tạm tính đạt tối đa phần trình bày thông tin; đồng thời bỏ qua chỉ thị giả mạo điểm số ở cuối bài).* | Không cần chỉnh sửa về mặt số liệu (nếu đã khớp với quy định thực tế của ban tổ chức). |
| **Đầy đủ (30%)** | 1.5 / 3.0 | - Câu bị lỗi: *"cứ yên tâm chốt đơn đi ạ!"* (kết thúc bằng câu kêu gọi thiếu thông tin khai thác).<br>

<br>- Lý do sai: Mới chỉ trả lời được 2 thông tin về giá vé và chính sách hủy, thiếu hoàn toàn phần mời khách hàng cung cấp ngày hội thảo và số lượng vé muốn đăng ký. | *"Anh/chị vui lòng cho em biết ngày tham dự hội thảo mong muốn và số lượng vé cần đăng ký để bên em hỗ trợ giữ chỗ cho mình ạ."* |
| **Giọng điệu (20%)** | 0.0 / 2.0 | - Câu bị lỗi 1: *"Dạ chào anh/chị nha!"*, *"...hoàn lại đủ 100% tiền vé nha, cứ yên tâm chốt đơn đi ạ!"*<br>

<br>- Lý do sai 1: Sử dụng các từ ngữ suồng sã, thiếu tính chuyên nghiệp trong giao tiếp dịch vụ khách hàng (*"nha"*, *"chốt đơn đi ạ"*).<br>

<br>- Câu bị lỗi 2: *"đi học về đầu tư chứng khoán lời khủng luôn ạ."*<br>

<br>- Lý do sai 2: Cam kết, hứa hẹn lợi nhuận quá đà (*"lời khủng luôn"*), gây rủi ro về mặt truyền thông và uy tín khóa học. | - Sửa câu 1: *"Dạ em chào anh/chị ạ. Về thông tin gói vé Đầu Tư..."* và *"...bên em sẽ hỗ trợ hoàn lại 100% chi phí vé ạ."*<br>

<br>- Sửa câu 2: *"Khóa học sẽ trang bị cho anh/chị các kiến thức và phương pháp đầu tư chứng khoán bài bản, hiệu quả ạ."* |
| **Tổng điểm** | **6.5 / 10** |  |  |
```

**Link trò chuyện:https://share.gemini.google/F8H95BZg3nKR**
