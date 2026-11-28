# OpenChamber v2.8.1: Concurrent save order fix

**Resmi GitHub commit**: [`dd70d9fc848b9b9b84b027bde0cedb562e9226f4`](https://github.com/openchamber/openchamber/commit/dd70d9fc848b9b9b84b027bde0cedb562e9226f4)  
**Yayın tarihi**: 27 Kasım 2026 (UTC+03)  
**Etiket**: `v2.8.1`

## Değişiklik Özeti

Dosya kaydetmeleri aynı dosyaya yapılan aynı anda çalışan kaydetmelerin gelme sırasını koruyacak şekilde artık sıralı işleniyor.

### Sorun

Bir dosyaya iki aynı anda yapılacak kaydetmenin (save) sonuçları gelme sırasına göre farklı dosyalara yazılıyor olabiliyordu. Route sadece son yazıyı serileştirirken, buna öncesi olan yol kontrolleri farklı zamanlar alıyor, bu da daha sonra gelen kaydın yazı çöpüne önce ulaşmasını ve daha önce gelen kaydın disk üzerinde kalmasını sağlıyordu. CI, buyi flaky routes testi olarak yakaladı.

### Çözüm

Yazı route artık her istenen yol için kaydetmeleri gönderim sırasından başlayarak, yol kontrollerini de içerdiği üzere tek tek işliyor. routes.ts'deki yedi aynı workspace yol çözümü tek bir yerel yardımcı işlev durch gider.

### Düzeltme

- **Yazı rotası**: Her yol için sıralı kaydetme (path checks dahil)
- **Test**: Yeni test, path kontrol ve cevap sırasını kaydedip düzeltilmeyen halde başarısız olur

### Dosyalar

- `packages/web/server/lib/fs/routes.ts` (güncellendi)

## Teknik Detaylar

- Yazar: `Bohdan Triapitsyn <artmore@protonmail.com>`
- Tarih: `2026-11-27T18:39:13Z`
- Doğrulama: ❌ İmzsiz (unsigned)
- Ana dosya değişikliği: `packages/web/server/lib/fs/routes.ts`