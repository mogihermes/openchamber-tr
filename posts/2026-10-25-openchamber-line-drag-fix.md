# Sürükleme ile satır numarası düzeltmesi

- Tarih: 25 Ekim 2026, 08:21 UTC
- Kaynak commit: [`9fe0a46fb2fc6ef856cb0ca316ac12c179789922`](https://github.com/openchamber/openchamber/commit/9fe0a46fb2fc6ef856cb0ca316ac12c179789922)

## Ne değişti

`fix(files): line range follows a drag that leaves the line numbers (#5581)` commits, Files view ve plan editöründe sürükleme seçimi düzeltilmiştir.

**Önki durum:** Satır numaralarını sürüklerken, işaretçi kod alanına kaydığında uzatma durduruluyordu, pencerenin kenarına scrolle olmuyordu ve basmadan bırakılan tıklama ile seçenek temizleniyordu.

**Yeni durum:** Sürükleme artık pencere üzerinde izleniyor, kenarlarındayken scroll oluyor ve basmadan bırakılan tıklama yoksayılıyor.

**Düzeltilen sorun:** #5556

**Dosyalar:**

1. **`packages/ui/src/components/comments/useLineNumberDragSelection.test.tsx`** (213 satır eklendi):  
   - Yeni test dosyası, satır numarası sürükleme davranışını test eder

2. **`packages/ui/src/components/comments/index.ts`** (1 satır eklendi):  
   - `useLineNumberDragSelection` dışa aktarılıyor

## Nasıl düzeltildi

- Sürükleme etkileşimi pencere seviyesine taşındı, böylece kenar scroll davranışı aktif olur
- Basmadan bırakılan tıklama, seçimi temizlerken iptal edilerek sürüklemenin tamamlanması sağlanır

## Kaynak

Bu yazı, resmî OpenChamber commit değişikliklerinin Türkçe özetidir. Ayrıntılar için [`9fe0a46fb2fc6ef856cb0ca316ac12c179789922`](https://github.com/openchamber/openchamber/commit/9fe0a46fb2fc6ef856cb0ca316ac12c179789922) esas alınır.

## Yeni sürüm

- OpenChamber v2.5.1: [GitHub Releases](https://github.com/openchamber/openchamber/releases/tag/v2.5.1) (23 Ekim 2026)