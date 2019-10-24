# So sánh 2 công cụ kiểm thử tĩnh FindBugs và PMD với bộ Juliet Test Suites

## Cách thức triển khai

- Ngôn ngữ: Java
- Dữ liệu kiểm thử: Juliet Test Suites for Java
- Cài đặt 2 công cụ trên dưới dạng plugin trong Intellij IDE

## Giao diện plugin FindBugs trên Intellij IDE

![](https://lh3.googleusercontent.com/Qt5rxL-750v_QItaWXY1orzmjcpXMh-xQDAI2HR-ASVdI7tDBt4g2bTvIq_LaFNaMroFdnJAC-lO2_NuzZ-U4r0ENvp7lRmWbsdiiTVCrcbm_MWUMeW1tbbv6J9bbfMtOFEO-XEOPUi7zLKRaG8b_Dy9-N44ARdioFcPaxT0YdwzpswNTLOc8xrQdSd_pVLf05rIOgek1LHcjiEKQTXAyWwE4GDUplu-YU75-JEJnOg_1BUZUWq8HCBuP8mCudt54Bi8h2CApbF25Cjqw4SgFn8gmMmt3Qzsnu_6qrYpRY-dfi5mtm7OcaKrrIyYen_vReBdmgKBdXzHvwRTkYX29hiYYI2SUQVHIWhtOPU9umrJSr1d1qrnq5xqA2uD1j1fXg9gh-SXpwBNysdDzCuh3biEcZkDSpFINDcv-SUGvBj_8O09KgeH0NpsLM9CwuKudzR_ryG-1xghrN0wWkLr91bLLr-cnCoXwQYR95sZuw0tXzeS3Hr3hAEYVPTJJzhdqu-IzSDJrDX29clxH91QYy29bVrjFp8HkWJxZC6yTBBFKcvvLx2aOLnwyY2Zu6wE1hIjTF4Px8OFZK4fbJGERQV9RiRrWKZKcCri90W__cYULCnMLNSQSRXHvE4_hPoxlFz-VRnLEp-f2Xz0jOHTSmHv9j5mdfeP_iz-OAX2zrzrRXzBrkjZ-TtnnNzLD1opOnYhIqp4kVL8Z36aF_3rURqzeyd1g_-jJzFLnTRMlwL-hF4=w1775-h915-no)

## Giao diện plugin PMD trên Intellij IDE

![](https://lh3.googleusercontent.com/uZNPDmYYhOFBlhncjS6qGJRDvqdHPyMu_-9DfPM-JH8hKWvMsEIuwkAEmIrSl0FFvb-rqwSmgmAx7e8wqLtCG2XSzCvZs4rgsDow_k1HTpfWTuxheqdUtk2pGK0C5lP6O6W7AFoQIh99Nsq2Ds18K8WEOlGDQpc_p2r5Nph8Aiq-hn8Lz5dGw1yVtIaD1z8VioHBe5x--1LWdBP9TzZK3EDA0HRqAax068neeh40mlTLG0Zsgj4CiGiBEASLliiVaLhiHXPCmwYeAVS9wgfZ6oKC41tK0mHpeneX0mgyOYR9XFEYkK9VwO5dlJ9lW4ELEWE4o7mgmpH8HO9_sP-8Hkv8p44My6DfhoRoRCrQsL2aG-xu7Uz-KAVIUhlhNYTQnZBpQ2fhJbJO6dEYxogdjlQqwcnTat5H_eEqkyU12gZwfbpZwOJyssuDUT2HixpR2GixbH2TVZ3_X6Ag7MxJQQYKSheWED0fqDtkNGhUM-JKhimmBMWhI5L3BLqWMs0bE1g20B5D1rREWaVuUHg10-gKZg_Vgk-QnOk0UmgOmblmk406deD_wZ73YgbUf7EGzrTeau3BmjnXo2BzxCthcw9kZjhYVEtSkkdUwTMGqr0ku0flHLqeW6CD6r9iHZPwG6t_NBFHopIGZQRLBY4nEdwl31rL6zvhWdFnTarUgcHfhSdYCRVyHwMgTtN5FTc1aBqlzYctuvzpwFhSHPx3ycwwm3st7I9ZC3nlG2zHNwRIcn8=w1719-h915-no)

## Giải thích cấu trúc thư mục

- Do dung lượng của bộ test Juliet quá lớn, chia thành nhiều phần, mỗi phần ứng với một thư mục
- Tên thư mục là kí hiệu là số code CWE, xxx ứng với bộ test CWExxx, một thư mục có thể lưu kết quả của nhiều bộ test
- Trong thư mục có lưu kết quả test ứng với 2 công cụ FindBugs và PMD
- Kết quả test của công cụ FindBugs được lưu trong file .html
- Kết quả test của công cụ PMD được lưu dưới dạng ảnh trong thư mục pmd
- File report.xlsx chứa kết quả so sánh giữa 2 công cụ với 21 bộ test tương ứng với 21 lỗi mà chúng ta thường xuyên mắc phải
(Do thời gian có hạn nên không thể so sánh được toàn bộ các bộ test)