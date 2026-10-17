# BUG-03: POST /api/books буруу JSON биетэй хүсэлтэд 400 биш STATUS_CODE алдаа буцаадаг

Орчин: Уншлагын жагсаалт v2.0, curl.exe, Windows, 2026-10-17
Урьдчилсан нөхцөл: node app.js-ийг шинээр асаасан (анхны 3 ном)

## Дахин гаргах алхам
1. `body.json` файлд буруу JSON бичнэ: `{"title": "Test", "author": `
2. Дараах командыг ажиллуулна:
   `curl.exe -i -X POST http://localhost:3000/api/books -H "Content-Type: application/json" --data-binary "@body.json"`
3. Хариуны эхний мөрийг (HTTP/1.1 ...) харна.

Хүлээгдэж байсан: «Буруу JSON биетэй POST хүсэлтэд 400 алдаа буцаана» (спецификаци).
Бодит үр дүн: <the exact status line you saw, and anything else odd>
Ноцтой байдал: <Major / Minor, with a reason>
Хавсралт: evidence/bug-03-curl.txt
Олдсон аялал: Saboteur