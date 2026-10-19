# Sohbet klasörleri aynı sunucudaki cihazlar arasında eşitleniyor

- Tarih: 19 Ekim 2026, 01:07 UTC
- Kaynak commit: [`bf977d2ed89c079ec592210d7cd0e2d649ba0636`](https://github.com/openchamber/openchamber/commit/bf977d2ed89c079ec592210d7cd0e2d649ba0636)

## Ne değişti

Aynı OpenChamber sunucusuna bağlı bilgisayar, web uygulaması ve telefon artık sohbet klasörlerini ortak kullanıyor. Bir cihazda klasör oluşturma, yeniden adlandırma, silme veya sohbete klasör atama işlemi yapıldığında diğer bağlı istemciler güncel klasörleri okuyor.

İstemciler klasörün tamamını yazmak yerine her işlemi `PATCH /api/session-folders` ile gönderiyor. Sunucu değişikliği kaydedip kontrol akışında `session-folders-changed` duyurusu yapıyor. İstemci, sunucu yazmayı tamamlayana kadar değişikliği depolamada bekletiyor.

Bir cihaz ilk kez bağlandığında kendi klasörlerini sunucuya aktarabiliyor. Aynı konumdaki aynı ada sahip klasörler birleştiriliyor. Sohbet silinirse sunucudaki klasörlerinden çıkarılıyor. Proje kapatılırsa o projenin klasörleri kaldırılıyor. Daraltılmış klasör durumu cihazda kalıyor.

Telefon, ortak klasörleri Tree görünümünde yalnızca okunur olarak gösteriyor. `PATCH` desteği olmayan sunucular önceki tam-kopya yazma yöntemini kullanıyor.

## Kaynak

Bu yazı, resmî OpenChamber commit açıklaması ve değişikliklerinin Türkçe özetidir. Ayrıntılar için [`bf977d2ed89c079ec592210d7cd0e2d649ba0636`](https://github.com/openchamber/openchamber/commit/bf977d2ed89c079ec592210d7cd0e2d649ba0636) esas alınır.
