# Pertemuan 1, 23 September 2024

## Apa itu Software Evolution?
  - Melanjutkan software yang sudah pernah dibuat oleh para pendahulu-pendahulu kita
  - Karena kemungkinan besar pada praktikalnya, seorang *software engineer* lebih besar kemungkinannya melanjutkan sebuah proyek *legacy* atau yang sudah pernah dibuat dibandingkan membuat *software* baru dari nol.
## Apa saja yang akan dipelajari disini?
  1. Software Maintenance
     	- Biaya dari *Software Maintenance* pasti selalu lebih besar dibandingkan *Software Development*
  2. Metodologi *Software Maintenance*
     	- Reverse Engineering
     	- Alteration
     	- Software Engineering
     	- Semua tahap tersebut dikenal sebagai *The Stages Models*
  3. Devops
     	- *Devops* memiliki keunggulan dimana *operational* dan *development* bisa berjalan bersamaan.
  4. Software Re-engineering
   	  - Merupakan lawan dari *Software Evolution* dimana *Software Evolution* melakukan *maintenance* pada *software* yang sudah ada, *Software Re-engineering* melakukan pembuatan ulang dari *software* yang sudah pernah ada.
  5. Software Configuration Management
     	- Umumnya juga disebut sebagai *versioning*.
  6. Software Refactoring
     	- Merapikan / menstruktur ulang sebuah *code* dari program agar lebih rapi tanpa mengubah fungsionalitas dari *code* tersebut.
     	- *Maintenance cost* dari *code* yang sudah di *refactor* umumnya pasti lebih kecil dibandingkan *code* yang belum di *refactor*.
  7. Software Repository
      - Berupa Dokumentasi baik bagi eksternal ataupun internal.
      - Untuk dokumentasi internal umumnya lebih baik berupa *comment*, sedangkan untuk eksternal biasanya berupa model seperti *data dictionary*, *erd*, *dfd*.

# Pertemuan 2, 30 September 2024

# Pertemuan 3, 3 Oktober 2024

## SPE (Specified, Problem, Evolving)
- S-type (Specified) programs memiliki karakteristik sebagai berikut:
	- Semua properti program yang non-fungsional ataupun yang fungsional, yang penting bagi *stakeholders* di definisikan secara formal.
	- Ketepatan program dengan mematuhi spesifikasinya hanyalah kriteria yang dapat diterima sebagai solusi bagi *stakeholders*
	- Problemnya jelas, langkahnya jelas dan tidak berevolusi
- P-type (Problem) program yang dibuat untuk menyelesaikan sebuah permasalahan. 
	- Contohnya adalah : program yang dapat menyelesaikan catur.
	- Jenis program yang dihasilkan dari perubahan ini tidak dapat dianggap sebagai solusi dari sebuah masalah baru, tapi hanya bisa dianggap sebagai modifikasi dari solusi yang sudah ada. Namun yang dapat terjadi adalah, dunia berubah sehingga problemnya juga berubah.
	- Berbeda dengan S-type, jenis program ini akan berevolusi.
- E-type (Evolving)
	- Dimana program ini akan berubah sesuai kebutuhan, apabila kebutuhan berubah maka program juga akan ikut berubah.
	- Berbeda dengan P-type, requirements dari E-type akan terus berubah, dan dari sini maka program jenis ini pasti akan berevolusi.
## Laws of Software Evolution

| Law Number |                Names of the Laws                |                                                                                                                                       Descriptions                                                                                                                                        |
| :--------: | :---------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|     I      |            Continuing Change (1974)             |                                                                                               E-type programs must be continually adapted, else they become progressively less satisfactory                                                                                               |
|     II     |          Increasing Complexity (1974)           |                                                                                           As an E-type program evolves, its complexity increases unless work is done to maintain or reduce it.                                                                                            |
|    III     |             Self Regulation (1974)              |                                         The evolution process of E-type programs is self-regulating, with the time distribution of measures of process and products being close to normal. (Update dilakukan berkala dan umumnya sedikit-sedikit)                                         |
|     IV     | Conservation of organizational stability (1978) | The average effective global activity rate in an evolving E-type program is invariant over the product's lifetime. (Evolusi software erat hubungannya dengan developer yang bekerja di organisasi tersebut, semaking stabil sebuah organisasi maka proses evolusinya juga semakin rendah) |
|     V      |       Conservation of familiarity (1978)        |                                                                                        The average content of successive releases is constant during the life-cycle of an evolving E-type program                                                                                         |
|     VI     |            Continuing growth (1991)             |                                                                       To maintain user satisfaction with the program over its lifetime, the functional content of an E-type program must be continually increased.                                                                        |
|    VII     |            Declining Quality (1996)             |                                                                           An E-type program is perceived by its stakeholders to have declining quality if it is not maintained and adapted to its environment.                                                                            |
|    VIII    |          Feedback system (1971 - 1996)          |                                                                                        The evolution processes in E-type programs constitute multi-agent, multi-level, multi-loop feedback systems                                                                                        |

Hukum 4,5,6,8 erat hubungannya dengan organisasi yang menggunakan software, sementara hukum 1, 2,3,7 erat hubungannya dengan software itu sendiri

