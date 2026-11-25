# OpenChamber Integration Sessions Fix Türkçe Özeti

- **Düzeltme tarihi**: 25 Kasım 2026, 05:35 UTC+3
- **Commit**: [200587b00662bcea7d65ce216373c79a94cbcb07](https://github.com/openchamber/openchamber/commit/200587b00662bcea7d65ce216373c79a94cbcb07)
- **Sürüm**: (dev - main head)

## Değişiklik Özeti

Sunucu geçici checkout'ı kaldırdığında istemci oturumları actions after the server removed the temporary checkout, bu bağlantı arası kesintide veya tab'i kapatıldığında onlar deleted folder'a kalıyordu.

### Düzenlemeler

- **Abort and Continue**: Operating agent artık running agent'ı durdurup, checkout'tan her oturumu önce taşıyıp sonra kaldırıyor. Bu, bağlantı arası kesintide veya tab kapandığında remaining sessions'in deleted folder'a düşmesini önliyor.
- **Outcome recorded first**: Outcome kaydı öncelikle yapılıyor, bu nedenle bir restart sonrası işin tamamlanması sağlıyor.
- **Offline folder support**: Offline folder'lar bekletiliyor ve işin tamamlanmasını await ediyor.
- **Session restoration**: Hidden checkout'taki bir oturum bağlantısı again oturumu tekrar açabiliyor.

### Test kapsamı

- Idle, running ve archived sessions ile test edildi
- Tab kapatma ve bağlantı kaybedilme senaryoları test edildi
- Server switched ve killed senaryoları test edildi
- Detached volume senaryoları test edildi
- Running app ortamında test edildi

## Etkilenen Dosyalar

- `packages/ui/src/components/views/git/IntegrateConflictCard.tsx` - Sessions yönetimi güncellendi

## Referans

- Ana commit: [200587b00662bcea7d65ce216373c79a94cbcb07](https://github.com/openchamber/openchamber/commit/200587b00662bcea7d65ce216373c79a94cbcb07)
- Release notları: [v2.8.0](https://github.com/openchamber/openchamber/releases/tag/v2.8.0)