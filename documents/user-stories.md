# User Stories — Cryptowetrics
## Nền tảng Phân tích Dữ liệu Crypto & DeFi

> **Vai trò:** Business Analyst · CD Group · 2022

---

## Actor

| Actor | Mô tả |
|---|---|
| **Investor** | Nhà đầu tư cá nhân theo dõi fund/project |
| **Analyst** | Chuyên viên phân tích thị trường Crypto |
| **Fund Manager** | Quản lý quỹ đầu tư Crypto/VC |

---

## Module 1 — Dashboard (CWT.001)

**US-001**
> As an **Investor**,  
> I want to **xem tổng quan thị trường Crypto ngay khi đăng nhập**,  
> So that **tôi nắm được tình hình chung trước khi ra quyết định đầu tư**.

**Tiêu chí chấp nhận:**
- Hiển thị số lượng Crypto Hedge Funds, Venture Capital Funds, Total Funds
- Hiển thị Fund of the Day kèm ROI
- Biểu đồ Total Funding Amount theo tháng (Jan–Dec)
- Bộ lọc thời gian 1D/1W/1M/1Y hoạt động đồng bộ trên tất cả chart

---

**US-002**
> As an **Analyst**,  
> I want to **xem phân bổ thị trường theo category (Top Categories by Market Cap)**,  
> So that **tôi xác định được lĩnh vực nào đang chiếm ưu thế để định hướng nghiên cứu**.

**Tiêu chí chấp nhận:**
- Donut chart hiển thị: Lending 55% · Metaverse 15% · Gaming 25% · NFT 20.5% · DAO 9.5%...
- Bộ lọc 1D/1W/1M/1Y cập nhật chart real-time
- Click vào từng category → filter danh sách fund tương ứng

---

**US-003**
> As an **Investor**,  
> I want to **xem bản đồ phân bổ quỹ theo quốc gia (Funds by Country)**,  
> So that **tôi hiểu được nguồn vốn đang tập trung ở đâu trên thế giới**.

**Tiêu chí chấp nhận:**
- Heatmap thế giới với 4 mức màu theo số lượng fund
- Hover vào quốc gia → tooltip hiển thị số fund cụ thể
- Filter: 12 tháng gần nhất

---

**US-004**
> As an **Analyst**,  
> I want to **xem lịch sử Dominance của các fund lớn**,  
> So that **tôi theo dõi được sự thay đổi vị thế của các quỹ theo thời gian**.

**Tiêu chí chấp nhận:**
- Bảng Dominance History: Fund · Total · Date · Project
- Hiển thị màu xanh (tăng) / đỏ (giảm) cho từng dòng
- Nút "View all" dẫn đến trang chi tiết

---

## Module 2 — Funds (CWT.002)

**US-005**
> As an **Investor**,  
> I want to **xem danh sách toàn bộ quỹ đầu tư Crypto có thể lọc theo nhiều tiêu chí**,  
> So that **tôi tìm được quỹ phù hợp với khẩu vị rủi ro và chiến lược của mình**.

**Tiêu chí chấp nhận:**
- Bảng hiển thị: Fund Name · MarketCap · Volume · AUM · Investor Type · Investments
- Bộ lọc: AUM range · Investor Type (Foundation/Corporate/Angel/DAO/Fund) · Projects · All times
- Thanh tìm kiếm theo tên fund
- Phân trang "View all"

---

**US-006**
> As an **Analyst**,  
> I want to **xem top Gainers và Losers trong 24h**,  
> So that **tôi theo dõi được fund nào đang biến động mạnh nhất để phân tích nguyên nhân**.

**Tiêu chí chấp nhận:**
- Hiển thị top 3 Gainers với % tăng màu xanh
- Hiển thị top 3 Losers với % giảm màu đỏ
- Cập nhật theo khung giờ 24h

---

**US-007**
> As an **Investor**,  
> I want to **đánh dấu fund vào Watchlist cá nhân**,  
> So that **tôi theo dõi nhanh các quỹ quan tâm mà không cần tìm kiếm lại**.

**Tiêu chí chấp nhận:**
- Icon ⭐ trên mỗi dòng fund — click để thêm/bỏ Watchlist
- Watchlist lưu theo tài khoản người dùng
- Menu Watchlist trên sidebar hiển thị danh sách đã đánh dấu

---

**US-008**
> As an **Analyst**,  
> I want to **xem Hot News liên quan đến các fund**,  
> So that **tôi cập nhật được thông tin mới nhất ảnh hưởng đến thị trường**.

**Tiêu chí chấp nhận:**
- Carousel 4 tin tức với ảnh thumbnail · tiêu đề · mô tả ngắn · ngày đăng
- Click vào tin → mở link bài viết gốc
- Tự động cập nhật tin mới

---

## Module 3 — Fund Detail (CWT.002.1)

