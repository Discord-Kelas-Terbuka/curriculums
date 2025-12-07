## Layout & Positioning dalam CSS

Di tahap ini, CSS berhenti jadi cat tembok dan mulai jadi arsitektur. Salah sedikit, bangunannya ambruk.

### Konsep Layout Dasar

Layout menentukan **bagaimana elemen disusun** di halaman.

@@CODE@@
/_ Display dasar _/
block /_ lebar penuh, baris baru _/
inline /_ selebar konten, satu baris _/
inline-block /_ inline tapi bisa diset ukuran _/
none /_ tak terlihat, tak ada ruang _/

@@CODE@@

- `block` untuk struktur utama
- `inline` untuk teks
- `inline-block` untuk komponen kecil
- `none` benar-benar menghilangkan elemen

@@INFO_START:Catatan Penting@@
`display: none` menghapus elemen dari layout. `visibility: hidden` tidak.
@@INFO_END@@

---

## Positioning

Positioning mengatur **di mana** elemen berada relatif terhadap siapa.

### Jenis Position

@@CODE@@
position: static; /_ default _/
position: relative; /_ jadi anchor _/
position: absolute; /_ lepas dari flow _/
position: fixed; /_ nempel ke viewport _/
position: sticky; /_ hybrid aneh tapi berguna _/
@@CODE@@

@@CODE@@
.box {
position: absolute;
top: 10px;
right: 20px;
}
@@CODE@@

- `relative` tidak pindah konteks layout
- `absolute` mencari parent terdekat yang positioned
- `fixed` cocok untuk navbar
- `sticky` aktif setelah scroll tertentu

@@INFO_START:Kesalahan Umum@@
Absolute tanpa parent positioned = chaos global.
@@INFO_END@@

---

## Flexbox (Layout Favorit Manusia Waras)

Flexbox dibuat untuk menyusun item **satu dimensi**: baris atau kolom.

### Container Flex

@@CODE@@
.container {
display: flex;
flex-direction: row; /_ row | column _/
justify-content: space-between;
align-items: center;
gap: 12px;
}
@@CODE@@

### Item Flex

@@CODE@@
.item {
flex: 1; /_ grow _/
flex-shrink: 0;
flex-basis: 200px;
}
@@CODE@@

- `justify-content` = sumbu utama
- `align-items` = sumbu silang
- `gap` lebih bersih dari margin

@@INFO_START:Rule Emas Flexbox@@
Ingat: arah dulu, baru alignment. Manusia sering kebalik.
@@INFO_END@@

---

## Responsive Design

Web tidak hidup di satu ukuran layar saja. Terimalah.

### Media Queries

@@CODE@@
/_ Mobile-first _/
.container {
padding: 12px;
}

@media (min-width: 768px) {
.container {
padding: 24px;
max-width: 960px;
margin: auto;
}
}
@@CODE@@

- Mulai dari layar kecil
- Tambahkan aturan untuk layar besar
- Jangan desain desktop duluan kecuali mau frustrasi

---

## Responsive dengan Flexbox

@@CODE@@
.cards {
display: flex;
flex-wrap: wrap;
gap: 16px;
}

.card {
flex: 1 1 240px;
}
@@CODE@@

- `flex-wrap` mengizinkan baris baru
- `flex-basis` menentukan ukuran minimum item

@@INFO_START:Prinsip Sehat@@
Biarkan layout beradaptasi. Jangan paksa piksel absolut.
@@INFO_END@@

---

## Contoh Kasus Sederhana

@@CODE@@

<nav class="navbar">
  <div class="logo">Brand</div>
  <div class="menu">
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
  </div>
</nav>

<style>
  .navbar {
    display: flex;
    justify-content: space-between;
    padding: 16px;
  }

  .menu {
    display: flex;
    gap: 12px;
  }
</style>

@@CODE@@

---

## Ringkasan Mental Model

- Layout = struktur
- Position = konteks lokasi
- Flexbox = susun elemen dengan waras
- Responsive = desain untuk realita

@@INFO_START:Penutup Jujur@@
Kalau layoutmu masih berantakan, itu normal. CSS bukan gagal. Kamu cuma belum cukup sering jatuh.
@@INFO_END@@
