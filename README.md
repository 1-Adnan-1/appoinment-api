# Nadevu API

Randevuları yönetmek için Node.js ve Express ile hazırlanmış basit bir REST API. Veriler `data/db.json` dosyasında saklanır.

## Başlatma

```bash
npm install
node server.js
```

Sunucu `http://localhost:3000` adresinde çalışır.

## Uç noktalar

| Metot | Uç | İşlem |
| --- | --- | --- |
| GET | `/api/appointments` | Randevuları listele |
| GET | `/api/appointments/doctor/:doctor` | Doktorun randevularını listele |
| GET | `/api/appointments/:id` | Randevu detayını getir |
| POST | `/api/appointments` | Randevu oluştur |
| PATCH | `/api/appointments/:id` | Randevuyu güncelle |
| DELETE | `/api/appointments/:id` | Randevuyu sil |

## Örnek

```bash
curl http://localhost:3000/api/appointments
```

Yeni randevu için JSON gövdesi gönderin. `id`, `createdAt` ve `updatedAt` alanları sunucu tarafından oluşturulur.

> GitHub'a yüklemeden önce `data/db.json` içindeki kişisel bilgi biçimindeki örnek verileri anonimleştirin.
