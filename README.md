# mlops1
Implementasi Docker untuk Data Science: Instalasi, Konfigurasi, dan Eksplorasi Jupyter Notebook

## Download Docker & Jupyter Notebook
1. Download sesuai dengan OS https://docs.docker.com/desktop/install/windows-install/
2. Setup settings default
3. Download Jupyter Notebook https://hub.docker.com/r/jupyter/datascience-notebook via cmd
4. Setelah itu jalankan perintah 'docker images' via cmd untuk mengecek Jupyter Notebook sudah terdownload di docker
5. Copy id images dari Jupyter Notebook
6. Jalankan perintah 'docker run -p 8888:8888 -v -$(pwd) id_image'
7. Buka web browser dan ketik 'localhost:8888'
8. Untuk memasukkan token, copy token yang terdapat di terminal cmd

## Notebook berisi analisis data dan eksplorasi fitur
Pada analisis data, penulis menggunakan dataset iris dan menggunakan algoritma Naive Baiyes untuk di analisis.
Tahapan pertama pada algoritma Naive Bayes adalah perhitungan prior. Prior suatu kelas merupakan peluang awal munculnya kelas tersebut. Atau dengan kata lain, prior merupakan frekuensi relatif dari suatu kelas terhadap keseluruhan data. Semua fitur pada dataset iris memiliki tipe numerik. Dengan demikian, perhitungan likelihood dilakukan menggunakan Gaussian Model. Tahapan yang perlu dilakukan sebelum perhitungan likelihood adalah menghitung rata-rata dan deviasi standar masing-masing fitur per kelas.
Proses training pada Naive Bayes dengan model Gaussian dilakukan untuk menghitung prior serta rata-rata dan deviasi standar pada masing-masing fitur dan kelas.
Proses testing dilakukan dengan menghitung nilai posterior dari data uji berdasarkan nilai model yang diperoleh saat training. Nilai posterior diperoleh dari perkalian prior dengan likelihood masing-masing fiturnya. Setelah itu, penentuan kelas data uji dilakukan berdasarkan nilai posterior terbesar.
