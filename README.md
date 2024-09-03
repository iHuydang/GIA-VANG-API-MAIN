# Tác giả

API này được phát triển bởi **Huy Dang Tran**.

# Giá Vàng/Đô La Mỹ API

API này cung cấp dữ liệu giá vàng theo cặp XAU/USD (vàng/đô la Mỹ) theo thời gian thực và lịch sử. Đây là công cụ hữu ích cho các nhà đầu tư, phân tích tài chính, hoặc bất kỳ ai cần truy cập nhanh chóng và chính xác vào thông tin giá vàng.

## Tính năng

- **Dữ liệu giá theo thời gian thực**: Cập nhật liên tục giá vàng theo cặp XAU/USD.
- **Dữ liệu lịch sử**: Truy xuất thông tin giá vàng từ các ngày trước đó.
- **Độ chính xác cao**: Giá vàng được lấy từ các nguồn đáng tin cậy và được cập nhật liên tục.
- **Dễ sử dụng**: Giao diện API đơn giản, dễ tích hợp vào các ứng dụng và dịch vụ web.

## Cách sử dụng

### 1. Yêu cầu giá theo thời gian thực

Để lấy giá vàng hiện tại theo cặp XAU/USD:

```bash
GET /api/v1/xauusd/price
```

**Phản hồi:**

```json
{
  "symbol": "XAUUSD",
  "price": 1805.25,
  "timestamp": "2024-09-03T12:34:56Z"
}
```

### 2. Yêu cầu dữ liệu lịch sử

Để lấy dữ liệu giá vàng XAU/USD từ ngày cụ thể:

```bash
GET /api/v1/xauusd/history?date=2024-09-01
```

**Phản hồi:**

```json
{
  "symbol": "XAUUSD",
  "date": "2024-09-01",
  "open": 1795.50,
  "high": 1810.75,
  "low": 1785.25,
  "close": 1802.00
}
```

## Tham số API

| Tham số       | Loại       | Mô tả                                                     |
| ------------- | ---------- | --------------------------------------------------------- |
| `symbol`      | `string`   | Cặp tiền tệ, ví dụ: `XAUUSD`                              |
| `price`       | `float`    | Giá hiện tại của vàng theo USD                            |
| `timestamp`   | `string`   | Thời gian lấy dữ liệu theo định dạng ISO 8601             |
| `date`        | `string`   | Ngày muốn truy xuất dữ liệu lịch sử (định dạng `YYYY-MM-DD`) |
| `open`        | `float`    | Giá mở cửa của vàng trong ngày                            |
| `high`        | `float`    | Giá cao nhất của vàng trong ngày                          |
| `low`         | `float`    | Giá thấp nhất của vàng trong ngày                         |
| `close`       | `float`    | Giá đóng cửa của vàng trong ngày                          |

## Cài đặt

### 1. Yêu cầu hệ thống

- Python 3.x hoặc Node.js
- Thư viện HTTP (requests, axios, v.v.)

### 2. Cài đặt

Clone repo này về máy:

```bash
git clone https://github.com/iHuydang/GIA-VANG-API-MAIN/new.git
cd xauusd-price-api
```

Cài đặt các phụ thuộc:

```bash
pip install -r requirements.txt
```

### 3. Chạy API

Chạy server:

```bash
python app.py
```

API sẽ hoạt động tại `http://localhost:5000`.

## Giấy phép

API này được phát hành dưới [MIT License](LICENSE). Bạn có thể sử dụng tự do cho các dự án cá nhân và thương mại.

## Đóng góp

Chúng tôi hoan nghênh các đóng góp từ cộng đồng. Hãy fork dự án, tạo pull request, hoặc mở issue để chúng tôi có thể cải thiện API này tốt hơn.

## Tác giả

API này được phát triển bởi **Huy Dang Tran**.

## Liên hệ

Nếu bạn có bất kỳ câu hỏi hoặc yêu cầu hỗ trợ, vui lòng liên hệ qua email: [huydanginvest@gmail.com](mailto:huydanginvest@gmail.com).
``
