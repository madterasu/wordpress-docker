---
title: "🛠️ Ngedokering WordPress: Deploy Santuy Pakai Docker & Compose"
description: "Tutorial ringan ala DevOps pemula buat nge-deploy WordPress bareng MariaDB dalam container. Gak ribet, tinggal jalanin aja!"
date: 2025-07-22
tags: ["Docker", "WordPress", "DevOps", "Containerization"]
---

# 😺 WordPress-an Gak Pake Ribet: Cuma Butuh Docker & Sedikit Niat!

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Docker Compose](https://img.shields.io/badge/Docker%20Compose-339933?style=for-the-badge&logo=docker&logoColor=white)

Halo rek~ 👋  
Kali ini aku nyobain sesuatu yang *kelihatannya* ribet tapi aslinya nyenengin pol: **nge-deploy WordPress langsung di dalem container Docker!** 😻

Gak perlu install Apache, PHP, MariaDB satu-satu. Cukup tulis `docker-compose.yml`, tinggal `up`, langsung meluncur ke browser! 🚀

---

## 🐾 Apa Sih Proyek Iki?

Proyek iki buat nunjukkin kalo deployment aplikasi tuh bisa **gak ribet** asal ngerti konsep *containerization*.  
Semua layanan (WordPress & DB-nya) dikemas jadi container. Gak ada tuh cerita "kok beda di server ya?" karena semuanya konsisten di mana pun Docker bisa jalan 😎

---

## 🧠 Ilmu Sing Tak Pakai di Proyek Iki

- 🔹 **Dockerization:** Semua aplikasi + dependensinya dijadikan container. Beres!
- 🔹 **Infrastructure as Code:** Semua setting ditulis rapi di `docker-compose.yml`. Gak perlu utak-atik server manual.
- 🔹 **Multi-Container Orchestration:** Ada 2 container utama: `wordpress` & `mariadb`, dan dua-duanya jalan bareng!
- 🔹 **Docker Networking:** Otomatis bisa saling ngobrol lewat jaringan internal Docker, aman sentosa.
- 🔹 **Persistent Data:** Pake volume `db_data` biar data database tetep aman walaupun container dimatiin 😺👍

---

## 🔧 Peralatan Tempur

Berikut senjata yang tak pakai buat ngejalanin proyek iki:

- 🐳 **Docker**
- 🧰 **Docker Compose**
- 📦 Image resmi dari Docker Hub:
  - `wordpress:latest`
  - `mariadb:latest`

---

## 🐣 Cara Nyobain Proyek Ini di Komputermu

### 📋 Syarat Wajib

- Wajib install **Docker Desktop** (Windows/Mac/Linux)  
  Kalau belum install, mampir ke [docker.com](https://www.docker.com/) dulu yaa~ 🐾

### 🚀 Langkah Instalasi

1. **Clone repositoriku:**
   ```bash
   git clone https://github.com/NAMA-ANDA/NAMA-REPO-ANDA.git
   ```

2. **Masuk ke folder project:**

   ```bash
   cd NAMA-REPO-ANDA
   ```

3. **Jalankan container-nya:**

   ```bash
   docker compose up -d
   ```

4. **Buka browser, akses WordPress:**

   ```
   http://localhost:8000
   ```

   Selamat\~ Kamu bakal liat halaman instalasi WordPress 🐱✨

5. **Kalau mau matiin:**

   ```bash
   docker compose down
   ```

   Tapi tenang ajaa, datamu tetep aman karena udah disimpen di volume 🛡️



Semoga bermanfaat yo rek\~ 😺
Ayo kita belajar bareng, biar DevOps gak cuma jadi istilah keren, tapi juga bisa kita praktekkan langsung! 💪✨
