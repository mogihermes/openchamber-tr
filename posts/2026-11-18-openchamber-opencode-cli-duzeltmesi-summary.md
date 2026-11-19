# OpenChamber Özet: opencode CLI Retired Check Düzeltmesi

- **Düzeltme tarihi**: 18 Kasım 2026, 22:43 UTC
- **Sürüm**: v2.7.2 (resmi sürüm)
- **Commit**: [fix(opencode): narrow the retired bundled CLI check and apply it in VS Code](https://github.com/openchamber/openchamber/commit/f698cd04dea8c286b029afafd8ae16c4afe31cdc)

## Değişikler

- **retired bundled CLI check**: `opencodeBinary` ayarının `resources/opencode-cli` içerdiği her yolu eşleştirmeye çalışıyordu, alıntılı yol veya trailing ayracı kaçırılıyorsa VS Code eklentisi eski yol üzerinde başlatılma reddinde kalıyordu. Düzenleme, yalnızca OpenChamber'ın kendi masaüstü düzenine, temizlenmiş yola uyması gerekliğini sağlamakta ve eklenti böyle bir değer üzerinde atlamıyor.

- **Platform ayrımı**: Paylaşımlı sayfa shim araması sadece Windows'ta backslash'ları çeviriyor, bu yüzden POSIX klasör adında bir backslash remaining isim parçası olduğu gibi çalışmaya רצוי.

- **Contribution gate güncelleme**: `.github/scripts/pr-checks.cjs` ve `.github/workflows/pr-intake.yml` dosyaları etkilenmedi, `in-house` etiketi değişikliklerinden etkilenmiyor.

## Kullanıcı Etkileri

- VS Code üzerinden OpenChamber başlatan kullanıcılar için, eski `resources/opencode-cli` yolunu settings dosyasında belirtilmesi artık gereksiz kalıyor; eklentı otomatik olarak atlayıp varsayılan OpenCode'ı kullanacak.
- Windows kullanıcıları için backslash içeren yol isimleri unchanged kalıyor; düzeltme sadece Windows ortamında uygulanıyor.
- Diğer platformlar (macOS/Linux) için backslash değişmez, yol 그대로 işleniyor.

## İlgili dosyalar

- `packages/vscode/src/opencode.ts` - Retired check eklentisi eklendi, `isRetiredBundledCliSetting` fonksiyonu aktifleştirildi
- `packages/web/server/lib/opencode/bundled-opencode-server.ts` - `isRetiredBundledCliSetting` fonksiyonu eklendi, retired path tespiti iyileştirildi
- `packages/web/server/lib/opencode/env-runtime.test.js` - Retired CLI test durumları güncellendi
- `packages/web/vite-share-document.ts` - Windows slash dönüşümü logic'ı paylaşımlı shim içine taşındı
- `packages/web/vite-build-plugins.test.ts` - Share document testlerine Windows backslash testi eklendi

## Özet

Bu düzeltme, OpenChamber'ın masaüstü/UWP sürümlerinde OpenCode CLI yol tespit mekanizmasını iyileştirerek, kullanıcıların VS Code eklentisi "eskı yol üzerinde baştan başlatılamıyor" hatasını almasını engelledi. Artık kullanıcılar ayarlarında eski `resources/opencode-cli` yolunu silebilir veya geçersiz yollar belirtebilir; sistem otomatik olarak durumunu tespit edip varsayılan OpenCode'ı kullanacak. Düzeltme, chemin'lerdeki platform-specific backslash işlemlersel ayrımları doğru ele alacak şekilde yapılandırılmıştır.