# SIMRS

**Aplikasi Sistem Informasi Manajemen Rumah Sakit** \(SIMRS\) dikembangkan untuk menangani Sistem Administrasi \(Bussiness Process\) dan Rekam Medis \(Medical Record\) di Rumah Sakit.

**Aplikasi SIMRS** yang kami kembangkan dirancang untuk dapat berjalan dengan baik pada semua Sistem Operasi \(Multi Platform Operating System\) seperti : Windows, Linux, Apple Machintosh, termasuk juga Tablet PC maupun Mobile Phone. Mengakomodasi Sistem Proses backup Automatic antar Server \(Redundant System\), Mengakomodasi Sistem Proses Pembagian Beban Kerja antar Server \(Paralel Computing\), Mengakomodasi Sistem Proses pooling data pada Sistem Layanan Awan \(Private Cloud System\) sehingga bisa diakses dimana saja, serta dukungan Komputasi bergerak dengan pemanfaatan media komunikasi layanan internet.

**MODUL DAN FITUR SIMRS PAKET STANDAR**

**A. MODUL REGISTRASI**

Modul ini berfungsi sebagai Pencatatan Kedatangan Pasien pada Unit Rawat Jalan, Rawat Inap ataupun Gawat Darurat dengan dukungan Finger Print Scanner sebagai media pengenal pasien. Aplikasi ini dapat dihubungkan dengan Aplikasi Antrian Pasien yang ditawarkan secara terpisah.

Modul ini bisa disesuaikan dengan kondisi lapangan yang dapat mengakomodir Jenis Pelayanan:

* Registrasi Sentralisasi : Registrasi yang melayani seluruh pelayanan dalam satu tempat
* Registrasi Pooling : Layanan Registrasi untuk beberapa ruang rawat yang di jadikan satu
* Registrasi Desentralisasi : Registrasi dapat langsung dilakukan pada tiap ruang rawat – ruang rawat tujuan

RINCIAN APLIKASI SUB MODUL REGISTRASI RAWAT JALAN

Fitur :

* Registrasi berdasarkan perjanjian / jadwal
* Registrasi berdasarkan pencarian identitas/no RM/nama/alamat/identitas pelengkap lain
* Registrasi dapat dikembangkan berdasarkan barcode

SUB MODUL ADMISI RAWAT INAP

Fitur :

* Registrasi berdasarkan perjanjian / jadwal
* Registrasi berdasarkan pencarian identitas/no RM/nama/alamat/identitas pelengkap lain
* Registrasi dapat dikembangkan berdasarkan barcode

SUB MODUL REGISTRASI UNIT/INSTALASI GAWAT DARURAT

Fitur :

* Registrasi pasien
* Registrasi berdasarkan pencarian identitas/no RM/nama/alamat/identitas pelengkap lain
* Registrasi dapat dikembangkan berdasarkan barcode

**B. MODUL BILLING**

Modul ini berfungsi sebagai Pencatatan tindakan-tindakan selama pasien di rawat inap, maupun pencatatan tindakan pasien saat di ruang rawat rawat jalan maupun di rawat darurat, begitu juga dengan proses pembelian obat di Instalasi Farmasi Rumah Sakit bisa menangani system pembayaran cash maupun piutang pasien kerjasama.

Fitur :

* Pencatatan Jasa Tindakan dokter, perawat, asisten selama Pasien di-Rawat Jalan secara otomatis sesuai dengan golongan kategori Pasien
* Cetak Karcis Pelayanan Rawat Jalan secara otomatis pada form Registrasi Pasien
* Master Kontrak Kerjasama Perusahaan atau Asuransi \(Askes, Jamsostek, Askin\) maupun BPJS
* Breakdown Billing Pasien Perusahaan atau Asuransi

RINCIAN APLIKASI

SUB MODUL BILLING PASIEN RAWAT JALAN

Fitur :

* Pencetakan Tagihan Layanan Pemeriksaan.
* Status Pasien, secara otomatis menyesuaikan dengan tarip pada tiap-tiap ruang rawat \(poli\) dengan masing-masing kategori pasien.
* Cetak Laporan Pendapatan pada masing-masing Departemen.
* Cetak Laporan Verifikasi Jasmkesmas, Jamkesda, Askes.
* Cetak SJP \(Surat Jaminan Pelayanan\) Rawat Jalan \(tergantung perjanjian sebelumnya\)
* Breakdown Tarip Jasa Pelayanan dan Jasa Sarana.

