# TUTORIAL 10 (Broadcast Chat)
#### Rafi Ghani Harditama (2206081364)
#### ADPRO A / VRO

## Original code of broadcast chat
![alt text](image.png)

Dalam gambar tersebut, terlihat bahwa saya membuka empat terminal di mana salah satu terminal menjalankan perintah cargo `run --bin server`, sementara terminal lainnya menjalankan perintah `cargo run --bin client`. Setiap client mengirim pesan ke server, yang kemudian diterima dan dikirim kembali ke semua client.

## Modifying the websocket port
![alt text](image-1.png)


Dari gambar-gambar yang disajikan, terlihat bahwa program tetap berjalan dengan baik setelah port diubah menjadi 8080. Ini menunjukkan bahwa penggantian port tidak mempengaruhi fungsi komunikasi antara client dan server selama protokol yang digunakan tetap sama. Keduanya menggunakan protokol WebSocket yang dikelola oleh library tokio_websockets yang memastikan konsistensi dalam komunikasi. Meskipun port diubah, program tetap berjalan normal karena perubahan tersebut sudah direfleksikan dalam kode pada `client.rs` dan `server.rs.`