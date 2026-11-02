# AIMS-mini – Use case

```mermaid
flowchart LR
    KH([Khách hàng])
    KH --> UC1((Thêm đĩa vào giỏ))
    KH --> UC2((Xóa đĩa khỏi giỏ))
    KH --> UC3((Xem giỏ hàng & tổng tiền))
    KH --> UC4((Tìm đĩa theo tiêu đề))
```

| Use case | Mô tả | Hiện thực |
|---|---|---|
| Thêm đĩa | Thêm DVD, tối đa 20 đĩa | `Cart.add_dvd` |
| Xóa đĩa | Xóa DVD khỏi giỏ | `Cart.remove_dvd` |
| Xem giỏ | In danh sách và tổng tiền | `Cart.print_cart`, `Cart.total_cost` |
| Tìm theo tiêu đề | Lọc đĩa theo từ khóa | `search_by_title` |