SUB MODUL BILLING PASIEN RAWAT DARURAT

Fitur :

* Labeling berdasarkan status kedaruratan penderita \(Triage\)
* Pencetakan Retribusi Layanan Pemeriksaan Rawat Darurat, Status Pasien, secara otomatis menyesuaikan dengan tarip masing-masing kategori pasien.
* Pencatatan Jasa Tindakan dokter, perawat, asisten selama Pasien di-UGD/IGD
* Cetak Karcis Pelayanan Rawat Darurat secara otomatis pada form Registrasi Pasien UGD/IGD

SUB MODUL BILLING PASIEN RAWAT INAP

Fitur :

* Mencetak tanda bukti Pembayaran Pasien Pulang \(Rawat Inap\)
* Pembagian Pendapatan dapat dialokasi sampai sub yang lebih detail seperti jasa sarana, jasa pelayanan dan lain-lain
* Mendukung multi kategori pasien, sehingga pembiayaan dapat diorganisir pada golongan tunai maupun piutang untuk pasien kerjasama
* Mendukung penentuan tarip tindakan berdasar kelas perawatan pasien
* Mendukung sistem penanganan multi petugas medis, seperti tindakan operasi yang bisanya dilakukan lebih dari satu petugas
* Mendukung sistem pelaporan pendapatan petugas medik secara periodik
* Pencatatan jasa tindakan dokter, perawat, asisten selama pasien di rawat inap
* Layanan billing pasien pindah kelas layanan rawat inap
* Informasi bed / kamar kosong untuk layanan rawat inap
* Informasi lokasi pasien di rawat untuk layanan rawat inap
* Informasi billing pasien yang sedang dirawat baik berupa bill terbayar, terhutang ataupun klaim pasien asuransi untuk layanan rawat inap
* Informasi billing pasien yang sedang dirawat baik berupa jasa medis maupun pemakaian obat apotik.
* Cetak billing pasien pulang untuk layanan rawat inap
* Laporan statistik rujukan

**C. MODUL REKAM MEDIK**

Modul ini menangani pencatatan data medis pasien guna keperluan informasi riwayat kesehatan pasien dan juga untuk keperluan evaluasi manajemen.

Fitur :

* Pencatatan data sosial pasien, data morbiditas dengan pedoman sistem informasi rumah sakit
* Master ICD yang bisa disesuaikan dengan ICD yang berlaku saat itu ICD 10 atau ICD 11
* Pencatatan Master ICD sampai batas level tak terhingga
* Pengisian diagnose \(ICD dan DTD\) pasien dapat dengan mudah dilakukan pada kolom pencarian dengan otomatis sesuai dengan diagnose masing-masing ruang rawat
* Penyesuaian ICD dan DTD pada tiap-tiap ruang rawat dapat dilakukan sendiri oleh petugas dengan mudah
* Pencatatan No Rekam Medis Pasien Rawat Jalan secara otomatis
* Pencatatan Rekam Medis Pasien Rawat Jalan sesuai dengan asuhan keperawatan SOAP \(Subjective Objective Assesment Planning\) untuk mencatat Therapy Pasien
* Pencatatan data sosial pasien, data morbiditas dengan pedoman sistem informasi rumah sakit
* Pencarian Riwayat Kunjungan Pasien yang pernah dilakukan Pasien pada masing-masing Poli Rawat Jalan
* Pengolahan Data Statistik Pasien hingga level RT, RW \(Data Sensus Pasien\)
* Tracking System Status Rekam Medik Pasien
* Layanan pelaporan standart Departemen Kesehatan
* Menghasilkan pelaporan manajemen seperti BOR, LOS, BTO, TOI dll.
* Layanan Laporan RL2a, RL2b, Register Pelayanan Pasien Rawat Jalan, Analisa Wabah
* Layanan Laporan-laporan \(RL2.1, RL2.2, RL2.3\) untuk Rawat Inap

**D. MODUL FARMASI**

Menangani masalah transaksi obat rawat jalan, rawat inap, rawat darurat maupun pembelian bebas, Kartu stok obat per Gudang, mutasi dengan multi gudang, hingga penyesuai stok akibat obat rusak atau hilang, semua tercatat dan terlaporkan. Daftar Kode Obat berbasis ISO.

RINCIAN APLIKASI :

SUB MODUL PENJUALAN

