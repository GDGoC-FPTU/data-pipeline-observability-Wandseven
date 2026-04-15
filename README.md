[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23573978&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** junsikkun@gmail.com
**Name:** Nguyễn Tuấn Kiệt

---

## Mo ta

Bài lab này yêu cầu xây dựng một ETL pipeline để xử lý dữ liệu từ file JSON, bao gồm các bước: Extract, Validate, Transform, và Load. Ngoài ra, thực hiện thí nghiệm kiểm tra tác động của dữ liệu chất lượng thấp (Garbage Data) đến kết quả của một AI Agent.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Thí nghiệm với dữ liệu sạch
python agent_simulation.py

# Thí nghiệm với dữ liệu lỗi
# Đảm bảo file garbage_data.csv có trong thư mục
python agent_simulation.py
```
### Cau truc thu muc
```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```
---

## Ket qua

- **ETL Pipeline**: 3 records được xử lý thành công, 2 records bị loại bỏ do lỗi dữ liệu.
- **Agent Simulation**:
  - Với dữ liệu sạch: Agent chọn Laptop với giá $1200.
  - Với dữ liệu lỗi: Agent chọn Nuclear Reactor với giá $999,999, cho thấy tác động tiêu cực của dữ liệu không hợp lệ.
