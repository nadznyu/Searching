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



