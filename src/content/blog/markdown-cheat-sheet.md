---
author: Dev Rando
pubDatetime: 2024-10-10T21:16:03.000+07:00
title: Markdown Cheat Sheet
featured: false
draft: false
tags:
  - Markdown 
description: ini adalah syntax markdown untuk membuat tulisan blog 
---

 Markdown merupakan salah satu format penulisan yang berekstensi `.md` di akhir filenya.

## Table of contents

## Syntax Dasar (Basic Syntax)
Ini adalah elemen-elemen yang diuraikan dalam dokumen desain asli John Gruber. Semua aplikasi Markdown mendukung elemen-elemen ini.

| Element           | Markdown Syntax                                                 | Penjelasan Singkat                       |
| ----------------- | --------------------------------------------------------------- | ---------------------------------------- |
| **Heading**       | # H1<br>## H2<br>### H3<br>#### H4<br>##### H5<br>###### H6       | Membuat judul/bagian utama.              |
| **Bold**          | `**teks text**`                                                 | Menebalkan teks.                         |
| **Italic**        | `*italicized text*`                                              | Memiringkan teks.                        |
| **Blockquote**    | `> blockquote`                                                  | Mengutip teks blok.                      |
| **Ordered List**  | 1. First item<br>2. Second item<br>3. Third item                | Membuat daftar bernomor.                 |
| **Unordered List**| - First item<br>- Second item<br>- Third item                   | Membuat daftar tanpa nomor.              |
| **Code**          | `code                                                          | Menampilkan kode program.<br> **note**: tambahkan ` di akhir                |
| **Horizontal Rule**| - - -                                                          | Membuat garis pemisah.                   |
| **Link**          | `[title](https://www.example.com)`                              | Menambahkan link ke teks.                |
| **Image**         | `![alt text](image.jpg)`                                        | Menambahkan gambar ke dokumen.           |

---

## Syntax Tambahan (Extended Syntax)
Elemen-elemen ini memperluas sintaks dasar dengan menambahkan fitur-fitur tambahan. Tidak semua aplikasi Markdown mendukung elemen-elemen ini.

| Element             | Markdown Syntax                                                                                     | Penjelasan Singkat                       |
| ------------------- | --------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| **Table**           | \| Syntax \| Description \| <br> \| ----------- \| ------------- \| <br> \| Header \| Title \| <br> \| Paragraph \| Text \| | Membuat tabel.                           |
| **Fenced Code Block** | ``` <br> { <br>  "firstName": "John", <br>  "lastName": "Smith", <br>  "age": 25 <br> } <br>    | Blok kode dengan format khusus.<br> **note**: tambahkan ``` di akhir.          |
| **Footnote**        | Here's a sentence with a footnote. [^1] <br> <br> [^1]: This is the footnote.                        | Catatan kaki pada teks.                  |
| **Heading ID**      | ### My Great Heading \{#custom-id\}                                                                 | Menambahkan ID ke judul.                 |
| **Definition List** | term <br> : definition                                                                              | Daftar istilah dan definisi.             |
| **Strikethrough**   | `~~The world is flat.~~`                                                                            | Garis tengah pada teks (coret).          |
| **Task List**       | - [x] Write the press release <br> - [ ] Update the website <br> - [ ] Contact the media            | Daftar tugas dengan kotak centang.       |
| **Emoji**           | That is so funny! :joy:                                                                             | Menyisipkan emoji di teks.               |
| **Highlight**       | I need to highlight these ==very important words==.                                                 | Menyorot teks.                           |
| **Subscript**       | `H~2~O`                                                                                             | Menampilkan teks subscript.              |
| **Superscript**     | `X^2^`                                                                                              | Menampilkan teks superscript.            |

