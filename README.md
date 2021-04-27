# RajaOngkir CodeIgniter
Merupakan library CodeIgniter untuk mengkonsumsi API dari [RajaOngkir](http://rajaongkir.com). Library ini dapat digunakan untuk semua tipe Akun (**starter, basic** maupun **pro**), dengan penggunaan dan batasan sesuai yang terdapat di [Dokumentasi Rajaongkir](http://rajaongkir.com/dokumentasi) .

## Note!

Repo ini merupakan modifikasi dari [cahyadsn/rajaongkir_ci](https://github.com/cahyadsn/rajaongkir_ci) dengan sedikit perubahan :
- Case sensitif penamaan file dan class di CodeIgniter 3
- variable originType pada file endpoint.php


## Instalasi
Copy file sesuai dengan lokasinya masing-masing.
## Konfigurasi
Buka "**application/config/rajaongkir.php**" dan masukkan API key di sana.
## Contoh Penggunaan
### Memuat library
```php
$this->load->library('rajaongkir');
```
### Melakukan request
```php
//Mendapatkan nama semua propinsi
$provinces = $this->rajaongkir->province();

//Mendapatkan nama semua kota
$cities = $this->rajaongkir->city();

//Mendapatkan data ongkos kirim dari kota Jakarta Barat (151) ke kabupaten Gianyar (128) seberat 1000 gram 
//dengan kurir pengiriman 'jne'
$cost = $this->rajaongkir->cost(151, 128, 1000, "jne");
```
### Response
Response yang dihasilkan berupa string JSON balasan dari RajaOngkir.
### Dokumentasi lebih lanjut
Silakan lihat code di dalam library, di dalamnya terdapat komentar yang dapat membantu Anda.
### Referensi
[Dokumentasi RajaOngkir](http://rajaongkir.com/dokumentasi)
