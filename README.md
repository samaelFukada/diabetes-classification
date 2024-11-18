# Final Submission : Machine Learning Pipeline - Diabetes Classification
Nama: Ahmad Reginald Syahiran

Username dicoding: ahmadreginald


| | Deskripsi |
| ----------- | ----------- |
| Dataset | [Diabetes prediction dataset](https://www.kaggle.com/datasets/iammustafatz/diabetes-prediction-dataset) |
| Masalah | Penyakit gula atau diabetes harus diwaspadai karena merupakan penyakit yang berlangsung lama. Meningkatnya kadar gula darah melebihi nilai normal adalah tanda utama diabetes. Ini terjadi ketika tubuh seseorang yang menderita kondisi ini tidak lagi mampu menyerap gula (glukosa) ke dalam sel dan menggunakannya sebagai energi, yang menyebabkan penumpukan gula tambahan dalam aliran darah. Diabetes memiliki tingkat kematian yang tinggi. Pada tahun 2021, diabetes menyebabkan 6,7 juta kematian di seluruh dunia, atau 1 kematian setiap 5 detik. |
| Solusi machine learning | Untuk mendeteksi diabetes, pasien biasanya menjalani pengecekan kadar gula darah mereka. Dokter tidak lansung dapat menentukan apakah pasien memiliki diabetes hanya dengan melihat kadar gula darah mereka. Dengan sistem klasifikasi diabetes yang menggunakan deep learning, dokter diharapkan dapat memperoleh pengetahuan tentang diabetes pasien untuk digunakan dalam pertimbangan dan pemeriksaan pasien di masa depan. |
| Metode pengolahan | Dalam kasus ini, terdapat sembilan fitur, delapan di antaranya akan digunakan untuk fitur klasifikasi, satu sebagai class, dua fitur kategoris, dan enam fitur numerik. Selanjutnya, split data akan dilakukan menjadi 80:20 untuk train dan eval data, dan fitur yang telah ditransformasi akan direname. Untuk class data, satu hot encoding akan digunakan. |
| Arsitektur model | Dalam struktur model sendiri, tiap lapisan menggunakan Dense 256, Dense 64, dan Dense 16 dengan aktivasi relu, dan lapisan terakhir menggunakan Dense 1 dengan aktivasi sigmoid. Ini dilakukan karena akan mengklasifikasikan kelas dengan hanya dua nilai, yaitu diabetes dan tidak diabetes. Untuk mengkompilasi model, gunakan optimizer Adam dengan learning_rate 0.001, loss binary_crossentropy, dan BinaryAccuracy metrics. |
| Metrik evaluasi | Metrik evaluasi yang digunakan yaitu AUC, Precision, Recall, ExampleCount dan BinaryAccuracy |
| Performa model | Untuk performa model, keakuratan dan loss sangat baik, dengan keakuratan 0.97 pada proses pelatihan dan validasi dan loss 0,08 pada proses pelatihan dan validasi. Ini menunjukkan bahwa model ini layak untuk klasifikasi. |
| Opsi deployment | Untuk deployment, sistem ini akan dideploy menggunakan platform railway |
| Web app | [diabetes-classification]()|
| Monitoring | Untuk memantau sistem ini, hanya Prometheus yang digunakan. Proses pengawasan dilakukan dengan menampilkan permintaan yang masuk ke sistem serta status untuk setiap permintaan yang diterima. Tiga status yang ditampilkan oleh sistem adalah: proses permintaan pada sistem klasifikasi tidak ditemukan, argumen yang salah, dan proses klasifikasi berhasil yang ditandai dengan ok. |
