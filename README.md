
# Xây Dựng Mô Hình Phân Loại Trái Cây Bằng Hình Ảnh Sử Dụng Dữ Liệu Fruits-360

Phương pháp nghiên cứu khoa học trong CNTT


## Thông tin liên hệ 
**Nhóm sinh viên thực hiện** :
- Trần Hoàng Khanh _ 3121410257 _ 20hoangkhanh03@gmail.com 
- Nguyễn Ngọc Hải _ 3121410175 _ emkotenrr@gmail.com 
- Dương Duy Khang _ 3121410250 _ duongduykhang03@gmail.com

**Giảng Viên Hướng Dẫn** : TS. Đỗ Như Tài

**Cơ Quan** : Khoa Công nghệ Thông tin, Trường Đại học Sài Gòn, TPHCM

## Tổng quan 
Nghiên cứu này được thực hiện với mục đích chính là xây dựng một hệ thống tự động nhận diện và phân loại trái cây dựa trên hình ảnh, nhằm thay thế quy trình thủ công còn nhiều hạn chế hiện nay. Việc phát triển hệ thống này không chỉ giúp tăng độ chính xác và tốc độ xử lý trong khâu phân loại, mà còn góp phần hiện đại hóa quy trình sản xuất, đóng gói và kiểm định chất lượng nông sản tại Việt Nam.

## Mục tiêu đề tài

-	**Ứng dụng phương pháp học sâu** để phát triển mô hình có khả năng nhận diện và phân loại các loại trái cây phổ biến dựa trên hình ảnh đầu vào.
-	**Xây dựng quy trình huấn luyện mô hình** dựa trên tập dữ liệu hình ảnh thực tế, đảm bảo mô hình học được đặc trưng quan trọng của từng loại trái cây trong điều kiện chụp ảnh đa dạng.
-	**Đánh giá hiệu suất mô hình** thông qua các chỉ số đo lường như độ chính xác, độ nhạy và tốc độ xử lý, đồng thời so sánh với các mô hình học sâu khác để chọn ra phương pháp tối ưu.


## Bộ dữ liệu Fruits-360 
**Mô tả** : Bộ dữ liệu Fruits-360 là một bộ dữ liệu hình ảnh gồm hơn 90.000 ảnh trái cây thuộc 131–166 loại (tùy phiên bản), được chụp trong môi trường kiểm soát (nền trắng, ánh sáng đều). Mỗi ảnh có kích thước 100×100, chụp từ nhiều góc khác nhau, phục vụ huấn luyện và kiểm thử các mô hình thị giác máy tính phân loại trái cây.

**Một số bài báo có sử dụng bộ dữ liệu** :
| STT             | Tên Bài Báo                                                                | Tác giả       |
| ----------------- | ------------------------------------------------------------------ | -------------|
| 1 | Fruit recognition from images using deep learning  |Horea Mureșan, Mihai Oltean (2018) |
| 2 |  A fruits recognition system based on a modern deep learning technique| Dang Thi Phuong Chung, Dinh Van Tai (2019)| 
| 3 | Performance Analysis of Different Optimizers for Deep Learning-Based Image Recognition | Seda Postalcıoğlu (2020)| 
| 4 |Centre-loss—A preferred class verification approach over sample-to-sample in self-checkout products datasets  |Ciapas B., Treigys P. (2024)  |
|5|  Image classification based on tensor network DenseNet model| Chunyang Zhu, Lei Wang, Weihua Zhao, Heng Lian (2024)|



**Trích dẫn** : Oltean, Mihai (2018), “Fruits 360 dataset”, Mendeley Data, V1, **DOI**: 10.17632/rp73yg93n8.1

## Kế hoạch thực hiện
|STT|Giai Đoạn|Mô Tả|Thời Gian Thực Hiện| 
| ----- | --------------------- | --------------------------| ---------------|
|1|Tìm kiếm | Tìm hiểu và đọc các bài báo nghiên cứu khoa học|2 tuần|
|2|Xác định đề tài|Nghiên cứu, xác định và chọn đề tài,  tìm và đọc các bài báo liên quan| 2 tuần|
|3|Xây dựng kế hoạch| Xác định input/output, độ đo bài toán , xây dựng đề cương|3 tuần|
|4|Khám phá dữ liệu /EDA| Kiểm tra/Thống kê mô tả dữ liệu, xử lý dữ liệu lỗi/ thiếu| 2 tuần|
|5|Tiền xử lý dữ liệu| Chuẩn hóa hình ảnh trước khi đưa vào huấn luyện| 1 tuần |
|6| Huấn luyện model|Xây dựng và huấn luyện các mô hình (CNN,MobileNet,ResNet, ...)|3 tuần |
|7|Đánh giá mô hình| So sánh các kết quả và tối ưu |1 tuần|
|8|Báo cáo|Tổng hợp kết quả , hoàn thiện và viết báo cáo nghiên cứu|1 tuần|
|9|||||15/15 tuần|

## Tài liệu tham khảo 
[1] H. Mureșan and M. Oltean, “Fruit recognition from images using deep learning,” Acta Univ. Sapientiae, Informatica, vol. 10, no. 1, pp. 26–42, 2018. DOI: 10.2478/ausi-2018-0002.

[2] Frida Femling, Adam Olsson, Fernando Alonso-Fernandez, “Fruit and Vegetable Identification Using Machine Learning for Retail Applications”,  arXiv:1810.09811v1 [cs.CV] 23 Oct 2018.

[3] J. Brownlee. (2016). Machine Learning Mastery With Python: Understand Your Data, Create Accurate Models and Work Projects End-To-End. Melbourne, VIC, Australia: Machine Learning Mastery.

[4] Cheng, H., Damerow, L., Sun, Y., and Blanke,M. Early yield prediction using image analysis of apple fruit and tree canopy features with neural networks. Journal of Imaging 3, 1 (2017). 
