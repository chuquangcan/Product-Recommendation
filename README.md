# Dự đoán sản phẩm khách hàng sẽ mua bằng Học máy

## 1. Giới thiệu
Dự án này áp dụng các mô hình học máy để dự đoán sản phẩm mà khách hàng có khả năng mua tiếp theo dựa trên dữ liệu giao dịch và hành vi tài chính của họ. Điều này giúp ngân hàng tối ưu hóa hệ thống gợi ý sản phẩm, cải thiện trải nghiệm khách hàng và tăng hiệu suất kinh doanh.

## 2. Hướng dẫn chạy
### Yêu cầu môi trường
Trước khi chạy dự án, hãy đảm bảo cài đặt đầy đủ các thư viện cần thiết bằng cách sử dụng tệp `requirements.txt`:
```bash
pip install -r requirements.txt
```

### Các bước thực hiện
1. **Tiền xử lý dữ liệu:**
   - Chạy tệp `Clean.ipynb` để làm sạch và chuẩn bị dữ liệu.
2. **Khám phá dữ liệu:**
   - Chạy `Visualize.ipynb` để phân tích và trực quan hóa dữ liệu.
3. **Huấn luyện mô hình:**
   - Chạy `Model_KNN.ipynb` để huấn luyện mô hình KNN.
   - Chạy `Ensemble_model.ipynb` để huấn luyện mô hình tổng hợp.

## 3. Bài toán đặt ra
Ngân hàng cung cấp các sản phẩm tài chính như thẻ tín dụng, tài khoản tiết kiệm, vay thế chấp, v.v. Tuy nhiên, hệ thống đề xuất sản phẩm hiện tại chưa hiệu quả, dẫn đến mất cân đối trong việc tiếp cận khách hàng. Một số khách hàng nhận được quá nhiều gợi ý, trong khi nhiều người khác lại bị bỏ sót.

### Mục tiêu
- Xây dựng mô hình dự đoán chính xác nhu cầu sản phẩm của từng khách hàng.
- Cải thiện trải nghiệm cá nhân hóa, tăng mức độ hài lòng và trung thành của khách hàng.
- Hỗ trợ chiến lược bán chéo (cross-selling) và bán thêm (up-selling), tối ưu hóa doanh thu.

## 4. Yêu cầu thực hiện
### 1. Khám phá & Làm sạch dữ liệu
- Phân tích dữ liệu về khách hàng, sản phẩm, thời gian giao dịch.
- Xử lý giá trị thiếu, dữ liệu ngoại lệ và không nhất quán.

### 2. Xây dựng đặc trưng (Feature Engineering)
- Tạo ra các biến đặc trưng có ý nghĩa phục vụ mô hình.
- Lựa chọn các đặc trưng quan trọng nhất giúp tăng độ chính xác của dự đoán.

### 3. Huấn luyện mô hình
- Áp dụng nhiều kỹ thuật học máy như hồi quy, lọc cộng tác (collaborative filtering), học sâu (deep learning) và mô hình tổng hợp (ensemble model).
- Đánh giá hiệu suất mô hình bằng chỉ số Mean Average Precision (MAP).

### 4. Dự đoán sản phẩm
- Đối với mỗi khách hàng tại thời điểm dự đoán, xác định danh sách sản phẩm phù hợp để gợi ý.

### 5. Tối ưu hóa mã nguồn
- Cải thiện tốc độ và hiệu suất xử lý dữ liệu lớn.
- Tối ưu hóa thuật toán nhằm đảm bảo mô hình hoạt động hiệu quả.

### 6. Trình bày kết quả
- Trực quan hóa dữ liệu, kết quả dự đoán bằng bảng biểu, biểu đồ.
- Giải thích phương pháp tiếp cận và phân tích ý nghĩa của các kết quả.

## 5. Mô tả dữ liệu
Ngân hàng cung cấp dữ liệu giao dịch của khách hàng trong **1,5 năm**, từ **28/01/2015 đến 28/05/2016**. Dữ liệu này bao gồm thông tin về các sản phẩm mà khách hàng đã sở hữu mỗi tháng.

### Nhiệm vụ dự đoán
- Dự đoán các sản phẩm khách hàng sẽ mua vào **tháng cuối cùng (28/05/2016)**.
- Các sản phẩm cần dự đoán nằm trong các cột `ind_(xyz)_ult1` (cột 25 đến 48 trong dữ liệu huấn luyện).
- Loại trừ những sản phẩm mà khách hàng đã sở hữu vào **ngày 28/04/2016**.

**Bộ dữ liệu:** [Kaggle Dataset](https://www.kaggle.com/datasets/grizmo/dataflow2025-product-recommendation)
