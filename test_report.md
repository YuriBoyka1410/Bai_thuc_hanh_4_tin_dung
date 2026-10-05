# Test Report - EasyLoan Loan Eligibility Checker

## Mock Data (được sinh ra để bao phủ toàn bộ nhánh)

1. { isActive: false, age: 25, income: 15000000, creditScore: 700, hasBadDebt: false }
   - Kết quả: "Từ chối: Tài khoản đang bị khóa"

2. { isActive: true, age: 17, income: 15000000, creditScore: 700, hasBadDebt: false }
   - Kết quả: "Từ chối: Khách hàng chưa đủ tuổi"

3. { isActive: true, age: 25, income: 9000000, creditScore: 700, hasBadDebt: false }
   - Kết quả: "Từ chối: Thu nhập không đủ điều kiện"

4. { isActive: true, age: 25, income: 15000000, creditScore: 500, hasBadDebt: false }
   - Kết quả: "Từ chối: Điểm tín dụng quá thấp"

5. { isActive: true, age: 25, income: 15000000, creditScore: 700, hasBadDebt: true }
   - Kết quả: "Từ chối: Khách hàng đang có nợ xấu"

6. { isActive: true, age: 25, income: 15000000, creditScore: 700, hasBadDebt: false }
   - Kết quả: "Thành công: Đủ điều kiện vay vốn!"

## Kết luận

- Tất cả các nhánh Guard Clause hoạt động đúng.
- Không có lỗi logic, không còn if-else lồng nhau.
