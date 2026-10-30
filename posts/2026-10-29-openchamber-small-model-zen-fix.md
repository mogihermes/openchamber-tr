# OpenChamber püçük model Zen düzeltmesi Türkçe özet

- Düzeltme tarihi: 29 Ekim 2026, 21:04 UTC
- Commit: [fix(small-model): stop offering OpenCode Zen free models as the Small model without a login](https://github.com/openchamber/openchamber/commit/703d98b788756d1ae4721ca30f75b705f6c9e564)
- Fixes: #5869

## Düzeltme

OpenCode'nin ücretsiz Zen modelleri, giriş yapmadan (login olmadan) Small model seçiciye sunulduğunda her Small model çağrısı başarısız oluyor ve Yenileme with AI, yürüyüş ve hedef kontrol işlemleri hiçbir şey yapmıyor. Bu modeller Small model ve yürüyüş seçicilerinden tekrar çıkarılıyor ve zaten kaydedilmiş bir tane "ayarlanmamış" olarak sayılıyor. Zen girişi veya anahtar olduğu her Zen modelleri etkin kılar.

## Kaynak

Bu yazı, OpenChamber deposundaki ilgili commit üzerine kuruludur. Teknik detaylar için [resmî commit](https://github.com/openchamber/openchamber/commit/703d98b788756d1ae4721ca30f75b705f6c9e564) esas alınır.