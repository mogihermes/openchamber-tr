# OpenChamber v2.5.3 Türkçe özet

- Yayın tarihi: 28 Ekim 2026, 15:15 UTC
- Resmî yayın: [OpenChamber v2.5.3](https://github.com/openchamber/openchamber/releases/tag/v2.5.3)

## Yeni özellikler

- **Snippets:** Mesajınız, seçili metin veya taslağınızı menüden veya `#` picker'ıyla bir snippet olarak kaydedebilirsiniz. Ayarlar'dan snippet'i yeniden adlandırıp proje arasında taşıyabilir ve neye genişleyeceğini önizleyebilirsiniz.
- **Images:** Ayarlar > Genel > OpenChamber Tools'undan bir resim modeli seçerek agent'lar resim üretebilir. Resimler chat'ta indirme butonu ile görünür. Öntanımlı kapalıdır.
- **Auto-review:** Review döngüsü tab'i kapalıysa veya telefon kilitliyse devam eder. 5 turdan sonra durur, bittiği kullanıcıya bir bildirimi gönderir ve tartışmalı sonuç ikonikada her iki konumda gösterilir.
- **Header tabs:** Her proje ve worktree için ayrı sekmeler seçeneği eklenerek, mevcut bulunduğunuz sekmenin gösterimi sağlandı.
- **Agents:** Agent, pull request'ını bekleyebilir ve bir kontrol başarısız/başarılı olduğunda, yorum geldiğinde veya birleştirildiğinde uyanır. Composer'da pull request gösterilir ve "watch" durumu kaldırılır.
- **Sidebar:** Worktree'lar menüsünden sabitleyebilirsiniz. "Worktree'leri dal adıyla adlandır" seçeneği dalı adını öncelikle gösterir.
- **Terminal:** Sekme terminallerde işlem bittiğinde otomatik olarak kapanır. Ayarlar > Genel > Terminal'de devre dışı bırakarak çıktıyı saklayabilirsiniz.
- **Drafts:** Yeni bir session "${N drafts}" göstererek, aynı klasördeki diğer bekleyen draft'ları açma veya discard etme seçeneği sağlar.
- **Dictation:** Whisper large-v3 turbo ve Qwen3-ASR yerel modeller eklenerek kısa ifadelerin tanınması iyileştirildi. "Yanlış duymuş kelimeler" seçeneği ile metin düzeltilebilir.

## İyileştirmeler

- **Sidebar:** Her satır sola ne olduğu, sağında durumunu gösterir. Project headers section olarak görüntülenir, zaman ve dallar daha okunabilir hale getirildi. Worktree'lar branch adına adlandırılır.
- **Sidebar:** Track ve Done sadece kendi çalışmaları olan satırlar üzerinde gösterilir, fork'lar kendi çalışmaları olarak sayılır.
- **Yeni session:** İlk mesaj anında gösterilir, ikinci Enter ile yeni session başlatılamaz (yulia-ivashko için teşekkürler).
- **Work Status:** Kart Files, Changes veya browser yanında varsa gösterilir.
- **Themes:** Tüm built-in thematiclerde ikinci metin, linkler ve atıf okunabilir, dark thematiclerde ikinci metin daha sakin gösterilir.
- **Files:** Document toolbars paylaşılmış görünüm elde ederek butonları aynı konumda tutar, açık dosya veya plan disk değişikliği olduğunda anında güncellenir.
- **Composer:** `@` session araması başlıktaki kelimeler üzerinden de eşleşir.
- **Small Model:** DeepSeek veya GLM flash gibi küçük modellerde side work devam eder.
- **Worktrees:** Issue worktree'ları agent'ın dal adını issue numarası önünde gösterir (örnek: `fix/5747-stale-favorite-models`).
- **Sidebar rows:** Satırların solunda ne olduğu, sağında durum görünümlüdür. Project headers section olarak görüntülenir, zaman ve dallar daha okunur. Worktree bir taskına bağlıysa issue numarası öne gelir.
- **New session:** İlk mesaj anında görünür, ikinci Enter ile yeni session başlatılamaz.
- **Work Status:** Kart Files, Changes veya browser yanında gösterilir.
- **Themes:** Tüm built-in temalarda ikinci metin, linkler ve atıf okunabilir, dark thematiclerde ikinci metin daha sakin gösterilir.
- **Files:** Document toolbars ortak görünüm, butonlar aynı konumda tutulur. Açık dosya veya plan disk değiştiğinde anında güncellenir.
- **Composer:** `@` session araması başlıktaki kelimeler arasında eşleşir.
- **Small Model:** DeepSeek veya GLM flash gibi küçük modellerde side work devam eder.
- **Worktrees:** Issue worktree'ları agent'ın dal adını issue numarası öne gelir (örnek: `fix/5747-stale-favorite-models`).

## Düzeltmeler

- **Providers:** API key veya OAuth ile bağlantı ilk denemede çalışır.
- **Sessions:** Çok session'lı bir klasörde çalışırken, agent artık saatlik olarak gigabayt veri göndermez.
- **Git:** GitHub Enterprise ve self-hosted GitLab'arında şirket sertifikası arkasında git bağlantıları ilk denemede çalışır.
- **Windows:** OpenCode'yu uygulama üzerinden güncellemek daha sonra broken kalmaktan kaçınır.
- **Worktrees:** Main üzerinde sitting bir worktree silindiğinde main'i silme teklifi göstermez (yulia-ivashko için teşekkürler).
- **Sessions:** Başka klasöre taşınan session'lar arkasında kopya bırakmaz, permission kartları agent mid-turn taşıdığı session'a ulaşır.
- **Sidebar:** Sessions in work dışındaki project'lar "In work" içinde kalır.
- **Sidebar:** Satırın herhangi bir yerine tık ile açılır, sürlendiğinde pointer altındaki folder'a sadece düşer.
- **Issues and PRs:** Birkaç GitHub checkout'lu bir klasör, validation hatası yerine list gösterir (guidan-nick için teşekkürler).
- **Desktop:** Başka bir örneğin bildirimi, onu gösteren pencere içinde açılır (timothywang21 için teşekkürler).
- **Desktop:** Update download progress %100'da durur (bashrusakh için teşekkürler).
- **Desktop:** Dock badge sadece sidebar'da gösterilen chat'lar sayar.
- **Browser:** Agent'in gizli sekmesinde çalışan app tam hızda çalışır.
- **Settings/Providers:** `opencode.jsonc` içinde kaydedilmiş custom provider düzenlenebilir (yulia-ivashko için teşekkürler).
- **Skills:** Non-Latin klasör isimli projelerde skill'lar kapatılabilir (yulia-ivashko için teşekkürler).
- **Plugins:** Plugin listesinde enable/disable kuralları "broken plugin" olarak gösterilmez.
- **Chat:** Folder'a bir link açıldığında Finder'da açılır (yulia-ivashko için teşekkürler).
- **Chat:** Reference chips harflerini kesilmez.
- **Models:** Favorite-model shortcutı, provider'ı disconnected favori'leri atlar.
- **Header:** Session menü, sekmeler kapalı olduğunda "Move to project" seçeneği sunar.
- **Composer:** Drafts menüsündeki çarpı, draft'ı discard etmetinstead of opening it.
- **Comments:** Whole-file comment field, bulunduğunuz konumda açılarak uzun dosyalarda da çalışır.
- **Folder trust:** Uygesta bir plugin'import edilen yerel dosya değiştiğinde tekrar sorar.
- **Web:** İlk yükleme başarısız olursa tekrar deneme yapar, boş kalmaz.

## Misc

- Bundled OpenCode 2.2.0, atualmente desteklenen en düşük sürüm güncellendi.
- Git library güvenlik ilanları geçti.
- **Desktop:** Help > Suggest a Feature, feature request açar.

## Kaynak

Bu yazı, resmî OpenChamber yayın notlarının Türkçe özetidir. Eksiksiz teknik ayrıntılar için [resmî yayın](https://github.com/openchamber/openchamber/releases/tag/v2.5.3) esas alınır.

## Kaynak commit

[c90a081c5a4a33766ee751ba6951f2f88d2fb6f80](https://github.com/openchamber/openchamber/commit/90a081c5a4a33766ee751ba6951f2f88d2fb6f80)