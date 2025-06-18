🧠 Repositori Pembelajaran Robotik - Catatan Perkuliahan

Halo dan selamat datang! Repositori ini disusun sebagai wadah dokumentasi dan rekam jejak perjalanan belajar saya di bidang *robotics*. Di dalamnya terdapat berbagai file kode, log eksperimen, hingga catatan refleksi selama mengikuti mata kuliah ini.

## Week 1
### 🔍 Pengenalan Mata Kuliah & Dosen
Di minggu pertama, kegiatan diawali dengan sesi perkenalan bersama dosen pengampu, Pak Basuki. Selain itu, kami juga mulai diperkenalkan pada ruang lingkup mata kuliah ini, termasuk sistem penilaian, rencana pembelajaran, serta gambaran umum tentang topik yang akan dipelajari seperti UTS dan UAS berbasis proyek.

## Week 2
### 🛠️ Instalasi Arduino IDE
Pertemuan kedua difokuskan pada persiapan teknis, khususnya instalasi *Arduino IDE* sebagai alat utama untuk pemrograman mikrokontroler. Selain memasang software, kami juga diminta menginstal beberapa pustaka penting dan menyesuaikan pengaturan agar sesuai dengan kebutuhan project ke depan.

## Week 3
### 💡 Eksperimen LED Dengan ITCLab
Pada minggu ketiga, kami mulai praktik langsung menggunakan fasilitas ITCLab. Materi berpusat pada pengoperasian pin digital pada Arduino. Kami mencoba program sederhana untuk menyalakan dan mematikan LED, serta memahami bagaimana proses unggah kode dari IDE ke perangkat.

## Week 4
### ⚙️ Simulasi Gerakan Mesin
Pertemuan keempat kami menggunakan IMCLab untuk menjalankan kode yang telah disiapkan oleh dosen. Eksperimen kali ini melibatkan aktivasi sebuah mesin yang memutar roda gigi. Roda tersebut awalnya berputar cepat, lalu secara bertahap melambat hingga berhenti — simulasi ini bertujuan memperkenalkan prinsip kontrol kecepatan.

## Week 5
### 🔄 Kendali Motor via PWM
Pada minggu kelima, kami melanjutkan praktik dengan IMCLab, kali ini untuk mengontrol motor. Fokus pembelajaran adalah pada penggunaan sinyal PWM (Pulse Width Modulation) untuk mengatur kecepatan motor lewat perintah dalam Arduino IDE.

## Week 6
### 🌐 Dasar IoT & Setup MQTT
Pertemuan keenam memperkenalkan konsep *Internet of Things (IoT)*. Kami diminta untuk mengunduh aplikasi MQTT Panel di smartphone. Dengan menggunakan library *PubSubClient*, kami mencoba membuat komunikasi antara Arduino dan jaringan internet. Koneksi dilakukan melalui hotspot pribadi, dan konfigurasi kredensial disisipkan langsung ke dalam kode program.

## Week 7
### 🤖 Remote Robot BNU V2 via MQTT
Minggu ketujuh adalah tahap penerapan nyata IoT. Kami mengirimkan instruksi ke robot BNU V2 lewat aplikasi MQTT Panel. Perintah tersebut dieksekusi secara real-time oleh robot. Latihan ini memperkuat pemahaman kami terkait komunikasi berbasis protokol MQTT dalam sistem robotik.

---

## 🎯 Final Project: Lock-Target Robot Using YOLO and ESP32

Proyek akhir ini merupakan implementasi sistem pelacakan objek secara otomatis berbasis visi komputer dan mikrokontroler. Sistem ini dirancang untuk mengenali objek tertentu dalam video secara real-time, mengunci satu target, dan mengendalikan arah gerak robot menuju target tersebut.

### 🔧 Komponen Utama:
- **Model Deteksi Objek:** Menggunakan YOLOv8 untuk mengenali objek melalui kamera secara langsung.
- **Tracking System:** DeepSort digunakan untuk melacak posisi objek yang telah dikenali dan menjaga fokus pada satu target (locked target).
- **ESP32 & Motor Driver:** ESP32 menerima perintah arah (maju, kiri, kanan) dari komputer berdasarkan posisi target, lalu mengendalikan dua motor melalui pin PWM.

### 🧪 Mekanisme Kerja:
1. Kamera menangkap video dan diproses oleh model YOLO.
2. Objek yang terdeteksi dilacak menggunakan DeepSort dan dipilih satu target untuk dikunci.
3. Posisi target dianalisis untuk menentukan apakah robot perlu belok kiri, kanan, atau maju.
4. Perintah dikirim melalui serial ke ESP32 yang menggerakkan motor sesuai instruksi tersebut.

### 🔗 Integrasi:
Proyek ini menggabungkan:
- Python (untuk deteksi dan pelacakan)
- Arduino C++ (untuk kontrol motor via ESP32)
- OpenCV + YOLOv8 + DeepSort
- Komunikasi serial antara PC dan ESP32

🎥 File video output dan log koordinat target juga disertakan sebagai bukti keberhasilan pelacakan.
👉 [Tonton di YouTube](https://drive.google.com/file/d/1SGGPJMIF_751zInjermGRN3qG_wzIuwl/view?usp=sharing)
