# Xây Dựng Kho Dữ Liệu Quản Lí Các Ca Tai Nạn Giao Thông US từ 2016 - 2021 
--------------------------------------
## 1. Giới thiệu đề tài
![image](https://github.com/nguyenthanhhungDE/DATA-WAREHOUSE-ACCIDENT-US-2016-2021/assets/134383281/b5668439-fd71-4e9c-bac7-ff02461a3144)

Tai nạn giao thông cũng ảnh hưởng đến kinh tế và tài chính của các quốc gia. Các chi phí liên quan đến tai nạn giao thông, bao gồm chi phí y tế, bảo hiểm, chi phí sửa chữa và thay thế phương tiện và nhiều chi phí khác, đều ảnh hưởng đến tài chính cá nhân và của quốc gia.
Phân tích dữ liệu tai nạn giao thông cũng có thể cung cấp thông tin giá trị cho các nhà lãnh đạo và quyết định chính sách. Dữ liệu có thể giúp các nhà quản lý địa phương và quốc gia hiểu rõ hơn về các nguyên nhân và mô hình tai nạn giao thông, từ đó đưa ra quyết định chính sách phù hợp để giảm thiểu số vụ tai nạn.
## 2. Thông tin về dataset
- Mỗi bản ghi trong tập dữ liệu này chứa thông tin chi tiết về các tai nạn giao thông, bao gồm địa điểm, thời gian, điều kiện thời tiết, tình trạng đường, loại xe, số lượng và tính chất của các phương tiện tham gia, và mức độ nghiêm trọng của các thương vong. Tập dữ liệu này cũng cung cấp thông tin về địa lý, bao gồm vị trí địa lý của các tai nạn, cũng như các thông tin về địa lý khác như tên tiểu bang, thành phố, mã bưu chính, v.v.
- Dataset được lấy từ Dataset: https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents 
- Sau khi nghiên cứu, thì em đã lấy ra các thuộc tính và các bảng cần thiết cho dự án của mình, bao gồm các bảng:
- DimDate : Thông tin về ngày xảy ra tai nạn
- DimDriver : Thông tin về tài xế lái xe
- DimLocation : Thông tin về vị trí xảy ra tai nạn.
- DimRoadFeature : Thông tin về đoạn đường xảy ra tai nạn
- DimRoadSurfaceCondition : Thông tin về chi tiết mặt đường
- DimRoadType : Thông tin về loại đường
- DimSpeedLimit : Thông tin về giới hạn tốc độ đoạn đường
- DimTwilight : Thông tin về điều kiện ánh sáng lúc xảy ra tai nạn
- DimVehicle : Thông tin về phương tiện xảy ra tai nạn
- DimWeather : Thông tin về thời tiết
- DimWeatherCondition : Thông tin về điều kiện thời tiết
- Diagram :
![image](https://github.com/nguyenthanhhungDE/DATA-WAREHOUSE-ACCIDENT-US-2016-2021/assets/134383281/5c7756c4-8144-41ff-876b-b4c01aeca09e)
- Link Video Báo Cáo: https://www.youtube.com/watch?v=asq4lMO2jKk&t=837s
## 3. Nội dung chính của dự án
3.1 Xây dựng kho dữ liệu bằng công cụ SSIS
- Tạo StageAccident lưu trữ các table stage và DwAccident lưu trữ các tabel Dim - Fact
- Đổ dữ liệu từ excel vào các bảng stage
- Đổ dữ liệu từ stage vào các bảng Dim và Fact
- Tạo các khoá ngoại giữa các bảng Fact và các bảng Dim
-----------------------
3.2 Xây dựng cube và truy vấn bằng công cụ SSAS
- Tạo Data Source từ kho dữ liệu database DWAccident
- Tạo Data Source View
- Tạo cube, thêm measure và các dim cần thiết,tạo các phân cấp 
- Truy vấn các câu hỏi mà nhóm đưa ra bằng công cụ SSAS, Pivot Table, PowerBI
3.3. Xây dựng Dashboard với PowerBI
- Dashboard Thống kê tất cả các ca tai nạn và thương vong theo địa điểm:
![image](https://github.com/nguyenthanhhungDE/DATA-WAREHOUSE-ACCIDENT-US-2016-2021/assets/134383281/4a7b8e9c-c7f6-4299-98fc-5f5172504695)
- Dashboard Thống kê tất cả các ca tai nạn và thương vong theo thời gian:
![image](https://github.com/nguyenthanhhungDE/DATA-WAREHOUSE-ACCIDENT-US-2016-2021/assets/134383281/ab79bd1f-5431-4a80-8aa6-f241f9b1a5a7)
- Dashboard Thống kê tất cả các ca tai nạn và thương vong theo các điều kiện có thể dãn đến tai nạn:
![image](https://github.com/nguyenthanhhungDE/DATA-WAREHOUSE-ACCIDENT-US-2016-2021/assets/134383281/2edfd562-1fd7-4195-9761-d4ddcabdfcbf)



