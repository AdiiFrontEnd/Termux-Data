# Ini Berisi Pertanyaan = Image -> Teks Markdown
yang bisa di baca ai Biat Ga Boros Token

# Pengalaman & Kesimpulan Belajar SQL JOIN (MariaDB/MySQL)

## 1. FULL JOIN Tidak Didukung di MariaDB/MySQL
**Kesimpulan:** MariaDB/MySQL tidak punya `FULL JOIN` bawaan. Solusinya menggabungkan `LEFT JOIN` dan `RIGHT JOIN` pakai `UNION`.

*Analogi: (belum tercatat)*

## 2. Self JOIN
**Kesimpulan:** Self JOIN adalah join sebuah tabel dengan dirinya sendiri, memakai dua alias berbeda (misalnya `e` dan `m`). Berguna untuk kasus atasan-bawahan (`manager_id` merujuk ke `id` di tabel yang sama) atau mencari pasangan baris dengan nilai sama.

*Analogi: (belum tercatat)*

## 3. Error Syntax Akibat Lupa Koma
**Pengalaman:** Sempat menemui error `You have an error in your syntax` saat menulis `SELECT` dengan banyak kolom.
**Kesimpulan:** Penyebabnya lupa koma antar kolom — `SELECT a.kolom b.kolom` membuat `b.kolom` dianggap alias dari `a.kolom`, bukan kolom terpisah.

*Analogi: (belum tercatat)*

## 4. Perbedaan ON vs WHERE
**Kesimpulan:**
- `ON` → syarat pencocokan antar tabel (foreign key = primary key).
- `WHERE` → syarat filter data (misalnya nilai kolom >= angka tertentu).

*Analogi: (belum tercatat)*

## 5. Kesalahan ON Hanya Berisi Kolom dari Satu Tabel → Cross Join
**Pengalaman:** Menulis `ON WEAPONS.POWER >= 700` yang hanya melibatkan satu tabel.
**Kesimpulan:** Ini bukan syarat pencocokan, sehingga menghasilkan cross join — semua baris `USER` dikombinasikan dengan semua baris `WEAPONS` yang lolos filter. Perbaikannya, `ON` harus menghubungkan foreign key ke primary key (`U.WEAPON_ID = W.ID`), sedangkan filter seperti `POWER >= 700` ditaruh di `WHERE` atau digabung dengan `AND` di `ON`.

*Analogi: (belum tercatat)*

---

**Catatan:** Bagian "Analogi" di atas belum bisa saya isi karena analogi spesifik yang kamu berikan saat sesi belajar tidak tersimpan dalam memori saya. Kalau kamu ceritakan ulang analoginya, saya akan langsung update file ini persis sesuai yang kamu maksud.
