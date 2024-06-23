# TUGAS-IOT-14

Proses Berjalannya Simulasi dan Kode Program Arduino
1. Inisialisasi dan Setup
Library dan Deklarasi
Program dimulai dengan mengimpor library LiquidCrystal.h, yang digunakan untuk mengontrol layar LCD.
Pin-pin untuk komunikasi dengan LCD dan sensor suhu diinisialisasi.

Fungsi setup()
Fungsi setup() berjalan satu kali ketika Arduino pertama kali dihidupkan atau di-reset.
LCD diinisialisasi dengan ukuran 16 kolom dan 2 baris.
Pesan awal "CEK SUHU RUANGAN" dan "TUNGGU 1 DETIK" ditampilkan untuk memberi tahu pengguna bahwa sistem sedang mempersiapkan dirinya.
Program menunggu selama 1 detik sebelum membersihkan layar.

2. Loop Utama
Fungsi loop()
Fungsi loop() berjalan berulang-ulang selama Arduino menyala.
Setiap iterasi dari loop ini membaca nilai analog dari sensor suhu yang terhubung ke pin A0.
Nilai analog tersebut diubah menjadi suhu dalam derajat Celsius menggunakan rumus konversi yang sesuai.

Menampilkan Data pada LCD
Setelah suhu dihitung, kursor LCD diatur untuk menampilkan teks "SUHU RUANGAN:" pada baris pertama.
Kursor kemudian dipindahkan ke baris kedua untuk menampilkan nilai suhu yang diukur, diikuti oleh simbol derajat (°) dan huruf "C" untuk Celsius.

3. Penjelasan Proses Simulasi
Setup Awal

Saat simulasi dijalankan, program akan menginisialisasi LCD dan menampilkan pesan awal.
Pesan ini bertujuan untuk memberi tahu pengguna bahwa sistem sedang mempersiapkan dirinya.
Pembacaan Sensor

Arduino membaca data analog dari sensor suhu yang memberikan nilai tegangan yang sesuai dengan suhu yang diukur.
Nilai ini dikonversi menjadi derajat Celsius menggunakan formula (5.0 / 1024.0) * analogRead(sensor_Pin) * 100. Konstanta 5.0 adalah tegangan referensi Arduino, 1024.0 adalah resolusi ADC (Analog-to-Digital Converter) 10-bit, dan 100 adalah faktor konversi untuk sensor suhu yang digunakan.
Penampilan Data

Hasil konversi suhu kemudian ditampilkan pada LCD.
Simbol derajat (°) dan huruf "C" untuk Celsius ditambahkan untuk memberikan indikasi yang jelas tentang unit suhu yang diukur.
4. Loop Berulang
Fungsi loop() terus berjalan berulang-ulang, memastikan pembaruan data suhu secara real-time.
Ini memungkinkan pengguna untuk melihat perubahan suhu secara langsung pada LCD.
Dengan demikian, simulasi di Proteus akan menampilkan suhu yang diukur oleh sensor secara real-time pada layar LCD, memberikan visualisasi yang jelas dari pembacaan sensor yang dikendalikan oleh Arduino.
