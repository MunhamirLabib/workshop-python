# minggu-13

Pandas

Pandas merupakan toolkit yang powerfull sebagai alat analisis data dan struktur untuk bahasa pemrograman Python. Dengan menggunakan pandas kita dapat mengolah data dengan mudah, salah satu fiturnya adalah Dataframe. Dengan adanya fitur dataframe kita dapat membaca sebuah file dan menjadikannya tabble, kita juga dapat mengolah suatu data dengan menggunakan operasi seperti join, distinct, group by, agregasi, dan teknik lainnya yang terdapat pada SQL.
Banyak format file yang dapat dibaca menggunakan Pandas, seperti file .txt, .csv, .tsv dan lainnya. Agar lebih jelas mari kita mencobanya secara langsung. (Catatan: Pada artikel ini saya menggunakan python versi 3.6, jika teman-teman menggunakan versi 2.7 mungkin akan sedikit berbeda)
Menginstall Pandas
Untuk dapat menginstall pandas, kita bisa menjalankan perintah berikut :
pip install pandas
Atau jika teman-teman menggunakan library Anaconda, kita bisa menginstallnya dengan perintah beriktu :
conda install pandas
Mencoba Series
Series merupakan sebuah array satu dimensi yang memiliki label dan digunakan untuk menyimpan beragam tipe data seperti integer, string, float, bahkan objek, dan lain sebagainya. Label pada series disebut dengan index. Bagaimana cara membuat series ? Perintah dasar untuk membuat sebuah Series dengan pandas adalah
pandas.Series( data, index, dtype, copy)
Penjelasan Kode : 
data : parameter ini diisi dengan data yang akan dibuat series
index : parameter ini diisi dengan index dari series. Jumlah index harus sama dengan jumlah data. Jika kita tidak mengisi parameter index, maka series akan memiliki index integer seperti halnya array biasa.
dtype : parameter ini diisi dengan tipe data dari series, sebenarnya kita tidak perlu untuk mengisi parameter ini, karena secara otomatis python akan menyimpulkan tipe data yang kita masukkan.
copy : parameter untuk copy data, secara default akan bernilai false.
Bingung ? yuk mari langsung saja kita coba dengan beberapa contoh sederhana:
import pandas as pd
import numpy as np
data = np.array(['a','b','c','d'])
karakter = pd.Series(data)
print(karakter)
Pada contoh diatas kita membuat sebuah Series yang berisi karakter a,b,c, dan d. Jika kode diatas dijalankan maka hasilnya adalah:
>>> print(karakter)
0 a
1 b
2 c
3 d
dtype: object
Series yang kita buat memiliki index default, lalu bagaimana jika kita ingin membuat custom index ? Yup benar, kita harus menambahkan parameter kedua yaitu index. Berikut contoh sederhananya:
import pandas as pd
import numpy as np
data = np.array(['a','b','c','d'])
karakter = pd.Series(data,index=['satu','dua',tiga','empat'])
print(karakter)
Jika kita jalankan, maka hasilnya adalah sebagai berikut:
>>> print(karakter)
satu a
dua b
tiga c
empat d
dtype: object
Yey, sekarang kita berhasil membuat custom index pada Series kita. Sekarang bagaimana caranya untuk mengakses series berdasarkan indexnya. Caranya sama seperti kita mengakses sebuah array.
print(karakter[“satu”])
Jika dijalankan hasilnya adalah:
>>> print(karakter[“satu”])
a
Lalu apa bedanya Series dengan array biasa pada python?
Seperti yang sudah kita bahas sebelumnya, pandas menyediakan beragam fungsi operasi untuk mengolah data. Contoh jika kita menggunakan series kita bisa mencari nilai max, min, dan mean secara langsung, bahkan kita juga bisa melakukan operasi perpangkatan pada nilai Series secara langsung. Biar gak bingung yuk mari kita coba.
Sekarang kita coba membuat sebuah Series baru yang akan berisi nilai float. Berikut adalah kode nya:
angka = pd.Series(np.array([60.5,70.45,80.00,90.64]));
Sekarang mari kita coba mencari tahu berapa nilai minimum, maximum dan nilai rata-ratanya. Caranya cukup mudah, kita tinggal menggunakan saja method yang sudah disediakan oleh pandas. Berikut contoh sederhanya :
angka.max()
angka.min()
angka.mean()
Hasilnya adalah sebagai berikut:
>>> angka.mean()
75.397499999999994
>>> angka.max()
90.640000000000001
>>> angka.min()
60.5
>>> angka.mean()
75.397499999999994
>>>
Cukup mudah bukan? bayangkan jika semua operasi tersebut harus kita lakukan secara manual. Contoh yang lain kita akan mencoba memangkatkan setiap nilai pada Series angka dengan pangkat 2. Bagaimana caranya? yuk langsung kita coba.
angka.pow(2, axis=0)
Jika perintah diatas dijalankan, maka seluruh nilai yang ada pada Series angka akan dipangkatkan 2. Hasilnya adalah sebagai berikut:
>>> angka.pow(2, axis=0)
0 3660.2500
1 4963.2025
2 6400.0000
3 8215.6096
dtype: float64
