<a id="top"></a>

<!-- Banner -->
<p align="center">
  <a href="https://www.uit.edu.vn/" title="Trường Đại học Công nghệ Thông tin" style="border: none;">
    <img src="https://i.imgur.com/WmMnSRt.png" alt="Trường Đại học Công nghệ Thông tin | University of Information Technology">
  </a>
</p>

<h1 align="center"><b>MÁY HỌC<br>(MACHINE LEARNING)</b></h>

[![Status](https://img.shields.io/badge/status-done-darkgreen?style=flat-square)](https://github.com/pahopu/CS114.N11.KHCL_SceneTextDetection_Project)
[![GitHub contributors](https://img.shields.io/github/contributors/pahopu/CS114.N11.KHCL_SceneTextDetection_Project?style=flat-square)](https://github.com/pahopu/CS114.N11.KHCL_SceneTextDetection_Project/graphs/contributors)
[![Status](https://img.shields.io/badge/language-python-blue?style=flat-square)](https://github.com/pahopu/CS114.N11.KHCL_SceneTextDetection_Project)

## [BẢNG MỤC LỤC](#top)
* [Giới thiệu môn học](#giới-thiệu-môn-học)
* [Thông tin các thành viên](#thông-tin-về-các-thành-viên-nhóm)
* [Mô tả bài toán](#mô-tả-bài-toán)
* [Colab Notebook](#colab-notebook)
* [Mô tả bộ dữ liệu](#mô-tả-bộ-dữ-liệu)
* [Mô tả thuật toán](#mô-tả-thuật-toán)
* [Đánh giá](#đánh-giá)
* [Kết quả](#kết-quả)

## [GIỚI THIỆU MÔN HỌC](#top)
* **Tên môn học:** Máy học - Machine Learning
* **Mã môn học:** CS114
* **Mã lớp:** CS114.N11.KHCL
* **Năm học:** HK1 (2022 - 2023)
* **Giảng viên:** Ths. Phạm Nguyễn Trường An

## [THÔNG TIN VỀ CÁC THÀNH VIÊN NHÓM](#top)
| STT    | MSSV          | Họ và Tên                |Vai trò    | Github                                          | Email                   |
| :----: |:-------------:| :-----------------------:|:---------:|:-----------------------------------------------:|:-------------------------:
| 1      | 20521446      | Huỳnh Nguyễn Vân Khánh   |Trưởng nhóm|[hnvkhanh](https://github.com/hnvkhanh)          |20521446@gm.uit.edu.vn   |
| 2      | 20520278      | Phạm Hoàng Phúc          |Thành viên |[pahopu](https://github.com/pahopu)              |20520278@gm.uit.edu.vn   |
| 3      | 20521663      | Nguyễn Đặng Bảo Ngọc     |Thành viên |[ngocndb03](https://github.com/ngocndb03)        |20521663@gm.uit.edu.vn   |

## [MÔ TẢ BÀI TOÁN](#top)
* **Tên đồ án:** Scene Text Detection
* **Framework:** TextFuseNet
* **Input:** 1 bức ảnh chụp mà text là thành phần có sẵn trong ảnh
* **Output:** Tọa độ của vùng chứa text gồm có 4 điểm là 4 góc của 1 hình tứ giác, gốc tọa độ được tính từ góc trên bên trái của bức ảnh và tọa độ chỉ gồm số dương
* **Các ngữ cảnh ứng dụng:** Ứng dụng trong các hệ thống hỗ trợ người khiếm thị và những hệ thống xe tự lái

## [COLAB NOTEBOOK](#top)
* Train mô hình: [colab](https://colab.research.google.com/drive/1d8Wa1fsXedJmEkuxo7nQTqXmqu81u7XE?usp=sharing)
* Thay đổi định dạng của file annotate và tạo pseudo-label: [colab](https://colab.research.google.com/drive/1btynHjJ9uRFz_l096jOhcCoqgKBOxKIr?usp=sharing)
* Đánh giá mô hình: [colab](https://colab.research.google.com/drive/1qpmX6y38oZm0yOghBMdjOo585O7eB1Bp?usp=sharing)

## [MÔ TẢ BỘ DỮ LIỆU](#top)
* **Tên bộ dữ liệu:** VinText
* **Số lượng:** 2000 ảnh
* **Phân chia:**
  * **Training set:** 
    * **Số lượng:** 1200 ảnh --> Loại bỏ các ảnh có Width x Height vượt quá 300000 pixels --> 384 ảnh
    * **Thống kê số lượng các instance trong tập train**:

      |  category  | #instances   |  category  | #instances   |  category  | #instances   |
      |:----------:|:-------------|:----------:|:-------------|:----------:|:-------------|
      |    text    | 6003         |     0      | 212          |     1      | 120          |
      |     2      | 137          |     3      | 109          |     4      | 71           |
      |     5      | 69           |     6      | 71           |     7      | 67           |
      |     8      | 74           |     9      | 70           |     A      | 1127         |
      |     B      | 221          |     C      | 574          |     D      | 343          |
      |     E      | 483          |     F      | 32           |     G      | 583          |
      |     H      | 899          |     I      | 447          |     J      | 9            |
      |     K      | 157          |     L      | 202          |     M      | 302          |
      |     N      | 1213         |     O      | 798          |     P      | 238          |
      |     Q      | 62           |     R      | 197          |     S      | 176          |
      |     T      | 781          |     U      | 559          |     V      | 160          |
      |     W      | 32           |     X      | 60           |     Y      | 178          |
      |     Z      | 3            |     a      | 150          |     b      | 18           |
      |     c      | 41           |     d      | 29           |     e      | 95           |
      |     f      | 12           |     g      | 94           |     h      | 110          |
      |     i      | 91           |     j      | 0            |     k      | 14           |
      |     l      | 26           |     m      | 93           |     n      | 156          |
      |     o      | 107          |     p      | 19           |     q      | 1            |
      |     r      | 43           |     s      | 21           |     t      | 63           |
      |     u      | 79           |     v      | 9            |     w      | 12           |
      |     x      | 1            |     y      | 30           |     z      | 0            |
      |            |              |            |              |            |              |
      |   total    | 18153        |            |              |            |              |  


  * **Validation set:** 300 ảnh
  * **Testing set:** 500 ảnh
* **Cách thức xây dựng:** Các hình ảnh trong bộ dữ liệu được tải xuống từ Internet hoặc được chụp bởi chính nhóm tác giả.
* **Repository chính thức của dataset:** [link](https://github.com/VinAIResearch/dict-guided)
* **Dataset đã được giải nén:** [drive](https://drive.google.com/drive/folders/1--sjdzVcuY37ouAKISydf5aCE3DmBowM?usp=share_link)
    
## [MÔ TẢ THUẬT TOÁN](#top)

TextFuseNet giải quyết các vấn đề khó trong bài toán Scene Text Detection bằng cách sử dụng các phương pháp kết hợp đặc trưng (feature fusion). Không giống với các phương pháp trước đó, TextFuseNet khai thác các đặc trưng ở nhiều mức độ khác nhau (mức toàn cục, mức từ và mức chữ cái) để bổ sung thêm thông tin cho quá trình dự đoán.

TextFuseNet gồm có 5 thành phần:
  * Feature Pyramid Network (FPN)
  * Region Proposal Network (RPN)
  * Nhánh Sematic Segmentation 
  * Nhánh Mask
  * Nhánh Detection

**Pipeline của TextFuseNet:**

![image](https://github.com/ying09/TextFuseNet.pytorch/blob/master/TextFuseNet.jpg)


## [ĐÁNH GIÁ](#top)

Mô hình được đánh giá theo độ đo Precision và Recall.
Trong đó, mỗi bounding box mà mô hình dự đoán được sẽ được tính là một trường hợp true positive nếu IoU giữa bounding box đó và một bounding box trong groundtruth vượt ngưỡng 50%. Mỗi trường hợp đạt ngưỡng chỉ được tính một lần, trường hợp có nhiều bounding box cùng trùng lắp với một groundtruth thì chỉ được tính là một trường hợp true positive, còn lại tính là false negative.


## [KẾT QUẢ](#top)
* Mô hình đạt kết quả như sau:
  * Precision: 0.892
  * Recall: 0.743
  * F1: 0.811
* Mô hình: [link](https://drive.google.com/file/d/1bFoGlytWUVzi7VlF2_kKNvaryaho542z/view?usp=sharing)
* Kết quả dự đoán trên tập test: [drive](https://drive.google.com/drive/folders/1gDZZgt8Qx5TeveXg_Lh8oR1Mj7fkhUdF?usp=sharing)
* Thư mục Drive Đồ án cuối kỳ: [drive](https://drive.google.com/drive/folders/1GvzxT-uVkWQiIiSbFMV-Q_iTCqA5z5j1?usp=sharing)
* Báo cáo đồ án: [pdf](https://github.com/pahopu/CS114.N11.KHCL_SceneTextDetection_Project/blob/main/CS114_FinalReport.pdf)
