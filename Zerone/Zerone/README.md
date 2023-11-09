# Nhóm 14
## 
Môn Xây dựng HTTT trên các framework - IS220.M11
Lớp thực hành .2

[![N|Solid](https://media.discordapp.net/attachments/871665355108520006/926860577740046416/Logo_UIT_updated.jpg?width=300&height=300)](https://nodesource.com/products/nsolid)

# Tên đồ án: Xây dựng website bán đồ công nghệ
  website sẽ thực hiện việc mua và bán các sản phẩm công nghệ như laptop, điện thoại,...Ở mỗi sản phẩm có thể xem các cấu hình chi tiết và các thông tin liên quan đến sản phẩm
  và nếu người dùng đăng nhập thì có thể để lại đánh giá. Ở trang Admin có chức năng thống kê để kiểm tra số liệu và các hoạt động của website.
 
## Thành viên nhóm

| Tên thành viên | MSSV | Facebook | SDT | Nhiệm vụ | Đánh giá |
| ------ | ------ | ------ | ------ | ------ | ------ |
| Đặng Phúc Toàn | 19522357 | https://www.facebook.com/phuctoanz | 0329 487 988 | làm những thứ còn lại | 100% |
| Nguyễn Đình Trải| 19522371 | https://www.facebook.com/19522371k14 | 0376 101 877 | giao diện người dùng | 100% |
| Nguyễn Ngọc Thiện | 19522264 | https://www.facebook.com/n.ngocthie.n0203 | 0877 581 945 | appchat | 100% |
| Đinh Công Thành | 19522221  | https://www.facebook.com/dinh.cong.thanh.1108 | 0936 117 465 | excel, data | 100% |

  
# Chức năng

#### Chung

- Đăng nhập/ đăng ký/ đăng xuất/ logout / nhớ mật khẩu

- Phân quyền (admin, staff, customer)

- Gửi mail để xác nhận đăng nhập và reset mật khẩu 

- Chi tiết sản phẩm (được lọc theo phiên bản và màu sắc của sản phẩm)

- GỢi ý các sản phẩm tương tự (Comming soon....)

#### Thành viên

- Giỏ hàng

- Thanh toán (tiền mặt/ VNpay) (chưa có ship và khuyến mãi)

- Đánh giá sản phẩm

- Phản hồi đánh giá của khách hàng khác (chức năng đang phát triển)

- Chat online với admin (chức năng đang bảo trì)

- Đơn hàng đã mua, theo dõi tình trạng đơn hàng

- Quản lý thông tin cá nhân (đóng tài khoản, cập nhật mật khẩu, xác thực 2 lớp, backup dữ liệu cá nhân, liên kết tài khoản với google và facebook)

#### Admin

- Danh mục sản phẩm, sản phẩm

- Tổng quan bán hàng, thống kê thu chi

- Quản lý nhân sự

- Quản lý hàng hóa

- Quản lý bán hàng 

- Quản lý mua hàng

- Quản lý kho, số lượng hàng hóa trong kho

- Duyệt bình luận

## Tech

- [C#] 
- [.Net 6.0] 
- [ASP.Net Core MVC]
- [Bootstrap] 
- [Identity]
- [SignalR]  (chức năng chat đang bị lỗi nên đã gỡ quyền truy cập nhưng vẫn còn trong project)
- [Thư viện kèm theo]

## Hướng dẫn cài đặt    

- website sử dụng: 
> IDE: [Visual Studio 2022]
Database: [SQLServer]

File database trong thư mục Data-> Database_Design (bản hiện tại: version 6.1 được cập nhật vào ngày 6/12)

Dữ liệu được lưu dưới dạng .sql trong thư mục Data -> Script 

- B1: clone web từ github: bật terminal, powercell, cmnd.... và chạy câu lệnh sau

```sh
    git clone https://github.com/Toan-Dang/framework_IS220.M11_14.git
```


- B2: Chạy file backup_database.sql trong data -> Script trên sqlserver

- B3: chỉnh lại đường dẫn ở appsettings.js: 
  đổi serve là Server của người dùng, và database là tên database đã tạo trong file .sql ở trên 


``` 
 "ConnectionStrings": {
    "DefaultConnection": "Server = <tên server>; Database = <tên database>  ; Trusted_Connection=True;MultipleActiveResultSets=True"
  }
```
#### ví dụ: 
![alt server](https://media.discordapp.net/attachments/871665355108520006/926858688097058846/unknown.png)
và 
![alt database](https://media.discordapp.net/attachments/871665355108520006/926859024337600542/unknown.png)

thì đổi chuỗi ConnectionStrings thành : 

``` 
 "ConnectionStrings": {
    "DefaultConnection": "Server = TOANDANG\\TOANDANG; Database = website ; Trusted_Connection=True;MultipleActiveResultSets=True"
},
```
- B4: Chạy project bằng cách ấn ctrl + f5 trong [Visual Studio 2022]

![alt success](https://media.discordapp.net/attachments/871665355108520006/926859983654621194/unknown.png?width=1191&height=670
)

## License

MIT

**Readme by [Toan Dang]**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

 [C#]: <https://docs.microsoft.com/vi-vn/dotnet/csharp/>
 [.Net 6.0]: <https://dotnet.microsoft.com/en-us/download/dotnet/6.0>
 [ASP.Net Core MVC]: <https://docs.microsoft.com/vi-vn/aspnet/core/tutorials/first-mvc-app/start-mvc?view=aspnetcore-2.1&tabs=visual-studio>
 [Bootstrap]: <https://getbootstrap.com/>
[Toan Dang]: <https://github.com/Toan-Dang>
 [Visual Studio 2022]: <https://visualstudio.microsoft.com/downloads/>
 [SQLServer]: <https://www.microsoft.com/en-us/sql-server/sql-server-downloads>
 [SignalR]: <https://dotnet.microsoft.com/en-us/apps/aspnet/signalr>
 [Identity]: <https://docs.microsoft.com/en-us/aspnet/core/security/authentication/identity?view=aspnetcore-6.0&tabs=visual-studio>
 [Thư viện kèm theo]: <https://github.com/Toan-Dang/framework_IS220.M11_14/network/dependencies>