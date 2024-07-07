# Deploy Private Registry

Có nhiều lựa chọn Triển khai Registry khác nhau, nhưng ở đây mình chỉ soạn lại Documents với:

- Docker Registry: v2.0
- Harbor: v2.11.0

Nó sẽ tương ứng với 2 thư mục trong Repos này.
Branch Main là những update mới nhất cho projects
Các Branch khác sẽ phù hợp các version hay trên hệ thống khác nhau.

### Thông tin phần cứng tôi triển khai cho cả hai loại là:

```
CPU: 4
Ram: 8Gb
Disk: 125
```

Lưu ý: Đây không phải là cấu hình tối thiểu.

### OS

OS: `Ubuntu 22.04.2 LTS` bản Optimized shortened version
Nginx: `v.1.24.0`
Registry: `v.2.0`

- Note: Tuy nhiên đây không phải cấu hình tối thiểu để setup cho 2 App này.

### Note:

Tôi setup thêm Docker Registry hay Harbor vào một network system đã có từ trước. Ở đây là nginx. Và Documents là tham khảo và edit lại từ một số nguồn trên internet.
Bởi vậy nên sẽ có một số config chưa tối ưu hoàn toàn, ví dụ:

- Harbor: Trong tài liệu setup dựng Harbor có sẵn nginx được setup config kèm theo là nguyên bộ. SSL dùng là OpenSSL.
  Trong khi network system tôi đã có sẵn nginx và dùng certbot --nginx để general SSL cho các domain.
- Docker Private Registry: Các tài liệu trên Internet sẽ hướng dẫn là setup Docker Registry + Nginx hoặc proxy tương tự trên cùng Host. Trong tài liệu của tôi chỉ setup Docker Registry và tận dụng nginx đã dựng sẵn để sử dụng.

Bạn có thể góp ý hoặc nêu vấn đề cho tôi bằng cách tạo các Issue. Tôi sẽ xem và thử tìm cách giải quyết.

**Trân trọng**
