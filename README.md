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

## Evaluasi
<img style="display:flex; width:auto; height:auto;" alt="Word Cloud Berita Fakta" src="https://github.com/AptaArkana/hoax_pilpres_24/assets/79633073/d1122244-6528-4719-b093-b906f437b1dd">
Dalam lima epoch pertama pelatihan model, terlihat adanya perbaikan kinerja yang signifikan. Pada epoch pertama, model mencapai tingkat akurasi sebesar 93.68%, dengan nilai presisi, recall, dan F1 masing-masing sekitar 97.24%, 88.94%, dan 92.90%. Kinerja ini terus meningkat pada epoch-epoch berikutnya, mencapai akurasi tertinggi pada epoch keempat dengan nilai 95.87%. Meskipun terjadi kenaikan validation loss pada epoch ketiga, model tetap mampu mempertahankan tingkat akurasi yang tinggi. Dapat disimpulkan bahwa model ini secara keseluruhan telah berhasil mengatasi overfitting, mengingat terdapat penurunan validation loss pada epoch yang berikutnya. Nilai-nilai presisi, recall, dan F1 yang stabil dan tinggi menunjukkan bahwa model ini memiliki keseimbangan yang baik antara kemampuan untuk mengidentifikasi kelas positif dan negatif. Sebagai tambahan, proses pelatihan model ini juga terlihat sangat efisien, dengan nilai training loss yang menurun secara signifikan dari epoch ke epoch, mencapai nilai terendah pada epoch kelima.</p>

## Validasi Model
<img style="display:flex; width:auto; height:auto;" alt="Word Cloud Berita Fakta" src="https://github.com/AptaArkana/hoax_pilpres_24/assets/79633073/22bbdac4-c036-49ff-a02f-6be3545b9867">
<p align='justify'>Kita dapat membuat kesimpulan sebagai berikut. Model telah berhasil mengklasifikasikan 8 artikel dengan label "fakta" dengan benar, tanpa adanya prediksi yang salah pada kategori ini. Namun, model mengalami kesulitan dalam mengidentifikasi artikel dengan label "hoax", di mana terdapat 2 artikel yang seharusnya diklasifikasikan sebagai "hoax" tetapi diprediksi sebagai "fakta", dan 6 artikel berhasil diklasifikasikan dengan benar. Dengan demikian, model memiliki performa yang baik dalam mengenali artikel dengan label "fakta", namun masih memerlukan peningkatan dalam mengidentifikasi artikel dengan label "hoax". Evaluasi lebih lanjut, seperti melibatkan metrik presisi, recall, dan F1-score, dapat memberikan wawasan yang lebih mendalam terkait performa model pada setiap kategori.</p>

## Data Test
<img width="357" alt="image" src="https://github.com/AptaArkana/hoax_pilpres_24/assets/79633073/e44ae98c-ff67-41ff-9399-f2cf61ed2696">


## Link Hugging Face
Link model bisa diakses <a href="https://huggingface.co/AptaArkana/hoaxpemilu">disini</a>


