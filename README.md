# Proyek Akhir: Menyelesaikan Permasalahan Jaya Jaya Institute
## Business Understanding
Jaya Jaya Institute adalah sebuah lembaga pendidikan tinggi yang telah berdiri sejak tahun 2000 dan berhasil menghasilkan banyak lulusan dengan reputasi yang sangat baik. Namun, terdapat sejumlah siswa yang tidak menyelesaikan pendidikan mereka atau mengalami dropout. Tingginya angka dropout ini menjadi tantangan besar bagi institusi pendidikan. Untuk mengatasi hal tersebut, Jaya Jaya Institut berupaya mendeteksi siswa yang berpotensi mengalami dropout lebih awal, sehingga dapat memberikan bimbingan khusus kepada mereka.
## Permasalahan Bisnis
Permasalahan utama yang dihadapi oleh Jaya Jaya Institut adalah tingginya jumlah mahasiswa yang melakukan dropout. Dropout mahasiswa mengakibatkan kerugian baik bagi institusi maupun mahasiswa tersebut secara pribadi. Bagi institusi, ini berarti kehilangan pendapatan dari mahasiswa yang tidak menyelesaikan pendidikan mereka, serta dapat merusak reputasi institusi. Sedangkan bagi mahasiswa, dropout dapat berdampak negatif pada masa depan mereka, termasuk kesempatan kerja dan penghasilan.
## Cakupan Proyek
Proyek ini berfokus pada analisis terkait faktor yang mempengaruhi mahasiswa dalam melakukan dropout. Pembuatan business dashboard digunakan untuk memvisualisasikan faktor yang berpengaruh dan pengembangan model maachine learning untuk memprediksi mahasiswa apakah dropout atau tidak

