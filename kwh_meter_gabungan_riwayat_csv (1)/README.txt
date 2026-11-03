KWH METER - PROGRAM GABUNGAN

Paket ini mempertahankan website asli dari kwh_meter.zip (Dashboard, Real-time Data,
Riwayat Data, Energy, Pengaturan, Tentang), lalu menambahkan penyimpanan riwayat
di browser (IndexedDB) dan tombol Unduh CSV pada halaman Riwayat Data.

FILE:
- kwh_meter.ino
- data/index.html
- data/real-time.html
- data/riwayat.html
- data/energy.html
- data/pengaturan.html
- data/tentang.html
- data/style.css
- data/script.js

CARA PASANG:
1. Ekstrak ZIP.
2. Buka kwh_meter.ino dengan Arduino IDE.
3. Program menggunakan SSID/password dari file program yang dikirim. Ubah bila perlu.
4. Upload sketch ke ESP32.
5. Upload seluruh isi folder data/ ke LittleFS (bukan folder .git).
6. Buka Serial Monitor 115200 baud, catat IP ESP32.
7. Buka http://IP-ESP32/ di perangkat yang tersambung ke Wi-Fi yang sama.
8. Buka menu Riwayat Data, lalu tekan Unduh CSV.

CATATAN:
- Program .ino tetap menggunakan data simulasi/random; belum terhubung ke PZEM-004T.
- Riwayat disimpan di browser saat browser menerima data WebSocket. Data tidak direkam
  ketika browser tertutup atau terputus dari ESP32.
- IndexedDB tersimpan pada browser/perangkat yang sama, bukan otomatis di ESP32.
- Library yang diperlukan: WebSockets by Markus Sattler dan ArduinoJson versi yang
  mendukung JsonDocument (ArduinoJson 7).
- File HTML/CSS/JS di-upload ke LittleFS; jangan meng-upload mklittlefs.bin.
