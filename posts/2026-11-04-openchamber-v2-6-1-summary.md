# OpenChamber v2.6.1 Türkçe Özeti

- Düzeltme tarihi: 4 Kasım 2026, 01:39 UTC
- Sürüm: [v2.6.1](https://github.com/openchamber/openchamber/releases/tag/v2.6.1)
- Commit: [release v2.6.1](https://github.com/openchamber/openchamber/commit/ce853f415704d1bfe8d076a5cfb2caabac00fffd)

## Yenilikler

- **Code review: pull request'i diff içinde direkt incele.** Satırlar, aralıklar ve tam dosyalar üzerinde yorum yapabilir, değişikler önerebilir ve satırların altında açık threads'i okuyup Review butonuna basarak vermiş olsunuz gibi gönderilir. GitHub, GitLab, Gerrit, Gitea ve Forgejo ile çalışır; taslağını diğer cihazlarınıza de takip edebilirsiniz.
- **Git: Kontrolünüz halürken bir PR otomatik birleşir.** PR eylemleri "In merge queue" konumunu veya Auto-merge on/Shows position gösterir. Hazır olduğunda kendisi birleşir, bildirimi kapatabilirsiniz. Repository'da GitHub'da auto-merge izin verilmelidir.
- **Sessions: Bir session'ı başka klasöre taşı.** Session ve başlık menülerinden taşı; klasör yeniden adlandırılmış veya silinmişse bileComposition, seçtiğiniz içeriği korur.
- **Linked items: Başka repo'daki issue veya PR'yi uygulamada açar.** Açıklama, aktivite, kontroller ve diff'leri birlikte gösterir; üzerine PR/issue'a ekleyebilirsiniz.
- **Unread: Daha fazlası gizlenen sitteleri belirtir, "Mark all as read" display menüsü ve dock (macOS) / taskbar (Windows) jump list'indeki okunmamışların listesi.**
- **Themes: Yeni Aurora açık ve koyu temaları.**
- **Themes: Custom theme dosyasındaki düzenlemeler uygulama içinde ayrıcalıksız olarak uygulanır, diff'ler de dahil.** Bozuk dosya, en son çalışan önceki sürümü korur.

## İyileştirmeler

- **Performance: Idleken çok daha az kaynak kullanır.** Masaüstü uygulamasında yaklaşık 3,400 session'da idle CPU 8.4'ten 3.4'te, saatlik background request'ler 3,800'ten 450'a düşer.
- **Add project: İletişim yeniden düzenlenir.** Home, proje klasörleri, Clone repository ve From OpenCode tek bir listede, ana buton ne eklediğini söyler ve seçim klasörler arasında kalıcıdır. From OpenCode sadece gerçek repository'leri gösterir.
- **Goal Mode: Ajant'i tek bir çalışmada tamamlamayı söyler.** İstek verilen commit veya pull request 'iş yapması gereken' sayılır olaraksayılır.
- **Settings/MCP: OpenCode kendi sunucularını readonly satırlar gösterir** (thanks to @DeryFerd).
- **Chat: Wrap toggles tables ve code blocks'da gösterilir aktifken** (thanks to @DeryFerd).

## Düzeltmeler

- **Worktrees: Birleştirildikten sonra temizleme tekrar worktre'leri arşivler, Context kaynaklardaki linked PR'ler ve issues canlı durum gösterir.**
- **Worktrees: Nested submodule'lar üzerinde fail olmadan creating one** (`filter=` in `.gitattributes`, remote without URL gibi git-annex'ten).
- **Git: PR'ler PIN ister** (security key), sadece Fetch branches in New worktree remotes'leri Kontakt eder.
- **Git: Ever fetched branch'lar olmadan stacked PR compare "not available locally" hatası vermez.**
- **Agents: Chat'ları yeniden isimlendiremez.** Naming artık sadece worktrees ve izole boşluklar için geçerlidir.
- **Safety mode: Global package installs ve commands uncommitted changes dropped** (örnek: `git checkout -- .`), onay sizi ister önce.
- **Sessions: Arka plan komutu, workflow veya pull request bekleyen session** working olarak everywhere gösterir: Unread section, dock badge, tray, Running section ve worktree rows.
- **Chat: Beklemeden bir mesaj gelince veya Activity açıkken soru/ sayfa chat'ta kalır** (thanks to @yulia-ivashko).
- **Chat: @ list saniyeler boyunca stall olmaz** (thanks to @yulia-ivashko).
- **Chat: @ listelerindeki agent'ların forms her zaman Send butonuna sahiptir.** Yanlış tag yazılmış bir block draw eder, nedenini belirtir.
- **Chat: Renderlenen sayfa artık daha yüksek büyütülmez.** (continue...)
- **Chat: @ listesi artık hızında stallsmaz** (thanks to @yulia-ivashko).
- **Chat: Message altında @ listeleri desktop'larda hover olmadığında gösterilir** (thanks to @DeryFerd).
- **Composer: Seçilen model tutarlı tutar** (agent değiştiğinde bile), göndermenin her zaman shown agent'iyle geçiş yapar.
- **Composer: Uzun message referansı metni kenarı geçmemesi** (continues past edge).
- **Multi-run: Armed goal her lane'de çalışır, next prompt'a sızamaz.** Agent picker parallel mode'da kalır.
- **Changes: Last turn sayacı an güncel olur, turn'un final adımı dahildir.**
- **Agents: Birden fazla prompt aldıysa parent result bir sonuç per run raporlar, parent aynı cevabı tekrarlamaz.**
- **Mobile: Workflows panel canlı güncelleme, cevap bekleyenleri sayfaya gösterir.** Web ve masaüstü SSE transport ayarıyla aynı.
- **Android: Bağlantı linki yapıştırıldığında bağlanır** (thanks to @yulia-ivashko).
- **Notifications: Telefon'un revoked olsa bile bildirimler gelir.**
- **Private relay: Chat images, file previews ve GitLab pictures gösterir.** HTML dosyası preview'ı yoksayabilir, Show code sunar.
- **Private relay: Saatlerce reconnect stuck host kendi içinde kurtar.**
- **Desktop: Session link uygulama'yı o session'ı açar, pencere açarken uygulama kapanmaz veya HMI'yi açık kalmaz.**
- **Desktop: Cmd+DevTools'ten ve built-in browser'ten Cmd+C kopyalar.**
- **Add project: Folder picker butonu Windows'ta File Explorer, Linux'ta File Manager** (thanks to @DeryFerd).
- **MCP: Bağlantı kurmuş sunucu kendi üzerinde olduğu için kapatmaz, consent ister sign-in** (thanks to @DeryFerd).
- **Chat: Wrap toggles tables ve code blocks'da aktif olduğunda gösterir** (thanks to @DeryFerd).
- **Chat: Wrap toggles codes blocks and tables aktive olduğunda gösterir** (thanks to @DeryFerd).
- **Chat: Wrap toggles code blocks and tables aktive olduğunda gösterir** (thanks to @DeryFerd).

## Fixes (continued)

- **Chat: @ listelerinden long stall ortadan kalkar** (thanks to @yulia-ivashko).
- **Chat: Message page long reply after scroll yapar, mesaj sayfaya appeared önceden beklemez** (thanks to @yulia-ivashko).
- **Chat: @ listesi hiçbir gecikmeden (seconds) stallsmaz** (thanks to @yulia-ivashko).
- **Chat: The @ list no longer stalls for seconds** (thanks to @yulia-ivashko).
- **Chat: the @ list no longer stalls for seconds with gitignored files hidden** (thanks to @yulia-ivashko) or dotfiles shown (thanks to @ChangeHow).
- **Chat: agents' forms always have a Send button** (continues...).
- **Chat: a rendered page no longer keeps growing taller**.
- **Chat: going back to a session restores your place more reliably** (thanks to @DeryFerd).
- **Chat: the @ list no longer stalls for seconds**.
- **Chat: the @ list no longer stalls for seconds with gitignored files hidden** (thanks to @yulia-ivashko).
- **Chat: links in tool rows follow your link settings**.
- **Chat: going back to a session restores your place more reliably** (thanks to @DeryFerd).
- **Chat: the @ list no longer stalls for seconds**.
- **Chat: links in tool rows follow your link settings**.

## SDK

- **Services: Her project'den session events'e subscribe contributes.sessionEvents, phone yanıtextra notifications channel** (thanks to @deatheros).
- **Trackers: Work items YouTrack, Jira veya Plane next to Linear with provides: ["tracker"] ve contributes.tracker** (thanks to @deatheros).
- **Shared surfaces: Key events carry keyCode computed by viewer's browser** (thanks to @JosueGalRe).
- **UI kit: Panels match app shadows ve badges, progress 100% only when done** (thanks to @JosueGalRe).

## Kaynakça

- Bu yazı, [resmî commit ce853f415704d1bfe8d076a5cfb2caabac00fffd](https://github.com/openchamber/openchamber/commit/ce853f415704d1bfe8d076a5cfb2caabac00fffd) üzerine kuruludur. Teknik detaylar ve tam workflow değişiklikleri için esas alınır.
- [Resmî GitHub release v2.6.1](https://github.com/openchamber/openchamber/releases/tag/v2.6.1)
- [Commit: release v2.6.1](https://github.com/openchamber/openchamber/commit/ce853f415704d1bfe8d076a5cfb2caabac00fffd)
- [OpenCode 2.2.5 güncellemesi](https://github.com/openchamber/openchamber/releases/tag/v2.6.1) (Bundled OpenCode updated to 2.2.5)
- Electron updated to 45.