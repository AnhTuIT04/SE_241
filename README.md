# CÔNG NGHỆ PHẦN MỀM 2024 - HCMUT_SSPS

### Current Week : 8

### CÔNG VIỆC

| STT | Họ và tên           | MSSV    | Vai trò           |
| --- | ------------------- | ------- | ----------------- |
| 1   | Lê Hoàng Ngọc Hân   | 2210935 | Front-end         |
| 2   | Huỳnh Văn Tú        | 2213841 | Front-end         |
| 3   | Lê Hoàng Khánh Vinh | 2213963 | Front-end         |
| 4   | Chu Minh Tâm        | 2213009 | Manage + Back-end |
| 5   | Huỳnh Thị Minh Tâm  | 2213013 | Back-end          |
| 6   | Trần Mạnh Tuấn      | 2213807 | Back-end          |
| 7   | Phạm Việt Anh       | 2210128 | Back-end          |
| 8   | Võ Quốc Huy         | 2211303 | Back-end          |

### Lưu ý :

- Không push lên main, chỉ pull request lên branch (ai phụ trách phần nào thì pull lên ở brand đó).
- Sau đó code sẽ được merge lại và đẩy lên nhánh develop.
  Main chỉ là nơi up code lên, code clean nhất vào thời điểm đó và là source code dùng để nộp bài.
- Bất cứ thay đổi nào khi commit lên phải có thông báo.
- Mỗi service đều phải đính kèm Documents (README.md) giải thích, Code phải có comment.
- Không hardcode, các service đều phải scale được.

### Cách push code lên branch:

Check git branch

```bash
git branch
```

Thêm file muốn commit

```bash
git add <file-name>
```

hoặc thêm tất cả file

```bash
git add .
```

Tạo commit với thông điệp mô tả thay đổi

```bash
git commit -m "Text"
```

Push code lên branch

```bash
git push origin <branch-name>
```

---

## FRONT-END

### Công việc

- Thiết kế UI/UX
  - Admin
  - Student
  - SPSO
  - Payment
  - Printer
- Thiết kế RESTful APIs
  - Dựa vào các diagram đã làm để thiết kế RESTful APIs.

### Công nghệ

- TypeScript / Javascript
- ReactJS
- TailwindCSS

---

## Back-end

### CÔNG VIỆC

- Ai đảm nhận diagram nào thì tiếp tục hoàn thiện tất cả những module của diagram đó (_Use-case, Acitvity, Sequence, Class_)
- Thiết kế Database.
- Thiết kế API theo kiến trúc Microservice.
- Các services :
  - **Authentication** -> Tâm
    - HCMUT_SSO. **(Oauth2, JWT)**
    - API gateway, security.
  - **Printer Management** -> Huy
    - Thêm, sửa xóa, kích hoạt, vô hiệu hóa
    - Quản lý dữ liệu liên quan tới máy in: ID, model, địa điểm, trạng thái
  - **Print Process** -> Việt Anh
    - Xử lý quá trình in: nhận file, thuộc tính in (kích cỡ giấy, số trang, số mặt,...).
    - Tích hợp với trang **Student** và **SPSO**.
    - __Mornitoring + Alerting.__
  - **Logging and Reporting** -> Tâm Huỳnh
    - Ghi nhận và lưu lại lịch sử in, tạo báo cáo hàng tháng/ năm.
  - **Payment** -> Tuấn
    - Mua thêm trang in, tích hợp với hệ thống thanh toán trực tuyến.
    - Quản lý số trang in của sinh viên và kiểm tra số dư khi sinh viên thực hiện lệnh in.
    - Payment logging.

### CÔNG NGHỆ

- Tạo API, Server : **NodeJs, Go.**
- Thực hiện logic _(printer, payment)_ : **Python.**
- Database : **MongoDB, mySQL.**
- Host-server : **Cloud (AWS, Azure, GCP)** (cân nhắc)
- CI/CD : Docker, Jenkins, Grafana, ...

# TIẾN ĐỘ

| Tuần | Công Việc                                                                                       |
| ---- | ----------------------------------------------------------------------------------------------- |
| 9    | Hoàn thiện tất cả Diagram + Thiết kế hệ thống (API, Service, etc...)</br> **Fe code giao diện** |
| 10   | **Fe :** Final </br> **Be:** Code các service theo **Document**                                 |
| 11   | Core-code                                                                                       |
| 12   | Core-code                                                                                       |
| 13   | Core-code + Integrate + Containerize + Test                                                     |

### Họp 18/10
- Activity diagram -> Hỏi lại thầy chia làm nhiều module hay 1 
- Sequence diagram -> Thêm database, active line?
- Class diagram -> Check lại
- Push hết những cái diagram lên github.
