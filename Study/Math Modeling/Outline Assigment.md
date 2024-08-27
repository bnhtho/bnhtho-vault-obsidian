---

cssclasses:
  - banner
  - banner-fade
---
![[Book-Banner.jpg|banner]]
# Vấn đề 

Một công ty sản xuất 100 thanh kim loại với tổng **độ dài là 100 đơn vị** ( unit long )
- **Mục tiêu :** Làm cách nào để có cắt các thanh kim loại có độ dài là 100 với <mark style="background: #FFB86CA6;">CHI PHÍ BỎ RA THẤP NHẤT</mark>.
Vấn đề trên được gọi là [Cutting-stock problem](https://en.wikipedia.org/wiki/Cutting_stock_problem) ( hay vấn đề cắt kho)

>[!info]
>### Định Nghĩa
>Trong nghiên cứu vận hành, vấn đề cắt kho là vấn đề cắt các mảnh vật liệu có kích thước tiêu chuẩn, chẳng hạn như cuộn giấy hoặc kim loại tấm, thành các mảnh có kích thước xác định trong khi giảm thiểu lãng phí vật liệu. Nó là một bài toán tối ưu hóa trong toán học nảy sinh từ các ứng dụng trong công nghiệp.

>[!warning]
>- Có nhiều cách để xác định Cutting-stock problem. Nhưng phạm vi trong bài tập lớn sẽ phải xác định thông qua phương pháp **1D** (one-dimensional)


 
## One-dimensional Cutting Stock Problem (Bài toán cắt một chiều)

- Là một bài toán kinh điển trong ngành nghiên cứu vận hành và kỹ thuật công nghiệp 
- Cắt thành các thành phần nhỏ (offer) từ phần lớn hơn (stock) với <mark style="background: #FFB86CA6;">độ dư thừa ở mức tối thiểu</mark>
- Độ phức tạp tăng lên khi số lượng kích thước tăng và đơn hàng tăng.

# Yêu Cầu Bài Tập Lớn

### Công thức hoá bài toán

Công thức hoá bài toán cắt thanh một chiều dưới dạng bài toán lập trình tuyến tính nguyên (integer linear programming)

- Biến quyết định **(decision variables)**
- Hàm mục tiêu **(objective function)**
- Các ràng buộc **(constraints)**
### Phân tích thuật toán

Phân tích và viết tóm tắt ngắn gọn về ít nhất hai thuật toán hoặc phương pháp heuristics được sử dụng để giải bài toán cắt thanh một chiều
### Nghiên cứu tình huống

- Sử dụng các ví dụ ngoài đời sống để thực hiện bài toán cắt thanh một chiều. 
- Đưa ra lợi thế / thứ yếu 

### Đánh giá hiệu suất

- Thảo luận về cách bạn sẽ đánh giá hiệu suất của thuật toán được sử dụng trong bài tập 3. 
- Các chỉ số nào sẽ được sử dụng? Làm thế nào để thu thập dữ liệu cần thiết?