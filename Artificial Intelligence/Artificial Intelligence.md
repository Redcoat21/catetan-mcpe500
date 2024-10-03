# Pertemuan 1, 19 September 2024

## Kenapa AI?

- Manusia itu tidak efisien.
- Manusia itu cerdas, dan komputer tidak cerdas, sehingga para peneliti berusaha mempelajari dan menirukan bagaimana persepsi dan kecerdasan manusia.
- AI tidak mungkin menggantikan manusia sepenuhnya, karena meskipun AI dapat melakukan hal sederhana (Code simple), namun pada akhirnya AI tidak akan bisa membuat sesuatu seperti membuat keputusan penting, membagi pekerjaan, merancang dan mendesain sistem.

## Artificial Intelligence

- Component
  - Perception, _perception_ adalah meng-organisir, meng-identifikasi, dan interpretasi dari informasi sensorik dengan tujuan untuk mewakili dan mengerti informasi atau lingkungan yang diberikan. Perception berarti bagaimana, input dari sensor bisa diterjemahkan.
  - Thinking, _thinking_ adalah _flow_ atau jalur dari bagaimana ide dan asosiasi bisa menghasilkan kesimpulan yang _logical_.
  - Action, _action_ adalah melakukan sesuatu berdasarkan kesimpulan _logical_ yang dihasilkan dari _thinking_.
- Definisi AI adalah pembuatan sistem komputer yang dapat melakukan hal yang biasa manusia lakukan, seperti membuat keputusan, mendeteksi dan pengenalan objek, penyelesaian masalah yang komples, dan lain-lain.
- Stuart Russel dan Peter Norvig mengelompokkan definisi dari AI menjadi 4 kategori yaitu :
  - Thinking Humanly
    - Berfokus pada simulasi proses berpikir manusia.
    - Tujuannya adalah untuk membuat mesin yang dapat meniru cara berpikir manusia, termasuk pemahaman, pembelajaran, dan pengambilan keputusan.
    - Metode yang sering digunakan di sini adalah ilmu kognitif dan pemodelan.
    - Pada tahun 1950 **Alan Turing** merancang ujian apakah komputer dapat mengelabui manusia dan dianggap seperti manusia, pendekatan yang dilakukan terbagi menjadi 2 cara yaitu :
      - Introspeksi : berusaha menangkap pemikiran - pemikiran saat kita berpikir.
      - Eksperimental :
  - Acting Humanly
    - Dalam kategori ini, tujuannya adalah untuk membuat mesin yang dapat bertindak seperti manusia.
    - Ini mencakup kemampuan untuk berkomunikasi dalam bahasa alami, mengenali objek dan suara, serta menunjukkan emosi dan kepribadian.
    - AI harus mengerti :
      - Natural Language Processing
      - Knowledge Based and Reasoning
      - Computer Vision
      - Machine Learning
      - Robotics
  - Thinking Rationally
    - Definisi ini berfokus pada rasionalitas sebagai dasar dari kecerdasan.
    - Sebuah sistem dianggap cerdas jika ia dapat melakukan inferensi yang logis.
    - Logika formal sering digunakan sebagai alat untuk mencapai tujuan ini.
  - Acting Rationally
    - _Act rationally_ untuk mencapai sebuah tujuan.
    - Di sini, fokusnya adalah pada tindakan yang menghasilkan hasil terbaik dalam situasi tertentu, berdasarkan informasi yang ada dan prinsip-prinsip rasional.
    - Algoritma pencarian dan perencanaan, serta teori keputusan.
    - Untuk berpikir secara rasional, maka berarti berpikir dengan benar
    - Pemikiran yang benar : Akan selalu memberikan jawaban yang benar ketika diberikan premis yang tepat.

## Stages of AI

- Artificial Narrow Intelligence
  - Juga dikenal sebagai _Weak AI_, **ANI** adalah fase dimana AI hanya dapat melaksanakan _tasks_ yang sudah diatur sebelumnya.
  - Contoh : Siri, Google Assistant, Face Recognition, Face Detection
- Artificial General Intelligence
  - Juga dikenal sebagai _Strong AI_, **AGI** adalah fase dimana AI sudah mendekati kemampuan manusia.
- Artificial Super Intelligence
  - **ASI** adalah fase dimana AI sudah melebihi kemampuan manusia.
  - Contoh : **Ultron** dari Marvel.
- Reactive Machine AI
  - Adalah sebuah mesin yang beroperasi hanya dari data saat ini, dan hanya mempertimbangkan situasi saat ini, tidak mempertimbangkan masa lalu dan masa depan. _Reactive Machine AI_ tidak dapat menyimpulkan dari data untuk mengevaluasi masa depan.
  - Contoh : **Deep blue** sebuah mesin yang dapat memainkan catur.
- Limited Memory AI
  - Adalah AI yang dapat membuat keputusan dari mempelajari data masa lalu dan memori. AI jenis ini biasanya memiliki umur yang pendek.
  - Contoh : Self driving car.
- Self-Aware AI
  - Merupakan mesin yang memiliki _consciusness_ atau kesadaran mereka sendiri.

# Pertemuan 2, 3 Oktober 2024

## State Space Representation
Berarti model matematika dari sebuah sistem physical yang berupa kumpulan input, output dan variabel *states.*

State Space mengarah ke ruang yang sumbunya merupakan variabel *states*.

States dari sistem bisa direpresentasikan sebagai bentuk *tree* atau *vertex* dalam *directed graph*

State space terdiri dari :
	- Kumpulan states yang *finite*.
	- Start state dari permasalahan
	- Goal states atau solusi dari permasalahan
	- Kumpulan operator

## State Space Search
- SSS bisa diterapkan untuk berbagai macam permasalahan, contohnya:
	- Puzzle solving
	- Jarak terpendek
	- Pathfinding
- SSS dapat dideskripsikan sebagai proses untuk menemukan urutan state untuk mencapai goal state nya.
- Permasalahannya terletak pada bagaimana cara kita menemukan urutan dari state tersebut dari start state yang diberikan.
- SSS dapat direpresentasikan sebagai *directed graph* atau sebuah *tree*