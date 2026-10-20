# Automated exploratory probes — actual observations

Энэ нь реаль browser/API шалгалтын бүртгэл бөгөөд 60 минутын SBTM session биш. Тест бүр аппыг шинээр асаасан.

## BUG-01
- UTC: 2026-10-20T13:27:54+00:00
- Үйлдэл: Нэмэх товчийг бүх талбарыг хоосон орхин дарав
- Бодит: Эхэнд 3 ном → 4 ном; мессеж: 'Ном нэмэгдлээ'
- Хүлээгдсэн: Шинэ ном нэмэгдэхгүй, ойлгомжтой алдаа харагдана
- Evidence: `screenshots/bug-01.png`

## BUG-02
- UTC: 2026-10-20T13:27:54+00:00
- Үйлдэл: Он=999, бусад талбар бүрэн бөглөж нэмэв
- Бодит: Он=999 бүхий ном хүснэгтэд нэмэгдсэн: True
- Хүлээгдсэн: 1000–2100 хүрээнээс гадуур онтой ном нэмэгдэхгүй
- Evidence: `screenshots/bug-02.png`

## BUG-03
- UTC: 2026-10-20T13:27:55+00:00
- Үйлдэл: Одоо байгаа Clean Code / Robert C. Martin нэртэй номыг өөр оноор дахин нэмэв
- Бодит: Clean Code гэсэн 2 мөр харагдсан
- Хүлээгдсэн: Гарчиг, зохиолч ижил бол давхар оруулахгүй
- Evidence: `screenshots/bug-03.png`

## BUG-04
- UTC: 2026-10-20T13:27:56+00:00
- Үйлдэл: Хайлтад clean code (жижиг үсгээр) оруулж Хайх дарсан
- Бодит: 0 мөр буцсан
- Хүлээгдсэн: Clean Code ном 1 мөрөөр олдоно
- Evidence: `screenshots/bug-04.png`

## BUG-05
- UTC: 2026-10-20T13:27:57+00:00
- Үйлдэл: Эхний ном дээр Устгах дарсан
- Бодит: Номын мөр 3→2 болов, мессеж: 'Ном нэмэгдлээ'
- Хүлээгдсэн: Ном устгалаа гэсэн үйлдэлд тохирсон мессеж гарна
- Evidence: `screenshots/bug-05.png`

## BUG-06
- UTC: 2026-10-20T13:27:57+00:00
- Үйлдэл: Аппыг шинээр нээж Нийт ном тоолуурыг хүснэгтийн мөрийн тоотой харьцуулав
- Бодит: Хүснэгт: 3 мөр; статистик: 'Нийт ном: 4 · Хамгийн шинэ он: 2008'
- Хүлээгдсэн: Нийт ном 3 гэж харуулна
- Evidence: `screenshots/bug-06.png`

## BUG-07
- UTC: 2026-10-20T13:27:58+00:00
- Үйлдэл: Footer дахь Хуучин хувилбар холбоосын /old endpoint шалгав
- Бодит: HTTP 500; body: 'HTTP/1.1 500 Internal Server Error\nContent-Type: text/plain; charset=utf-8\nDate: Tue, 20 Oct 2026 13:27:58 GMT\nConnection: keep-alive\nKeep-Alive: timeout=5\nTransfer-Encoding: chunked\n\nInternal Server Error'
- Хүлээгдсэн: Хуудас/линк ажиллана; HTTP 2xx
- Evidence: `screenshots/bug-07.png; evidence/bug-07-curl.txt`

## BUG-08
- UTC: 2026-10-20T13:27:58+00:00
- Үйлдэл: POST /api/books руу malformed JSON илгээв
- Бодит: HTTP 200; хариу: 'HTTP/1.1 200 OK\nContent-Type: application/json\nDate: Tue, 20 Oct 2026 13:27:58 GMT\nConnection: keep-alive\nKeep-Alive: timeout=5\nTransfer-Encoding: chunked\n\n{"result":"OK"}'
- Хүлээгдсэн: HTTP 400
- Evidence: `evidence/bug-08-curl.txt`

