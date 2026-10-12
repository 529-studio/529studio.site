# 529 Studio Official Showcase Site

Mã nguồn trang chủ và showcase kỹ thuật chính thức của **529 Studio** ([https://529studio.site](https://529studio.site)).

---

## 1. Giới Thiệu

Website giới thiệu hệ sinh thái công nghệ, các giải pháp phần mềm phân tán, ứng dụng thị giác máy tính và hệ thống AI mà team 529 Studio trực tiếp thiết kế, triển khai và vận hành:
* **Warded (projectKV):** Hệ thống phân tích camera giao thông TP.HCM thời gian thực (Golang + OpenVINO YOLOv8n p50 16ms + Uber H3 + Cloudflare R2).
* **F1 Virtual Engineer:** Trợ lý phân tích chiến thuật và telemetry đua xe F1 (Next.js SSR + FastAPI + FastF1 + RabbitMQ Celery + Google Gemini LLM).
* **Autonomous SRE & Zero-Trust Ingress:** Cụm máy chủ tự lưu trữ 24/7 trên phần cứng tiết kiệm điện, bảo vệ bởi Cloudflare Argo Tunnel, Traefik v3 ACME DNS-01, n8n Centralized Alert Gateway.

---

## 2. Công Nghệ Xây Dựng

* **Framework:** [Astro v5/v7](https://astro.build/) (Static Site Generation — Zero JS mặc định)
* **Styling:** [Tailwind CSS v4](https://tailwindcss.com/)
* **Hosting:** Cloudflare Pages (Toàn cầu hóa tại Edge CDN)
* **Design Aesthetic:** Monochromatic Dark Theme, chuẩn phong cách kỹ thuật cao cấp.

---

## 3. Lệnh Phát Triển & Build

```bash
# Cài đặt thư viện
npm install

# Chạy máy chủ dev cục bộ tại localhost:4321
npm run dev

# Build tĩnh ra thư mục ./dist
npm run build

# Xem trước bản build tĩnh
npm run preview
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
