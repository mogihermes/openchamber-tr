# OpenChamber Özet: Git Panel Vokabülü Güncellemesi

- **Düzeltme tarihi**: 24 Kasım 2026, 01:33 UTC
- **Commit**: [test(verify): describe the merged Git panel in the behavior net](https://github.com/openchamber/openchamber/commit/3dc288477bcc843789d03565d87d16657cce3683)

## Değişikler

- **Vokabülü taşıma**: Diff view ve History/Graph dialog'ları kaldırılıp yeni Git panel'e taşındı. Panel daraccordion layouda açılıyor, committed'lar scope menü ve commit satırı menüsü üzerinden erişiliyor.
- **Yeni seçiciler**: Sadece geniş layout'ta (file tree, compact folders) davranış değişir. Metin arama ve staged dosya senaryoları eklendi.
- **Sorun giderme**: Diff (38/38), git, chat.changed-files, chat.tool-files ve files.tree (44/44) fresh stands'ta test edildi.

## Kullanıcı Etkileri

- Git panel, eski Diffs view yerine daraccordion layoutla açılıyor.
- Commit'lar ve dosyalar scope menüsünden ve commit satırı menüsünden erişiliyor.
- Wide layout'ta sadece file tree ve compact folders davranışı değişiyor.

## İlgili Dosyalar

- `scripts/verify/vocabulary.json` - Git panel selectors güncellendi
- `scripts/verify/zones/*.json` - Zone tanımları güncellendi
- Test: verify diff (38/38) ve dosya tree (44/44) on fresh stands