<div align="center">

# Granite AI Playground

Playground **React + Vite** untuk bereksperimen dengan model **IBM Granite** — antarmuka chat dengan manajemen loading global.

[![Status](https://img.shields.io/badge/status-prototype-orange?style=flat-square)](#)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev)
[![Tailwind](https://img.shields.io/badge/Tailwind%20CSS-4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![IBM Granite](https://img.shields.io/badge/IBM-Granite-0F62FE?style=flat-square&logo=ibm&logoColor=white)](https://www.ibm.com/granite)

<!-- lang-switcher -->
[English](README.md) · **Bahasa Indonesia**

</div>

---

## Tentang

Eksperimen antarmuka chat untuk model **IBM Granite**. Dibangun untuk menguji bagaimana rasanya berinteraksi dengan Granite lewat API, sekaligus mempelajari pola **global loading state** di React menggunakan Context.

Struktur kodenya sengaja dijaga sederhana agar mudah dijadikan basis project lain.

## Fitur

- **Antarmuka chat** — kirim prompt dan tampilkan respons model.
- **Global loading state** — `LoadingContext` + hook `useLoading` agar indikator loading konsisten di seluruh komponen.
- **Auto-scroll** — daftar pesan otomatis menggulir saat data baru masuk.
- **Tailwind CSS 4** via plugin Vite (`@tailwindcss/vite`).
- **Siap deploy** — konfigurasi Netlify sudah disertakan.

## Tech Stack

| Bagian | Teknologi |
| --- | --- |
| Framework | React 18 |
| Bundler | Vite |
| Styling | Tailwind CSS 4 (`@tailwindcss/vite`) |
| HTTP | Axios |
| Lint | ESLint 9 (flat config) |
| Deploy | Netlify |

## Menjalankan

### 1. Clone & install

```bash
git clone https://github.com/Ilhamaji/granite-ai-playground.git
cd granite-ai-playground
npm install
```

### 2. Environment

```env
VITE_GRANITE_API_URL=your_endpoint_here
VITE_GRANITE_API_KEY=your_key_here
```

### 3. Jalankan

```bash
npm run dev          # development
npm run build        # build produksi ke dist/
npm run preview      # preview hasil build
npm run lint         # ESLint
```

## Struktur

```
src/
  main.jsx                     # entrypoint React
  App.jsx                      # komposisi aplikasi
  context/LoadingContext.jsx   # provider + hook useLoading
  pages/Home.jsx               # halaman utama (input & daftar pesan)
public/
index.html
netlify.toml                   # konfigurasi deploy + SPA redirect
```

## Catatan

Ini project **eksperimen**, bukan aplikasi produksi — belum ada penyimpanan riwayat chat, autentikasi, atau penanganan error yang lengkap. Dokumentasi kode ditulis di `README.md` karena project ini juga dipakai sebagai latihan mendokumentasikan arsitektur.

## Lisensi

MIT.

---

<div align="center">
Dibuat oleh <a href="https://github.com/Ilhamaji">Ilham Aji</a>
</div>
