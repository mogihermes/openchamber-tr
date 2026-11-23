# OpenChamber Özet: OpenCode Sunucu Pin Kontrolü Düzeltmesi

- **Düzeltme tarihi**: 23 Kasım 2026, 00:23 UTC
- **Commit**: [fix(scripts): check the OpenCode server pin @openchamber/web bundles, not the Docker CLI install](https://github.com/openchamber/openchamber/commit/3a0dbeafb42c6ea6d7ebb65ea5686b0b96ac566d)

## Değişikler

- **Pin kontrolü kaynağı**: OpenCode pin check'i Docker CLI install'ından @opencode/server pins'inin paket içindeki sürümlerle karşılaştırılmaya taşındı. Pin artık üç manifest'ta kontrol edilir: root package.json (@opencode/client), packages/electron/package.json (@opencode/server) ve packages/web/package.json (@opencode/server).

- **Dockerfile çıkarıldı**: `readDockerCliPin` fonksiyonu ve ilgili testler kaldırıldı, çünkü Docker imajı artık @opencode/cli paketiyle birlikte gelmiyor.

- **Hata mesajı güncellendi**: `checkOpencodePins` çıktısı artık `workspaceClient` pin'ını gösteriyor ve güncelleme komutları packages/web/package.json'u de dahil ediyor.

## Kullanıcı Etkileri

- OpenCode sürüm uyumluluğu artık Docker imajı yerine paket manifest'leri üzerinden kontrol edilir.
- Eğer pin'ler uyuşmazsa, güncelleme komutları packages/web/package.json'ı da içerecek şekilde genişletildi.
- Dockerfile'da @opencode/cli manuel pin yapılandırması artık gerekli değil; kontroller package.json'lara taşınmıştır.

## İlgili Dosyalar

- `scripts/check-opencode-pins.mjs` - Pin kontrolü three manifest'tan (workspace, electron, web) yapılıyor
- `scripts/check-opencode-pins.test.mjs` - Testler updated, Docker pin testi kaldırıldı

## Özet

Bu düzeltme, OpenCode sunucu pin'lerinin Docker CLI install yerine ofﬁce paket manifest'lerinde (packages/electron ve packages/web) kontrol edilmesini sağlayarak, versi uyumluluk kontrollerinin daha doğru ve güncel sürümlerle yapılmasını sağlar. Artık `@opencode/server` ve `@opencode/client` pin'leri packages/ dizinlerinde tek bir kaynak olarak tutulup Docker bağımsızca yönetildiği kontrol ediliyor.