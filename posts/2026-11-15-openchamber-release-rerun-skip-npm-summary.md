# OpenChamber Özet: Release Rerun npm Atlaması

- **Düzeltme tarihi**: 15 Kasım 2026, 01:55 UTC
- **Sürüm**: v2.7.2 (resmi sürüm)
- **Commit**: [ci(release): let a rerun skip npm when the packages are already out](https://github.com/openchamber/openchamber/commit/aa1031fcc3e742803beeaa96d568407b6f543554)

## Değişikler

- **Rerun npm atlama**: Bir release yeniden çalıştırması (workflow_dispatch) närä npm publishing'ı atlayabilir. Önceki bir release whose desktop build failed after npm publishing could not be run again: npm refuses to publish a version twice. workflow_dispatch artık skip_npm seçeneği içerir; finalize-release skip_npm'li bir işi Completed sayar.

## Kullanıcı Etkileri

- Release workflow'unda npm publishing'ı manuel olarak atlayabilebilirsiniz
- Desktop build başarısız olsa bile, packages already on npm ise tekrarı skip edebilirsiniz
- finalize-release, skip_npm olan bir işi Completed olarak sayıyor
- Paket zaten npm'deyseAdded bir sürüm yayımlamaya gerek kalmaz

## İlgili dosyalar

- `.github/workflows/release.yml` - `skip_npm` seçeneği eklendi, `finish_published_release` koşulu güncellendi

## Özet

Bu güncelleme, release workflow'larında npm publishing'ı atlama seçeneği sağlar. Eğer bir önceki release'ın npm'de yayımlanmışsa ve desktop build başarısız olsa bile, rerun aşamasında npm atlayıp sadece remaining'leri publish edebilirsiniz. Bu, yanlışlı npm publish'ları önleyerek zaman ve kaynak tasarrufu sağlar.