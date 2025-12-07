## Apa itu CSS?

CSS (Cascading Style Sheets) mengatur tampilan HTML. HTML memberi struktur, CSS memberi baju — model yang layak pakai, bukan sisa karung.

### Inti Singkat

- CSS menentukan warna, ukuran, spasi, layout, dan bagaimana elemen tampil.
- "Cascading" = aturan tumpuk: yang lebih spesifik menang.
- Styling tidak merusak HTML; ia melekat padanya melalui selector.

@@CODE@@
/_ Contoh CSS sederhana _/
body {
font-family: Arial, sans-serif;
line-height: 1.5;
}
h1 {
color: #1f2937;
font-size: 2rem;
}
@@CODE@@

@@INFO_START:Catatan Cepat@@
Jangan gunakan CSS untuk konten penting. Gunakan CSS untuk tampilan saja. Struktur tetap di HTML.
@@INFO_END@@

---

## Cara Menyisipkan CSS

### Metode Umum

@@CODE@@

<!-- Inline -->
<p style="color: red;">Teks</p>

<!-- Internal -->
<style>
  p { color: blue; }
</style>

<!-- External -->
<link rel="stylesheet" href="styles.css">
@@CODE@@

- External file = recommended untuk skalabilitas.
- Inline = cepat tapi berantakan; hindari kecuali darurat.

@@INFO_START:Praktik Baik@@
Selalu gunakan file eksternal untuk proyek nyata. Cache browser menyukai itu.
@@INFO_END@@

---

## Selector (Dasar)

### Tipe Selector

@@CODE@@
/_ Element _/
p {}

/_ Class _/
.card {}

/_ ID _/
#header {}

/_ Descendant _/
nav a {}

/_ Attribute _/
input[type="text"] {}
@@CODE@@

- `.class` untuk reusable styling
- `#id` untuk satu elemen unik (pakai hemat)
- `element` untuk target tag langsung

---

## Properti Dasar

@@CODE@@
/_ Layout & Box _/
margin: 16px;
padding: 8px;
border: 1px solid #ddd;

/_ Typography _/
color: #333;
font-size: 16px;
line-height: 1.4;

/_ Visual _/
background-color: #f7fafc;
display: block; /_ inline, inline-block, flex, grid, none _/
@@CODE@@

- Margin = ruang luar, Padding = ruang dalam
- Display dan box model menentukan tata letak

@@INFO_START:Debugging Cepat@@
Gunakan inspector (F12). Jika sesuatu menghilang, cek display, visibility, dan z-index.
@@INFO_END@@

---

## Specificity & Cascade (Singkat)

- Inline style > ID selector > class/attribute/pseudo-class > element selector.
- Jika specificity sama, yang terakhir dideklarasikan menang.
- `!important` memaksa aturan (pakai hanya kalau benar-benar butuh).

@@CODE@@
/_ Contoh spesifisitas _/
#menu .item a { color: red; } /_ lebih spesifik daripada .item a _/
@@CODE@@

---

## Contoh: HTML + CSS

@@CODE@@

<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Contoh CSS</title>
    <style>
      body { font-family: sans-serif; margin: 20px; }
      .card { padding: 12px; border: 1px solid #e5e7eb; border-radius: 8px; }
      .card h2 { margin: 0 0 8px 0; }
      .primary { background-color: #3b82f6; color: white; padding: 8px 12px; border-radius: 6px; display: inline-block; }
    </style>
  </head>
  <body>
    <div class="card">
      <h2>Judul Kartu</h2>
      <p>Ini contoh kartu sederhana.</p>
      <a class="primary" href="#">Tombol</a>
    </div>
  </body>
</html>
@@CODE@@

@@INFO_START:Tip Efisien@@
Buat file `variables` (CSS custom properties) bila ingin tema konsisten. Contoh: `:root { --brand: #3b82f6; }`.
@@INFO_END@@

---

## Next Steps Singkat

- Pelajari box model lebih dalam.
- Praktikkan flexbox & grid untuk layout nyata.
- Eksperimen dengan media queries untuk responsivitas.
