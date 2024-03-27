<b>POINT UTAMA</b>
---
> #### KENAPA PHP UNIT TEST
> - PHPUnit merupakan kerangka kerja pengujian yang digunakan untuk melakukan pengujian unit pada aplikasi PHP.
> - Ini adalah proses pengujian yang dilakukan pada unit terkecil dari kode yang dapat diuji secara terpisah, seperti fungsi, metode, atau kelas tertentu dalam PHP.
> - PHPUnit memungkinkan pengembang untuk menulis skrip pengujian otomatis untuk memeriksa perilaku unit kode PHP.
> - Dengan PHPUnit, pengembang dapat menuliskan serangkaian pengujian yang mencakup berbagai skenario dan kasus uji yang mungkin terjadi.
> -  Pengujian unit membantu memastikan bahwa setiap bagian kecil dari kode berfungsi dengan benar secara terpisah. Ini mempermudah dalam memperbaiki bug, memelihara, dan memperbarui kode.
---
> #### ASSERTIONS
> -  Assertions adalah pernyataan dalam PHPUnit untuk memeriksa hasil dari unit yang diuji.
> -  Memvalidasi apakah perilaku unit sesuai dengan harapan.
> -  Contoh Assertions: `assertEquals`, `assertTrue`, `assertFalse`, `assertNull`, `assertNotNull`, dan lain-lain.
> -  Assertion berhasil jika hasil sesuai dengan yang diharapkan, dan PHPUnit akan menandai pengujian sebagai gagal jika sebaliknya.
> -  PHPUnit menyediakan berbagai jenis assertions dan juga memungkinkan assertions kustom.
> -  Memastikan kepercayaan dalam kualitas perangkat lunak yang dikembangkan.
> -  Assertions merupakan bagian integral dari pengujian unit dalam PHPUnit dan digunakan secara luas dalam skrip pengujian otomatis.
---
> #### ANNOTAION
> -  @test: Menandai metode sebagai metode pengujian yang akan dijalankan oleh PHPUnit.
> -  @dataProvider: Menyediakan data untuk pengujian dari metode yang ditandai.
> -  @depends: Menentukan ketergantungan antara metode pengujian.
> -  @expectedException: Menandai pengecualian yang diharapkan terjadi dalam pengujian.
> -  @before, @after: Menandai metode yang akan dijalankan sebelum atau setelah setiap metode pengujian.
---
> #### TEST DEPENDENCY
> - Test Dependency adalah hubungan antara metode pengujian di mana satu metode membutuhkan hasil sukses dari metode lain.
> - `@depends` Digunakan untuk menandai ketergantungan antara dua metode pengujian. Metode yang bergantung akan dijalankan hanya setelah metode yang menjadi ketergantungan berhasil.
> - Memastikan urutan eksekusi pengujian dan memastikan bahwa kondisi yang dibutuhkan telah terpenuhi sebelum pengujian yang bergantung dijalankan.
> - Berguna ketika ada tahapan yang perlu dilakukan sebelum pengujian yang lain dapat berjalan dengan benar, seperti persiapan data atau kondisi lingkungan tertentu.
---
> #### DATA PROVIDER
> - Data Provider adalah fitur dalam PHPUnit yang memungkinkan pengguna untuk menyediakan data dinamis kepada metode pengujian.
> - Memungkinkan pengujian dilakukan dengan berbagai set data input tanpa perlu menulis ulang metode pengujian untuk setiap set data yang berbeda.
> - Pengguna membuat metode yang mengembalikan array dari set data yang akan digunakan dalam pengujian. Setiap elemen dalam array mewakili satu set data input untuk metode pengujian yang terkait.
> - Sebuah data provider menyediakan berbagai set data untuk metode pengujian `testAdd()`, dan PHPUnit akan menjalankan `testAdd()` untuk setiap set data yang diberikan.
> - Menghindari pengulangan kode, membuat pengujian lebih efisien dan terstruktur.
---
> #### TEST EXCEPTION
> - Test Exception adalah fitur dalam PHPUnit yang memungkinkan pengguna untuk menguji apakah suatu metode menghasilkan pengecualian yang diharapkan saat dieksekusi.
> - Memastikan bahwa aplikasi dapat menangani kondisi yang tidak biasa atau kesalahan dengan benar, dengan menguji pengecualian yang dihasilkan oleh metode.
> - Pengguna menandai bahwa suatu metode pengujian diharapkan menghasilkan pengecualian tertentu saat dieksekusi, dan jika pengecualian yang ditentukan tidak terjadi, PHPUnit akan menandai pengujian sebagai gagal.
---
> #### TEST OUTPUT
> - Test Output adalah kemampuan untuk memeriksa output yang dihasilkan oleh suatu kode selama pengujian berlangsung.
> - Memungkinkan pengujian terhadap output yang diharapkan dari suatu proses atau fungsi dalam kode.
> -  PHPUnit menyediakan metode dan assertion yang memungkinkan pengujian terhadap output, seperti `expectOutputString()`.
> -  Memastikan bahwa output yang dihasilkan sesuai dengan yang diharapkan, meningkatkan kepercayaan dalam kualitas perangkat lunak yang dikembangkan.
---
> #### FIXTURE
> - Fixture dalam PHPUnit adalah kondisi awal atau lingkungan yang diperlukan untuk menjalankan serangkaian pengujian.
> - Fixture membantu menjaga konsistensi pengujian dengan memastikan bahwa setiap pengujian dimulai dari kondisi awal yang sama.
---
> #### INCOMPLETE TEST
> - Incomplete Test adalah kondisi di mana suatu pengujian tidak dapat diselesaikan sepenuhnya karena alasan tertentu dalam PHPUnit.
> - Menandai bahwa suatu pengujian tidak dapat diselesaikan karena alasan tertentu, seperti implementasi kode yang belum tersedia atau ketergantungan eksternal yang tidak tersedia.
> - Pengujian ditandai sebagai incomplete menggunakan metode `markTestIncomplete()`.
> - PHPUnit tidak akan menganggap pengujian tersebut sebagai pengujian yang gagal atau berhasil. Sebaliknya, PHPUnit akan melaporkannya sebagai incomplete.
---
> #### SKIP TEST
> - Skip Test adalah proses penandaan suatu pengujian untuk diabaikan atau dilewati selama eksekusi dalam PHPUnit.
> - Menandai pengujian untuk diabaikan ketika kondisi lingkungan tidak memungkinkan atau ketika pengujian tidak relevan dalam konteks tertentu.
> -  Pengujian ditandai sebagai skip menggunakan metode `markTestSkipped()`.
> -  PHPUnit tidak akan menjalankan pengujian yang ditandai sebagai skip. Pengujian tersebut dilewati dan dilaporkan sebagai pengujian yang dilewati.
---
> #### STUB
> - Stub dalam PHPUnit adalah objek tiruan yang digunakan untuk menggantikan perilaku objek nyata dalam pengujian.
> - Digunakan untuk mengisolasi unit yang diuji dari dependensi eksternal atau sumber daya yang kompleks, sehingga memungkinkan fokus pada pengujian unit.
> - Stubs dapat dibuat menggunakan metode `getMockBuilder()` atau `createStub()` dalam PHPUnit.
> - Anda dapat menetapkan perilaku tertentu untuk metode-metode yang dipanggil pada stub, seperti nilai kembalian atau penanganan argumen.
---
> #### Mock Object
> - Mock Object dalam PHPUnit adalah objek tiruan yang digunakan untuk merekam dan memeriksa perilaku pemanggilan pada objek yang diuji.
> - Digunakan untuk memverifikasi interaksi antara objek yang diuji dengan objek-objek lainnya, serta menguji perilaku metode pada objek yang di-mock.
> - Mock objects dapat dibuat menggunakan metode `getMockBuilder()` dalam PHPUnit.
> - Anda dapat mengatur harapan pemanggilan metode pada mock object, termasuk jumlah pemanggilan, argumen yang diterima, dan nilai kembalian yang diharapkan.
---

<p align="center" >
  <b>PERTANYAAN DAN CATATAN TAMBAHAN</b>
</p>

> - tidak ada

---

<p align="center" >
  <b>KESIMPULAN</b>
</p>

---

> - PHPUnit adalah alat yang sangat berguna bagi pengembang PHP untuk memastikan kualitas perangkat lunak mereka melalui pengujian unit yang efektif dan otomatis. Itu membantu meningkatkan keandalan, keterbacaan, dan pemeliharaan kode PHP
