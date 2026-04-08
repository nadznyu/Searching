# Searching

***Pertanyaan 6.2.3***
1. Jelaskan perbedaan metod tampilDataSearch dan tampilPosisi pada class MahasiswaBerprestasi!
2. Jelaskan fungsi break pada kode program di bawah ini! 
    if (listMhs[j].ipk == cari) {
        posisi = j;
        break;
    }
3. Apa fungsi variabel pos atau indeks hasil pencarian dalam program sequential search?
4. Jika terdapat lebih dari satu data dengan nilai yang sama, hasil pencarian sequential search yang dibuat di atas akan menampilkan data ke berapa? Jelaskan.
5. Berkaitan dengan pertanyaan nomor 2 di atas, apa yang terjadi jika perintah break dihapus dari kode di atas?

***Jawaban 6.2.3***
1. - tampilDataSearch : menampilkan detail lengkap data mahasiswa (nim, nama, kelas, ipk) yang ditemukan berdasarkan posisi hasil 
                        pencarian.
   - tampilPosisi : hanya menampilkan posisi/indeks tempat data ditemukan di dalam array, tanpa menampilkan datanya.
2. Untuk menghentikan perulangan for secara paksa setelah data yang dicari sudah ditemukan. Tanpa break, loop akan terus berjalan 
   meskipun data sudah ditemukan.
3. Sebagai penanda lokasi data yang ditemukan dalam array listMhs[], pos ini digunakan oleh method tampilDataSearch dan tampilPosisi untuk mengakses elemen listMhs[pos] yang tepat. Jika pos==-1, berarti data tidak ditemukan.
4. Program akan menampilkan data pertama yang ditemukan (indeks terkecil), karena loop berjalan dari j = 0 ke atas, jika IPK sudah cocok program akan menghentikan loop (break).
5. Jika break dihapus loop akan terus berjalan sampai selesai meskipun data sudah ditemukan.

***Pertanyaan 6.3.3***
1. Tunjukkan pada kode program yang mana proses divide dijalankan!
2. Tunjukkan pada kode program yang mana proses conquer dijalankan!
3. Apa fungsi left, right, dan mid?
4. Jika data IPK yang dimasukkan tidak urut. Apakah program masih dapat berjalan? Mengapa demikian? 
5. Jika IPK yang dimasukkan dari IPK terbesar ke terkecil (misal: 3.8, 3.7, 3.5, 3.4, 3.2) dan elemen 
   yang dicari adalah 3.2. Bagaimana hasil dari binary search? Apakah sesuai? Jika tidak sesuai maka ubahlah kode program binary seach agar hasilnya sesuai
6. Jelaskan bagaimana binary search menentukan bahwa data yang dicari tidak ditemukan di dalam array.
7. Modifikasi program di atas yang mana jumlah mahasiswa yang diinputkan sesuai dengan masukan dari 
   keyboard.

***Jawaban 6.3.3***
1. Proses divide ada di baris ini : 
   mid = (left + right) / 2;
   disini array dibagi dua dengan menghitung indeks tengah.
2. Proses conquer terjadi pada bagian ini : 
   if (cari == listMhs[mid].ipk) {
       return (mid);
    } else if (listMhs[mid].ipk > cari) {
       return findBinarySearch(cari, left, mid - 1);
    } else {
       return findBinarySearch(cari, mid + 1, right);
    }
    disini program akan memutuskan akan mencari ke bagian kiri atau kanan, lalu emmanggil dirinya sendiri secara rekursif untuk menyelesaikan submasalah tersebut.
3. - left : batas indeks paling kiri
   - right : batas indeks paling kanan
   - mid : indeks tengah hasil dari (left + right) / 2, digunakan sebagai titik pembanding antara nilai yang dicari dengan nilai di posisi tengah array.
4. Program tetap bisa berjalan, namun hasilnya bisa saja salah/tidak akurat. Ini karena binary search 
   yaitu mengerjakan sesuai dengan 
   data yang sudah diurutkan.
5. Hasilnya tidak sesuai/tidak ditemukan.
   Modifikasi sudah di commit.
6. Ketika konsisi right >= left sudah tidak teroenuhi, itu artinya area pencarian sudah habis.
7. Modifikasi sudah di commit.

