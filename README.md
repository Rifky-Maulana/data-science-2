# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

### Latar Belakang Bisnis

Jaya Jaya Institut adalah institusi pendidikan tinggi yang telah beroperasi sejak tahun 2000 dan telah menghasilkan banyak lulusan berkualitas. Meskipun institusi ini memiliki reputasi yang baik, mereka menghadapi masalah serius berupa tingginya tingkat *dropout* (siswa yang tidak menyelesaikan pendidikan).

Fenomena ini tidak hanya berdampak buruk pada citra institusi, tetapi juga pada efektivitas sistem pembelajaran serta kepercayaan calon mahasiswa dan orang tua. Oleh karena itu, penting bagi pihak manajemen untuk memahami dan mendeteksi lebih awal siswa-siswa yang berisiko tinggi mengalami *dropout*, sehingga dapat dilakukan intervensi tepat waktu untuk mencegahnya.

## Permasalahan Bisnis

Permasalahan utama yang ingin diselesaikan oleh Jaya Jaya Institut adalah:

1. **Tingginya tingkat dropout siswa** yang berdampak pada reputasi dan performa institusi.
2. **Kurangnya sistem deteksi dini** untuk mengidentifikasi siswa yang berisiko mengalami dropout.
3. **Keterbatasan informasi visual dan real-time** untuk memonitor performa siswa dan mengambil keputusan cepat.
4. **Minimnya alat bantu bagi pihak manajemen dan staf akademik** untuk memahami faktor-faktor yang mempengaruhi dropout.

## Cakupan Proyek

Proyek ini memiliki beberapa ruang lingkup utama yang akan dikerjakan, yaitu:

1. **Eksplorasi dan Analisis Data**

   * Menganalisis dataset performa siswa yang telah disediakan oleh Jaya Jaya Institut.
   * Mengidentifikasi pola dan faktor-faktor penting yang berkontribusi terhadap risiko dropout.

2. **Pembuatan Model Prediktif**

   * Mengembangkan model machine learning untuk memprediksi kemungkinan seorang siswa akan dropout.
   * Menggunakan teknik klasifikasi dan evaluasi performa model untuk memilih model terbaik.

3. **Pembuatan Dashboard Interaktif**

   * Merancang dashboard interaktif yang memvisualisasikan performa siswa dan prediksi risiko dropout.
   * Memberikan insight yang mudah dipahami bagi staf dan manajemen kampus.

4. **Dokumentasi dan Rekomendasi**

   * Menyusun laporan akhir yang berisi hasil analisis, performa model, serta rekomendasi intervensi yang bisa dilakukan berdasarkan hasil prediksi.

## Persiapan

### Sumber Data
Dataset yang digunakan dalam proyek ini adalah **Students' Performance** yang tersedia secara publik melalui repositori GitHub Dicoding:

📂 [Students' Performance Dataset - Dicoding](https://github.com/dicodingacademy/dicoding_dataset/blob/main/students_performance/data.csv)

### Setup Environment

Untuk menjalankan notebook dan aplikasi dashboard, ikuti langkah-langkah berikut:

1. **Clone repositori ini** (jika belum):
    ```bash
    git clone https://github.com/username/repo-anda.git
    cd repo-anda
    ```

2. **Buat dan aktifkan virtual environment** menggunakan pipenv:
    ```bash
    pip install pipenv
    pipenv install
    pipenv shell
    ```

    > Atau jika menggunakan `requirements.txt`, jalankan:
    ```bash
    python -m venv venv
    
    source venv/bin/activate  # untuk Linux/macOS
    
    venv\\Scripts\\activate   # untuk Windows

    pip install -r requirements.txt
    ```

3. **Dengan Conda**
      - Buat environment baru dengan Conda
      
      Jalankan perintah berikut untuk membuat environment baru bernama dropout-prediction menggunakan Python 3.9.15 <br>
      ```
      conda create -n dropout-prediction python=3.9.15
      ```
      
      - Aktifkan environment yang telah dibuat
      
      Setelah environment berhasil dibuat, aktifkan environment tersebut dengan perintah berikut<br>
      
      ```
      conda activate dropout-prediction
      ```
      
      - Install dependencies
      
      Setelah environment aktif, install semua dependensi yang diperlukan untuk menjalankan aplikasi dan model prediksi dropout. Anda dapat menggunakan file `requirements.txt` yang sudah disediakan dalam proyek        ini <br>
      
      ```
      pip install -r requirements.txt
      ```

5. **Jalankan Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```

6. **(Opsional) Jalankan Streamlit dashboard**:
    ```bash
    cd streamlit_dashboard
    streamlit run app.py
    ```

---


## Business Dashboard - Education Overview

### 📘 Deskripsi
Dashboard ini dibuat menggunakan **Metabase** (versi lokal) untuk memvisualisasikan data mahasiswa secara menyeluruh. Fokus utama dashboard adalah memberikan wawasan terkait status pendidikan, demografi, status sosial ekonomi, dan distribusi mahasiswa.
![image](https://github.com/user-attachments/assets/02c8d28e-dce9-41cd-a05c-120dc553b8b1)

![image](https://github.com/user-attachments/assets/d7acf156-208d-4dc1-ab6b-59fe8a7cbb0e)

---

Business dashboard telah dikembangkan menggunakan teknologi web modern dengan fitur-fitur komprehensif untuk monitoring attrition analysis. Dashboard ini dapat diakses dengan kredensial berikut:
Akses Dashboard:
```
URL: http://localhost:3000 atau http://localhost:3001 
Username: root@mail.com
Password: root123
```

### 📊 Ringkasan Utama

| Keterangan           | Nilai     |
|----------------------|-----------|
| Total Mahasiswa      | 4.424     |
| Total Drop Out       | 1.421     |
| Rate Drop Out        | 32.12%    |
| Graduated Student    | 2.209     |
| Student Active       | 794       |

---

### 📌 Statistik Dasar Mahasiswa

- **Jumlah Pria**: 1.556
- **Jumlah Wanita**: 2.868
- **Rata-rata Usia Masuk**: 23.27 tahun
- **Rata-rata Nilai Masuk**: 126.98
- **Jumlah Penerima Beasiswa**: 1.099

---

### 🧩 Status Pendidikan Mahasiswa (Grouped by Status)

- **Graduate**: 49.9%
- **Dropout**: 32.1%
- **Enrolled (Aktif)**: 17.9%

---

### 💍 Distribusi Status Pernikahan Mahasiswa

- **Single**: mayoritas
- **Married, Divorced, Widowed**: minoritas

---

### 💰 Analisis Status Ekonomi (Debtor)

#### Status Hutang vs Jumlah Mahasiswa:
- **Tidak Memiliki Hutang**: 3.921 (88.6%)
- **Memiliki Hutang**: 503 (11.4%)

#### Rata-rata Nilai Masuk:
- **Tanpa Hutang**: 127.05
- **Dengan Hutang**: 126.4

#### Status Hutang vs Penerima Beasiswa:
- Mayoritas penerima beasiswa berasal dari mahasiswa **tanpa hutang**.

---

### 🌍 Mahasiswa Internasional

- **Mahasiswa Lokal**: 97.51%
- **Mahasiswa Internasional**: 2.49%

---

### 🎂 Distribusi Umur Mahasiswa

- **< 20 tahun**: paling banyak
- **20–25 tahun**: signifikan
- **26–35+ tahun**: relatif sedikit

---

### 🛠 Teknologi yang Digunakan

- **Metabase (Localhost)**
- **Visualisasi Pie Chart, Bar Chart, Donut Chart, dan Summary Cards**

---


## Menjalankan Sistem Machine Learning

Prototype sistem machine learning telah dikembangkan menggunakan **Streamlit** dan dapat dijalankan secara **online** maupun **lokal**.

### 🔗 Akses Online (Prototype)
Klik link berikut untuk mencoba prototype yang telah dideploy:

🌐 [Akses Prototype di Streamlit Cloud](https://data-science-2-nkw2bgsiiank6wtotz6odp.streamlit.app/)

---
Langkah menjalankan di lokal:
```
streamlit streamlit_dashboard.py
```

File penting:

1. `streamlit_dashboard.py`: untuk input prediksi.
2. `best_model.pkl`: Model machine learning terlatih.
3. `class_names.pkl`: Urutan fitur untuk input model.
4. `scaler.pkl`: Skaler fitur untuk preprocessing data.

## Conclusion

Proyek ini berhasil menunjukkan potensi besar penerapan machine learning dalam menangani permasalahan kompleks seperti prediksi dropout mahasiswa di Jaya Jaya Institut. Dataset yang digunakan sangat kaya, terdiri dari 4424 entri dengan puluhan fitur penting yang mencakup berbagai aspek kehidupan mahasiswa — mulai dari status sosial ekonomi, latar belakang pendidikan orang tua, hingga performa akademik mahasiswa pada semester pertama dan kedua. Semua data bersifat lengkap (non-null), sehingga mendukung proses eksplorasi data dan pelatihan model secara optimal.

Model prediktif yang dibangun pada proyek ini tidak hanya memanfaatkan variabel sederhana seperti **Gender**, **Age_at_enrollment**, dan **Tuition_fees_up_to_date**, tetapi juga menggali wawasan dari variabel yang lebih kompleks dan informatif, seperti jumlah **Curricular_units** yang diambil, **lulus**, atau **gagal di semester awal**, nilai **Admission_grade**, serta apakah mahasiswa merupakan **Debtor**, **Scholarship_holder**, atau **Displaced**. Selain itu, fitur latar belakang seperti **Mothers_qualification**, **Fathers_occupation**, dan vEducational_special_needs** juga ikut dimasukkan ke dalam analisis. Bahkan, variabel makro seperti **Unemployment_rate**, **Inflation_rate**, dan **GDP** menunjukkan bahwa kondisi ekonomi global juga turut dipertimbangkan sebagai faktor pendukung risiko dropout.

Hasil analisis mengungkapkan bahwa mahasiswa yang memiliki utang (Debtor), tidak memperoleh beasiswa (Scholarship_holder = 0), nilai masuk rendah (Admission_grade rendah), serta menunjukkan performa akademik yang buruk pada semester pertama dan kedua (misalnya jumlah mata kuliah tidak diselesaikan atau nilai Curricular_units_1st/2nd_sem_grade yang rendah) cenderung memiliki risiko dropout yang lebih tinggi. Selain itu, usia masuk yang lebih tua (Age_at_enrollment), status perkawinan tertentu (Marital_status), serta tidak adanya keterlibatan dengan kurikulum (misalnya Curricular_units_without_evaluations) juga berkontribusi terhadap peningkatan risiko.

Dengan menggunakan model seperti **Logistic Regression**, **Random Forest**, dan **Gradient Boosting**, sistem ini mampu menghasilkan prediksi dengan akurasi dan interpretabilitas yang baik. Random Forest dan Gradient Boosting menunjukkan keunggulan dari sisi performa, sementara Logistic Regression tetap relevan karena transparan dan mudah dijelaskan kepada pemangku kepentingan non-teknis. Evaluasi menyeluruh menggunakan cross-validation dan berbagai metrik seperti accuracy, AUC, dan confusion matrix menunjukkan bahwa sistem memiliki generalisasi yang baik dan dapat diandalkan.

Lebih dari sekadar prediksi, sistem ini dapat digunakan sebagai alat early warning system oleh Jaya Jaya Institut. Dengan adanya model ini, pihak kampus dapat mengidentifikasi mahasiswa berisiko tinggi secara proaktif dan mengambil tindakan intervensi seperti bimbingan akademik, bantuan keuangan, atau dukungan psikososial. Selain itu, proyek ini membuka peluang untuk integrasi lebih lanjut dalam bentuk dashboard analitik interaktif yang menampilkan data visual mahasiswa berisiko dropout secara real-time.

## Rekomendasi Action Items

Berdasarkan analisis data serta insight dari dashboard *Jaya Jaya Institut Student Dropout Monitoring*, berikut adalah sejumlah rekomendasi strategis yang dapat diterapkan untuk menurunkan tingkat mahasiswa dropout dan meningkatkan retensi pendidikan:

1. **Penguatan Program Beasiswa dan Dukungan Finansial**  
   - Perluasan akses beasiswa bagi mahasiswa dari latar belakang ekonomi rendah.  
   - Fokus bantuan kepada mahasiswa yang terdeteksi memiliki risiko tinggi untuk dropout, khususnya yang tidak memperoleh beasiswa dan berasal dari keluarga dengan kondisi ekonomi lemah (misalnya orang tua tidak bekerja).

2. **Penerapan Intervensi Akademik Sejak Awal**  
   - Lakukan pemantauan akademik intensif pada semester awal (semester 1 dan 2).  
   - Mahasiswa dengan nilai akademik awal yang rendah perlu diarahkan ke program bimbingan, mentoring, atau kelas remedial secara proaktif.

3. **Perbaikan Proses Seleksi Masuk**  
   - Tinjau ulang kriteria penerimaan mahasiswa baru berdasarkan korelasi dengan keberhasilan studi.  
   - Implementasikan sistem prediksi risiko dropout sebagai salah satu indikator dalam proses seleksi.

4. **Peningkatan Peran Orang Tua dan Dukungan Sosial**  
   - Bangun komunikasi yang intensif dengan orang tua, terutama bagi mahasiswa dari keluarga yang kurang stabil secara ekonomi.  
   - Sediakan layanan konseling sosial dan psikologis untuk mahasiswa yang mengalami tekanan dari faktor lingkungan atau personal.

5. **Fleksibilitas dalam Skema Pembayaran Kuliah**  
   - Kembangkan sistem pembayaran uang kuliah yang lebih fleksibel dan bersahabat.  
   - Siapkan dana bantuan darurat bagi mahasiswa yang mengalami kesulitan finansial mendadak agar tetap dapat melanjutkan studi.

6. **Pemantauan Keterlibatan dan Kesejahteraan Mahasiswa**  
   - Terapkan sistem pelaporan berkala (mingguan/bulanan) melalui platform digital untuk memantau aktivitas dan keterlibatan mahasiswa.  
   - Gunakan sistem peringatan dini (early warning system) berbasis data untuk mendeteksi potensi dropout dan melakukan intervensi tepat waktu.

Dengan melaksanakan langkah-langkah di atas secara terstruktur dan berbasis data, institusi dapat secara aktif mencegah dropout dan menciptakan ekosistem pendidikan yang lebih inklusif dan suportif.