## Declining Quality
- Sebuah program E-type dianggap kualitasnya menurun apabila tidak di *maintain* dan diadaptasikan dengan lingkungannya.
- Hal hal itu bisa dilihat dari:
	- Terdapat penurunan kepuasan yang signifikan karena entropi yang terus bertumbuh, makin banyaknya error, dll.
	- Faktor diatas juga menyebabkan penurunan kualitas dari perspektif user.
	- Penurunan kualitas seiring berjalannya waktu berhubungan dengan pertumbuhan entropi yang sering diasosiasikan dengan *code decay*
	- Maka dari itu, penting untuk melakukan tindakan preventif untuk menurunkan entropi dengan cara memperbaiki arsitektur dari software, high-level dan low-level design, dan coding.
### Code Decay
- Berhubungan dengan hukum ke 7 Lehmann, sebuah code dikatakan sudah membusuk apabila ketika code tersebut sudah sangat sulit untuk diubah yang ditunjukkan dengan 3 respon:
	1. The cost of change, which is effective only on the personnel cost for the developers who implement it.
	2. The calendar or clock time to make the changes; and
	3. The quality of the changed software
- Penting untuk dicatat bahwa *code decay* merupakan kebalikan atau antithesis dari evolusi, dengan artian evolusi berusaha membuat code menjadi lebih baik, perubahan umumnya bersifat degeneratif yang mengarah pada code decay.

## Evolusi dari Sistem FOSS (Free Open Source Software)
- Terdapat perbedaan utama dari evolusi software FOSS dan COTS (Commercial off the shelf), dan dapat dibedakan dari:
	1. Team structure
	2. Process
	3. Releases
	4. Global Factors
- Contoh dari FOSS seperti: Linux (Diciptakan oleh **Linus Benedict Torvald**)
- Contoh dari COTS seperti: Windows, OS X

# Pertemuan 4,  7 Oktober 2024

## Reuse Oriented Model
- Iterative vs Incremental
	- Istilah *Iteration* dan *Increment* umumnya digunakan untuk membahas development iterative dan incremental.
	- *Iteration* menunjukkan bahwa sebuah proses adalah sebuah siklus, maka dari itu artinya aktivitas dari proses akan diulang terus secara terstruktur.
	- *Iterative* didasarkan dari strategi *scheduling* darimana sebagian waktu disisihkan untuk mengembangkan dan memperbaiki bagian dari sistem yang sedang dibangun.
	- *Incremental* didasarkan dari strategi *staging* dan *scheduling* yang dimana bagian dari sistem akan dikembangkan dalam waktu yang berbeda, lalu diintegrasikan ketika sudah selesai.
- Cohesion dan Coupling
	- Coupling artinya ketergantungan antar modul, contoh sederhanaya adalah *global variable*.

## The Staged Model For CSS
- Rajlich dan Bennet pernah mempresentasikan model yang deskriptif soal *software evolution* yang disebut dengan **staged model of maintenance and evolution**.
- Tujuan utamanya adalah untuk mengembangkan pemahaman akan seberapa lama sebuah software berevolusi, dan bukan untuk membantu dalam manajemen.
- Modelnya dibagi menjadi 4 fase yaitu:
	- **Initial Development**
		- Saat pertamakali membuat software.
	- **Evolution**
		- Saat sebuah software ditambahkan fitur fitur.
	- **Servicing** 
		- Saat software sudah hampir mencapai akhir hidupnya, karena kebanyakan orang yang mengerti soal program ini sudah pergi.
		- *Software Re-engineering* umumnya mulai dilakukan dalam tahap ini.
	- **Phase out**
		- Saat software mulai ditinggalkan atau di buat ulang, karena biaya maintenance yang terlalu besar atau para *maintainer* sudah pergi semua.
		- Hasil akhirnya adalah software ini akan di *shut down*.
	[[Staged Model For CSS.canvas|Staged Model For CSS]]

## The Staged Model For FLOSS
- Secara umum, perbedaan dari FLOSS dan CSS adalah semua orang bisa menjadi developer dalam FLOSS, developer FLOSS yang lama akan terus digantikan oleh orang yang baru, maka dari itu dalam siklus FLOSS tahap *Phaseout* bisa transisi ke fase *Evolution*.

## Software Configuration Management
- Software Configuration Management (SCM) dibuat untuk mengatur perubahan dalam sebuah sistem yang besar.
- Analoginya adalah seperti: Ketika sebuah software sedang dibuat perubahan, software yang sudah di-*deploy* saat ini tidak boleh berhenti.
- Tujuan dari SCM adalah:
	- Mengidentifikasi setiap versi dari setiap software pada titik waktu tertentu.
	- Tetap memiliki versi software yang lama dan dokumentasi yang lama.
	- Memberikan jejak audit dari setiap perubahan yang dilakukan.
	- Sepanjang software life-cycle, merawat integritas dan *traceability* dari perubahan sistem.
- SCM diberlakukan pada software artifact yang meliputi *Executeable Software*, *Source code*, *Hardware* dan *Disks*.

## SCM Spectrum of Functionality
- Version Control
	- Untuk menghindari kebingungan ketika proses dari evolusi artifak, sebuah *identifier* dibuat dan dibagikan ke artifak setiap kali artifak tersebut diubah.
	- Ide dasar dari Version Control adalah memiliki 2 versi file, master dan working copies, dimana master copies akan disimpan dalam repository utama.
	- Software Developer *check out* working copies dari repositori, lalu mengubah working copies, dan akhirnya kalau sudah selesah *check in* working copies ke repository.
	- *Checking in* artinya *commit* perubahan dari working copies.
- *Conflicts* dapat muncul ketika banyak software developer ingin menggunakan file dengan versi yang sama.
- *Conflicts* dapat diselesaikan dengan 2 cara, yaitu: *lock-modify-unlock* dan *copy-modify-merge*.
