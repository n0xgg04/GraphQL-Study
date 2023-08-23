## GraphQL

------------------------------

#### So sánh với RestfulAPI

| Nội dung | GraphQL                                                                                                                   | RestfulAPI                                                                                           |
|---------:|---------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Cấu trúc | Có thể tuỳ biến những nội dung cần thiết để sử dụng, giới hạn/ lấy thêm tài nguyên, tránh được việc lấy thừa, thiếu thông tin | Bắt buộc client phải sử dụng cấu trúc cố định, không có khả năng tuỳ biến loại tài nguyên khi yêu cầu |
| endpoint | Một endpoint duy nhất                                                                                                     | Nhiều endpoint dạng URL để tuỳ chỉnh thông tin                                                       |
| Hiệu quả | Với graphQL, front-end và back-end có thể hoạt động độc lập                                                               | Khó hoạt động độc lập                                                                                |
| HttpCode | Luôn trả 200, nếu có error cần parse và kiểm tra trong JSON                                                               | Đa dạng                                                                                              |

---------------
### Query
Truy vấn dữ liệu

```js
query getProducts {
  products {
    name
    price
  }
}
```

Tương đương GET trong RestfulAPI

### Mutation
Thay đổi dữ liệu

```js
mutation addProduct {
      addProduct(name: "Product 1", price: 100) {
        name
        price
          }
        }  
```

Tương đương POST, PUT, DELETE trong RestfulAPI

### Subscription
Lắng nghe sự kiện, cập nhật realtime

```js
subscription {
      productAdded {
        name
        price
          }
        }  
```

Tương đương Websocket trong RestfulAPI
