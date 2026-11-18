# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 01
- **Họ tên: Nguyễn Minh**
- **Lớp: CNTT4**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt tour ra JSON

**KET QUA AI**

```text

[
  {
    "ma_tour": "SP2N",
    "ngay_khoi_hanh": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_phong": "doi",
    "ghi_chu": null
  },
  {
    "ma_tour": "PQ4N",
    "ngay_khoi_hanh": "2027-01-05",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_phong": null,
    "ghi_chu": "1 người ăn chay"
  },
  {
    "ma_tour": "DL3N",
    "ngay_khoi_hanh": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_phong": "doi",
    "ghi_chu": "Ông nội đi xe lăn"
  }
]

```

**Link trò chuyện: https://chatgpt.com/share/6afd03ff-2a80-83ec-a809-83ef5510eb70**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
BẢNG TÍNH GIÁ TOUR DL3N – ĐÀ LẠT
Bước 1: Tính tiền người lớn

5 × 3.200.000 = 16.000.000 đồng

Bước 2: Tính tiền trẻ em
- 2 trẻ (8 và 10 tuổi): 2 × 3.200.000 × 70% = 4.480.000 đồng
- 1 bé (3 tuổi): 0 đồng (miễn phí)
Tổng tiền trẻ em = 4.480.000 + 0 = 4.480.000 đồng

Bước 3: Tính tiền tour

16.000.000 + 4.480.000 = 20.480.000 đồng

Bước 4: Tính giảm giá đoàn

Đoàn có 5 người lớn nên được giảm 5%.
- Tiền giảm: 20.480.000 × 5% = 1.024.000 đồng
- Tiền tour sau giảm: 20.480.000 − 1.024.000 = 19.456.000 đồng
Bước 5: Tính phụ thu

1 người ở phòng đơn:

1 × 800.000 = 800.000 đồng

Bước 6: Tính tổng tiền

19.456.000 + 800.000 = 20.256.000 đồng

TỔNG TIỀN THANH TOÁN
20.256.000 đồng

[RESULT: 20.256.000 đồng]
```

**Link trò chuyện: https://chatgpt.com/share/6afd03ea-e8d8-83ec-95a2-c8ba09380180**

### b) Kiểm tra kết quả AI

AI trả lời đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text

{
  "loai_su_co": "Khách sạn không đúng tiêu chuẩn cam kết, phòng ẩm mốc",
  "so_khach": 2,
  "so_dem_bi_anh_huong": 2,
  "tom_tat": "Khách sạn 3 sao thay vì 4 sao, phòng ẩm mốc trong 2 đêm đầu."
}

```

**Link trò chuyện: https://chatgpt.com/share/6afd03cf-0a28-83ec-89e2-6913726f1528**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
KẾT QUẢ CHẤM ĐIỂM NHÂN VIÊN
2,5/10
Chưa đạt

Đánh giá theo RUBRIC của công ty

Tiêu chí	Điểm tối đa	Điểm đạt	Nhận xét
Đúng thông tin (50%)	5	0	Sai giá tour (2.200.000đ thay vì 2.400.000đ) và sai chính sách huỷ (hoàn 100% thay vì 50%).
Đầy đủ (30%)	3	1,5	Đã trả lời cả hai câu hỏi nhưng thông tin sai. Chưa mời khách cung cấp ngày đi và số lượng khách.
Giọng điệu (20%)	2	1	Có lời chào lịch sự nhưng dùng từ chưa chuyên nghiệp như “đi rất vui luôn”, “nha anh”.
Tổng cộng	10	2,5	Chưa đạt yêu cầu

Nhận xét chung
Nhân viên có thái độ thân thiện nhưng mắc hai lỗi nghiêm trọng về giá tour và chính sách hoàn tiền. Cần kiểm tra kỹ thông tin trước khi tư vấn khách hàng và chủ động hỏi ngày khởi hành, số lượng khách để hỗ trợ đặt tour.
Câu trả lời đề xuất
Dạ, em chào anh ạ! Tour Sa Pa 2 ngày 1 đêm có giá 2.400.000 đồng/người lớn. Nếu anh huỷ tour trước ngày khởi hành 3 ngày, công ty sẽ hoàn lại 50% tiền tour theo chính sách. Anh vui lòng cho em xin ngày dự kiến khởi hành và số lượng khách để em hỗ trợ đặt tour ạ!
```

**Link trò chuyện: https://chatgpt.com/share/6afd03bb-bb3c-83ec-a5be-c49d9abc4821**
