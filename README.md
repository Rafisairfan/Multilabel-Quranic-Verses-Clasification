#Description
Klasifikasi multilabel merupakan salah satu jenis klasifikasi yang cukup berbeda dengan klasifikasi pada umumnya. Pada kasus ini saya menggunakan data ayat suci Al-Quran sebagai data karena ayat Al-Quran memiliki struktur yang unik dan memiliki beberapa makna dalam setiap ayatnya.
Pada klasifikasi multiabel kali ini terbagi menjadi 16 label dengan banyak data sebanyak kurang lebih 6236 data sesuai dengan jumlah ayat Al-Quran.
Klasifikasi dilakukan dengan menggunakan model kombinasi Antara CNN-LSTM, Bi-LSTM dan LSTM. 

#Main
## 1. Preproses
Pada kasus data text perlu dilakukan beberapa proses agar data dapat bersih dan model dapat memproses kata dengan baik yaitu :
- mengubah dataframe menjadi array
- memisahkan data dan label
- menghilangkan tanda baca
- mengubah semua huruf menjadi kecil
- menghilangkan kata kata yang tidak diperlukan
- mengubah kata berimbuhan menjadi kata dasar.
- Tokenizing

Sebelumnya saya juga sempat menggunakan word2vec tetapi memberikan hasil yang kurang maksimal. Maka dari itu Word2vec tidak digunakan.

## 2.  Modeling
Karena teradapat 2 model yaitu model kombinasi CNN-LSTM dan Bi-LSTM, maka arsitektur kedua model tersebut juga berbeda.
- C-LSTM :  Embedding Layer-CNN-LSTM-Dropout-Output Layer
- Bi-LSTM :  Embedding Layer-Bi LSTM-Dropout-Output Layer

Kedua model menggunakan total layer yang tidak jauh berbeda agar perbandingan kedua model adil. Kedua model menggunakan activation softmax karena untuk kasus multilabel softmax jauh lebih baik dibandingkan activation function lainnya

  
