# Tên dự án : Credit Card Fraud Detection Analysis

## 1. Giới thiệu dự án
- Dự án này thực hiện phân tích dữ liệu giao dịch thẻ tín dụng nhằm phát hiện các mẫu gian lận (fraud detection) dựa trên phương pháp phân tích dữ liệu (Data Analysis), thống kê suy diễn (Inferential Statistics) và trực quan hóa dữ liệu (Data Visualization).
- Dataset sử dụng là bộ dữ liệu **Credit Card Fraud Detection**, bao gồm hơn 284,000 giao dịch với 31 đặc trưng, trong đó các biến V1–V28 đã được ẩn danh nhằm bảo mật thông tin người dùng.

## 2. Mục tiêu của dự án
- Khám phá đặc điểm của dữ liệu giao dịch thẻ tín dụng.
- Phân tích sự khác biệt giữa giao dịch bình thường và giao dịch gian lận.
- Khai thác các biến V1–V28 để tìm các đặc trưng có khả năng phân biệt gian lận.
- Thực hiện các kỹ thuật thống kê mô tả và thống kê suy diễn.
- Xây dựng dashboard tương tác cho phép người dùng lựa chọn biến và tự động hiển thị các chỉ số thống kê cùng biểu đồ phù hợp.
- Xuất báo cáo nghiên cứu dưới dạng PDF.

## 3. Dataset
- Tên dataset : **Credit Card Fraud Detection** (Nguồn: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Thông tin dữ liệu :
| Thuộc tính | Mô tả |
|------------|--------|
| Time | Thời gian giao dịch |
| Amount | Giá trị giao dịch |
| V1–V28 | Các biến đã được ẩn danh bằng PCA |
| Class | Nhãn giao dịch (0: Bình thường, 1: Gian lận) |

## 4. Pipeline dự án
- Dự án được triển khai theo pipeline phân tích dữ liệu chuẩn :
>  Tiền xử lý dữ liệu (Preprocessing data) -> Phân tích khám phá dữ liệu (EDA) -> Thống kê suy diễn (Statistical Analysis) -> Dashboard tương tác 

### 1. Tiền xử lý dữ liệu

- Kiểm tra dữ liệu thiếu.
- Kiểm tra dữ liệu trùng lặp.
- Phát hiện và xử lý ngoại lai.
- Chuẩn hóa dữ liệu khi cần thiết.
- Phân tổ dữ liệu (Binning).

### 2. Phân tích khám phá dữ liệu (EDA)

- Thống kê mô tả.
- Phân tích phân phối dữ liệu.
- Lập bảng tần số.
- Phân tích tương quan.
- So sánh giao dịch gian lận và bình thường.
- Khai thác các biến V1–V28.

### 3. Thống kê suy diễn (Statistical Analysis)

- Ước lượng trung bình.
- Ước lượng tỷ lệ giao dịch gian lận.
- Khoảng tin cậy.
- Kiểm định t-test.
- Kiểm định Chi-square (nếu phù hợp).

### 4. Dashboard tương tác

Dashboard được xây dựng bằng Python và xuất ra định dạng HTML.
Các chức năng chính:

#### Phân tích một biến
- Chọn một biến bất kỳ trong dataset.
- Nếu biến là định lượng:
  - Mean
  - Median
  - Mode
  - Variance
  - Standard Deviation
  - Min
  - Max
  - Quartiles
  - Histogram
  - Boxplot
- Nếu biến là định tính:
  - Bảng tần số
  - Bảng tỷ lệ
  - Bar Chart
  - Pie Chart
  - 
#### Phân tích hai biến
- Numeric × Numeric → Scatter Plot
- Numeric × Categorical → Boxplot
- Categorical × Categorical → Crosstab và Bar Chart
  
## 5. 


## 6. Cấu trúc thư mục 
```text
project/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── dashboard/
│   └── dashboard.py
│
├── reports/
│   ├── report.qmd
│   └── report.pdf
│
├── images/
│
├── requirements.txt
│
└── README.md
