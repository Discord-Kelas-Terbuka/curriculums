# Belajar LaTeX – Panduan Praktis untuk Engineer

LaTeX itu cara berpikir, bukan sekadar alat ngetik. Anggap kamu sedang menulis source code untuk dokumen. Kamu mendefinisikan struktur, LaTeX yang mengurus tampilan.

---

## Dokumen Paling Minimal

Ini bentuk LaTeX paling sederhana yang valid.

```latex
\documentclass{article}

\begin{document}
Hello, world!
\end{document}
```

documentclass menentukan jenis dokumen.  
document berisi semua konten yang akan dirender ke PDF.

---

## Struktur Dokumen

Gunakan struktur, bukan styling manual.

```latex
\section{Pendahuluan}
\subsection{Latar Belakang}
\subsubsection{Detail Teknis}
```

Paragraf baru dibuat dengan baris kosong, bukan enter berulang.

---

## Formatting Teks Dasar

```latex
\textbf{Tebal}
\textit{Miring}
\underline{Garis bawah}
```

Gunakan seperlunya. LaTeX unggul saat konsisten, bukan dekoratif.

---

## List

Bullet list:

```latex
\begin{itemize}
  \item Item pertama
  \item Item kedua
\end{itemize}
```

List bernomor:

```latex
\begin{enumerate}
  \item Langkah satu
  \item Langkah dua
\end{enumerate}
```

---

## Mode Matematika

Inline math:

```latex
$x^2 + y^2 = z^2$
```

Block math:

```latex
\[
\int_0^\infty e^{-x} dx = 1
\]
```

Rule sederhana:  
kalau rumus dibaca → inline  
kalau dianalisis → block

---

## Simbol Matematika Umum

```latex
\alpha \beta \gamma
\leq \geq \neq
\sum_{i=1}^n
\frac{a}{b}
\sqrt{x}
```

Subscript dan superscript:

```latex
x_i^2
```

---

## Equation dengan Nomor

```latex
\begin{equation}
E = mc^2
\end{equation}
```

---

## Tabel Dasar

```latex
\begin{tabular}{c c c}
A & B & C \\
1 & 2 & 3
\end{tabular}
```

c = center  
l = left  
r = right  

---

## Comment

```latex
% Ini tidak akan muncul di PDF
```

---

## Package

```latex
\usepackage{amsmath}
\usepackage{graphicx}
```

---

## Mental Model

LaTeX bekerja baik jika kamu:
- fokus ke struktur
- iterasi cepat
- anggap dokumen sebagai kode

---

## Workflow

1. Tulis `.tex`
2. Compile
3. Lihat PDF
4. Iterasi
