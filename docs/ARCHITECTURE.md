# Arsitektur Tingkat Tinggi

Sistem menggunakan pola MVC pada aplikasi web berbasis CodeIgniter 4. Browser
berinteraksi dengan antarmuka aplikasi dan lapisan API, lalu request diteruskan
ke controller untuk menjalankan aturan bisnis melalui model serta layanan
database.

```text
Browser / API Client
        |
        v
Application Layer
  - Authentication & role-based access
  - POS, inventory, transaction, reporting
  - REST API integration
        |
        v
Business Logic & Data Access
  - Controllers
  - Models
  - Database transactions and row locking
        |
        v
      MySQL
```

## Modul utama

- **Authentication:** membatasi akses berdasarkan peran owner, admin, dan
  cashier.
- **Inventory:** mengelola produk, kategori, pergerakan stok, dan Reorder Point.
- **Point of Sale:** mengelola keranjang, checkout, invoice, dan pembaruan stok.
- **Reporting:** menyajikan ringkasan transaksi serta laporan yang dapat
  diekspor.
- **API:** menyediakan kapabilitas integrasi untuk data produk, transaksi,
  inventori, dan dashboard.

Detail implementasi, endpoint, konfigurasi deployment, dan skema database tidak
disertakan dalam repository showcase ini.