* Mendukung transaksi penjualan obat, mutasi obat antar gudang, retur penjualan resep
* Mendukung transaksi obat resep maupun transaksi obat bebas
* Mendukung transaksi internal rumah sakit meliputi pemakaian barang, mutasi barang, laporan stok per gudang
* Dukungan penyimpanan stok obat multi gudang
* Dukungan penyesuai stok akibat penambahan obat baru, obat rusak atau hilang, semua tercatat dan terlaporkan
* Retur penjualan resep dengan pengembalian stok berdasarkan masing-masing gudang UPT/ outlet \(multi gudang\)
* Terintegrasi dengan billing sistem rawat inap, hal ini memungkinkan pembayaran piutang obat bagi pasien rawat inap sehingga total penggunaan obat selama pasien dirawat bisa ditagihkan pada saat pasien pulang

SUB MODUL PEMBELIAN

* Mendukung input pembelian obat dari rekanan distributor/PBF mulai Order pembelian, Pembelian barang COD, Penerimaan barang, Retur pembelian Obat.
* Pencatatan Hutang Distributor bisa disesuaikan dengan Jatuh Tempo Pembayaran dari Distributor/PBF
* Pelunasan Hutang Distributor berdasar Jatuh Tempo Pembayaran dari Distributor/PBF, sehingga pembayaran hutang bisa dipantau.

SUB MODUL INVENTORY CONTROL

* Menggunakan multi gudang dengan sistem ini memungkinkan penyimpanan lebih dari satu gudang, sehingga distribusi obat dapat lebih mudah dipantau
* Dukungan Informasi Analisa Stock dan Kontrol Stock oleh pihak manajemen
* Terdapat metode Transfer barang/obat antar gudang yang memungkinkan terjadi serah terima barang/obat

**E. MODUL SARANA PENUNJANG LABORATORIUM**

Modul ini berfungsi untuk menampung dan mencatat hasil dari pemeriksaan Laboratorium dengan hasil yang bisa secara otomatis membandingkan langsung dengan nilai normal parameter tiap-tiap pemeriksaan laboratorium, sehingga hasil pemeriksaan Laboratorium sudah siap cetak.

**F. MODUL SARANA PENUNJANG RADIOLOGI**

Modul ini berfungsi untuk menampung dan mencatat hasil dari pemeriksaan Radiologi dengan hasil yang bisa secara otomatis membandingkan langsung dengan nilai normal parameter tiap-tiap pemeriksaan laboratorium, sehingga hasil pemeriksaan radiologi sudah siap cetak, berdasarkan template pemeriksaan hasil diagnosis.

Fitur :

* Aplikasi input hasil pemeriksaan laboratorium dan radiologi
* Master Parameter Pemeriksaan Lab dibuat sangat sederhana sehingga petugas dapat dengan mudah menambah atau menyesuaikan nilai normal parameter pemeriksa laboratorium dan radiologi
* Master Template Pemeriksaan Laboratorium dan Radiologi, menu ini gunanya untuk membuat format cetak hasil pemeriksaan laboratorium dan radiologi
* Terdapat Input Tindakan Jasa Pemeriksaan Laboratorium dan Radiologi dengan tarif yang bisa ditambah maupun disesuaikan oleh petugas tanpa harus mengubah program

**MODUL DAN FITUR SIMRS PAKET TAMBAHAN**

Berikut ini adalah modul dan fitur tambahan sebagai pelengkap paket program standar di atas, dengan pengerjaan akan kami selesaikan setelah Aplikasi Standar sudah berjalan dengan baik.

**MODUL SISTEM KEUANGAN**

Modul ini berfungsi untuk menampung dan mencatat seluruh transaksi pada rumah sakit untuk menghasilkan pelaporan pada level manajemen secara cepat dan akurat.

Fitur :

* Terintegrasi secara penuh dengan sistem akuntansi standar
* Mendukung pencatatan transaksi Kas Masuk dan Kas Keluar dengan laporan pendukungnya
* Mendukung pencatatan Hutang dan Piutang dengan laporan pendukungnya seperti Hutang Piutang Jatuh Tempo, Histori Pelunasan Hutang Piutang, Saldo Hutang Piutang
* Dukungan Jurnal Otomatis dan Manual
* Sistem pelaporan Real time sehingga laporan dapat diproses dan dicetak sewaktu-waktu tanpa menunggu proses tutup buku
* Laporan Jurnal Harian, GL, Neraca Saldo, Laba Rugi, Neraca dan Analisa Keuangan

