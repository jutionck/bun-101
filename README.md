# Bun is an all-in-one JavaScript runtime & toolkit

## Introduction

Bun adalah runtime JavaScript yang ringan dan cepat. Bun ini diciptakan untuk alternatif dari penggunaan Node.js dan Deno.serve(). Bun di klaim lebih cepat dari kedua yang disebutkan di atas.

Sejak dokumen ini dibuat Bun sudah masuk versi `1.0.4`.

Berikut kenapa Bun dicipatakan:

1. `Speed` -> Bun dimulai dengan cepat dan berjalan dengan cepat. Ia memperluas JavaScriptCore, mesin JS yang mengutamakan performa yang dibuat untuk Safari. Saat komputasi bergerak ke tepi, ini sangat penting.
2. `Elegant APIs` -> Bun menyediakan sekumpulan API minimal yang sangat dioptimalkan untuk melakukan tugas-tugas umum, seperti menjalankan server HTTP dan menulis file.
3. `Cohesive DX` -> Bun adalah toolkit lengkap untuk membangun aplikasi JavaScript, termasuk pengelola paket, runner uji coba, dan bundler.

Bun dirancang sebagai pengganti drop-in untuk Node.js. Bun mengimplementasikan ratusan Node.js dan API Web, termasuk `fs`, `path`, `Buffer`, dan banyak lagi.

Tujuan Bun adalah untuk menjalankan sebagian besar JavaScript sisi server di dunia dan menyediakan alat untuk meningkatkan kinerja, mengurangi kerumitan, dan melipatgandakan produktivitas pengembang.

Selengkapnya bisa cek di website ini https://bun.sh/.

## Instalation

Untuk melakukan instalasi bisa menggunakan `curl` berikut command lengkapnya:

```bash
curl -fsSL https://bun.sh/install | bash

######################################################################## 100.0%
bun was installed successfully to ~/.bun/bin/bun

Added "~/.bun/bin" to $PATH in "~/.zshrc"

To get started, run:

  exec /bin/zsh
  bun --help
```

## Common Command

Secara command sama seperti penggunaan `npm` dan `yarn`.

- `Bun Install` -> `bun install`
- `Bun Run` -> `bun run`
- `Bun Test` -> `bun test`

Contoh sederhana kode dalam menggunakan Bun.

```tsx
// index.ts
const server = Bun.serve({
  port: 3000,
  fetch(request) {
    return new Response('Welcome to Bun!');
  },
});

console.log(`Listening on localhost:${server.port}`);
```

Kemudian untuk menjalankannya adalah dengan command berikut:

```bash
bun index.ts
```

Jika dilihat kode di atas, dengan Bun kita bisa langsung menjalankan file TypeScript tanpa membutuhkan sebuah `ts-node`, ini adalah salah satu kelebihan dari Bun.

## Docs
