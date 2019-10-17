# React Native - Coding Challenge

Thông qua bài test, chúng tôi mong hiểu được một phần kiến thức, và kinh nghiệm của ứng viên trong việc giải quyết các vấn đề thường gặp đối với một Frontend developer. Bên dưới là các bước để hoàn thành bài test.


## Mô tả
#### 1. Thời lượng bài test và liên hệ

Thời lượng đặt ra cho bài test này nằm trong khoảng 1-2 ngày để hoàn thành hết tất cả các tính năng yêu cầu. Nếu ứng viên có câu hỏi hay gặp vấn đề gì thì có thể liên lạc tới email [INSERT_EMAIL_HERE] để được hỗ trợ


#### 2. Yêu cầu
|![tamboon-react-screenshot](https://lh3.googleusercontent.com/WlG3ipXMSukI40HCcnxXwHGGhsokqteqAAZNTCJAj0UQVO6Yj-fZN5mKCbt5vqUsudZVUl6I29H589VNUXjWjeftGUbWCJma5AMnO_69zLk-cGEKhcIDpIDaSm0QSNc4OB1mdASakbffBaHOQ7gWbbi-NAotNqRBht-eoFS9cmkcIiAuGwQV1atPDn75iWihAA7JnTmaUki1G7SMMWz-59dGT0KhMWhXicxjTQ79QoIVZ4RyvOk000YTWhi71nwRKH_arv_2r-__h1UZiQZXsieOjgCjk_VqzxFJzZPsA5lKd9Mkg_vehBPyDzRbsYt4LrssyCyND_UlaKSXsF6B8Vthoxv3Yw65_UIbsRSsWYBYCSPwRNU5xwvksLTZRWNDYg3E9vgOYgLBbEUmDS7IHrEPTkfGQQKpO-8-2OeijGofuB1D8ojFnkU8URe6JwQTlcu-5JqEAW7Pc1k0s4hKApAA6A9wrjBxED-gz48Lv3Jup3rF7i-Irf6QlV8nCymHnYyt1gz3gOAFUVR0iumEfJBMPLr01zeW0OH-JCvMeuz2WwKxFx29OHulT_sUng18Hsixd5GfsYcDkUPomiwPzXwc0X3MrsMkc7O6978L0PAUwJV02jkmSSUrxmYbPVIomsBc8Vz9jmjrOZc9y_XR-5rUxuoP0CO6mw1sHSGMRhIC-4IsPcxB-scLN_p2TeB2InDO49SMq_lKOFYf8ooCTPzRyj5UoHzpaEM1FJF82uZ8MX_B=w696-h1776-no)|
|---|
**Dưới đây là những tính năng cơ bản ứng viên sẽ phải hoàn thành:**

- [ ] Hoàn thành app theo design (image có đính kèm trong thư mục resources của repo này).
- [ ] Hiển thị tổng số tiền đã donate
- [ ] Hiển thị thông báo khi donate thành công
- [ ] Đảm bảo cho tính năng donate hoạt động tốt.
  - Database (`server/db.json`) phải được cập nhật mỗi khi donate thành công.
  - Users tháo app cài lại thì số tiền đã donate vẫn còn trên server mà không bị mất
- [ ] Viết code dễ đọc và code các component có thể sử dụng lại được
- [ ] Viết commit message đẩy đủ và sắp xếp thứ tự dễ hiểu
- [ ] Hiển thị tốt trên những thiết bị có tai thỏ như IPhone X, [Android với màn hình bị cutouts](https://developer.android.com/guide/topics/display-cutout).

#### 3. Chạy server

Clone repo này về:
```
$ cd server
$ npm install
$ npm run server # server được start ở port 3001
```

Server API được mock sử dụng thư viện [json-server](https://github.com/typicode/json-server), ứng viên sẽ sử dụng 2 endpoint dưới đây:

1. `GET /charities` - trả về JSON danh sách các chương trình từ thiện:

   ```json
   [
     { "id": 0, "name": "Ban Khru Noi", "logo_url": "http://rkdretailiq.com/news/img-corporate-baankrunoi.jpg" },
     { "id": 1, "name": "Habitat for Humanity Thailand", "logo_url": "http://www.adamandlianne.com/uploads/2/2/1/6/2216267/3231127.gif" },
     { "id": 2, "name": "Paper Ranger", "logo_url": "https://myfreezer.files.wordpress.com/2007/06/paperranger.jpg" },
     { "id": 3, "name": "Makhampom", "logo_url": "http://www.makhampom.net/makhampom/ppcms/uploads/UserFiles/Image/Thai/T14Publice/2554/January/Newyear/logoweb.jpg" }
   ]
   ```

2. `POST /donations` - Dùng để donate, chấp nhận JSON payload theo định dạng sau:

   ```json
   {
     "id":        0, // id của charities
     "currency":  "฿", // currency mặc định
     "amount":    10000 // số tiền muốn donate
   }
   ```

#### 4. Quy tắc

**Ứng viên hoàn toàn có thể:**
- Sửa design nhưng vẫn đảm bảo các tính năng cơ bản được hoàn thành
- Sử dụng bất cứ boilerplate nào ứng viên muốn

**Ứng viên không thể:**
- Thay đổi API server.
- Sử dụng ngôn ngữ khác ngoài JS.
- Sử dụng `AsyncStorage` để lưu thông tin donate

**Điểm cộng lớn nếu ứng viên:**
- Cải thiện design sao cho dễ sử dụng và đẹp hơn
- Sử dụng TypeScript
- Thêm animation
- Sử dụng Redux/MobX/Flux
- Sử dụng storybook để lưu trữ component
- Sắp xếp cấu trúc thư mục cụ thể hợp lý (nên ghi thêm vào `README.md` giải thích sao).
- Sửa `README.md` mô tả rõ hơn những gì ứng viên đã hoàn thành, cách để chạy và test app


**Note**: You can see design inside folder `resources`.

#### 5. Hình thức nộp bài
Gửi email cho chúng tôi tại [INSERT_EMAIL_HERE] bằng 1 trong 2 cách sau:
- Đẩy code lên 1 repository như `github`, `gitlab`, `bitbucket`,... sau đó gửi link

hoặc

- Zip hết source code và gửi file zip qua email attachment