# Insyst Backend Test - Product & Transaction Management API

RESTful API untuk manajemen produk dan transaksi pembelian menggunakan Laravel 11.

## Deskripsi

API ini dibuat sebagai bagian dari technical assessment Insyst untuk posisi Backend Developer Intern. API menyediakan endpoint CRUD untuk produk dan transaksi dengan validasi stok otomatis.

## Fitur

- CRUD Products (Create, Read, Update, Delete)
- Soft Delete untuk products dan transactions
- Validasi input di setiap endpoint
- POST Transactions dengan validasi stok
- Perhitungan total harga otomatis
- Pengurangan stok otomatis setelah transaksi berhasil
- Relasi foreign key antara products dan transactions
- Response JSON di semua endpoint

## Tech Stack

- Laravel 11
- MySQL 8.4.3
- Eloquent ORM
- RESTful API Architecture

## Cara Instalasi

1. Clone repository
```bash
git clone https://github.com/YabesEdward/insyst-backend-test.git
cd insyst-backend-test
```

2. Install dependencies
```bash
composer install
```

3. Copy file `.env.example` ke `.env`
```bash
cp .env.example .env
```

4. Generate application key
```bash
php artisan key:generate
```

5. Setup database di `.env`
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=insyst_backend
DB_USERNAME=root
DB_PASSWORD=
```

6. Buat database `insyst_backend` di MySQL

7. Jalankan migration
```bash
php artisan migrate
```

8. Jalankan server
```bash
php artisan serve
```

Server akan berjalan di `http://localhost:8000`

## API Endpoints

### Products

- `GET /api/products` - Ambil semua produk
- `POST /api/products` - Tambah produk baru
- `PUT /api/products/{id}` - Update produk
- `DELETE /api/products/{id}` - Hapus produk (soft delete)

### Transactions

- `POST /api/transactions` - Buat transaksi pembelian

## Testing

Testing dilakukan menggunakan Postman. Collection dan dokumentasi lengkap tersedia di file PDF.

## Dokumentasi

Dokumentasi lengkap dengan screenshot dan penjelasan struktur kode tersedia di file `YabesEdwardSihombing_BackendTest.pdf`.

## Author

Yabes Edward Sihombing  
November 2025
