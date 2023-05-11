<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]




<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/IntekSolutions/domain_classification_alas">
  </a>

  <h3 align="center">Klasifikasi Alas Domain</h3>

  <p align="center">
    Data yang crowdsourced dalam bahasa Alas akan digunakan untuk klasifikasi domain untuk bahasa sumber daya rendah.
    <br />
    <a href="https://github.com/IntekSolutions/domain_classification_alas/issues">Membuat Saran</a>
    <br />
    <a href="https://github.com/IntekSolutions/domain_classification_alas/blob/main/README.md">     Bahasa Inggris</a>
  </p>
</div>



<!-- Daftar Isi -->
<details>
  <summary>Daftar Isi</summary>
  <ol>
    <li>
      <a href="#Tentang-Proyek">Tentang Proyek</a>
    </li>
    <li><a href="#Peta-Jalan">Peta Jalan</a></li>
    <li><a href="#Berkontribusi">Berkontribusi</a></li>
    <li><a href="#lisensi">Lisensi</a></li>
    <li><a href="#Hubung-Kami">Hubung Kami</a></li>
    <li><a href="#Terima-Kasih">Terima Kasih</a></li>
  </ol>
</details>



<!-- TENTANG PROYEK -->
## Tentang Proyek

Dataset ini dibuat oleh PT Intercultural Technology Solutions bekerja sama dengan International Literacy and Development. Intek Solutions menguji aplikasi pembuatan kumpulan data bahasa urun daya mereka, ikata, dalam [bahasa Alas](https://en.wikipedia.org/wiki/Alas_language) Aceh Tenggara di Indonesia. Data ini disumbangkan oleh masing-masing pengguna yang menanggapi Alas di aplikasi Android untuk membuka petunjuk yang diberikan dalam bahasa Indonesia. Saat pengguna mendapatkan poin, mereka diberi kompensasi dengan pembayaran mikro berdasarkan jumlah data yang disumbangkan yang dipastikan sebagai Alas. Ada juga sekitar 1500 kalimat yang dikumpulkan secara manual dari tiga pembicara unik dalam proyek terpisah yang telah dimasukkan ke dalam dataset.

Dataset berisi total 238.305  kata dan 22.264 kata unik. Ini termasuk 103.287 bigram unik dan 145.686 trigram unik.

Sifat dari proses pengumpulan data cocok untuk data yang berantakan. Alas dituturkan oleh sekitar 90.000 penutur, tetapi jarang ditulis dan ortografinya tidak baku. Dengan demikian, kumpulan data ini akan membutuhkan lapisan standardisasi sebelum digunakan. Data dikumpulkan dengan pertanyaan yang dirancang untuk memperoleh tanggapan di salah satu dari empat domain:
* Cerita / narasi
* Sejarah
* Instruksi
* Budaya / pariwisata
  
Jika domain tidak diketahui, kolom domain dibiarkan null. Dalam beberapa kasus, ikata juga dapat memunculkan terjemahan balik bahasa Indonesia. Dalam hal ini, terjemahan belakang juga disertakan. Tujuan dari proyek ini adalah untuk menguji alat pengumpulan data ikata dan untuk melihat apakah kumpulan data yang dibuat dapat digunakan untuk melatih model Klasifikasi Domain dalam konteks bahasa rendah hingga tanpa sumber daya.

Jumlah dataset per domain adalah:

|Cerita/narasi|Sejarah|Budaya/pariwisata|Petunjuk|Jumlah|
|---|---|---|---|---|
|9.128|2.735|2.215|1.952|16.030|

Contoh standardisasi yang diperlukan adalah Alas biasanya menggunakan 'kh' sebagai pengganti 'r'. Namun, karena pengaruh bahasa Indonesia, keduanya terjadi di seluruh dataset. Ada juga beberapa kata yang sering disingkat, misalnya malet menjadi mlt, dll.

Harap berhati-hati karena ada bias dalam data. Terutama aplikasi yang mengumpulkan data yang condong ke kelompok usia yang lebih muda. Ada juga data yang dikumpulkan di dua acara di mana sekelompok orang mengunduh aplikasi dan menggunakannya bersama. Ada beberapa orang yang mengisi prompt secara manual di luar aplikasi dan data dimasukkan secara manual ke dalam dataset. Meskipun kami tidak memiliki data demografis tentang para kontributor tersebut, mereka cenderung berada dalam kelompok usia 25-34 dan 35-44. Data yang dikumpulkan secara manual sedikit lebih tua. Dengan semua data demografis, mayoritas pengguna memilih untuk tidak mengungkapkan data mereka atau menghapus akun aplikasi mereka yang juga menghapus metadata mereka. Data tersebut berasal dari total 181 orang. Secara linguistik, sebagai aturan umum, kelompok usia yang lebih tua menggunakan Alas yang lebih tepat dan kelompok usia yang lebih muda menggunakan Alas yang lebih informal dengan sedikit lebih bercampur dengan bahasa Indonesia. Berdasarkan informasi yang kami miliki, berikut adalah beberapa perincian demografis dalam data:

|Umur|Jumlah kalimat|Jumlah Orang|
|---|---|---|
|18-24|2568|20|
|25-34|796|10|
|35-44|190|3|
|45-54|0|0|
|55-64|1284|1|
|65+|0|0|
|Tidak Diungkapkan|11197|156|

Data dilaporkan dari pengguna yang tinggal di 17 kabupaten terpisah. 16 kabupaten di antaranya berada di Aceh Tenggara. Lokasi lainnya adalah Berastagi di Sumatera Utara.

Menariknya, sekitar 6,1% dari data dilaporkan berasal dari penutur Batak, Jawa, dan Gayo. Aceh Tenggara sangat beragam dan setiap suku bangsa ini hadir. Ada juga kesamaan bahasa antara Alas dan Gayo dan Alas dan Batak pada khususnya.

|Suku|Jumlah kalimat|Jumlah Orang|
|---|---|---|
|Alas|4095|25|
|Batak|272|2|
|Java|146|3|
|Gayo|1301|8|
|Tidak Diungkapan|10221|150|




<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- PETA JALAN -->
## Peta Jalan

- [ ] Buat skrip standardisasi untuk membakukan variasi ejaan


Lihat [masalah terbuka](https://github.com/IntekSolutions/domain_classification_alas/issues) untuk mengetahui daftar lengkap fitur yang diusulkan (dan masalah umum).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- BERKONTRIBUSI -->
## Berkontribusi

Kontribusi adalah yang membuat komunitas open source menjadi tempat yang luar biasa untuk belajar, menginspirasi, dan berkreasi. Setiap kontribusi yang Anda berikan **sangat dihargai**.

Khususnya jika Anda adalah pembicara Alas dan melihat kalimat yang dapat diperbaiki agar lebih akurat atau konsisten, mohon pertimbangkan untuk berkontribusi.

Jika Anda memiliki saran yang akan membuat ini lebih baik, silakan fork repo dan buat permintaan penarikan. Anda juga dapat membuka masalah dengan tag "peningkatan".
Jangan lupa memberi proyek bintang! Terima kasih lagi!

1. Fork Proyek
2. Buat Cabang Fitur Anda (`git checkout -b fitur/AmazingFeature`)
3. Komit Perubahan Anda (`git commit -m 'Add some AmazingFeature'`)
4. Dorong ke Cabang (`git push origin feature/AmazingFeature`)
5. Buka Permintaan Tarik

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LISENSI -->
## Lisensi

Didistribusikan di bawah Lisensi Internasional Creative Commons Attribution-NonCommercial-NoDerivatives 4.0. Lihat `LICENSE.md` untuk informasi lebih lanjut.

[![MIT License][license-shield]][license-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- HUBUNG KAMI -->
## Hubung Kami

Andrew Brumleve - andrew@intekindonesia.com

Project Link: [https://github.com/IntekSolutions/domain_classification_alas](https://github.com/IntekSolutions/domain_classification_alas)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- TERIMA KASIH -->
## Terima Kasih

Proyek ini tidak mungkin terjadi tanpa beberapa mitra.

* [Template README](https://github.com/othneildrew/Best-README-Template)
* [International Literacy and Development](https://ilad.ngo)
* [Majelis Adat Aceh Tenggara](https://maa.acehprov.go.id/)
* Seluruh komunitas Alas yang telah mencoba aplikasi baru ini dan mengatasi bug bersama kami. Semoga hasil dari data ini mendukung pengembangan berkelanjutan dan inklusi bahasa Alas dan bahasa-bahasa Indonesia lainnya dalam teknologi bahasa secara global.
<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/IntekSolutions/domain_classification_alas.svg?style=for-the-badge
[contributors-url]: https://github.com/IntekSolutions/domain_classification_alas/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/IntekSolutions/domain_classification_alas.svg?style=for-the-badge
[forks-url]: https://github.com/IntekSolutions/domain_classification_alas/network/members
[stars-shield]: https://img.shields.io/github/stars/IntekSolutions/domain_classification_alas.svg?style=for-the-badge
[stars-url]: https://github.com/IntekSolutions/domain_classification_alas/stargazers
[issues-shield]: https://img.shields.io/github/issues/IntekSolutions/domain_classification_alas.svg?style=for-the-badge
[issues-url]: https://github.com/IntekSolutions/domain_classification_alas/issues
[license-shield]: https://img.shields.io/badge/License-CC_BY--NC--ND_4.0-lightgrey.svg
[license-url]: https://github.com/IntekSolutions/domain_classification_alas/blob/master/license.md


