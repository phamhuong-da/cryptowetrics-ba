# Tài liệu Yêu cầu Sản phẩm — Cryptowetrics
## Nền tảng Phân tích Dữ liệu Crypto & DeFi

> **Vai trò:** Business Analyst  
> **Công ty:** CD Group · 2022  
> **Figma UI:** [Xem thiết kế →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3)

---

## 1. Tổng quan sản phẩm

Cryptowetrics là nền tảng phân tích dữ liệu Crypto & DeFi dành cho trader,
nhà đầu tư và quỹ đầu tư — cung cấp insight tổng hợp về thị trường, theo dõi
fund/project, phân tích vesting schedule và hành vi đầu tư theo thời gian thực.

**Người dùng mục tiêu:**

| Nhóm | Nhu cầu chính |
|---|---|
| Trader cá nhân | Theo dõi giá, volume, market cap theo thời gian thực |
| Nhà đầu tư quỹ | Phân tích fund performance, ROI, dominance history |
| Analyst | Nghiên cứu project, vesting schedule, token allocation |
| Quỹ đầu tư (VC/Hedge) | Theo dõi danh mục, so sánh fund theo AUM và investor type |

---

## 2. Kiến trúc sản phẩm — 4 Module chính
Cryptowetrics

## 3. Đặc tả chức năng từng module

---

### CWT.001 — Dashboard

**Mục đích:** Trang tổng quan cung cấp cái nhìn toàn cảnh thị trường Crypto,
hiệu suất các quỹ và phân bổ theo category.

**Các thành phần chính:**

| Component | Mô tả | Metric hiển thị |
|---|---|---|
| KPI Cards | Số lượng quỹ theo loại | Crypto Hedge Funds · Venture Capital · Total Funds |
| Fund of the Day | Quỹ nổi bật trong ngày | Tên quỹ · ROI · Top performers |
| Top Categories by Market Cap | Phân bổ thị trường theo danh mục | Lending 55% · Metaverse 15% · Gaming 25% · NFT 20.5%... |
| Total Funding Amount | Biểu đồ cột theo tháng | Tổng vốn đầu tư theo thời gian (Jan–Dec) |
| Funding KPIs | Chỉ số tổng hợp | Total Funding: $1,042,177,729,398 · TFA Change: -1.24%/tháng · Total Rounds: 4,219 |
| Funds by Country | Bản đồ nhiệt thế giới | Phân bổ quỹ theo quốc gia (200 trở xuống / 200–300 / 300–400 / 400+) |
| Top Ecosystem | Biểu đồ tròn | BTC 55% · ETH 20.5% · ADA 15% · Others 9.5% |
| Dominance History | Bảng lịch sử | Fund · Total · Date · Project |

**Business Rules:**
- Bộ lọc thời gian: 1D · 1W · 1M · 1Y áp dụng cho tất cả chart
- Nút "Connect Wallet" tích hợp Web3 wallet
- Dark/Light mode toggle

---

### CWT.002 — Funds

**Mục đích:** Danh sách và phân tích toàn bộ quỹ đầu tư Crypto trên thị trường.

**Các thành phần chính:**

| Component | Mô tả |
|---|---|
| Market Overview Chart | Biểu đồ area chart theo thời gian — Market Cap tổng |
| Market KPIs | MarketCap · Change 24h · Altcoin Research Dominance |
| Hot News | Carousel tin tức nổi bật liên quan đến các fund |
| Gainers / Losers | Top fund tăng/giảm mạnh nhất trong 24h |
| ICO ROI / ATH ROI | Bảng so sánh ROI từ ICO và ATH |
| Fund List Table | Danh sách đầy đủ với filter |

**Fund List — Cấu trúc bảng:**

| Cột | Kiểu dữ liệu | Mô tả |
|---|---|---|
| Watchlist | Icon | Đánh dấu theo dõi cá nhân |
| Fund Name | Text + Logo | Tên quỹ và logo |
| MarketCap | Currency | Tổng vốn hóa |
| Volume | Currency | Khối lượng giao dịch |
| AUM | Range | Tài sản quản lý (100M–250M...) |
| Investor Type | Dropdown | Foundation · Corporate · Angel · DAO · Fund |
| Investments | Avatar group | Danh sách dự án đã đầu tư |

**Bộ lọc (Filter):**
- AUM range
- Investor Type: Foundation · Corporate · Angel Investor · DAO · Fund
- Projects
- All times

---

### CWT.002.1 — Fund Detail (Token View)

**Mục đích:** Trang chi tiết của từng quỹ — phân tích sâu portfolio và
danh sách project đã đầu tư.

**Các thành phần chính:**

| Component | Mô tả |
|---|---|
| Fund Profile | Tên · Mô tả · Year · Location · Rating · Social links |
| Twitter Feed | Embed feed Twitter của quỹ |
| Market Overview Chart | Biểu đồ giá theo thời gian (1D/1W/1M/1Y) |
| Fund KPIs | Total Funding Amount · Funding Rounds · Total Investors |
| Portfolio Breakdown | Mô tả chiến lược đầu tư và phân bổ danh mục |
| Investment Categories | Donut chart phân bổ theo category (DeFi · Gaming · NFT...) |
| Funding Rounds Table | Chi tiết các vòng gọi vốn đã tham gia |

**Funding Rounds Table — cấu trúc:**

| Cột | Mô tả |
|---|---|
| Project | Tên project và logo |
| Price | Giá tại thời điểm đầu tư |
| MarketCap | Vốn hóa hiện tại |
| Raise | Số tiền gọi vốn |
| Blockchain | Nền tảng blockchain |
| Total Locked % | % token bị lock |
| Funding | Vòng gọi vốn (Seed/Private/Public) |
| Category | Phân loại (Gaming · Data Management...) |
| Public Investing | Trạng thái đầu tư công khai |

