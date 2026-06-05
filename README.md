# 📋 BA Documents — Cryptowetrics
### Nền tảng Phân tích Dữ liệu Crypto & DeFi

**Vai trò:** Business Analyst  
**Công ty:** CD Group  
**Thời gian:** 2022  
**Lĩnh vực:** Fintech · Crypto · DeFi · Trading

---

## 🎯 Bối cảnh & Vấn đề

Cryptowetrics là nền tảng phân tích dữ liệu Crypto & DeFi dành cho trader,
nhà đầu tư và quỹ đầu tư — nơi dữ liệu từ hàng nghìn fund và project được
tổng hợp, chuẩn hóa và trình bày thành insight có giá trị ra quyết định.

**Bài toán cần giải quyết:**
- Dữ liệu fund/project Crypto nằm rải rác ở nhiều nguồn, thiếu chuẩn hóa
- Nhà đầu tư thiếu công cụ phân tích tokenomics và vesting schedule chuyên sâu
- Không có nơi tổng hợp thông tin quỹ đầu tư (AUM, investor type, portfolio) một cách có hệ thống
- Khó theo dõi các sự kiện quan trọng (IDO, TGE, token unlock) theo thời gian thực

---

## 🔧 Vai trò BA — Những gì tôi đã làm

- Thu thập & làm rõ yêu cầu nghiệp vụ từ stakeholder (trader, analyst, fund manager)
- Phân tích và chuẩn hóa hệ thống **metric** (MarketCap, AUM, ROI, TVL, Dominance, Vesting...)
- Đặc tả **5 module chính** với đầy đủ luồng nghiệp vụ, business rules và tiêu chí chấp nhận
- Viết **19 User Stories** bao phủ toàn bộ chức năng từ Dashboard đến Project Detail
- Phối hợp với team thiết kế và dev để đảm bảo logic nghiệp vụ được implement đúng
- Định nghĩa cấu trúc dữ liệu cho từng bảng (Fund List, Funding Rounds, Vesting Schedule...)

---

## 🗂 Kiến trúc sản phẩ
---

## 📁 Tài liệu trong repo này

| File | Mô tả |
|---|---|
| [`documents/product-requirements.md`](documents/product-requirements.md) | Đặc tả đầy đủ 5 module · Business Rules · Metric System · Cấu trúc bảng dữ liệu |
| [`documents/user-stories.md`](documents/user-stories.md) | 19 User Stories · Tiêu chí chấp nhận · 3 actor types |

---

## 🔗 Figma UI

| Màn hình | Mã | Link |
|---|---|---|
| Dashboard | CWT.001 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
| Funds | CWT.002 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
| Fund Detail | CWT.002.1 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
| Projects | CWT.003 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
| Project Detail | CWT.003.1 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |

---

## 💡 Điểm nổi bật về mặt nghiệp vụ

**Chuẩn hóa metric phức tạp** — Định nghĩa rõ ràng 8 metric cốt lõi
(MarketCap, AUM, ROI ICO/ATH, Total Locked %, Dominance, TFA Change...)
đảm bảo tính nhất quán dữ liệu giữa các module và team.

**Đặc tả Vesting Schedule** — Phân tích và mô tả chi tiết cấu trúc bảng
Gantt chart cho vesting (Seed · Private · Strategic · Public) với các cột
Token% · Price · TGE · Cliff — phục vụ nhà đầu tư đánh giá rủi ro unlock.

**Hệ thống filter đa chiều** — Thiết kế logic bộ lọc cho Fund List và
Project List với nhiều chiều (AUM · Investor Type · Blockchain · Category ·
Time range) đảm bảo UX mượt mà và dữ liệu chính xác.

**Cross-cutting features** — Đặc tả các chức năng dùng chung toàn hệ thống:
Web3 Wallet Connect, Watchlist cá nhân, Global Search, Dark/Light mode,
Countdown real-time cho sự kiện IDO/TGE/Unlock.

---

## 🛠 Tools

`Notion` · `Figma` · `Draw.io` · `SQL`

---

*Tài liệu được viết dựa trên phân tích yêu cầu thực tế từ stakeholder.*