**US-009**
> As an **Fund Manager**,  
> I want to **xem chi tiết portfolio và các vòng đầu tư của một quỹ cụ thể**,  
> So that **tôi đánh giá được chiến lược và hiệu quả đầu tư của quỹ đó**.

**Tiêu chí chấp nhận:**
- Hiển thị profile đầy đủ: tên · mô tả · năm thành lập · địa điểm · rating · social links
- Biểu đồ Market Overview theo 1D/1W/1M/1Y
- KPI: Total Funding Amount · Funding Rounds · Total Investors
- Bảng Funding Rounds: Project · Price · MarketCap · Raise · Blockchain · Total Locked % · Category

---

**US-010**
> As an **Analyst**,  
> I want to **xem Twitter feed của quỹ ngay trong trang detail**,  
> So that **tôi nắm được hoạt động truyền thông gần nhất của quỹ mà không cần mở tab khác**.

**Tiêu chí chấp nhận:**
- Embed Twitter feed của quỹ (real-time)
- Nút "Follow on Twitter" dẫn đến profile Twitter
- Hiển thị tối thiểu 5 tweet gần nhất

---

## Module 4 — Projects (CWT.003)

**US-011**
> As an **Investor**,  
> I want to **xem danh sách project Crypto với bộ lọc đa chiều**,  
> So that **tôi tìm được project phù hợp để nghiên cứu đầu tư**.

**Tiêu chí chấp nhận:**
- Bảng: Project · Price · MarketCap · Raised · Blockchain · Total Locked % · Funding · Category
- Bộ lọc: Token/Funding Rounds tab · Planet · Blockchain · Category · All times
- Thanh tìm kiếm theo tên project

---

**US-012**
> As an **Analyst**,  
> I want to **xem countdown đến sự kiện IDO/TGE/Launch tiếp theo**,  
> So that **tôi không bỏ lỡ cơ hội tham gia các đợt mở bán quan trọng**.

**Tiêu chí chấp nhận:**
- Countdown real-time: Days · Hours · Minutes · Seconds
- Hiển thị tên sự kiện và tên project
- Cập nhật tự động khi sự kiện kết thúc → chuyển sang sự kiện tiếp theo

---

## Module 5 — Project Detail (CWT.003.1)

**US-013**
> As an **Investor**,  
> I want to **xem chi tiết tokenomics và vesting schedule của một project**,  
> So that **tôi đánh giá được rủi ro bán tháo (dump) token khi các vòng unlock**.

**Tiêu chí chấp nhận:**
- Donut chart Token Allocation: Marketing · Staking · Ecosystem · Team · Advisor · Exchange Liquidity · Pre-sale
- Bảng Vesting Schedule dạng Gantt: Round · Token% · Price · Return x · TGE · Cliff · timeline bars
- Countdown "Next Event Unlock" đến lần mở khóa tiếp theo
- Distribution Timeline hiển thị tiến độ phân phối tổng thể

---

**US-014**
> As an **Analyst**,  
> I want to **xem Key Metrics của project (MarketCap, 24h Volume, ATL)**,  
> So that **tôi có đủ dữ liệu định lượng để so sánh và đánh giá project**.

**Tiêu chí chấp nhận:**
- Market Cap · 24h Volume · All-time low hiển thị nổi bật
- Biểu đồ giá chi tiết với khung thời gian nhỏ (2h/7days/30days)
- Cập nhật real-time hoặc tần suất < 1 phút

---

**US-015**
> As an **Fund Manager**,  
> I want to **xem danh sách quỹ đã đầu tư vào project này**,  
> So that **tôi đánh giá được mức độ tin cậy và backing của project từ các tổ chức lớn**.

**Tiêu chí chấp nhận:**
- Bảng Funds List: Fund Name · MarketCap · Volume · AUM · Investor Type · Investments
- Bộ lọc AUM · Investor Type · Projects · All times
- Click vào fund → dẫn đến trang Fund Detail tương ứng

---

## Chức năng ngang (Cross-cutting)

**US-016 — Connect Wallet**
> As an **Investor**,  
> I want to **kết nối ví Web3 (MetaMask...)**,  
> So that **hệ thống cá nhân hóa dữ liệu theo portfolio thực tế của tôi**.

**US-017 — Watchlist**
> As an **Investor**,  
> I want to **quản lý danh sách fund/project yêu thích tập trung một chỗ**,  
> So that **tôi theo dõi nhanh mà không cần tìm kiếm lại mỗi lần**.

**US-018 — Global Search**
> As an **Analyst**,  
> I want to **tìm kiếm fund hoặc project từ bất kỳ trang nào**,  
> So that **tôi truy cập nhanh thông tin cần thiết mà không phải điều hướng thủ công**.

**US-019 — Dark/Light Mode**
> As an **User**,  
> I want to **chuyển đổi giữa Dark mode và Light mode**,  
> So that **tôi sử dụng thoải mái trong các điều kiện ánh sáng khác nhau**.
