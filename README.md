# <p align="center">Maze Adventures: Maze Game using Depth-First Search and Breadth-First Search </p>

## Autors

| Name  | University Registration  | GitHub | Email |
|---|---|---|---|
| Daniel Maike Mendes Gonçalves  | 16/0117003  | [DanMke](https://github.com/DanMke) | danmke@hotmail.com |
| Lucas Pereira de Andrade Macêdo  | 15/0137397  | [lukassxp](https://github.com/lukassxp) | lpalucas.10@gmail.com |

## Cara Instalasi
Ke command prompt kemudian jalankan pip3 install -r requirements.txt --user
dan eksekusi menggunakan python3 graph-list1.py

## Penjelasan game Maze

<p align="justify"> Game ini atau dalam bahasa indonesianya adalah labirin merupakan game dimana berisi kumpulan jalur acak, pengguna harus menemukan jalan dari pintu masuk ke goal. Ini termasuk ke dalam game teka-teki tur yang bercabang di mana pemain harus menemukan rute yang benar,
dan untuk menyederhanakan pola non-percabangan yang mengarah secara jelas melalui tata letak yang berbelit-belit ke tujuan. </p>

### Pembuatan Maze/Labirin

<p align="justify"> Ada banyak langkah dan algoritma yang dapat digunakan untuk membuat labirin. Dengan merancang tata letak lorong serta dinding pada labirin. Disini tersedia dua mekanisme utama dari pembuatan labirinnya sendiri yaitu "lintasan yang mengukir" serta "menambahkan dinding". </p>

### Memecahkan Puzzle Labirin

<p align="justify"> Memecahkan labirin berarti pemain harus menemukan rute dari pintu masuk menuju goal dari awal hingga akhir. Banyak metode yang dapat digunakan untuk memecahkan labirin. Labirin juga terbagi menjadi beberapa kategori salah satunya adalah labirin yang tidak memiliki loop (labirin standar). </p>

## Maze Adventure

### Maze generation algorithm
<p align="justify"> Pembuatan labirin ini menggunakan dua algoritma yang familiar di telinga kita yaitu Depth-First Search dan Breadth-First Search. </p>
<p align="justify"> Algoritma DFS merupakan algoritma yang secara terurut atau teratur dimulai dari urutan terakhir. Terbalik dengan BFS, ia akan melewati semua kemungkinan yang ada dari titik terakhir kemudian baru lah berpindah ke titik awal sebelumnya sampai ke titik pertama. Ini merupakan metode menjelajahi suatu pohon atau pun labirin. Ia akan menjelajahi rute jika goalnya tidak ada di rute tersebut maka akan kembali ke rute sebelumnya dan mencoba rute lain. </p>
<p align="justify"> Sedangkan algoritma BFS merupakan algoritma yang biasanya digunakan untuk mencari rute sederhana melalui semua titiknya. Dimulai dari titik awal, kemudian lanjut ke titik cabang secara terurut. Jika belum ditemukan maka perhitungan diulang lagi dari masing-masing titik cabang sampai akhirnya goal ditemukan. </p>

#### Pelacak mundur menggunakan Depth-First Search

- 1. Buat sel awal menjadi sel saat ini dan tandai sebagai telah dikunjungi. (Menandai rute yang telah dilewati) <br> 
- 2. Meskipun ada rute yang belum dilewati <br>
     - 1. Jika rute saat ini memiliki rute berdekatan yang belum dikunjungi <br>
         - 1. Pilih secara acak salah satu rute terdekat yang belum dikunjungi <br>
         - 2. Dorong rute saat ini ke tumpukan <br>
         - 3. Lepaskan dinding antara rute saat ini dan rute yang dipilih <br>
         - 4. Jadikan rute yang dipilih sebagai rute saat ini dan tandai sebagai telah dikunjungi <br>
     - 2. Lain jika tumpukan tidak kosong <br>
         - 1. Keluarkan rute dari tumpukan <br>
         - 2. Jadikan itu rute saat ini <br>

<br> ![generate-maze](gifs/generate_maze.gif) <br>

### Algoritma pemecah labirin

#### Breadth-First Search

- 1. Tentukan node awal, tandai sebagai dieksploitasi <br>
- 2. Tambahkan ke antrian <br>
- 3. Sementara antrian tidak kosong dan Anda belum menemukan ujung labirin <br>
       - 1. Hapus node pertama dari antrian, ** U ** <br>
       - 2. Untuk setiap tetangga ** V ** dari ** U ** <br>
         - 1. Jika Anda belum menjelajahi <br>
             - 1. Tandai ** U ** sebagai induk dari ** V ** <br>
             - 2. Tandai ** V ** sebagai dieksplorasi <br>
             - 3. Letakkan ** V ** di akhir antrian. <br>
             - 4. Jika ** V ** adalah ujung labirin <br>
                 - 1. Akhir ditemukan <br>
- 4. Tentukan node saat ini sebagai ujung labirin <br>
- 5. Sedangkan ayah dari node induk tidak kosong <br>
     - 1. Tetapkan simpul saat ini sebagai orang tuamu, untuk berjalan kembali <br>
       
<br> ![solving-maze](gifs/solving_maze.gif) <br>

## References

> * https://gifs.com/ <br>
> * https://en.wikipedia.org/wiki/Maze <br>
> * https://en.wikipedia.org/wiki/Maze_generation_algorithm <br>
> * https://en.wikipedia.org/wiki/Maze_solving_algorithm
