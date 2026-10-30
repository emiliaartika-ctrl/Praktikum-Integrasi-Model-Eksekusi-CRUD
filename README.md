## 8. Logbook Pengujian & Integritas Kode

Berikut adalah matriks penelusuran pengujian (*Traceability Matrix*) untuk aplikasi Master Data Buku Perpustakaan:

| ID Uji | Fitur / Operasi | Target Endpoint URL | HTTP Method | Skenario Pengujian | Hasil yang Diharapkan | Status | Bukti Tangkapan Layar |
| :--- | :--- | :--- | :---: | :--- | :--- | :---: | :--- |
| **TC-01** | Koneksi Pool | `App Startup` | - | Server dijalankan pertama kali | Terhubung ke MySQL Pool tanpa error | Pass | https://drive.google.com/drive/folders/1HJY6RKWoiQ_eRKIU-SpuNP6ISoeHd1uR?usp=sharing |
| **TC-02** | Read (All) | `/buku` | GET | Akses halaman daftar buku | Menampilkan seluruh record tabel MySQL ke antarmuka EJS | Pass | https://drive.google.com/drive/folders/1HJY6RKWoiQ_eRKIU-SpuNP6ISoeHd1uR?usp=sharing |
| **TC-03** | Create | `/buku/tambah` | POST | Submit formulir buku baru | Data tersimpan di DB, DevTools mencatat 302 Redirect ke `/buku` | Pass | https://drive.google.com/drive/folders/1HJY6RKWoiQ_eRKIU-SpuNP6ISoeHd1uR?usp=sharing |
| **TC-04** | Update | `/buku/edit/:id` | POST | Mengubah data & stok buku | Nilai kolom pada baris MySQL berubah sesuai input baru | Pass | https://drive.google.com/drive/folders/1HJY6RKWoiQ_eRKIU-SpuNP6ISoeHd1uR?usp=sharing |
| **TC-05** | Delete | `/buku/hapus/:id` | POST | Eksekusi tombol hapus buku | Baris record terhapus dari MySQL dan UI ter-refresh | Pass | https://drive.google.com/drive/folders/1HJY6RKWoiQ_eRKIU-SpuNP6ISoeHd1uR?usp=sharing |
| **TC-06** | Keamanan | `/buku` | GET | Input `' OR '1'='1` via URL / form | Prepared Statement memperlakukan input sebagai literal string (No Injection) | Pass | https://drive.google.com/drive/folders/1HJY6RKWoiQ_eRKIU-SpuNP6ISoeHd1uR?usp=sharing |
