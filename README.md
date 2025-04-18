## Getting Started
```js
fetch('https://example.com')  // Thay 'https://example.com' bằng URL bạn muốn tải
  .then(response => response.text())  // Chuyển đổi phản hồi thành văn bản
  .then(data => {
    console.log(data);  // In dữ liệu ra console
  })
  .catch(error => console.error('Có lỗi xảy ra:', error));  // Xử lý lỗi nếu có
```
