# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600232
**Name:** Nguyễn Tuấn Kiệt
**Date:** 15/04/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200. | 10 | |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999. | 1 | |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Dữ liệu lỗi chứa nhiều vấn đề nghiêm trọng:
- **Duplicate IDs**: ID `1` xuất hiện hai lần, gây nhầm lẫn khi xử lý.
- **Sai kiểu dữ liệu**: Giá của `Broken Chair` là "ten dollars" thay vì số, khiến việc tính toán thất bại.
- **Outliers**: Giá của `Nuclear Reactor` là $999,999, vượt xa giá trị hợp lý, làm sai lệch kết quả.
- **Null values**: `Ghost Item` thiếu giá trị ở cả `id`, `price`, và `category`, dẫn đến lỗi khi lọc dữ liệu.

Những vấn đề này làm giảm độ chính xác của Agent vì nó dựa vào dữ liệu đầu vào để đưa ra quyết định. Khi dữ liệu không đáng tin cậy, kết quả cũng sẽ không chính xác.

---

## 3. Ket luan

**Quality Data > Quality Prompt?**

Đồng ý. Dữ liệu chất lượng cao là nền tảng để đảm bảo kết quả chính xác. Một prompt tốt không thể bù đắp cho dữ liệu đầu vào kém chất lượng. Do đó, cần ưu tiên làm sạch và chuẩn hóa dữ liệu trước khi sử dụng.
