# pnpm-store yollarını tespit düzeltmesi

- Tarih: 24 Ekim 2026, 07:53 UTC
- Kaynak commit: [`1dc7e6c9396ef1b01303dab59c17451f19005680`](https://github.com/openchamber/openchamber/commit/1dc7e6c9396ef1b01303dab59c17451f19005680)

## Ne değişti

`detectPackageManager()` fonksiyonu, paket yöneticisini tespit etmek için pnpm-store yollarını (`/pnpm-store/`) artık tanıyor. Bu değişiklik, pnpm deponu farklı konumlarda kurulan sistemlerde doğru çalışmasını sağlar.

**Dosyalar:**

1. **`packages/web/server/lib/package-manager.js`** (1 satır değiştirme):
   - `detectPackageManagerFromInstallPath()` fonksiyonuna `/pnpm-store/` kontrolü eklendi
   - Artık `/pnpm-store/` içeren yollar `pnpm` olarak sınıflandırılır

2. **`packages/web/server/lib/package-manager.test.js`** (48 satır ekleme):
   - `path` ve `fileURLToPath` importları eklendi
   - `pnpm-store` yollarını test eden 5 test durumu eklendi:
     - Windows pnpm store yolu
     - POSIX pnpm store yolu
     - Büyük/küçük harf hassasiyetineensitive Windows pnpm store yolu
     - Digital pnpm virtual store yolu
     - npm install yolu
     - Benzer ama farklı bir store adı

## Nasıl düzeltildi

- Normalized yol (`pkgPath.toLowerCase()`) içinde `/pnpm-store/` dizgesi aranır
- Eğer yol `/pnpm-store/` içeriyorsa, paket yöneticisi `pnpm` olarak döndürülür
- Bu, kullanıcıların kustom pnpm-store konumlarında OpenChamber'ı kullandığında doğru paket yöneticisi tespitini sağlar

## Kaynak

Bu yazı, resmî OpenChamber commit değişikliklerinin Türkçe özetidir. Ayrıntılar için [`1dc7e6c9396ef1b01303dab59c17451f19005680`](https://github.com/openchamber/openchamber/commit/1dc7e6c9396ef1b01303dab59c17451f19005680) esas alınır.

## Yeni sürüm

- OpenChamber v2.5.1: [GitHub Releases](https://github.com/openchamber/openchamber/releases/tag/v2.5.1) (23 Ekim 2026)