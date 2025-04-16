# 📈 Time Series Analysis Project

Dự án này thực hiện phân tích và dự báo dữ liệu chuỗi thời gian (time series) từ bộ dữ liệu Superstore, tập trung vào cột **Sales** theo thời gian.

---

## 🎯 Mục tiêu

- Hiểu xu hướng (**trend**), mùa vụ (**seasonality**), và nhiễu (**noise**) trong dữ liệu.
- Xây dựng mô hình **ARIMA** để dự báo doanh số bán hàng trong tương lai.

---

## 🔧 Các bước và kỹ thuật đã dùng

### 1. Xử lý và khám phá dữ liệu
- Tổng hợp dữ liệu theo tháng
- Vẽ biểu đồ để quan sát xu hướng, mùa vụ
- Tính trung bình trượt (**rolling average**)

### 2. Kiểm tra tính dừng (Stationarity)
- Sử dụng kiểm định **ADF (Augmented Dickey-Fuller)**
- Dùng phép **lấy sai phân (differencing)** để làm cho chuỗi dừng

### 3. Phân rã chuỗi thời gian
- Tách chuỗi thành các phần: **Trend**, **Seasonality**, **Residuals**

### 4. Xác định tham số mô hình ARIMA
- Vẽ biểu đồ **ACF** và **PACF**
- Dò tìm bộ tham số tốt nhất: **(p, d, q)**

### 5. Xây dựng mô hình và dự báo
- Dùng **ARIMA** từ thư viện `statsmodels`
- So sánh giữa **giá trị thực tế** và **dự báo**
- Vẽ biểu đồ thể hiện kết quả dự báo

---

## 📌 Gợi ý cải tiến trong tương lai

- Áp dụng mô hình **SARIMA** hoặc **Prophet** để xử lý mùa vụ rõ hơn
- Tích hợp dự báo vào **Streamlit Dashboard**
- Tự động hóa việc chọn tham số ARIMA bằng `pmdarima`

