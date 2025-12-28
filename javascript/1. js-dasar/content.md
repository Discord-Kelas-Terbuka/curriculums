## Apa itu Javascript?

Javascript adalah _General Purpose Programming Language_ yang awalnya **cuma buat simple scripting website jadul**, tapi sekarang udah bisa maenan AI, bikin server, sampai aplikasi robot.

HTML itu tulangnya, CSS itu bajunya, dan **Javascript itu otaknya**. Tanpa JS, web cuma dokumen mati.

### Apa itu Scripting?

Scripting artinya kode ini **dijalankan langsung** oleh environtment-nya (misal: Browser), gak perlu dicompile ribet jadi binary file kayak bahasa C atau Java. Tulis, simpan, refresh, jalan.

### Kenapa Javascript Aneh?

Karena dia dibuat cuma dalam 10 hari oleh Brendan Eich. Jadi kalau nemu hal aneh, maklumin aja. Itu fitur, bukan bug.

## Variables

Variabel adalah **wadah penampung data**. Bayangkan kardus yang kamu tempeli label nama.

### Cara Deklarasi

Zaman now kita pakai `let` dan `const`. Lupakan `var` kalau mau hidup tenang.

@@CODE@@
let umur = 25; // Bisa diubah (Reassignable)
umur = 26; // Valid

const nama = "Faqihza"; // Konstan (Immutable-ish)
nama = "Pukis"; // ERROR! Gak bisa diganti woy
@@CODE@@

@@INFO_START:Variabel JS berbeda dengan Bahasa C++@@
JS itu *Dynamic Typing*. Kamu gak perlu bilang `int` atau `string` di awal. JS akan menebak sendiri isinya apa. Hari ini angka, besok bisa jadi teks.
@@INFO_END@@

## Tipe Data Dasar

Di Javascript, tipe data itu cair, tapi tetap ada aturannya.

- `String`: Teks, diapit kutip `'` atau `"`.
- `Number`: Angka, mau bulat atau desimal sama aja.
- `Boolean`: Cuma `true` atau `false`. Hidup itu biner.
- `Undefined`: Variabel udah dibuat, tapi belum diisi.
- `Null`: Sengaja dikosongin.

@@CODE@@
let pesan = "Halo Dunia"; // String
let harga = 15000.50;     // Number
let isLapar = true;       // Boolean
let otak;                 // Undefined (kosong)
let dompet = null;        // Null (sengaja kosong)
@@CODE@@

@@INFO_START:Fakta Menarik@@
`typeof null` hasilnya adalah `'object'`. Ini adalah bug Javascript yang sudah ada sejak lama dan gak diperbaiki biar web lama gak error.
@@INFO_END@@

## Operator & Logika

Tempat di mana matematika bertemu dengan keputusan hidup.

### Perbandingan yang Menipu

Hati-hati dengan tanda sama dengan.

@@CODE@@
let a = 5;
let b = "5";

// Double equals (Cek nilai doang)
console.log(a == b); // TRUE (Padahal satu angka, satu teks)

// Triple equals (Cek nilai DAN tipe data)
console.log(a === b); // FALSE (Ini yang bener)
@@CODE@@

@@INFO_START:Hukum Wajib@@
Selalu gunakan `===` daripada `==`. Kecuali kamu tau persis apa yang kamu lakukan (spoiler: biasanya enggak).
@@INFO_END@@

### Logika Dasar

@@CODE@@
const nilai = 80;

if (nilai >= 75) {
  console.log("Lulus");
} else {
  console.log("Remedial");
}
@@CODE@@

## Looping (Perulangan)

Komputer suka melakukan hal membosankan berulang kali. Manusia tidak.

### For Loop

@@CODE@@
for (let i = 0; i < 5; i++) {
  console.log("Putaran ke-" + i);
}
@@CODE@@

- `let i = 0`: Start di mana
- `i < 5`: Berhenti kapan
- `i++`: Langkahnya gimana

## Ringkasan Mental Model

- `const` adalah defaultmu, pakai `let` kalau terpaksa.
- Tipe data bisa berubah, jangan kaget.
- Selalu cek tipe data dengan `===`.
- Javascript itu teman, tapi kadang dia suka nge-prank.

@@INFO_START:Tips Debugging@@
Kalau kode gak jalan, klik kanan di browser > Inspect > Console. Di situlah dosa-dosamu (error) tertulis jelas.
@@INFO_END@@
