# Kampüs Etkinlik Backend API

## Çalıştırma Komutları

    npm install
    npm run seed
    npm run dev

## REST API Sözleşmesi

| Yöntem | Endpoint | Açıklama | Yanıt Kodları | Durum |
| :--- | :--- | :--- | :--- | :--- |
| GET | `/health` | Sunucu sağlık durumunu ve öğrenci numarasını döner | 200 OK | çalışıyor |
| GET | `/events` | Tüm etkinlik listesini tarihe göre sıralı döner | 200 OK | çalışıyor |
| GET | `/events?search=&category=` | Başlıkta arama ve kategoriye göre filtreleme yapar | 200 OK | çalışıyor |
| GET | `/events/upcoming` | Bugün ve sonrasındaki yaklaşan etkinlikleri tarihe göre sıralı döner | 200 OK | çalışıyor |
| GET | `/events/:id` | Belirtilen ID'li etkinliğin detayını döner | 200 OK / 404 Not Found | çalışıyor |
| POST | `/events` | Yeni etkinlik ekler (`GG-AA-YYYY` tarih biçimiyle) | 201 Created / 400 Bad Request | çalışıyor |
| PATCH | `/events/:id` | Belirtilen etkinliğin gönderilen alanlarını kısmi günceller | 200 OK / 400 Bad Request / 404 Not Found | çalışıyor |
| DELETE | `/events/:id` | Belirtilen etkinliği siler (gövde döndürmez) | 204 No Content / 404 Not Found | çalışıyor |