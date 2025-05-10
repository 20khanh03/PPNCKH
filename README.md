FRUITS CLASSIFICATION - PHÂN LOẠI TRÁI CÂY 

I. TÓM TẮT: Phân loại trái cây dựa trên hình ảnh sử dụng các kĩ thuật machine learning
1. Bài toán:
Sự tiến bộ trong kỹ thuật xử lý hình ảnh và tự động hóa trong lĩnh vực công nghiệp thúc đẩy việc sử dụng nó trong hầu hết các lĩnh vực. Trong đó, phân loại trái cây dựa trên hình ảnh của nó vẫn còn là một thách thức. Việc phân loại trái cây có thể được sử dụng để thực hiện quá trình săp xếp và phân loại trái cây giúp quản lý, bảo quản những loại trái cây một cách tốt nhất có thể (những phương pháp bảo quản khác nhau dựa trên từng loại trái cây). Phương pháp truyền thống để phân loại trái cây là phân loại một cách thủ công, tốn thời gian và luôn phải có sự hiện diện của con người.
2. Phương pháp giải quyết:
Sử dụng Machine Learning để xây dựng model phân loại trái cây dựa trên hình ảnh. Từ đó, có thể giúp quá trình sắp xếp và phân loại trái cây trở thành một quá trình tự động gần như hoàn toàn.
Input: Ảnh của một loại trái cây trên nền đơn giản (1 màu).
Output: Tên của loại trái cây đó.

II. DỮ LIỆU

Nghiên cứu này tập trung vào ứng dụng Machine Learning để nhận diện trái cây, sử dụng tập dữ liệu Fruits-360 gồm hơn 130.000 hình ảnh của 194 loại trái cây và rau củ. Phạm vi nghiên cứu được xác định như sau: 
Đối tượng nghiên cứu: Các thuật toán Machine Learning, đặc biệt là mạng nơ-ron tích chập (CNN), được sử dụng để phân loại trái cây dựa trên hình ảnh trong tập dữ liệu Fruits-360. 

Dữ liệu nghiên cứu: Chỉ sử dụng hình ảnh của trái cây từ Fruits-360, đảm bảo tính thống nhất và chất lượng dữ liệu phù hợp cho quá trình huấn luyện mô hình. 
Phương pháp nghiên cứu: Tiền xử lý hình ảnh, huấn luyện mô hình CNN, và đánh giá hiệu suất trên tập kiểm tra từ cùng tập dữ liệu Fruits-360. 
Giới hạn nghiên cứu:  
Không mở rộng nghiên cứu sang nhận diện thực phẩm khác ngoài trái cây. 
Không nghiên cứu tích hợp mô hình vào hệ thống kiểm tra chất lượng thực tế, chỉ tập trung vào phân loại hình ảnh. 
Không sử dụng dữ liệu bên ngoài ngoài Fruits-360 để đảm bảo tính nhất quán trong nghiên cứu. 

III. CÁC KĨ THUẬT XỬ LÍ DATA

 sử dụng 2 phương pháp tách biệt để xử lí data và training model đó là dựa trên màu sắc và cạnh. Sau đó kết hợp lại với nhau để train model.
1. Xử lý data dựa trên màu của bức ảnh
Resize ảnh về size 200x200.
Đưa bức ảnh về 2 màu sử dụng thuật toán K-means.
Loại bỏ màu sáng hơn của bức ảnh (Màu sáng hơn thường là màu nền, nên loại bỏ).
Chia nhỏ bức ảnh thành 25 section (40x40).
Tính trung bình và độ lệch chuẩn cho:
Hướng thứ nhất: Từng channel màu trong 3 channel màu RGB
Hướng thứ hai: Cho từng section
    

2. Xử lý data bằng kĩ thuật tìm cạnh
Resize ảnh về size 200x200.
Hướng thứ nhất:
Đưa bức ảnh về 2 màu sử dụng thuật toán K-means.
Sử dụng thuật toán Canny để tìm cạnh.
Chia nhỏ bức ảnh thành 25 section (40x40).
Tính trung bình và độ lệch chuẩn cho từng section.
Hướng thứ hai:
Sử dụng thuật toán Canny để tìm cạnh.
Chia nhỏ bức ảnh thành 25 section (40x40).
Tính trung bình và độ lệch chuẩn cho từng section.
    

IV. CÁC MODEL SỬ DỤNG ĐỂ TRAIN

Tận dụng CNN nhưng cải tiến kiến trúc: Sử dụng mô hình CNN nâng cao, có thể kết hợp với ResNet hoặc EfficientNet để cải thiện độ chính xác. 
Tăng cường dữ liệu thực tế: Áp dụng kỹ thuật tăng cường dữ liệu, như xoay ảnh, thay đổi độ sáng, làm mờ nền để mô hình hoạt động tốt hơn trong điều kiện thực tế. 
Đánh giá mô hình trên dữ liệu thực tế: Thay vì chỉ kiểm tra trên tập Fruits-360, nghiên cứu sẽ thử nghiệm mô hình với ảnh chụp thực tế, giúp đánh giá khả năng nhận diện trong môi trường đa dạng. 


VI. KẾT LUẬN

Tóm tắt kết quả đạt được
Đã xây dựng thành công một quy trình tạo tập dữ liệu ảnh trái cây quay 360 độ, kết hợp phần cứng đơn giản (camera, động cơ quay).


Đã thiết kế và triển khai thuật toán tách nền dựa trên phương pháp flood fill, giúp làm sạch nền ảnh hiệu quả trước khi đưa vào huấn luyện mô hình.


Đã xây dựng mô hình học sâu sử dụng mạng CNN gồm nhiều tầng Conv2D – MaxPooling – Dense, cho kết quả phân loại khả quan.


Đã thực hiện huấn luyện và đánh giá mô hình với độ chính xác cao trên tập dữ liệu được xử lý.

