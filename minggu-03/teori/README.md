# minggu-3

struktur data

•	list.insert (i, x) Masukkan item pada posisi tertentu. Argumen pertama adalah indeks dari elemen yang sebelumnya disisipkan, jadi sisipan a.insert (0, x) di bagian depan daftar, dan a.insert (len (a), x) ekivalen dengan a.append ( x).

•	list.remove (x) Hapus item pertama dari daftar yang nilainya sama dengan x. Ini menimbulkan ValueError jika tidak ada item seperti itu.

•	list.append (x) menambahkan item kebagian terahir. Setara dengan [len (a):] = [x].

•	list.extend (iterable) menambahkan semua item dari iterable. Setara dengan [len (a):] = iterable.

•	list.pop ([i]) Hapus item pada posisi yang ditentukan dalam daftar, dan kembalikan. Jika tidak ada indeks yang ditentukan, a.pop () menghapus dan mengembalikan item terakhir dalam daftar. (Tanda kurung persegi di sekitar i dalam tanda tangan metode menunjukkan bahwa parameter adalah opsional, bukan bahwa Anda harus mengetik tanda kurung siku pada posisi itu. Anda akan melihat notasi ini sering dalam Referensi Perpustakaan Python.)

•	list.clear () Hapus semua item dari daftar. Setara dengan del [:].

•	list.sort (key = None, reverse = False) Urutkan item dari daftar di tempat (argumen dapat digunakan untuk mengurutkan kustomisasi, lihat diurutkan () untuk penjelasannya).

•	list.reverse () Membalikkan unsur-unsur daftar di tempat.

•	list.copy () Kembalikan salinan dangkal daftar. Setara de

•	list.index (x [, start [, end]]) Kembalikan indeks berbasis nol dalam daftar item pertama yang nilainya sama dengan x. Meningkatkan ValueError jika tidak ada item semacam itu.

•	Argumen opsional awal dan akhir ditafsirkan sebagai dalam notasi slice dan digunakan untuk membatasi pencarian ke daftar urutan tertentu. Indeks yang dikembalikan dihitung relatif terhadap awal dari urutan penuh daripada argumen awal.

•	list.count (x) Kembalikan jumlah kali x muncul dalam daftar.
