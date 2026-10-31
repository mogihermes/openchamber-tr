# OpenChamber canary mobil uygulamalar ve release notes Türkçe özeti

- Düzeltme tarihi: 30 Ekim 2026, 23:21 UTC
- Commit: [feat(canary): mobile apps and nightly release notes in Canary builds](https://github.com/openchamber/openchamber/commit/d4a5a0ef13252fd60800c1a10c0eb08cc4aa15ff)
- Fixes: -

## Düzeltme

GitHub Actions canary workflow'ları güncellendi. Ana değişikler şunlar:

- **Mobil uygulamalar**: Phone apps store release'ları yok, bu yüzden Canary'lar olarak gider. Nightly workflow Android'i canary pre-release'e, iOS'yi TestFlight'a der. Stable release artık onları der.
- **Build numaraları**: Build numaraları epoch'tan geçen dakika sayısı olduğu için workflow'lar arası artış sağlar. Her Android app'en newest canary APK'i sunulur.
- **Canary notes (canary-notes.json)**: Nightly build, main'den since previous Canary'daki feat ve fix commits'ini canary-notes.json'ye yazar. Update dialog, kurulu build ile sunulan arasında gegeceki geceleri sekiz satıra folded gösterir.
- **Gece yazıları**: Notes, en yeni gecefirst, daha önceki geçmişle birlikte (en çok 30 gece saklanır). Her gece çalıştırıldığında, o gece yeni değişiklik varsa üzerine yazılır, yoksa bırakılır.
- **Desktop notes**: Shared version order kullanır, pre-release parçalarını okur.

## Yeni workflow değişiklikleri

### canary.yml
- Mobile app build job'ları eklendi (build-android, build-ios)
- Publish job'a build-android eklendi
- Canary notes generation eklendi (canary-notes.mjs kullanıcısı)
- Asset cleanup: eski canary notes ve sürüm dosyaları yönetildi

### mobile-release.yml
- `ref`, `app_version`, `build_number` inputs eklendi
- Build number: `${{ $(date -u +%s) / 60 }}` - epoch dakikası
- Platform ayrımı: Android ve iOS ayrı groups olarak izlenir
- App version setting: npm pkg set version ile yapılandırılabilir

### release.yml
- finish_published_release description güncellendi: sadece macOS ve iOS, npm, Windows, Linux ve Android atlar

## Kaynak

Bu yazı, OpenChamber deposundaki ilgili commit üzerine kuruludur. Teknik detaylar ve tam workflow değişiklikleri için [resmî commit](https://github.com/openchamber/openchamber/commit/d4a5a0ef13252fd60800c1a10c0eb08cc4aa15ff) esas alınır.

## Kaynak commit

[d4a5a0ef13252fd60800c1a10c0eb08cc4aa15ff](https://github.com/openchamber/openchamber/commit/d4a5a0ef13252fd60800c1a10c0eb08cc4aa15ff)