# Tên dự án : Credit Card Fraud Detection Analysis

## 1. Giới thiệu dự án
- Dự án này thực hiện phân tích dữ liệu giao dịch thẻ tín dụng nhằm phát hiện các mẫu gian lận (fraud detection) dựa trên phương pháp phân tích dữ liệu (Data Analysis), thống kê suy diễn (Inferential Statistics).
- Dataset sử dụng là bộ dữ liệu **Credit Card Fraud Detection**, bao gồm hơn 284,000 giao dịch với 31 đặc trưng, trong đó các biến V1–V28 đã được ẩn danh nhằm bảo mật thông tin người dùng.

## 2. Mục tiêu của dự án
- Khám phá đặc điểm của dữ liệu giao dịch thẻ tín dụng.
- Phân tích sự khác biệt giữa giao dịch bình thường và giao dịch gian lận.
- Khai thác các biến V1–V28 để tìm các đặc trưng có khả năng phân biệt gian lận.
- Thực hiện các kỹ thuật thống kê mô tả và thống kê suy diễn.
- Xây dựng dashboard tương tác cho phép người dùng lựa chọn biến và tự động hiển thị các chỉ số thống kê cùng biểu đồ phù hợp.
- Xuất báo cáo nghiên cứu dưới dạng PDF.

## 3. Dataset
- Tên dataset : **Credit Card Fraud Detection** (Nguồn: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud). Bao gồm các thuộc tính như sau : 

| Thuộc tính | Mô tả |
|------------|--------|
| Time | Thời gian giao dịch |
| Amount | Giá trị giao dịch |
| V1–V28 | Các biến đã được ẩn danh bằng PCA |
| Class | Nhãn giao dịch (0: Bình thường, 1: Gian lận) |

## 4. Vai trò của các thành viên

- Nhóm gồm 03 thành viên, làm việc theo mô hình cộng tác trên GitHub và quản lý tiến độ bằng Jira Kanban.

| Thành viên | Vai trò | Nhiệm vụ chính |
|------------|----------|----------------|
| **Lê Hoàng Nhân** | Tech Leader và Statistical Analyst | Quản lý tiến độ dự án trên Jira, quản lý GitHub, phân công công việc, review và hợp nhất mã nguồn. Phụ trách phân tích thống kê suy diễn (ước lượng, khoảng tin cậy, kiểm định giả thuyết), tổng hợp kết quả và hoàn thiện báo cáo cuối cùng. |
| **Nguyễn Quốc Bảo** | Data Analyst | Khảo sát dữ liệu, thực hiện tiền xử lý dữ liệu (kiểm tra dữ liệu thiếu, dữ liệu trùng lặp, ngoại lai), phân tổ dữ liệu và xây dựng các bảng thống kê mô tả, bảng tần số phục vụ phân tích. |
| **Nguyễn Thị Thu Hiền** | Data Visualization và Dashboard Developer | Thực hiện trực quan hóa dữ liệu, xây dựng các biểu đồ EDA, phân tích mối quan hệ giữa các biến và phát triển Dashboard tương tác HTML cho phép người dùng khám phá dữ liệu. |



## 6. Công cụ sử dụng

| Nhóm công cụ            | Công cụ                                      | Mục đích sử dụng                                           |
| ----------------------- | -------------------------------------------- | ---------------------------------------------------------- |
| Ngôn ngữ lập trình      | Python 3.10                                  | Phát triển toàn bộ hệ thống phân tích dữ liệu và dashboard |
| Xử lý dữ liệu           | Pandas                                       | Đọc, làm sạch, biến đổi và phân tích dữ liệu               |
| Tính toán số học        | NumPy                                        | Hỗ trợ tính toán ma trận và các phép toán số học           |
| Thống kê                | SciPy                                        | Thực hiện ước lượng và kiểm định thống kê                  |
| Trực quan hóa           | Matplotlib                                   | Vẽ các biểu đồ thống kê cơ bản                             |
| Trực quan hóa tương tác | Plotly                                       | Xây dựng biểu đồ tương tác cho Dashboard                   |
| Dashboard               | Panel                                        | Xây dựng Dashboard HTML tương tác                          |
| Báo cáo                 | Quarto (QMD)                                 | Viết báo cáo, tích hợp mã nguồn và kết quả phân tích       |
| Đầu ra báo cáo          | PDF                                          | Nộp báo cáo cuối cùng                                      |
| Quản lý mã nguồn        | GitHub                                       | Lưu trữ mã nguồn và làm việc nhóm                          |
| Quản lý dự án           | Jira Kanban                                  | Theo dõi tiến độ và phân công công việc                    |

## 7. Cấu trúc thư mục 
```text
credit-card-fraud-analysis/
│
├── data/
│   ├── raw/                  # Dữ liệu gốc (không commit - xem .gitignore)
│   └── processed/            # Dữ liệu đã tiền xử lý
│
├── notebooks/
│   ├── 01_preprocessing.qmd  # Chương 2: Tiền xử lý
│   ├── 02_eda.qmd            # Chương 3-4: Thống kê & Trực quan hóa
│   └── 03_inference.qmd      # Chương 5: Thống kê suy diễn
│
├── report/
│   └── final_report.qmd      # Báo cáo tổng hợp hoàn chỉnh
│
├── figures/                  # Biểu đồ xuất ra
├── .gitignore
├── requirements.txt          # Các thư viện Python cần thiết
└── README.md
```
## 8. Hướng dẫn chạy dự án

1. Clone repository
```bash
git clone https://github.com/<your-username>/credit-card-fraud-analysis.git
cd credit-card-fraud-analysis
```
2. Cài đặt thư viện
```bash
pip install -r requirements.txt
```
3. Tải dữ liệu

Tải file creditcard.csv từ Kaggle và đặt vào:

data/raw/creditcard.csv

4. Render báo cáo
```bash
quarto render report/final_report.qmd
```

## 9. Quy trình làm việc với Git

##### Tạo nhánh mới cho từng chương
git checkout -b feature/chuong-2-preprocessing

##### Commit thường xuyên với message rõ ràng
git commit -m "feat: xử lý missing values và outliers trong Amount"

##### Push và tạo Pull Request để thành viên khác review
git push origin feature/chuong-2-preprocessing

**Quy ước đặt tên nhánh:**

feature/chuong-X-ten-nhanh — Nhánh phát triển chương mới
fix/ten-loi — Nhánh sửa lỗi
docs/ten-tai-lieu — Nhánh cập nhật tài liệu

## 10. Sản phẩm đầu ra
- File mã nguồn Quarto (report.qmd)
- File PDF tiểu luận hoàn chỉnh (report.pdf)
- Dashboard tương tác HTML (dashboard.html)
