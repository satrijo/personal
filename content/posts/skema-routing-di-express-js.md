---
title: Skema Routing di Express JS
date: 2023-08-07T06:30:56.843Z
description: Membangun website yang patut diperhatikan adalah sistem routing.
  Hal ini agar memudahkan kita ketika sudah dalam tahap pengembangan yang
  kompleks. Dalam sistem routing Express JS sudah disediakan bagaimana kita
  untuk kemudahan dalam pengembangan aplikasi.
---
![](/img/http-requests-between-the-web-browser-and-the-server.png)

R﻿outing mengacu pada bagaimana mana kita merespon sebuah permitaan pada aplikasi kita. Permintaan ini berdasarkan pada URI (Uniform Resource Identifier) atau path dari sebuah aplikasi. Semisal

`get: h﻿ttps://aplikasi.kita/`

S﻿ebuah permintaan (kita sebut aja request) ini memiliki berbagai method yang bisa dibagi menjadi method GET, POST, PUT, PATCH, DELETE

S﻿ebelumnya kalau di NodeJS membuat route ini gampangnya seperti ini ya kodenya

```javascript
const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  const url = req.url
    if(url ==='/pelajaran'){
      res.write('data matapelajaran');
    } else if(url == '/kelas'){
      res.write('data kelas')
    } else {
      res.write('data apa yang kamu perlukan?'); 
    }
    res.end();
});
```

K﻿alau di Express JS sendiri sudah disiapkan sebuah module yang membantu dalam membuat route, jadi cara diatas ini bisa dibilang susah untuk diterapkan dipengembangan aplikasi

P﻿ada Express JS kode untuk membuat route cukup seperti dibawah ini:

```javascript
const express = require('express')
const app = express()

const port = 3000

app.get('/', (req,res) => {
  res.send('Ini Home dengan method GET')
})

app.post('/', (req,res) => {
  res.send('Ini home tapi method POST')
})

app.listen(port, () => {
  console.log(`Server running di ${port}`)
})
```

K﻿alau dilihat sekilas script pada expressJS lebih rapi ya dan mudah untuk dibaca, sedangkan kalau di nodeJS murni akan sangat susah untuk dimanage.

P﻿enjelasan dari script diatas pada baris 1 - 2 adalah inisialisasi / import ExpressJS dan menjalankannya pada variable app. 

U﻿ntuk bari 3 kita menentukan port mana yang ingin digunakan, biasanya kalau di Express menggunakan port 3000, kalau gagal berarti bisa menggunakan port yang lainnya.