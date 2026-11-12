# OpenChamber Özet: Markdown Önizleme Öğe Listesi

- **Düzeltme tarihi**: 11 Kasım 2026, 21:31 UTC
- **Sürüm**: v2.7.0 (resmi sürüm)
- **Commit**: [Outline özelliği eklendi](https://github.com/openchamber/openchamber/commit/d5c48e19e88267a5be25015525fdf2b5ea98cd66)

## Değişiklikler

- **Files toolbar (Dosya çubuğuna) Outline butonu**: Markdown dosyaları için eklendi. Önizleme'de filtrelenebilir başlık listesi açar ve seçilenine kaydırır; kaynak editörde ise editorın Sembol listesi'ni açar.

- **Düzeltilen hata**: #6320

## Kullanıcı etkileri

- Markdown önizlemede başlıkları filtreleyerek ve seçerek ilgili bölüme hızlıca gidebilirsiniz.
- Kaynak editörde Sembol listesi ile benzer şekilde navigation yapabilirsiniz.

## İlgili dosyalar

- `packages/ui/src/components/chat/markdown/markdownWindow.ts` - Outline fonksiyonu eklendi
- `packages/ui/src/components/chat/markdown/markdownWindow.test.ts` - Test eklendi

## Özet

Bu güncelleme, Markdown dosyalarında navigationı kolaylaştıran Outline özelliği ekler. Kullanıcılar artık uzun markdown dosyalarında başlıklar aramak ve önizlemede ilgili bölüme gitmek için Files toolbarundaki Outline butonunu kullanabilir.