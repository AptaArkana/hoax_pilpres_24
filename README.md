# Klasifikasi Hoax Pilpres 2024
<p align='justify'>Projek klasifikasi hoax Pilpres merupakan upaya untuk mengembangkan sistem yang dapat mengidentifikasi dan membedakan informasi yang bersifat palsu atau hoaks terkait pemilihan presiden (Pilpres). Tujuan dari proyek ini adalah untuk meningkatkan pemahaman masyarakat tentang kebenaran informasi selama periode pemilihan presiden, sehingga dapat mengurangi penyebaran berita palsu yang dapat memengaruhi opini publik dan proses demokrasi. Metode klasifikasi yang digunakan dalam proyek ini mencakup penggunaan teknik pembelajaran mesin dan analisis data untuk membedakan antara informasi yang dapat dipercaya dan yang tidak. Proyek ini diharapkan dapat memberikan kontribusi positif terhadap integritas dan keamanan proses demokrasi dalam konteks pemilihan presiden.</p>

## Dataset 
<p align='justify'>Dataset ini dikumpulkan melalui teknik scraping dari kanal berita online terkemuka seperti <b>Detik</b>, <b>Metro</b>, dan <b>CNN</b>. Informasi yang terkandung dalam dataset mencakup berbagai topik dan isu yang dilaporkan oleh sumber - sumber berita tersebut. Selain itu, berita kategori "hoax" spesifiknya dikumpulkan dari sumber <b>TurnBackHoax</b>. Proses scraping bisa dilihat pada <a href="https://github.com/AptaArkana/scraping_berita">link ini</a>. Dengan pendekatan ini, dataset mencakup berita dari sumber-sumber terpercaya dan juga berita yang telah diidentifikasi sebagai hoax oleh sumber yang mengkhususkan diri dalam memerangi informasi palsu.</p>

## Ciri Ciri Judul Berita Hoax
<p align='justify'>Judul berita yang mungkin mengindikasikan Hoax biasanya memiliki beberapa ciri tertentu. Beberapa ciri umum judul berita hoax melibatkan:</p>
<ol type="1">
  <li><p align='justify'><b>Sensasionalisme Berlebihan</b>: Judul berlebihan yang berusaha menarik perhatian dengan menyajikan klaim atau peristiwa yang sangat dramatis atau luar biasa.</p></li>
  <li><p align='justify'><b>Gaya Bahasa yang Emosional atau Provokatif</b>: Penggunaan kata-kata emosional atau provokatif untuk memanipulasi emosi pembaca tanpa memberikan dasar fakta yang kuat.</p></li>
  <li><p align='justify'><b>Tanda-Tanda Penulisan yang Buruk</b>: Penulisan yang buruk, banyak kesalahan tata bahasa, atau penggunaan huruf kapital berlebihan bisa menjadi indikasi kekurangan profesionalisme.</p></li>
  <li><p align='justify'><b>Ketidaksesuaian dengan Konteks atau Kronologi</b>: Judul yang tidak cocok dengan konteks atau urutan kronologis peristiwa yang sebenarnya dapat menunjukkan upaya manipulasi.</p></li>
</ol>  
Contoh : <b>IDI: Kematian Petugas KPPS PEMILU 2019 Bukan Karena Kelelahan tapi Karena DIRACUN</b>

## EDA Berita Fakta
<img style="display:flex; width:auto; height:auto;" alt="Word Cloud Berita Fakta" src="https://github.com/AptaArkana/hoax_pilpres_24/assets/79633073/dfe3c51c-6bda-452e-a1fc-6f97021627d6">
<p align='justify'>Meskipun mendekati akhir masa jabatannya, <b>Jokowi</b> tetap menjadi topik yang sering dibicarakan, menunjukkan keberlanjutan perhatian publik terhadap kepemimpinannya. Di antara calon-calon potensial untuk periode berikutnya, <b>Anies</b>, <b>Prabowo</b>, dan <b>Ganjar</b> juga muncul sebagai tokoh yang banyak diperbincangkan, mengindikasikan minat dan spekulasi terkait pemilihan presiden mendatang.</p>

## EDA Berita Hoax
<img style="display:flex; width:auto; height:auto;" alt="Word Cloud Berita Fakta" src="https://github.com/AptaArkana/hoax_pilpres_24/assets/79633073/44bd7c4c-3132-48cb-94de-c3ec2e9115e0">
<p align='justify'>Berdasarkan data, dapat diidentifikasi bahwa subjek utama dalam konteks berita hoax lebih sering membicarakan <b>Jokowi</b> dan <b>Anies</b>. Selain itu, objek hoax yang banyak dibicarakan terutama terfokus pada <b>foto</b> dan <b>video</b>. Hal ini menunjukkan adanya tren di mana berita palsu atau hoax sering kali memanfaatkan materi visual, seperti foto dan video, untuk menciptakan naratif yang dapat mempengaruhi opini publik.</p>

