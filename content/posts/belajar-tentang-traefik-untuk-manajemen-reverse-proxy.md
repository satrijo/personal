---
title: Belajar Tentang Traefik Untuk Manajemen Reverse Proxy
date: 2023-09-28T08:41:58.245Z
description: Kalau biasanya kita terbiasa dengan nginx atau apache, kali ini
  saya akan mencoba menggunakan tools baru yaitu Traefik. Saat ini implementasi
  pada production belum pernah saya coba tetapi kelihatannya menarik
---
![Traefik](/img/traefik-architecture.webp "Traefik Concepts")

Dulu mengembangkan aplikasi hanya cukup satu project yang dimana didalamnya sapu jagat apa saja dikerjakan atau sebut saja monolith, maka sekarang kita akan mencoba beralih ke microservices.