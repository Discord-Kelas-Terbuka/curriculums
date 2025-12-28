# Javascript Dasar: The Beginning

Selamat datang di dunia Javascript (JS). Kalau HTML adalah tulang, dan CSS adalah baju, maka **Javascript adalah otak dan ototnya**. Tanpa JS, web cuma poster digital yang diam mematung.

## Apa itu Javascript?

Javascript adalah bahasa pemrograman yang awalnya dibuat supaya website bisa "gerak". Dulu cuma buat bikin tombol kelap-kelip, sekarang Javascript menguasai dunia:
1.  **Frontend:** Mengatur interaksi user (React, Vue, Svelte).
2.  **Backend:** Mengatur server dan database (Node.js).
3.  **Mobile:** Bikin aplikasi HP (React Native).

### High-Level & Interpreted

Javascript itu bahasa tingkat tinggi (manusia bisa baca) dan _interpreted_ (dijalankan baris per baris oleh browser/engine, gak perlu compile ribet kayak Java atau C++).

@@INFO_START:Jangan Salah Gaul@@
Java **Bukan** Javascript. Hubungan mereka kayak "Ham" dan "Hamster". Cuma mirip nama, beda spesies.
@@INFO_END@@

## Output: Hello World

Cara paling purba untuk berkomunikasi dengan Javascript adalah lewat Console.

@@CODE@@
console.log("Halo Dunia fana!");
console.warn("Ini peringatan!");
console.error("Duh, error bang...");
@@CODE@@

- `console.log` adalah teman sejatimu saat debugging nanti.

## Variables (Wadah Data)

Variabel adalah tempat kita menyimpan data biar bisa dipakai lagi nanti.

### 3 Cara Deklarasi

1.  `var`: Cara kuno. Suka bocor (scope-nya aneh). **Hindari.**
2.  `let`: Cara modern. Nilainya bisa diubah.
3.  `const`: Cara modern. Nilainya paten (konstan).

@@CODE@@
// Jangan dipake lagi, nanti diketawain senior
var namaLama = "Budi";

// Pake ini kalau nilainya bakal berubah
let skor = 0;
skor = 10; // Valid

// Pake ini kalau nilainya gak boleh berubah
const gravitasi = 9.8;
gravitasi = 10; // ERROR! Gak bisa di-reassign
@@CODE@@

@@INFO_START:Mental Model@@
Selalu gunakan `const` secara default. Kalau ternyata butuh diubah, baru ganti jadi `let`. Lupakan `var`.
@@INFO_END@@

## Tipe Data Dasar

Javascript itu _Dynamic Typing_. Kamu gak perlu bilang tipe datanya apa, dia bakal nebak sendiri.

- **String**: Teks (`"Ayam"` atau `'Bebek'`).
- **Number**: Angka (`2024`, `3.14`, `-5`).
- **Boolean**: Kebenaran mutlak (`true` atau `false`).
- **Undefined**: Variabel ada, tapi isinya gaib (belum diisi).
- **Null**: Variabel ada, dan isinya sengaja dikosongin.

@@CODE@@
let nama = "Pukis";      // String
let umur = 25;           // Number
let isLapar = true;      // Boolean
let pacar;               // Undefined (sedih)
let dompet = null;       // Null (sengaja kosong)
@@CODE@@

## Operator & Logika

Tempat di mana matematika bertemu dengan keputusan hidup.

### Aritmatika Simpel

@@CODE@@
let x = 10 + 5; // 15
let y = 10 % 3; // 1 (Modulus/Sisa bagi)
let z = 2 ** 3; // 8 (Pangkat)
@@CODE@@

### Perbandingan (Hati-hati!)

Di JS, angka `5` dan teks `"5"` bisa dianggap sama kalau kamu ceroboh.

@@CODE@@
// Operator == (Loose Equality)
// Cuma cek nilai, tipe data bodo amat
console.log(5 == "5"); // TRUE (Bahaya!)

// Operator === (Strict Equality)
// Cek nilai DAN tipe data
console.log(5 === "5"); // FALSE (Aman & Waras)
@@CODE@@

@@INFO_START:Hukum Wajib@@
Selalu, dan selalu gunakan `===` (tiga sama dengan). Operator `==` adalah sumber bug yang bikin nangis darah.
@@INFO_END@@

## Control Flow (Percabangan)

Mengatur jalan cerita kodemu.

@@CODE@@
const nilai = 80;

if (nilai >= 90) {
  console.log("Grade A: Sepuh!");
} else if (nilai >= 75) {
  console.log("Grade B: Lumayan");
} else {
  console.log("Grade C: Remedial bang");
}
@@CODE@@

## Looping (Perulangan)

Biar gak capek nulis kode yang sama berulang kali.

### For Loop

Struktur paling klasik.

@@CODE@@
// Mulai dari 0; Selama i kurang dari 5; Tambah 1 setiap putaran
for (let i = 0; i < 5; i++) {
  console.log("Putaran ke-" + i);
}
@@CODE@@

## Ringkasan & Tips Menarik

Materi dasar selesai! Sebelum lanjut ke level menengah, ini oleh-oleh buat kamu.

@@INFO_START:Tips & Trick Javascript Dasar@@

1.  **Titik Koma (;)**
    Di JS, titik koma itu _optional_ (Automatic Semicolon Insertion). Tapi, disarankan tetap pakai biar kode rapi dan menghindari bug aneh saat kode di-minify.

2.  **NaN itu Number**
    Kalau kamu cek `typeof NaN` (Not a Number), hasilnya adalah `'number'`. Aneh kan? Terimalah kenyataan ini.

3.  **Template Literals**
    Daripada nulis ribet pake `+`:
    `console.log("Halo " + nama + ", umurmu " + umur);`
    
    Mending pake Backtick (\`):
    `console.log(\`Halo ${nama}, umurmu ${umur}\`);`
    Lebih bersih, lebih modern.

4.  **Cara Cepat Debug**
    Selain `console.log`, cobalah `console.table({namaVariable})` kalau mau liat data object atau array biar tampilannya rapi kayak Excel di terminal.

@@INFO_END@@
