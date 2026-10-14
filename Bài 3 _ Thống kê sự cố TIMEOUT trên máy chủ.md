Phần 1: Phân tích  
\[Tìm & Đọc các tệp log (ls \-r)\] ──\> \[Lọc từ khóa "TIMEOUT"\] ──\> \[Loại trừ "NOT TIMEOUT"\] ──\> \[Đếm tổng số đối tượng (.Count)\]  
Phần 2: Triển khai  
(ls \-r \-Filter "\*.log" | Get-Content | Select-String "TIMEOUT" | Where-Object { \$\_ \-notmatch "NOT TIMEOUT" }).Count