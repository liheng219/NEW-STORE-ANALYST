
# Retail Sales Performance Dashboard

## Overview
Dự án phân tích hiệu suất doanh thu bán lẻ của công ty Vanarsdel giai đoạn 2012–2019 nhằm:
Theo dõi xu hướng tăng trưởng doanh thu
Đánh giá hiệu suất theo quốc gia và phân khúc
Phân tích đóng góp doanh thu (Contribution %)
So sánh doanh thu năm hiện tại với năm trước (YoY Growth)
Mô phỏng tác động của Sales Discount

---

# Dataset

## Tables Used

| Table | Description |
|-------|------------|
| Sales | Transaction-level sales data |
| Product | Product categories & segmentation |
| Geography | Country and region information |
| DateDimension | Calendar table for time intelligence (creating from Sales[Date]) |

---
## Key Metrics (DAX)
RevenueAll = CALCULATE([TotalRevenue], all(Sales))

PreveousYearRevenue = CALCULATE([TotalRevenue], DATEADD(DateDimension[Date], -1, YEAR))

%Growth = DIVIDE([TotalRevenue]-[PreveousYearRevenue],[PreveousYearRevenue])

GTRevenue = DIVIDE([TotalRevenue], [RevenueAll])

## Dashboard Structure
### Overview Page
Revenue & Growth by Year

Revenue by Country (Map)

Units by Category

Region & Year slicers

### Performance Page

KPI summary cards

Revenue vs Amount comparison

Sales Discount What-if parameter

### Profit & Contribution Page

Revenue by Category & Segment

Contribution %

Previous Year comparison

## Business Insights
### Revenue & Growth: 
Doanh thu tăng trưởng ổn định từ 2012 đến 2019, đạt gần 0.5 tỷ USD vào năm 2019.
Tuy nhiên, tốc độ tăng trưởng có xu hướng giảm dần theo thời gian (từ ~27% xuống ~7–10%), cho thấy doanh nghiệp đang bước vào giai đoạn bão hòa — quy mô mở rộng nhưng động lực tăng trưởng chậm lại.
Phân khúc Urban đóng góp khoảng 80% tổng doanh thu, cho thấy sự phụ thuộc lớn vào thị trường đô thị.
Điều này tạo ra rủi ro nếu thị trường Urban bão hòa hoặc cạnh tranh gia tăng.

### Growth Opportunity Segments:
Các phân khúc Youth và Mix - Có tốc độ tăng trưởng cao (>24%) nhưng tỷ trọng doanh thu còn thấp (<2%).
Đây là nhóm tiềm năng để đa dạng hóa nguồn doanh thu

## Full files: 
[FILE .PBIX, DATASETS](https://drive.google.com/drive/folders/1A5F8P8bjoEcsNYOFlgpkeog6vbh1WyVB)


