# So sánh 2 công cụ kiểm thử tĩnh FindBugs và PMD với bộ Juliet Test Suites

## Cách thức triển khai

- Ngôn ngữ: Java
- Dữ liệu kiểm thử: Juliet Test Suites for Java
- Cài đặt 2 công cụ trên dưới dạng plugin trong Intellij IDE

## Giao diện plugin FindBugs trên Intellij IDE

![](https://photos.google.com/share/AF1QipMSdmCDeIpfa1Z_K-Ctt4CcRvqHykF3sbtI_Lmlmt76eHzq0ChsASoCQrLyA7r8VQ/photo/AF1QipMDbOfc0YP_4BomlOrldSyy5__e9-JRRrjOZa-b?key=a3ROWENORFJqNkpITUJMazBGdXNaaFNXSldEYmVB)

## Giao diện plugin PMD trên Intellij IDE

![](https://photos.google.com/share/AF1QipMSdmCDeIpfa1Z_K-Ctt4CcRvqHykF3sbtI_Lmlmt76eHzq0ChsASoCQrLyA7r8VQ/photo/AF1QipPs2FrH3uBJCHiDkPeHdch-M1F65SQtPn7lnpeu?key=a3ROWENORFJqNkpITUJMazBGdXNaaFNXSldEYmVB)

## Giải thích cấu trúc thư mục

- Do dung lượng của bộ test Juliet quá lớn, chia thành nhiều phần, mỗi phần ứng với một thư mục
- Tên thư mục là kí hiệu là số code CWE, xxx ứng với bộ test CWExxx, một thư mục có thể lưu kết quả của nhiều bộ test
- Trong thư mục có lưu kết quả test ứng với 2 công cụ FindBugs và PMD
- Kết quả test của công cụ FindBugs được lưu trong file .html
- Kết quả test của công cụ PMD được lưu dưới dạng ảnh trong thư mục pmd
- File report.xlsx chứa kết quả so sánh giữa 2 công cụ với 21 bộ test tương ứng với 21 lỗi mà chúng ta thường xuyên mắc phải
(Do thời gian có hạn nên không thể so sánh được toàn bộ các bộ test)