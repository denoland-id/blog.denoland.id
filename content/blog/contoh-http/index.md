---
title: HTTP Web Service
date: 2020-05-09
description: Contoh HTTP dengan Deno runtime
---

Web Service menggunakan `HTTP/S` adalah bagian yang paling umum, 🦕 Deno dapat menjalankan `HTTP/S` seperti contoh di bawah:

```js
import { serve } from "https://deno.land/std@0.50.0/http/server.ts"

const s = serve({ port: 8000 })
console.log("http://localhost:8000/")
for await (const req of s) {
  req.respond({ body: "Hello World\n" })
}
```

Gunakan browser dan ketik `http://localhost:8000/`, akan terlihat `Hello World`

🚀 lebih lengkap [contoh lainnya](https://deno.land/)
