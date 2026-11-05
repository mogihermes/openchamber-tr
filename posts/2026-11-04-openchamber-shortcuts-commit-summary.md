# OpenChamber Shortcuts Commit Türkçe Özeti

- Düzeltme tarihi: 4 Kasım 2026, 23:01 UTC
- Commit: [feat(shortcuts): list every keyboard command in Settings](https://github.com/openchamber/openchamber/commit/0137dc30eb3022af139ef5cbe26ed2d025c6c208)

## Yenilikler

- **Tüm klavye komutları tek bir schema'da** declared: Settings ve menülerde tüm komutlar belirtilerek görünür ve rebound edilebilir.
- **In-app komutlar registered handlers'a taşınmıştır**: Yerel listener'lar kaldırılıp kayıtlı handler'lar kullanılıyor.
- **Permission replies window capture ile önceliklendirildi**: Cümleceklikler pencere yakalama içinde olduğundan composer öncesinde çalışıyor.
- **Desktop menü tuşları native accelerators korunmuştur**: Renderer efektif comboları main process menüyü yeniden oluşturuyor.
- **Editor find tuzu binding takip eder**: Find tuşu artık binding'i takip ediyor.
- **Leader modifier tutulduğunda sequence tamamlanır**: Ctrl+K ardından Ctrl+Board tuşu board'i açar yerine Ctrl+B'i çalıştırıyor.
- **Web ve electron:macOS üzerinde unit tests ile test edildi**.

## Düşünceler

- Tüm klavay shortcut'ları tek bir yerde tanımlanarak keymap clearliği sağlandı.
- Menü accelerators'ı platformdan bağımsız tutmak için normalizeMenuShortcuts kullanıldı.
- Desktop ortamında native accelerators korunarak mevcut çalışan kısayollar bozulmadı.

## Kaynakça

- Bu yazı, [resmî commit 0137dc30eb3022af139ef5cbe26ed2d025c6c208](https://github.com/openchamber/openchamber/commit/0137dc30eb3022af139ef5cbe26ed2d025c6c208) üzerine kuruludur. Teknik detaylar ve tam workflow değişiklikleri için esas alınır.
- [Resmî GitHub release v2.6.1](https://github.com/openchamber/openchamber/releases/tag/v2.6.1)
- [Commit: release v2.6.1](https://github.com/openchamber/openchamber/commit/ce853f415704d1bfe8d076a5cfb2caabac00fffd)
- Electron updated to 45.