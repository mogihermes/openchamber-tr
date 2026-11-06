# OpenChamber Worktree Teardown Fix Türkçe Özeti

- Düzeltme tarihi: 5 Kasım 2026, 23:40 UTC
- Sürüm: main (son commit)
- Commit: [fix(worktrees): close the teardown gaps left after the teardown commands landed](https://github.com/openchamber/openchamber/commit/3e9d5bd5284651be3fc4823ea844a57b70ec28eb)

## Düzeltme

- **Contributor worktree silindiğinde teardown gap'leri kapatıldı**: VS Code'dan contributor-fork worktree silindiğinde, host never server's provenance store'ı okumamıştı. Newer trust prompt açıldığında delete personal commands sadece çalıştı ve stack devam etti.
- **Trusted teardown during merged cleanup**: Başarısız teardown during merged cleanup her seferinde session'ları archive ve restore etti.
- **Server's provenance store through isContributorForkGitDirectory**: Host artık server's store'dan answers veriyor; okuyamazsa store hiçbir şey çalıştırmadan worktree'i yaşıyor.
- **Archive route artık teardownCommand kullanmıyor**: Archive, teardown'ı kendi request'iyle çalıştırarak archive ediyor; hiçbir released client teardownCommand göndermiyor.
- **Newer prompt waits for open teardown prompt**: Open bir teardown prompt olduğu newer prompt bekliyor.

## Test

- sharedTrustConfirmation, worktreeArchive, worktreeManager, gitService.worktree-remove with store written by server's code
- contributor-provenance-storage routes and service tests
- extension build ve check:changed
- Live VS Code veya Windows'da çalıştırılmadı.

## Kaynakça

- [Resmî Commit 3e9d5bd5284651be3fc4823ea844a57b70ec28eb](https://github.com/openchamber/openchamber/commit/3e9d5bd5284651be3fc4823ea844a57b70ec28eb)
- [Güncel main sha: 3e9d5bd5284651be3fc4823ea844a57b70ec28eb]