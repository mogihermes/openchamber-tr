# OpenChamber Triage PR Finish Türkçe Özeti

- Düzeltme tarihi: 7 Kasım 2026, 01:50 UTC
- Sürüm: main (son commit)
- Commit: [docs(triage): record the latest standing decisions and finish PRs on Opus](https://github.com/openchamber/openchamber/commit/dbb862c5d889c9d9a1cae41eac2f515d4d391bd0)

## Düzeltme

- **Triage geçmiş kararlı kararları kaydetme**: OpenChamber artık triage sürecini बैठाकर standing decisions (durabilen kararları) records'ları korunur. Bu, PR'lerin tarihçe boyunca tutarlı değerlendirildiğinden emin olur.
- **Finish workflow'u Opus'a yönlendirme**: Finished workflownun Sol'dan Opus'a yönlendirilmesi. Workflow artık "fixes on Sol" zaslanıyor, "reviews on Sol" yerine "fixes on Opus" ve "reviews on Sol" yapılıyor.
- **Part of ifadesi korunması**: PR body'sinden issue linki dropped (atılması) bir PR'ı kapatır; `Part of #N` ifadesi açık bırakıldığında contribution gate PR'ı kapatmadan geçmesine izin verir.
- **Skill extensions read list**: Triage-prs skill artık extension read list'ini records. Bu, hangi eklentilerin okunup takip edileceği konusunda transparansi sağlar.
- **Plugin switch scope**: Plugin switch, OpenCode'daki her projeyi kapsar ve TUI, harici OpenCode ve kullanıcı config'ini etkilemeden bırakır.

## Test

- triage-prs skill testleri
- pr-triage-finish workflow testleri
- check:changed doğrulaması
- Upstream main commit doğrulaması

## Kaynakça

- [Resmî Commit dbb862c5d889c9d9a1cae41eac2f515d4d391bd0](https://github.com/openchamber/openchamber/commit/dbb862c5d889c9d9a1cae41eac2f515d4d391bd0)
- [Güncel main sha: dbb862c5d889c9d9a1cae41eac2f515d4d391bd0]