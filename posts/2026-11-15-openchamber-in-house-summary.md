# OpenChamber Özet: in-house Etiketleri

- **Düzeltme tarihi**: 15 Kasım 2026, 18:10 UTC
- **Sürüm**: v2.7.2 (resmi sürüm)
- **Commit**: [feat(intake): close outside PRs on issues the core team builds itself](https://github.com/openchamber/openchamber/commit/d1f6410a760a4609f0aaa397725cdcb07eb068c7)

## Değişikler

- **in-house etiketi**: Issue'lara `in-house` etiketi eklendiğinde, bu issue'ı core team (the chambermakers) üyeleri build eder. Marked issue'lara sahip outside PR'ler kapatılır - triage collaborators, trusted contributors ve docs-only değişiklikler dahildir.

- **Contribution gate güncelleme**: `.github/scripts/pr-checks.cjs` güncelleştirildi - `in-house` etiketili issue'lar linked olursa, sadece maintainer/admin sahip PR'ler geçer. Diğerleri kapatılır.

- **PR intake workflow**: `.github/workflows/pr-intake.yml` güncelleştirildi - `in-house` etiketi `accepted` ve `bug` etiketleriyle birlikte kabul edilecek label'lar listesine eklendi.

- **CONTRIBUTING.md**: `in-house` etiketine dair bilgi eklendi - core team tarafından build edilen issue'lara sahip outside PR'ler kapatılır.

- **Triage skills güncellendi**: `.agents/skills/triage-issues/SKILL.md`, `.agents/skills/triage-prs/SKILL.md`, `.agents/skills/triage-issues/references/idea-rounds.md` güncellenerek `in-house` etiketi desteklendi.

## Kullanıcı Etkileri

- Issue'a `in-house` etiketi eklendiğinde, core team o issue'ı build edeceği belirtilmiş sayılır
- `in-house` etiketi linked bir PR'dan dışarıdan (dışaryı chambermakers dışındaysa) gönderilmişse, PR otomatik olarak kapatılır
- `accepted` etiketine birlikte `in-house` eklendiğinde, sadece core team üyelerinin PR'leri kabul edilir
- Dışarıdan yapılan PR'ler, `in-house` li issue'ları linked olsalar bile reviewed/değil kapatılır

## İlgili dosyalar

- `.github/workflows/pr-intake.yml` - `in-house` label kabul edilmesi eklendi
- `.github/scripts/pr-checks.cjs` - Contribution gate `in-house` kontrolü eklendi
- `.agents/skills/triage-issues/SKILL.md` - Issue triage skill güncellendi
- `.agents/skills/triage-prs/SKILL.md` - PR triage skill güncellendi
- `.agents/skills/triage-issues/references/idea-rounds.md` - Idea rounds referansı güncellendi
- `CONTRIBUTING.md` - Documentation güncellendi

## Özet

Bu güncelleme, OpenChamber'ın contribution gate'ına `in-house` etiketini ekler. Core team (repository'de maintain/admin sahibleri) build ettiği issue'ler için `in-house` etiketi eklenebiliyor. Bu etikete linked outside PR'ler kapatılır - yani core team o özelliği kendi içinde geliştirdiği için dışarıdan duplicate PR'lar gerekli değildir. `accepted` etiketi together with `in-house` kullanılarak, hangi feature'ların team tarafından build edileceği sistematik olarak belirlenebiliyor. Bu, contributorların gereksiz PR açmasını engeller ve maintainerin odaklı gelişim yapmasını sağlar.