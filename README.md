<!-- Banner -->
<p align="center">
  <a href="https://www.uit.edu.vn/" title="Trường Đại học Công nghệ Thông tin" style="border: none;">
    <img src="https://i.imgur.com/WmMnSRt.png" alt="Trường Đại học Công nghệ Thông tin | University of Information Technology">
  </a>
</p>

<h1 align="center"><b>MÁY HỌC<br>(MACHINE LEARNING)</b></h>

[![Status](https://img.shields.io/badge/status-working-brightgreen?style=flat-square)](https://github.com/pahopu/CS114.N11.KHCL_SceneTextDetection_Project)
[![GitHub contributors](https://img.shields.io/github/contributors/pahopu/CS114.N11.KHCL_SceneTextDetection_Project?style=flat-square)](https://github.com/pahopu/CS114.N11.KHCL_SceneTextDetection_Project/graphs/contributors)
[![Status](https://img.shields.io/badge/language-python-green?style=flat-square)](https://github.com/pahopu/CS114.N11.KHCL_SceneTextDetection_Project)

## BẢNG MỤC LỤC
* [Giới thiệu môn học](#giới-thiệu-môn-học)
* [Thông tin các thành viên](#thông-tin-về-các-thành-viên-nhóm)
* [Mô tả bài toán](#mô-tả-bài-toán)

## GIỚI THIỆU MÔN HỌC
* **Tên môn học:** Máy học - Machine Learning
* **Mã môn học:** CS114
* **Mã lớp:** CS114.N11.KHCL
* **Năm học:** HK1 (2022 - 2023)
* **Giảng viên:** Ths. Phạm Nguyễn Trường An

## THÔNG TIN VỀ CÁC THÀNH VIÊN NHÓM
| STT    | MSSV          | Họ và Tên                |Vai trò    | Github                                          | Email                   |
| :----: |:-------------:| :-----------------------:|:---------:|:-----------------------------------------------:|:-------------------------:
| 1      | 20521446      | Huỳnh Nguyễn Vân Khánh   |Trưởng nhóm|[hnvkhanh](https://github.com/hnvkhanh)          |20521446@gm.uit.edu.vn   |
| 2      | 20520278      | Phạm Hoàng Phúc          |Thành viên |[pahopu](https://github.com/pahopu)              |20520278@gm.uit.edu.vn   |
| 3      | 20521663      | Nguyễn Đặng Bảo Ngọc     |Thành viên |[ngocndb03](https://github.com/ngocndb03)        |20521663@gm.uit.edu.vn   |

## MÔ TẢ BÀI TOÁN
* **Tên đồ án:** Scene Text Detection
* **Framework:** TextFuseNet
* **Input:** 1 bức ảnh chụp mà text là thành phần có sẵn trong ảnh
* **Output:** Tọa độ của vùng chứa text gồm có 4 điểm là 4 góc của 1 hình tứ giác, gốc tọa độ được tính từ góc trên bên trái của bức ảnh và tọa độ chỉ gồm số dương
* **Các ngữ cảnh ứng dụng:** Ứng dụng trong các hệ thống hỗ trợ người khiếm thị và những hệ thống xe tự lái

## MÔ TẢ BỘ DỮ LIỆU
* **Tên bộ dữ liệu:** VinText
* **Số lượng:** 2000 ảnh
* **Phân chia:**
  * **Training set:** 1200 ảnh --> Loại bỏ các ảnh có Width x Height vượt quá 300000 pixels --> 384 ảnh
  * **Validation set:** 300 ảnh
  * **Testing set:** 500 ảnh
* **Cách thức xây dựng:**
  * Các hình ảnh trong bộ dữ liệu được tải xuống từ Internet hoặc được chụp bởi chính nhóm tác giả.
* **Cách thao tác tiền xử lý:**
* **Repository chính thức của dataset:** [link](https://github.com/VinAIResearch/dict-guided)
* **Dataset đã được giải nén:** [drive](https://drive.google.com/drive/folders/1--sjdzVcuY37ouAKISydf5aCE3DmBowM?usp=share_link)
  
## MÔ TẢ THUẬT TOÁN

TextFuseNet giải quyết các vấn đề khó trong bài toán Scene Text Detection bằng cách sử dụng các phương pháp kết hợp đặc trưng (feature fusion). Không giống với các phương pháp trước đó, TextFuseNet khai thác các đặc trưng ở nhiều mức độ khác nhau (mức toàn cục, mức từ và mức chữ cái) để bổ sung thêm thông tin cho quá trình dự đoán.

## ĐÁNH GIÁ

## KẾT LUẬN
