# mysql001

## 1. KhachHang
### Columns:
- MaKH (Primary Key)
- Ho
- Ten 
- SoDT
- Email
- DiaChi
## 2. LoaiSanPham
### Columns:
- MaLoaiSP (Primary Key)
- TenLoaiSP
## 3. SanPham
### Columns:
- MaSP (Primary Key)
- TenSP
- Gia
- SoLuong
- GiaBan
- MoTa
- MaLoaiSP (Foreign Key referencing LoaiSanPham.MaLoaiSP)
### 4. HoaDon
## Columns:
- MaHoaDon (Primary Key)
- NgayMua
- MaKH (Foreign Key referencing KhachHang.MaKH)
## 5. HoaDon_SanPham (Contains)
### Columns:
- Composite Primary Key: MaHoaDon, MaSP
- SoLuong
- GiaBan
- MaHoaDon (Foreign Key referencing HoaDon.MaHoaDon)
- MaSP (Foreign Key referencing SanPham.MaSP)

## Relationships:
- One-to-Many between KhachHang and HoaDon (A customer can have many invoices).
- One-to-Many between LoaiSanPham and SanPham (A product category can contain many products).
- Many-to-Many between HoaDon and SanPham through HoaDon_SanPham.