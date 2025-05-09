FRUITS CLASSIFICATION - PHÂN LOẠI TRÁI CÂY
I. TÓM TẮT: Phân loại trái cây dựa trên hình ảnh sử dụng các kĩ thuật machine learning
1. Bài toán:
Sự tiến bộ trong kỹ thuật xử lý hình ảnh và tự động hóa trong lĩnh vực công nghiệp thúc đẩy việc sử dụng nó trong hầu hết các lĩnh vực. Trong đó, phân loại trái cây dựa trên hình ảnh của nó vẫn còn là một thách thức. Việc phân loại trái cây có thể được sử dụng để thực hiện quá trình săp xếp và phân loại trái cây giúp quản lý, bảo quản những loại trái cây một cách tốt nhất có thể (những phương pháp bảo quản khác nhau dựa trên từng loại trái cây). Phương pháp truyền thống để phân loại trái cây là phân loại một cách thủ công, tốn thời gian và luôn phải có sự hiện diện của con người.
2. Phương pháp giải quyết:
Sử dụng Machine Learning để xây dựng model phân loại trái cây dựa trên hình ảnh. Từ đó, có thể giúp quá trình sắp xếp và phân loại trái cây trở thành một quá trình tự động gần như hoàn toàn.
Input: Ảnh của một loại trái cây trên nền đơn giản (1 màu).
Output: Tên của loại trái cây đó.

II. DỮ LIỆU

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

VI. KẾT LUẬN
Hướng dẫn sử dụng
