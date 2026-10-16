# 529 Studio Official Showcase Site

Mã nguồn trang chủ và showcase kỹ thuật chính thức của **529 Studio** ([https://529studio.site](https://529studio.site)) - Phòng thí nghiệm phần mềm độc lập (Indie Engineering Lab) của 2 kỹ sư phần mềm.

---

## 1. Giới Thiệu

Website giới thiệu hệ sinh thái công nghệ, các giải pháp phần mềm phân tán, ứng dụng thị giác máy tính và hệ thống AI mà team 529 Studio trực tiếp thiết kế, triển khai và vận hành:
* **Warded (projectKV):** Hệ thống phân tích camera giao thông TP.HCM thời gian thực (Golang + OpenVINO YOLOv8n p50 16ms + Uber H3 + Cloudflare R2).
* **F1 Virtual Engineer:** Trợ lý phân tích chiến thuật và telemetry đua xe F1 (Next.js SSR + FastAPI + FastF1 + RabbitMQ Celery + Google Gemini LLM).
* **Autonomous SRE & Zero-Trust Ingress:** Cụm máy chủ tự lưu trữ 24/7 trên phần cứng tiết kiệm điện (Intel Celeron N2930), bảo vệ bởi Cloudflare Argo Tunnel, Traefik v3 ACME DNS-01, n8n Centralized Alert Gateway.

---

## 2. Công Nghệ Xây Dựng

* **Framework:** [Astro v5/v7](https://astro.build/) (Static Site Generation - Zero JS mặc định)
* **Styling:** [Tailwind CSS v4](https://tailwindcss.com/)
* **Typography:** [Geist & Geist Mono](https://vercel.com/font) (Google Fonts, hỗ trợ toàn diện tiếng Việt)
* **Hosting:** Cloudflare Pages (Toàn cầu hóa tại Edge CDN)
* **Design Aesthetic:** Engineered Monochromatic Minimalism, chuẩn phong cách kỹ thuật cao cấp.

---

## 3. Lệnh Phát Triển & Quản Lý Server

### Cài đặt thư viện ban đầu
```bash
npm install
```

### Quản lý máy chủ Dev ngầm (Khuyên dùng - Background Mode)
*Chế độ chạy ẩn, không chiếm dụng cửa sổ terminal và duy trì ổn định:*

```bash
# Bật server chạy ngầm tại localhost:4321
npx astro dev --background

# Kiểm tra trạng thái máy chủ (uptime, pid, url)
npx astro dev status

# Xem nhật ký hoạt động (logs)
npx astro dev logs

# Tắt máy chủ chạy ngầm
npx astro dev stop
```

### Chạy trực tiếp trên Terminal (Foreground Mode)
*Quan sát log trực tiếp trên cửa sổ dòng lệnh hiện tại:*

```bash
npm run dev
# Tắt server: Nhấn tổ hợp phím Ctrl + C
```

### Đóng gói & Kiểm tra bản tĩnh (Production Build & Preview)
```bash
# Build tĩnh ra thư mục ./dist (tốc độ siêu tốc ~200ms)
npm run build

# Chạy server xem trước bản build tĩnh giống hệt production
npm run preview
# Tắt preview: Nhấn tổ hợp phím Ctrl + C
```

---

## 4. Triển Khai Lên Cloudflare Pages

1. Đẩy mã nguồn lên kho lưu trữ GitHub `529-studio/529studio.site`.
2. Trên Cloudflare Dashboard:
   * **Project Name:** `529studio-site`
   * **Framework Preset:** `Astro`
   * **Build Command:** `npm run build`
   * **Build Output Directory:** `dist`
3. Gán Custom Domains: `529studio.site` và `www.529studio.site`.

---

© 2026 529 Studio • Autonomous Agentic Systems & High-Performance Infrastructure
