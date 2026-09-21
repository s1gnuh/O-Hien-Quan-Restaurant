# 🍜 Bún bò Huế O Hiền – Website Nhà hàng

Website giới thiệu và xem thực đơn cho nhà hàng **Bún bò Huế O Hiền** tại Cầu Giấy, Hà Nội. Dự án xây dựng bằng HTML + CSS + JavaScript thuần (không dùng framework), tối ưu cho cả desktop và mobile.


---

## 📋 Nội dung

- ✨ [Tính năng nổi bật](#-tính-năng-nổi-bật)
- 🛠️ [Công nghệ sử dụng](#-công-nghệ-sử-dụng)
- 🚀 [Cách chạy local](#-cách-chạy-local)
- 📁 [Cấu trúc dự án](#-cấu-trúc-dự-án)
- 🎨 [Bảng màu & Font](#-bảng-màu--font)
- 🧭 [Mục lục điều hướng](#-mục-lục-điều-hướng)
- 📞 [Liên hệ](#-liên-hệ)
- 📄 [License](#-license)

---

## ✨ Tính năng nổi bật

### Giao diện & UX
- 🏗️ **Responsive 100%** – hiển thị đẹp từ 320px (mobile) đến 1440px+ (desktop)
- 🎯 **Sticky Header có mờ kính (backdrop-filter blur)** khi cuộn xuống
- 🔗 **Active Nav Highlight** – link menu được đánh dấu theo section đang xem
- 🧊 **Scroll Reveal Animation** – mờ dần + trượt lên khi section đi vào khung nhìn (dùng `IntersectionObserver`)
- ✨ **Hiệu ứng hover nâng card lên** có bóng đổ 3D cho toàn bộ card (món ăn, địa chỉ, lẩu, đồ nhúng…)
- 📌 **Nút "Gọi đặt món" FAB trên mobile** có animation pulse nhịp đập
- ⬆️ **Nút Back-to-top** hiện ra khi scroll > 500px
- 💫 **Badge "MUST TRY" lắc nhẹ** (wiggle animation) thu hút sự chú ý
- 🍜 **Tô bún Hero lơ lửng** (floaty animation) với hơi nóng bốc lên
- 🎨 **Nền gradient radial + pattern chấm** tinh tế cho các section có màu
- 📍 **Thanh gạch chân cam 3D** dưới tiêu đề mỗi section
- ♿ **Accessibility:** hỗ trợ `prefers-reduced-motion` (tắt animation cho người dùng tiết kiệm chuyển động), skip-link cho tab key, focus-visible rõ ràng

### Nội dung
- 🍜 Thực đơn **Bún bò Huế / Bún riêu cua / Bún sườn bò / Bún gân bò** với 3 cỡ tô
- 🥘 **3 loại Lẩu**: đuôi bò, riêu cua sườn non, riêu cua bắp bò (tính theo cỡ nồi)
- 🥩 **13 loại Đồ nhúng** (bò tươi, nội tạng, chả nhúng)
- 🥟 **Bánh O Hiền**: bánh bột lọc, bánh ram ít (bán theo đĩa 3 cỡ)
- 🧂 Menu "Gọi thêm" 11 loại topping
- 🍽️ Menu "Khai vị" cho nồi lẩu
- 🏪 **2 cơ sở tại Cầu Giấy** (Tô Hiệu & Trung Kính) với giờ mở cửa, chỉ đường Google Maps
- 🎁 **Ưu đãi** – quét QR Facebook nhận ưu đãi
- ☎️ **Nút gọi trực tiếp** (tel: link) – 1 click gọi đặt món ngay

---

## 🛠️ Công nghệ sử dụng

| Thành phần | Công nghệ |
|---|---|
| **Markup** | HTML5 thuần, semantic (`header`, `main`, `section`, `article`, `nav`, `footer`, `address`) |
| **Styles** | CSS3 với CSS Variables (Custom Properties), Flexbox, CSS Grid, `@keyframes`, `backdrop-filter` |
| **Script** | Vanilla JS ES5+ (không cần build) – IIFE, IntersectionObserver, passive event listener |
| **SVG** | 100% minh hoạ món ăn bằng SVG inline sprite (tái sử dụng qua `<use>`) – không cần tải ảnh |
| **Font** | Google Fonts: **Baloo 2** (display) + **Be Vietnam Pro** (body) |
| **SEO** | Meta description, Open Graph friendly, Schema.org JSON-LD (`Restaurant` cho 2 cơ sở) |
| **Tối ưu** | Lazy load cho ảnh QR, `loading="lazy"`, `preconnect` cho Google Fonts |

> 💡 **Không cần build, không cần npm, không cần framework** – mở file `index.html` là chạy ngay.

---

## 🚀 Cách chạy local

### Cách 1 – Mở trực tiếp (đơn giản nhất)
Double-click vào file `index.html` trong trình duyệt bất kỳ (Chrome, Edge, Firefox…).

### Cách 2 – Chạy bằng Python HTTP Server (khuyến nghị)
Cần cài đặt Python 3.x:
```bash
cd O-Hien-Quan-Restaurant
python -m http.server 8080
```
Mở trình duyệt vào: **http://localhost:8080**

### Cách 3 – Dùng Node.js `serve`
```bash
npx serve .
```

### Cách 4 – Live Server (VS Code)
Cài extension **Live Server** của Ritwick Dey → nhấp phải `index.html` → **Open with Live Server**.

---

## 📁 Cấu trúc dự án

```
O-Hien-Quan-Restaurant/
├── 📄 index.html            # File HTML chính (toàn bộ nội dung + SVG sprite + JS)
├── 🎨 style.css             # Toàn bộ stylesheet + Design System + Responsive
├── 🖼️ images/
│   └── facebook-qr-code.png # Mã QR Facebook (được loading lazy)
└── 📝 README.md             # File bạn đang đọc 😊
```

**Kích thước tổng cộng chỉ ~20KB** (vì dùng SVG thay cho ảnh raster), load cực nhanh ngay cả trên 3G.

---

## 🎨 Bảng màu & Font

### Palette màu (từ nhận diện thương hiệu quán)
| Tên biến CSS | Giá trị | Mô tả |
|---|---|---|
| `--purple` | `#3f2380` | Tím thương hiệu (chính) |
| `--purple-deep` | `#2a1560` | Tím đậm (background Hero, Lẩu, Footer) |
| `--orange` | `#f8a11b` | Cam nghệ (chú trọng, CTA, đường kẻ) |
| `--orange-soft` | `#ffebc8` | Cam nhạt (nền thẻ ảnh món) |
| `--lavender` | `#ebe3f8` | Lavender (nền section Đồ nhúng, Địa chỉ) |
| `--lavender-deep` | `#d9ccf0` | Viền card |
| `--cream` | `#fffaf0` | Nền tổng thể trang |
| `--ink` | `#2a1560` | Màu chữ chính |
| `--muted` | `#5b4a85` | Màu chữ phụ |

### Fonts
- **Display (tiêu đề):** Baloo 2 – weights 500 → 800
- **Body (nội dung):** Be Vietnam Pro – weights 400 → 600
- **Fallback:** system-ui, -apple-system, "Segoe UI", Roboto, sans-serif

---

## 🧭 Mục lục điều hướng

| # | Section | ID | Mô tả |
|---|---|---|---|
| 1 | Hero | `#top` | Slogan, CTA xem menu, thông tin 2 cơ sở, tô bún minh hoạ |
| 2 | Thực đơn bún | `#thuc-don` | 4 món bún chính + cỡ tô + MUST TRY badge |
| 3 | Gọi thêm | `#goi-them` | 11 topping thêm cho tô bún |
| 4 | Lẩu O Hiền | `#lau` | 3 nồi lẩu + menu khai vị |
| 5 | Đồ nhúng | `#do-nhung` | 13 loại đĩa nhúng + menu món khác cho lẩu |
| 6 | Bánh O Hiền | `#banh` | Bánh bột lọc + Bánh ram ít (3 cỡ đĩa) |
| 7 | Ưu đãi | `#uu-dai` | QR Facebook quét mã |
| 8 | Ghé quán | `#dia-chi` | 2 card địa chỉ, giờ mở cửa, CTA chỉ đường & gọi |
| 9 | Footer | – | Logo, nav, số điện thoại, bản quyền |

---

## 📞 Liên hệ

| Thông tin | Giá trị |
|---|---|
| 🏷️ Nhà hàng | Bún bò Huế O Hiền |
| 📍 Cơ sở 1 | **106/C6 Tô Hiệu, Cầu Giấy, Hà Nội**<br>⏰ 6:30 – 14:00 & 17:00 – 22:00 |
| 📍 Cơ sở 2 | **62 Trung Kính, Cầu Giấy, Hà Nội**<br>⏰ 6:30 – 22:00 (cả ngày) |
| 📞 Hotline đặt món | **[0901 737 393](tel:0901737393)** |
| 🌐 Facebook | [fb.com/ohienquan](https://www.facebook.com/ohienquan) |
| 🗺️ Chỉ đường CS1 | [Google Maps](https://maps.app.goo.gl/vDe8FhtVygKZG9VVA) |
| 🗺️ Chỉ đường CS2 | [Google Maps](https://maps.app.goo.gl/cvtc2D3CnWioi4am7) |

---

## 📄 License

© Bún bò Huế O Hiền. Source code website được công bố công khai cho mục đích tham khảo & bảo quản nguồn mã.

---

<p align="center">
  <i>Made with 🧡 for the smell of Hue beef noodle soup at 6:30 AM in Cầu Giấy</i>
</p>
