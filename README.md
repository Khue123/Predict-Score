
# Fundamental Score Analysis and Decision Tree Modeling

## Giới thiệu
Dự án này thực hiện:
- Xử lý và làm sạch dữ liệu cơ bản về doanh nghiệp Việt Nam.
- Phân tích thống kê các giá trị lớn nhất và nhỏ nhất của một số chỉ tiêu tài chính.
- Xây dựng mô hình **Decision Tree Regressor** để dự đoán điểm số (Score) của doanh nghiệp dựa trên các đặc điểm tài chính.

## Nội dung chính
- **Đọc dữ liệu** từ file CSV `Filtered_Fundamental_score_VNstock.csv`.
- **Lọc dữ liệu**: Loại bỏ các dòng có giá trị âm ở các cột tài chính quan trọng.
- **Phân tích thống kê**:
  - Tính toán giá trị lớn nhất và nhỏ nhất cho từng chỉ tiêu tài chính.
  - Lưu kết quả ra file CSV.
- **Phân tích theo ngành**:
  - Lọc dữ liệu cho các ngành: Retail, Service, Tourism and entertainment, Petroleum, Mining, Utility.
  - Tính max và min theo từng ngành và thời gian.
- **Xây dựng mô hình**:
  - Chia tập dữ liệu thành tập huấn luyện và tập kiểm tra.
  - Huấn luyện **Decision Tree Regressor** với giới hạn số nút lá tối đa là 5.
  - Đánh giá mô hình bằng các chỉ số: MSE, MAE, R², MAPE.
- **Lưu và trực quan hóa kết quả**:
  - Lưu kết quả dự đoán vào file CSV.
  - Trực quan hóa cây quyết định bằng đồ thị.

## Yêu cầu
- Python 3.x
- Các thư viện:
  - `pandas`
  - `scikit-learn`
  - `pydotplus`
  - `IPython`

Cài đặt nhanh các thư viện cần thiết:
```bash
pip install pandas scikit-learn pydotplus IPython
```

## Cách sử dụng
1. Đặt file dữ liệu `Filtered_Fundamental_score_VNstock.csv` đúng đường dẫn yêu cầu (`/content/Filtered_Fundamental_score_VNstock.csv` nếu chạy trên Colab hoặc chỉnh sửa nếu chạy local).
2. Chạy file Python để:
   - Làm sạch dữ liệu
   - Phân tích
   - Xây dựng mô hình
   - Xuất ra các file CSV kết quả
   - Hiển thị cây quyết định.

## Tệp CSV được tạo ra
- `Filtered_Fundamental_score_VNstock.csv`
- `Max_Min_Values_Fundamental_score_VNstock.csv`
- `Grouped_Max_Min_Sectors.csv`
- `Decision_Tree_Predictions.csv`

## Ghi chú
- File được viết ban đầu trên Google Colab.
- Để vẽ được biểu đồ cây, cần chắc chắn môi trường có thể hiển thị hình ảnh từ `pydotplus`.
- Nếu chạy local, cần cài thêm Graphviz.
