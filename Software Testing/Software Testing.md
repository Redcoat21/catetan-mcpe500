# Pertemuan 1, Introduction to Software Testing

## Introduction to Software Testing
- Software testing dapat diartikan sebagai suatu aktivitas untuk melakukan uji coba software supaya dapat digunakan oleh *end user* atau pengguna. Testing bisa membuktikan adanya *error* tapi tidak bisa membuktikan tiadanya *error*, hal ini disebabkan karena software itu sifatnya terus berkembang.
- Siklus dari SDLC (Software Development Life Cycle):
  1. Planning (Tahap Perencanaan)
	2. Analysis
	3. Design
	4. Implementation
	5. Testing & Integration
	6. Maintenance
- Ada juga dikenal sebagai STLC (Software Testing Life Cycle):
	 1. Requirement Analysis
	 2. Test Planning
	 3. Test Case Development
	 4. Test Environment Setup
	 5. Test Execution
	 6. Test Closure
- *Computer Bug* adalah sebuah kesalahan yang dapat terjadi dalam komputer, hal ini pertama kali disebutkan pada tahun 1947 di *Harvard University* saat sebuah komputer bernama *IBM Mark II* mengalami suatu malfungsi saat menjalankan program, ketika diperiksa ternyata di dalam komputer tersebut terdapat seekor ngengat (*Moth*/*Bug*) sehingga tersebutkan istilah *Bug* untuk mendeskripsikan sebuah program yang terjadi error.
## Sources of Problems
- Requirements Definition
  - Erroneous, incomplete, inconsisten requirements.
	- Hal ini umumnya diperlukan seorang *System Analyst* yang dimana tugasnya adalah untuk menganalisa sistemnya dan apa yang perlu dilakukan saat suatu kesalahan terjadi.
	- Umumnya *Bug* atau kesalahan harus ditemukan pada saat tahap ini, karena jika tidak ditemukan di tahap ini maka dapat menimbulkan kemunduran dalam *progress* pekerjaan ataupun menyebabkan kerugian finansial.
- Design
  - Fundamental design flaws in the software.
- Implementation
  - Careless coding, malicious code.
- Support Systems
  - Poor programming languages, faulty compilters, misleading development tools.
- Testing
  - Incomplete testing, poor verification, debugging mistakes.
	- Testing tidak boleh dilakukan hanya dengan 1 metode, dan sebaiknya dilakukan metode yang berbeda-beda.
- Evolution
  - Sloppy redevelopment
## Origin of Bugs
- Umumnya asal-usul dari *bug* adalah:
	- Specifications - 55%
	- Design - 25%
	- Code - 15%
	- Other - 5%
## Spectacular Software Failures
### THERAC-25 Radiation Therapy
- THERAC-25 adalah sebuah mesin terapi radiasi yang dikendalikan oleh komputer mengalami *bug* yang menyebabkan kematian, setidaknya terdapat 6 *malfunction* dari 1985 - 1987.
- Hal ini terjadi karena terjadi *Race condition*.
### Shooting down of Airbus 300
- USS Vincennes menembak sebuah pesawat komersil Airbus 300 pada tahun 1988, hal ini terjadi karena komputer pada USS Vincennes salah mengidentifikasi pesawat Airbus 300 sebagai pesawat *fighter* F-14. Hal ini menyebabkan kematian 290 jiwa.
- Hal ini terjadi karena output yang tidak jelas dan membingungkan dari software-nya.
### The Ariane 5 Disaster
- Pada tahun 1996, sebuah roket luar angkasa bernama Ariane 5 gagal karena 38 detik setelah peluncuran, roket tersebut meledak.
- Hal ini terjadi karena programnya mencoba mengkonversi float 64 bit menjadi *signed integer* 16 bit, menyebabkan *integer overflow*
### Mars Climate Orbiter
- Pada 1998, sebuah *probe* luar angkasa yang seharusnya meneruskan signal dari *Mars Polar Lander* malah menabrakkan diri ke planetnya daripada mendaratkan di orbit dengan selamat.
- Hal ini terjadi karena *bug* gagal mengkonversikan *Imperial system* ke *Metric system*.
## Software Testing Terminologies
- Verification vs Validation
	- Verifikasi berarti "Apakah kita membuat produk ini dengan tepat?"
		- Produk yang dibuat seharusnya sesuai dengan spesifikasi.
	- Sementara validasi berarti "Apakah kita membuat produk yang tepat?"
		- Produk yang dibuat seharusnya sesuai dengan apa yang diinginkan oleh user.
- Static vs Dynamic testing
	 - Static testing berarti melakukan testing tanpa melakukan pemrograman, dan umumnya dapat dilakukan di semua fase.
	 - Dynamic testing berarti melakukan testing dengan tujuan meng-evaluasi dan mengobservasi *behaviour* product, dan umumnya dilakukan saat *runtime*.
- Black-box vs White-box testing
	 - Black-box Testing berarti melakukan test pada suatu sistem tanpa pengetahuan atau tanpa informasi soal cara kerjanya sebelumnya. Seorang *tester* harus memberikan sebuah input dan melihat output yang dihasilkan oleh sistem. (Equivalence Partitioning)
	 - White-box testing atau clear, glass box, atau structural testing. Merupakan teknik testing yang meng-evaluasi *code* dan cara kerja sebuah program. (Basis Path Testing)
- Software Testing Stages.
   - Unit Testing (*testing* terhadap masing masing komponen).
   - Module Testing (*testing* sebuah *collection* dari komponen-komponen yang saling berhubungan).
   - Sub-system Testing (*testing* sebuah *collection* dari module-module yang saling berintegrasi dalam sebuah *sub-system*).
   - System Testing (*testing* sistem secara penuh dan keseluruhan sebelum *deployment*).
   - Acceptance Testing (*testing* yang dilakukan oleh user untuk melihat apakah sistem memenuhi keinginan user). Atau biasa dikenal juga sebagai (Alpha / Beta testing). Alpha testing umumnya dilakukan di lingkup internal, dan Beta testing dilakukan di lingkup eksternal.
- Miscellaneous Testing.
	 - Stress Testing, *testing* ini digunakan untuk menguji program seberapa tahan ketika diminta *resources* dalam jumlah yang banyak dan tidak biasa.
	 - Recovery Testing, *testing* sistem yang memaksa program untuk gagal / *error* sehingga *recovery* dapat dilakukan dengan baik.
	 - Security Testing *testing* untuk menguji mekanisme perlindungan dari sebuah sistem.
	 - Performance Testing *testing* untuk menguji *run-time performance* dari sebuah software.
	 - Compatibility Testing *testing* untuk menguji apakah program dapat dijalankan di hardware, *operating system*, aplikasi, *network environments* yang berbeda.
	 - Usability Testing *testing* untuk menguji seberapa mudah sebuah *design* digunakan oleh kelompok demografi user.
- Test Automation.
	 - Adalah teknik untuk menggunakan *software* lain untuk melakukan *testing* pada sebuah program.
	 - Umumnya digunakan untuk mengontrol proses eksekusi dari test dan membandingkan hasil output yang terjadi dan hasil output yang diharapkan.
	 - *Test automation* penting dalam proses CI/CD atau *Continuous Integration and Continuous Delivery*
	 - Contohnya adalah:
	 - Regression testing adalah *testing* yang menjalankan ulang test yang fungsional dan non-fungsional untuk memastikan software yang sudah ditest sebelumnya tidak mengalami perubahan.
## Summary
- Lakukan Testing seawal mungkin
- Testing adalah aktivitas yang terus menerus
- Saat mendesain software, sebaiknya di desain untuk *test*-able
- *Test activities* sebaiknya di rencanakan, kontrol, dan dokumentasi dengan baik baik.

# Pertemuan 2, 24 September 2024

## Fundamental Software Testing

### Apa itu testing?
- Testing adalah suatu aktivitas untuk melakukan uji coba dengan kondisi tertentu, dan juga dilakukan sesuai kebutuhan bagi *end user* atau pengguna.
- Perlu diingat, bahwa perbedaan testing dan *debugging* adalah:
  - Testing berarti kita mencari *bug* dalam program kita.
  - Namun debugging artinya kita sudah tau *bug* nya apa, namun kita masih belum tau *bug* nya dimana dan berusaha memperbaiki *bug* yang ada.
### Why testing?
- Testing memeriksa apakah semua *requirement* sistem di implementasi secara benar dan *bug* dapat dideteksi sebelum deployment.
- Testing juga digunakan untuk mengukur kualitas sebuah software dan membantu menentukan apakah software sudah pantas untuk diluncurkan atau belum.
- Karena *bug* dapat ditemukan lebih awal, maka biaya pun bisa ditekan karena *bug* ditemukan lebih awal.
- Umumnya waktu yang dilakukan untuk melakukan testing adalah sekitar 50% dari awal sampai akhir masa pembuatan software.
### Prinsip testing
- Testing bisa menunjukan bahwa ada atau tidaknya suatu *bug*, namun tidak dapat membuktikan bahwa program yang di test tidak ada *bug* nya.
- *Exhaustive testing* (testing semuanya) itu mustahil.
- Testing sebaiknya dilakukan seawal mungkin dalam siklus **SDLC**
- Untuk masing masing produk diperlukan tipe atau teknik testing yang berbeda juga. Contohnya untuk tsting web dan mobile teknik dan *tools* yang digunakan juga bisa berbeda, untuk mobile mungkin digunakan **Catalon** dan untuk web mungkin digunakan **Selenium**.
### Seberapa banyak testing yang diperlukan?
- Tidak mungkin untuk melakukan testing pada keseluruhan sebuah program, karena kombinasi antara *event*, *dependency* manapun atau bahkan semua komponen dalam sistem bisa membuat program rusak. Jadi tidak mungkin untuk mengatakan bahwa program sudah ditest secara 100%.
- Testing juga memerlukan tenaga, waktu dan uang. Sehingga testing tidak mungkin dijalankan terus-terusan, harus ada titik berhentinya.
- *Risk Management* adalah salah satu aktivitas yang penting dalam sebuah **SDLC**. Menentukan seberapa banyak testing yang diperlukan seharusnya mempertimbangkan seberapa tingginya *risk* sebuah program (technical and business tricks).

## Tipe tipe Software Testing
### Static Testing (Reviews, Inspection, Walkthrough)
  - Static testing dapat dilakukan dalam tiap fase dalam **SDLC**.
  - Umumnya static testing tidak diperlukan pengetahuan mendalam soal program, hanya diperlukan dokumentasi.
  - *Design*, *code*, *test plan*, *test cases* ataupun dokumen-dokumen lain yang sudah diperiksa dan di *review* terhadap suatu *checklist* yang sudah dibuat.
  - *Error* yang ditemukan bisa berupa *missing requirement*, *design defects*, *non-maintainable code*, *inconsistent interface specifications*.
    - Reviews
      - Reviews me-representasi sebuah *project milestone* dan mendukung basis dari berdirinya suatu produk software.
      - Reviews mempertemukan bersama para stakeholders (customers/users) untuk memberikan *feedback* ke developer sebagai bentuk komunikasi dengan customer.
      - Studi mengatakan bahwa reviews dapat meningkatkan produktivitas dari sebuah tim software development yang juga dapat berdampak pada kualitas software.
      - Mengurangi jumlah error awal dalam **SDLC** yang juga berarti lebih sedikit waktu untuk testing dan *maintenance*.
    - Inspection
      - Merupakan testing yang termasuk sangat formal dan dikarakteristik-kan sebagai testing yang menggunakan prosedur dan keperluan yang di-dokumentasi.
      - Umumnya melibatkan sesama pembuat untuk menemukan error dalam dokumen yang sedang di *review* dan mendiskusikannya dalam sebuah rapat review.
      - Tujuannya adalah untuk membantu pembuat meningkatkan kualitas dari dokumennya.
      - Fasenya meliputi *planning*, *kick off*, *preparation*, *review meeting*, *rework*, dan *follow-up*
    - Walkthrough
      - Walkthrough dikarakteristik-kan dari pembuat dokumen yang membimbing partisipan melalui dokumen atau pemahamannya soal proses, untuk mendapatkan kesepatakan bersama.
      - Walktrhough ini dipimpin oleh sang pembuat dan umumnya ditemani seorang penulis yang membantu mencatat error-error yang ada.
      - Walkthrough dapat digunakan ketika orang non-teknis untuk mengerti dokumen yang dibuat seperti dokumen keperluan atau spesifikasi arsitektur.
  - Umumnya urutan dalam *Static Testing* adalah Reviews -> Walkthrough -> Inspection.
### Dynamic Testing (White-box, Black-box)
  - Merupakan teknik testing yang berdasarkan *execution*.
  - Output dari sebuah program, atau sistem dibandingkan dan dicek dengan hasil yang diinginkan.
  - Dynamic testing dapat dikategorikan sebagai:
    1. White-box testing
      - Umumnya memerlukan *Source code* dan pemahaman dari suatu program.
      - Dikenal juga sebagai **Structural Testing**.
      - White-box testing dapat digunakan untuk:
        - Melakukan test terhadap logic suatu program.
        - Meng-eliminasi code yang *redundant*. (*clean code*, *dead code*)
        - Meng-evaluasi hasil dengan *execution paths* yang berbeda.
        - Advantages:
          - Logika dari sebuah sistem dapat ditest.
          - *Redundant code* bisa di eliminasi.
          - Hemat biaya ketika teknik yang digunakan sesuai.
        - Disadvantages:
          - Tidak bisa menjamin bahwa kebutuhan user terpenuhi.
          - Mungkin tidak menggambarkan situasi nyatanya.
          - Level kemampuan yang diperlukan termasuk tinggi.
      - Biasanya dilakukan oleh *developernya* sendiri.
    2. Black-box testing
      - Umumnya tidak memerlukan *Source code* atau pemahaman dari suatu program.
      - Black-box testing memandang aplikasi yang ditest sebagai sebuah kotak hitam dan apapun yang terjadi pada internal program tidak dianggap.
      - Testing terjadi berdasarkan *Requirement Specifications*.
      - Testing berfokus pada fitur dan bukan pada implementasi.
      - Umumnya dilakukan setelah Unit dan Integration test dilakukan.
      - Advantages:
        - Menggambarkan situasi nyatanya.
        - Tidak membuat asumsi tentang program, menjalakannya apa adanya.
        - Umumnya lebih mudah dilakukan.
      - Disadvantages:
        - Untuk *logical errors* mungkin saja terjadi.
        - *Redundant Testing* lebih ungkin terjadi.
      - Biasanya dilakukan oleh timnya sendiri yaitu tim QA (*Quality Assurance*)
### Functional Testing (Unit, Integration, System, Acceptance)
  - Functional Testing berarti memverifikasi apakah sebuah module melakukan hal yang seharusnya dilakukannya sesuai dengan spesifikasi.
  - Tujuannya adalah untuk memastikan bahwa aplikasi berjalan seperti seharusnya.
  - Functional Testing bisa meliputi:
    - Non-formal Testing:
      - Melibatkan pihak pihak lain.
      - Contoh: Stress Testing, User Acceptance Testing
    - Formal Testing:
      - Contoh: Unit Testing, Integration Testing, System Testing
  - Dalam Integration Testing dikenal adanya *Stub* dan *Driver*:
    - *Stub* digunakan dalam *Top-Down Integration* dan digunakan untuk menggantikan modul bawah yang belum siap dan dipanggil oleh modul atas. Umumnya digunakan untuk menguji antarmuka pengguna tanpa perlu menunggu *backend*.
    - *Driver* digunakan dalam *Bottom-Up Integration* dan digunakan untuk menggantikan modul atas yang belum siap dan dipanggil oleh modul bawah. Umumnya digunakan untuk menguji backend meskipun UI nya belum jadi.

# Kesimpulan
- Seorang *Software Developer* perlu mengalokasi waktu yang cukup untuk melakukan testing dalam siklus **SDLC**.
- Testing sebaiknya dilakukan seawal mungkin.
- Sebaiknya melakukan White-box dan Black-box testing dalam tahap siklus **SDLC**.

# Pertemuan 3, 1 Oktober 2024

## White-box testing
- Dikenal juga sebagai Structural / Glass Box / Clear Box testing.
- Tujuannya adalah untuk menguji semua statement program.

### Basis Path Testing
- Step by step:
  1. Menggambar flow graph.
  2. Menghitung *cyclomatic complexity* nya.
  3. Menentukan *independent path* nya.
  4. Derive the test cases to exercise those paths.
- Flow Graph:
  Notasi yang dipakai hanya ada 2 yaitu, *node* dan *flow*.
- Cyclomatic Complexity / V(G) dihitung dengan salah satu dari tiga cara:
  - V(G) = **Jumlah daerah tertutup sebuah flow graph** + 1.
  - V(G) = E - N + 2
    Dimana E adalah jumlah dari *edges* dan N adalah jumlah dari *nodes* di dalam sebuah flow graph.
  - V(G) = P + 1
    Dimana P adalah jumlah *nodes* predikat (output dari node yang outputnya lebih dari 1) di dalam flow graph.