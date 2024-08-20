# ML - EcoSorter

EcoSorter adalah sebuah aplikasi yang bertujuan untuk membantu dalam pengelolaan sampah di lingkungan perkotaan, khususnya di Indonesia. Dengan pertumbuhan perkotaan yang pesat dan kurangnya sistem pengelolaan sampah yang efektif, EcoSorter hadir sebagai solusi modern untuk membantu mengatasi masalah tersebut.

## Teknologi Machine Learning

EcoSorter menggunakan teknologi machine learning untuk mengklasifikasikan sampah secara otomatis. Model machine learning yang digunakan telah dilatih dengan dataset yang besar dan beragam, sehingga mampu mengenali berbagai jenis sampah dengan tingkat akurasi yang cukup tinggi. Dengan demikian, pengguna dapat dengan mudah dan cepat mengetahui jenis sampah yang mereka hadapi dan mengambil tindakan yang sesuai untuk pengelolaannya.
Model yang digunakan dalam proyek EcoSorter adalah ResNet50, sebuah arsitektur jaringan saraf konvolusional (CNN) yang telah dilatih sebelumnya dengan dataset ImageNet. ResNet50 memiliki kemampuan untuk mengenali pola dan fitur pada gambar dengan tingkat akurasi yang tinggi. Di samping itu, model ini telah terbukti efektif dalam berbagai tugas pengenalan gambar, termasuk klasifikasi sampah dalam proyek EcoSorter.

## 7 Kelas Sampah

1. Kaca: Termasuk botol kaca, pecahan kaca, atau benda-benda kaca lainnya.
2. Kardus: Meliputi kotak kardus, kemasan kardus, atau barang-barang yang terbuat dari bahan kardus.
3. Logam: Termasuk kaleng aluminium, tutup botol, atau benda-benda logam lainnya.
4. Plastik: Meliputi botol plastik, kemasan plastik, atau barang-barang yang terbuat dari bahan plastik.
5. Kertas: Termasuk kertas bekas, koran, atau barang-barang yang terbuat dari kertas.
6. Organik: Meliputi sisa makanan, daun-daunan, atau sampah-sampah organik lainnya.
7. Khusus: Kategori khusus untuk sampah-sampah yang tidak termasuk dalam kategori lainnya.

## Arsitektur model:

- ResNet50 Base Model: Digunakan sebagai ekstraktor fitur. Lapisan-lapisan dari ResNet50 telah dilatih sebelumnya dengan dataset ImageNet untuk mempelajari representasi-fitur yang berguna dari gambar.

- Top Model: Lapisan teratas dari ResNet50 dihapus, dan kemudian ditambahkan lapisan-lapisan yang baru, termasuk lapisan flatten dan lapisan dense dengan fungsi aktivasi softmax sebagai output layer. Ini bertujuan untuk menyesuaikan model agar sesuai dengan tugas klasifikasi sampah dalam proyek EcoSorter.

- Preprocessing: Penggunaan fungsi preprocessing_input untuk menyesuaikan gambar masukan agar sesuai dengan format
