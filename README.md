# 🛒 DummyStore – React E-commerce

DummyStore adalah aplikasi toko online sederhana berbasis **React** yang dibuat sebagai proyek UTS mata kuliah **Pemrograman Web**. Aplikasi ini menampilkan daftar produk dari **DummyJSON API**, dilengkapi fitur keranjang, pencarian, filter kategori, hingga favorit produk.

---
LINK WEBSITE : https://uts-pemrograman-web-122140197-iv9v.vercel.app/
---

## ✨ Fitur Utama

- 🔍 Pencarian produk real-time (dengan riwayat pencarian)
- 🎛 Filter produk berdasarkan kategori
- ❤️ Tambah ke favorit (tersimpan di localStorage)
- 🛒 Tambah ke keranjang dengan preview modal dan jumlah dinamis
- 🧾 Halaman keranjang dengan kontrol kuantitas dan subtotal
- 💳 Tombol "Beli Sekarang" (simulasi checkout)
- 🗺 Routing dinamis (detail produk `/products/:id`)
- 🧭 Navigasi aman (404 Not Found, navigasi programatik)
- 🎨 UI modern dengan animasi halus menggunakan **Framer Motion**
- 🌐 Data diambil dari API eksternal: [dummyjson.com/products](https://dummyjson.com/products)

---

## 📌 Ketentuan UTS yang Terpenuhi ✅

### ✅ 1. Komponen Fungsional, Props, State, PropTypes
- 5+ komponen fungsional: `ProductCard`, `CartPreviewModal`, `Header`, `Footer`, `LoadingSpinner`, `ErrorMessage`
- Komunikasi antar komponen via props
- Validasi prop menggunakan `PropTypes`
- State lokal pada komponen (`useState`)

### ✅ 2. Hooks & Lifecycle
- `useState` → manajemen input dan local UI
- `useEffect` → fetch API dan efek awal
- `useRef` → untuk focus dan akses DOM
- `useCallback` → fungsi memoized agar tidak rerender
- `useMemo` → optimasi filter produk
- ✅ 1 Custom Hook: `useProducts` (handle fetch + loading/error)

### ✅ 3. Pengambilan Data dari API
- Menggunakan [dummyjson.com/products](https://dummyjson.com/products)
- Data produk diambil via `fetch` pada `useEffect`
- Loading state + error handling ditampilkan secara eksplisit

### ✅ 4. React Router
- 3+ Halaman: `/`, `/products`, `/products/:id`, `/favorites`, `/cart`, `/about`
- Routing dinamis + nested parameter `:id`
- Navigasi programatik (`useNavigate`)
- Penanganan halaman error 404

### ✅ 5. State Management
#### 📦 Menggunakan: **Context API + useReducer**

Saya memilih `Context + useReducer` karena:

- Cocok untuk aplikasi berskala menengah
- State yang digunakan cukup kompleks (search, cart, like)
- Perlu update dari banyak komponen → lebih efisien dibanding `useState` biasa
- Alternatif ringan dari Redux Toolkit
- Mudah dipisahkan, diorganisir, dan diuji

Global state yang dikelola:

| State             | Deskripsi                                    |
|------------------|----------------------------------------------|
| `likedProducts`  | ID produk yang di-like oleh user             |
| `cart`           | Daftar produk yang dimasukkan ke keranjang   |
| `searchQuery`    | Kata kunci pencarian                         |
| `selectedCategory` | Filter kategori                            |
| `searchHistory`  | Riwayat pencarian user                       |

---

## ⚙️ Teknologi yang Digunakan

- ⚛️ [React 19](https://reactjs.org/)
- ⚡ [Vite](https://vitejs.dev/)
- 💨 [Tailwind CSS](https://tailwindcss.com/)
- 📦 React Router v6+
- 🎞 [Framer Motion](https://www.framer.com/motion/)
- 🧠 Context API + useReducer
- 🧪 Custom Hook (`useProducts`)
- 📐 PropTypes

---

## 🚀 Cara Menjalankan Proyek

1. **Clone repo**:
   ```bash
   git clone https://github.com/samanbrembo14/uts_pemrograman_web_122140197.git
