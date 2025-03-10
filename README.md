# Analyze and Predict Weather

## 1. Dữ liệu thời tiết
### **data_29_06_22-30_06_23**
Đây là tập dữ liệu chứa thông tin thời tiết của các vùng thuộc khu vực Bắc Bộ trong khoảng thời gian từ ngày **29/06/2022** đến **30/06/2023**.

Dữ liệu gồm nhiều thuộc tính như:
- **Day**: Ngày thu thập dữ liệu
- **TempMax**: Nhiệt độ cao nhất trong ngày (°C)
- **TempMin**: Nhiệt độ thấp nhất trong ngày (°C)
- **TempAvg**: Nhiệt độ trung bình trong ngày (°C)
- **MaxWind_km/h**: Vận tốc gió mạnh nhất trong ngày (km/h)
- **TotalPrecip_mm**: Tổng lượng mưa trong ngày (mm)
- **AvgHumidity**: Độ ẩm trung bình trong ngày (%)

Ví dụ dữ liệu:
| Day         | TempMax | TempMin | TempAvg | MaxWind_km/h | TotalPrecip_mm | AvgHumidity |
|------------|---------|---------|---------|--------------|---------------|-------------|
| 2022-06-29 | 23.7    | 18.3    | 20.5    | 11.2         | 13.3          | 90.0        |
| 2022-06-30 | 23.5    | 17.7    | 20.2    | 7.9          | 8.9           | 89.0        |
| 2022-07-01 | 23.4    | 17.5    | 20.2    | 8.3          | 7.0           | 91.0        |
| 2022-07-02 | 26.1    | 17.4    | 21.7    | 9.7          | 6.8           | 84.0        |
| 2022-07-03 | 26.7    | 17.9    | 21.9    | 15.2         | 4.7           | 84.0        |

### **data_cac_tinh**
Dữ liệu thời tiết theo từng tỉnh/thành phố tại khu vực Bắc Bộ với các thông tin tương tự **data_29_06_22-30_06_23**, nhưng được chia nhỏ theo từng địa phương để phục vụ phân tích chi tiết.

---

## 2. Dữ liệu tổng hợp
### **data_tong_hop**
Dữ liệu tổng hợp từ nhiều nguồn khác nhau, giúp có cái nhìn toàn diện về tình hình thời tiết khu vực Bắc Bộ. Dữ liệu bao gồm:
- **Data Weather in Northern VietNam.xlsx**: Dữ liệu tổng hợp toàn bộ miền Bắc Việt Nam
- **Dong Bac Bo.xlsx**: Dữ liệu khu vực Đông Bắc Bộ
- **Dong bang song Hong.xlsx**: Dữ liệu khu vực Đồng bằng sông Hồng
- **Tay Bac Bo.xlsx**: Dữ liệu khu vực Tây Bắc Bộ

---

## 3. Thu thập và xử lý dữ liệu
### **thu_thap_data**
Chứa mã nguồn thực hiện thu thập dữ liệu từ các API thời tiết và các nguồn dữ liệu mở. Quá trình thu thập dữ liệu bao gồm:
- **Gửi yêu cầu API** đến các nguồn dữ liệu thời tiết
- **Lọc và lưu trữ dữ liệu** vào các file CSV hoặc Excel
- **Tạo bảng dữ liệu chuẩn hóa** để phục vụ phân tích

### **xu_ly_data**
Chứa mã nguồn xử lý và phân tích dữ liệu, bao gồm:
- **Xử lý dữ liệu thiếu** (missing values)
- **Chuyển đổi định dạng thời gian**
- **Chuẩn hóa đơn vị đo lường**
- **Làm sạch dữ liệu** để đảm bảo tính chính xác khi sử dụng

---

## 4. Phân tích và dự đoán
### **phan_tich_luong_mua.ipynb**
Tệp notebook chứa mã nguồn và phân tích dự đoán lượng mưa.

#### **Mục tiêu**
- **Dự đoán lượng mưa** trong tương lai dựa trên dữ liệu lịch sử
- **Đánh giá tiềm năng sản xuất điện năng** của các đập thủy điện dựa trên lượng mưa dự đoán
- **Xác định mối quan hệ giữa lượng mưa và sản lượng điện năng**

#### **Phương pháp phân tích**
- **Phân tích chuỗi thời gian** để dự báo lượng mưa
- **Sử dụng các mô hình hồi quy** để ước tính sản lượng điện dựa trên lượng mưa
- **Đánh giá độ chính xác của mô hình** bằng các chỉ số thống kê

---

Dự án này hướng tới việc cung cấp thông tin quan trọng giúp các nhà quản lý và nhà nghiên cứu có cái nhìn tổng quan về biến động thời tiết, từ đó tối ưu hóa việc vận hành và sản xuất điện năng từ thủy điện.