Tahapan analisis data meliputi pengumpulan data, pemroresan data (cleaning data), eksplorasi data dengan tujuan mengidentifikasi pola yang relevan
## Persiapan
Sumber data : [Dataset](https://github.com/dicodingacademy/dicoding_dataset/tree/main/students_performance)

Setup environment:
* Buat virtual environment
  ```
  python -m venv env
  ```
* Mengaktifkan virtual environment
  ```
  env\Scripts\activate
  ```
* Install library yang digunakan
  ```
  pip install -r requirements.txt
  ```
## Business Dashboard
![Jaya Jaya Institute Students](https://github.com/user-attachments/assets/e566ebcd-e2e9-4775-b9d8-a101b7587fd9)

[Dashboard](https://lookerstudio.google.com/reporting/da625855-12c5-4e80-88b5-b60f64e72f94) ini dibuat dengan tujuan memberikan gambaran tentang performa akademik mahasiswa di Jaya Jaya Institute. Total mahasiswa berjumlah 4.424 orang dengan mahasiswa yang lulus 2.209 orang, dropout 1.421, mahasiswa yang aktif 794 orang, dan rerata usia mahasiswa 23.27 tahun

Berdasarkan Gender, jumlah mahasiswa laki-laki dan perempuan yang dropout hampir seimbang yang artinya resiko dropout tidak terlalu terpengaruh oleh gender. Jumlah mahasiswa yang dropout didominasi oleh perempuan

Berdasarkan Deptor, sebagian besar mahasiswa yang melakukan dropout tidak memiliki utang. Namun, analisis lebih mendalam menunjukkan bahwa mahasiswa yang memiliki utang memiliki risiko dropout yang lebih tinggi, dengan sekitar 62,03% dari mahasiswa berutang mengalami dropout, sedangkan 28,28% mahasiswa dropout tidak memiliki utang. Oleh karena itu, institusi dapat mempertimbangkan pengembangan program pemantauan khusus bagi mahasiswa debitur, pemberian konseling keuangan, serta peninjauan ulang skema pembiayaan agar lebih fleksibel dan mendukung keberhasilan akademik. Selain itu, status debitur dapat dijadikan indikator dalam sistem prediksi risiko dropout untuk memungkinkan intervensi lebih dini. Upaya ini tidak hanya akan menurunkan angka dropout, tetapi juga menunjukkan komitmen institusi dalam mendukung keberhasilan mahasiswa dari berbagai latar belakang.

Berdasarkan beasiswa, sebagian besar mahasiswa yang mengalami dropout tidak memiliki beasiswa, yaitu sebesar 90,6%, sedangkan hanya 9,4% mahasiswa yang dropout memiliki beasiswa. Hal ini menunjukkan bahwa keberadaan beasiswa berpotensi menurunkan angka dropout, karena beasiswa dapat berperan sebagai dukungan finansial maupun motivasi tambahan yang membantu mahasiswa menyelesaikan studinya dengan lebih baik.

Berdasarkan data status mahasiswa menurut usia saat pendaftaran, terlihat bahwa mayoritas mahasiswa yang berhasil lulus mendaftar pada usia muda, khususnya antara 18 hingga 21 tahun. Pada rentang usia ini, jumlah lulusan mencapai puncaknya, dengan angka tertinggi pada usia 18 tahun. Meskipun jumlah mahasiswa yang mengalami dropout juga cukup tinggi pada usia muda tersebut, namun secara keseluruhan jumlah lulusan tetap lebih banyak dibandingkan yang dropout. Setelah usia 21 tahun, baik jumlah lulusan maupun mahasiswa yang dropout mengalami penurunan yang signifikan dan cenderung stabil pada angka yang rendah. Hal ini menunjukkan bahwa pendaftaran mahasiswa pada usia lebih tua relatif jarang terjadi. Pada usia di atas 30 tahun, jumlah mahasiswa yang mendaftar sangat sedikit, dan perbedaan antara lulusan dan dropout hampir tidak terlihat. Dari pola ini dapat disimpulkan bahwa usia saat pendaftaran memiliki pengaruh besar terhadap status kelulusan mahasiswa, di mana pendaftaran pada usia muda lebih dominan dan berkontribusi besar terhadap jumlah lulusan.

Berdasarkan grafik jumlah dropout menurut program studi, terlihat bahwa jurusan **Manajemen**, **Keperawatan**, dan **Jurnalisme** menempati posisi teratas dalam jumlah mahasiswa yang keluar. Jurusan Manajemen bahkan muncul dua kali, kemungkinan mengindikasikan dua konsentrasi atau program berbeda dengan beban dropout yang sama-sama tinggi. Hal ini mengindikasikan bahwa jurusan-jurusan populer dan dengan jumlah mahasiswa besar cenderung memiliki tingkat dropout yang tinggi pula. Sementara itu, jurusan-jurusan seperti **Biofuel Processing**, **Oral Hygiene**, dan **Communication** menunjukkan angka dropout yang jauh lebih rendah. Ini bisa mencerminkan beberapa faktor, seperti ukuran kelas yang lebih kecil, seleksi masuk yang lebih ketat, atau dukungan akademik yang lebih baik.

## Menjalankan Sistem Machine Learning
Sistem machine learning untuk mengetahui apakah mahasiswa melakukan dropout dapat dilakuakan dengan dua cara yaitu menjalankannya di local maupun secara [online](https://students-performance-apps.streamlit.app/). Sistem ini dibuat menggunakan streamlit dan untuk menjalankannya secara lokal dengan cara
```
streamlit run app.py
```
## Conclusion
Dari analisis yang dilakukan, ditemukan bahwa dari total 4.424 mahasiswa, terdapat 2.209 mahasiswa yang berhasil lulus, 794 masih aktif, dan 1.421 mengalami dropout. Fenomena dropout ternyata tidak dipengaruhi secara signifikan oleh gender, namun terdapat korelasi kuat antara dropout dengan status keuangan mahasiswa (utang dan beasiswa), usia saat mendaftar, serta program studi tertentu.

Faktor finansial terbukti menjadi penentu penting: mahasiswa dengan utang memiliki kemungkinan dropout yang jauh lebih tinggi, sementara penerima beasiswa justru cenderung menyelesaikan studi. Usia muda saat mendaftar (18–21 tahun) berkontribusi besar terhadap angka kelulusan, dan jurusan-jurusan populer seperti Manajemen, Keperawatan, dan Jurnalisme memiliki jumlah dropout paling tinggi, kemungkinan akibat tingginya jumlah pendaftar atau beban akademik.
## Rekomendasi Action Items
* Dukungan Finansial

  Mahasiswa dengan kesulitan keuangan, khususnya yang memiliki utang, menunjukkan kecenderungan lebih tinggi untuk mengalami dropout. Oleh karena itu, institusi perlu menyediakan dukungan finansial yang lebih luas dan tepat sasaran. Hal ini bisa dilakukan dengan menambah kuota beasiswa, merancang skema pembayaran kuliah yang lebih fleksibel seperti cicilan ringan atau grace period, serta menyediakan layanan konseling keuangan. Langkah-langkah ini diharapkan dapat meringankan beban mahasiswa dan mendorong mereka untuk menyelesaikan studi.
* Pendekatan Usia Saat Pendaftaran

  Usia saat pendaftaran juga memiliki peran penting dalam tingkat kelulusan. Mahasiswa yang mendaftar pada usia muda (18–21 tahun) menunjukkan tingkat kelulusan yang tinggi. Oleh karena itu, promosi dan sosialisasi program pendidikan tinggi kepada siswa sekolah menengah perlu diperkuat agar mereka dapat melanjutkan studi tanpa jeda. Untuk mahasiswa yang mendaftar di usia lebih tua, institusi dapat menyediakan program orientasi tambahan dan pendampingan adaptasi belajar agar mereka dapat mengejar ketertinggalan dan merasa lebih terintegrasi dalam lingkungan akademik.
* Evaluasi Program Studi Tertentu

  Beberapa program studi seperti Manajemen, Keperawatan, dan Jurnalisme memiliki angka dropout tertinggi. Ini dapat disebabkan oleh tingginya jumlah mahasiswa atau beban akademik yang berat. Maka dari itu, perlu dilakukan evaluasi menyeluruh terhadap kurikulum, beban belajar, dan rasio dosen-mahasiswa di program-program tersebut. Selain itu, sistem dukungan akademik seperti bimbingan belajar, sesi remedial, atau tutor sebaya bisa diperkuat untuk membantu mahasiswa yang kesulitan mengikuti materi.