---

### CWT.003 — Projects

**Mục đích:** Danh sách toàn bộ project Crypto/DeFi — lọc và theo dõi
theo nhiều tiêu chí.

**Các thành phần chính:**

| Component | Mô tả |
|---|---|
| Hot Projects | Top project theo ICO ROI và ATH ROI |
| New Projects | Project mới nhất được thêm vào hệ thống |
| Upcoming Event | Countdown đến sự kiện tiếp theo (IDO/TGE/Launch) |
| Project Table | Danh sách đầy đủ với bộ lọc đa chiều |

**Project Table — cấu trúc:**

| Cột | Mô tả |
|---|---|
| Project | Tên + Logo |
| Price | Giá hiện tại |
| MarketCap | Vốn hóa |
| Raised | Tổng vốn gọi được |
| Blockchain | Ethereum · BSC · Solana... |
| Total Locked % | % token đang bị khóa với progress bar |
| Funding | Investor logos |
| Category | Gaming · Data Management · DeFi... |
| Public Investing | Label trạng thái mở đầu tư |

**Bộ lọc:**
- Token / Funding Rounds tab
- Projects · Planet · Blockchain · Category · All times

---

### CWT.003.1 — Project Detail

**Mục đích:** Trang phân tích sâu từng project — đặc biệt quan trọng
cho nhà đầu tư cần hiểu tokenomics và vesting.

**Các thành phần chính:**

| Component | Mô tả |
|---|---|
| Project Profile | Tên · Ticker · Blockchain · Year · Location · Rating · Social |
| Twitter Feed | Embed feed Twitter của project |
| Market Overview Chart | Biểu đồ giá chi tiết theo khung thời gian nhỏ (2h/7days/30days) |
| Key Metrics | Market Cap · 24h Volume · All-time low |
| Next Event Unlock | Countdown đến lần mở khóa token tiếp theo |
| Token Allocation | Donut chart phân bổ token: Marketing 55% · Staking 10% · Ecosystem 5% · Team 20%... |
| Vesting Schedule | Bảng Gantt chart chi tiết theo từng round |
| Distribution Timeline | Timeline thanh ngang hiển thị tiến độ phân phối |
| Funds List | Danh sách quỹ đã đầu tư vào project này |

**Vesting Schedule — cấu trúc bảng:**

| Cột | Mô tả |
|---|---|
| Round | Loại vòng (Seed · Private Sale 1 · Private Sale 2 · Strategic · Public) |
| Token % | Tỉ lệ token phân bổ cho round |
| Price | Giá token tại round |
| Return x | Hệ số lợi nhuận so với giá hiện tại |
| TGE | % unlock tại Token Generation Event |
| Cliff | Thời gian khóa cứng trước khi unlock |
| Gantt bar | Biểu đồ trực quan lịch trình unlock theo tháng |

---

## 4. Yêu cầu chung toàn hệ thống

### Chức năng ngang (Cross-cutting)

| Chức năng | Mô tả |
|---|---|
| Watchlist | Người dùng đánh dấu fund/project yêu thích — icon ⭐ trên mọi bảng |
| Connect Wallet | Tích hợp Web3 wallet (MetaMask...) để cá nhân hóa trải nghiệm |
| Search | Thanh tìm kiếm toàn cục — tìm fund, project, token |
| Dark/Light mode | Toggle chế độ hiển thị |
| Notification | Chuông thông báo sự kiện (IDO, TGE, unlock...) |
| Time filter | 1D · 1W · 1M · 1Y áp dụng đồng bộ trên chart |
| Support | Module hỗ trợ người dùng |
| Settings | Cài đặt tài khoản và hiển thị |

### Yêu cầu phi chức năng

| Tiêu chí | Yêu cầu |
|---|---|
| Hiệu suất | Cập nhật dữ liệu thị trường real-time hoặc < 1 phút |
| Dữ liệu | Tích hợp API nguồn: CoinGecko / CoinMarketCap / on-chain data |
| Bảo mật | Xác thực Web3 wallet · Mã hóa dữ liệu người dùng |
| Giao diện | Responsive · Hỗ trợ Dark mode |
| Mở rộng | Thêm blockchain mới · Thêm loại quỹ |

---

## 5. Metric system — Chuẩn hóa định nghĩa

| Metric | Định nghĩa | Đơn vị |
|---|---|---|
| MarketCap | Giá hiện tại × Tổng cung lưu hành | USD |
| AUM | Tổng tài sản đang quản lý của quỹ | USD |
| Total Locked % | % token chưa được unlock / Tổng cung | % |
| ROI (ICO) | (Giá hiện tại - Giá ICO) / Giá ICO | % hoặc x |
| ROI (ATH) | (Giá ATH - Giá ICO) / Giá ICO | x |
| TFA Change | Thay đổi tổng vốn đầu tư so với tháng trước | % |
| Dominance | % vốn hóa của một tài sản / Tổng thị trường | % |
| 24h Change | Thay đổi giá trong 24 giờ gần nhất | % |

---

## 6. Figma UI Reference

| Màn hình | Mã | Link |
|---|---|---|
| Dashboard | CWT.001 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
| Funds | CWT.002 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
| Fund Detail | CWT.002.1 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
| Projects | CWT.003 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
| Project Detail | CWT.003.1 | [Xem →](https://www.figma.com/design/6IrCK5h1L8S98na1e6Liai/Cryptowetrics-2?node-id=1-3) |
