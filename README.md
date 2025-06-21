# MinionLab Bot

Bot tự động hóa cho MinionLab với các chức năng đa dạng bao gồm buff referral, treo node, và quản lý ví Solana.

## 📁 Cấu trúc thư mục

```
MinionLab/
├── config.json          # Cấu hình tool
├── imei_map.json        # File hệ thống (không cần chỉnh sửa)
├── start.bat            # File chạy bot
├── proxies.txt          # Danh sách proxies (ip:port:user:pass)
├── solanaWallets.txt    # Danh sách ví Solana (Address|Base58 PrivateKey)
└── tokens.txt           # Token để chạy các chức năng
```

## ⚙️ Cấu hình

Chỉnh sửa file `config.json`:

```json
{
    "waitTime": 86400,           // Thời gian chờ sau mỗi lần chạy xong (giây)
    "numberThread": 1,           // Số luồng chạy
    "checkProxy": true,          // Kiểm tra proxies live
    "refCode": "iweKIaCY",       // Mã referral MinionLab
    "password": "Tunzankies123@" // Password MinionLab
}
```

## 🚀 Các chức năng chính

### 1. Buff Referral
- **Mô tả**: Tạo tài khoản và buff referral vô hạn
- **Khuyến nghị**: Chạy từ 10-20 luồng để hiệu quả tối đa
- **Kết quả**: 
  - Lưu thông tin tài khoản vào `accounts.xlsx`
  - Token được lưu vào `tokens.txt` để sử dụng cho các chức năng khác

### 2. Treo Node
- **Mô tả**: Treo extension node
- **Mục đích**: Duy trì hoạt động node

### 3. Get Token
- **Mô tả**: Chế độ lấy lại token
- **Sử dụng**: Khi token bị mất hoặc cần refresh

### 4. Liên kết ví Solana
- **Mô tả**: Liên kết ví mạng Solana
- **Lưu ý**: Số ví phải bằng số token (số ví = số tài khoản cần liên kết)
- **Định dạng**: `Address|Base58 PrivateKey`

## 📋 Menu chức năng

```
╔═══════════════════════════════════════════════╗
║              MENU CHỨC NĂNG                   ║
╠═══════════════════════════════════════════════╣
║  [1] Buff Reff                                ║
║  [2] Treo Node                                ║
║  [3] Get token                                ║
║  [4] Liên kết ví sol                          ║
║  [5] Thoát                                    ║
╚═══════════════════════════════════════════════╝
```

## 📝 Định dạng file

### proxies.txt
```
ip:port:user:pass
```

### solanaWallets.txt
```
Address|Base58 PrivateKey
```

### accounts.xlsx (tự động tạo)
| email | password | refCode |
|-------|----------|---------|
| rpu3ol@punkproof.com | Tunzankies123@ | NAtarhNp |

## 🔧 Hướng dẫn sử dụng

1. **Chuẩn bị**:
   - Cấu hình `config.json` với thông tin của bạn
   - Thêm proxies vào `proxies.txt` (nếu cần)
   - Thêm ví Solana vào `solanaWallets.txt` (nếu cần)

2. **Chạy bot**:
   - Chạy lệnh sau : npm i ts-curl-impersonate và npm i keytar
   - Chạy: Start.bat

3. **Chọn chức năng**:
   - Nhập số tương ứng với chức năng mong muốn
   - Làm theo hướng dẫn trên màn hình

## ⚠️ Lưu ý quan trọng

- Token được lưu vào `tokens.txt` và **không bị mất** khi chạy các chức năng khác
- Số ví Solana phải bằng số token để liên kết thành công
- Khuyến nghị chạy Buff Referral với 10-20 luồng để tối ưu hiệu suất

## 📞 Hỗ trợ

Nếu cần hỗ trợ, liên hệ qua Telegram: [@tunankies](https://t.me/tunankies)

---
