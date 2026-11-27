# OpenChamber v2.8.1: File save fix (#7686)

**Resmi GitHub commit**: [`f613498effa1744c940e7096813eeba92d97a6b3`](https://github.com/openchamber/openchamber/commit/f613498effa1744c940e7096813eeba92d97a6b3)  
**Yayın tarihi**: 27 Kasım 2026 (UTC+03)  
**Etiket**: `v2.8.1`

## Değişiklik Özeti

Dosya kaydetme işlemi artık projede çalışan dev sunucularını yeniden başlatmaz.

### Sorun
Files panel'den yapılan kaydetmeler, geçici bir dosyayı hedefin yanına yazıp üzerine adlandırarak işlem yapıyordu. Windows'ta bu, klasörü izleyen watchexec uzantısı filtresi (watchexec -e ts) tarafından iki modify olayı tetikler, bu da her kaydedirme veya otomatik kaydetmede dev sunucuyu yeniden başlatıyordu.

### Çözüm
Kaydetmeler artık dosyayı yere yazıp eski kısmını keserek (editörler gibi) işlem yapıyor:
- Klasör `create` veya `rename` olayı görmez
- Kaydedilirken dosya asla boş kalmaz
- Dosyanın modu ve hard links korunur
- Aynı anda birden fazla kaydetme intertwine (çeşitlemez)
- Hedef dosyaya yazmadan önce özel (`wx`) bayrakla yeni dosya oluşturulur, bu da boşta kalıantasının hedef dışına yönlenmesini engeller

### Düzeltme
- **#7657**: Salt okunabilir dosyalara yazma denemesi "Access denied" hatasıyla reddedilip dosya unchanged kalır
- **#7686**: Dev server yeniden başlatma sorununa root cause çözümü

### Dosyalar
- `packages/web/server/lib/fs/text-write.ts` (yeni dosya)
- `packages/web/server/lib/fs/DOCUMENTATION.md` (güncellendi)
- `packages/web/server/lib/fs/routes.test.js` (güncellendi)
- `packages/web/server/lib/fs/routes.ts` (güncellendi)

## Teknik Detaylar
Yazar: `yulia-ivashko <yulia.ivashko@gmail.com>`  
Tarih: `2026-11-27T00:54:59Z`  
Doğrulama: ✅ Geçerli (PGP imzası var)  
Ana dosya değişikliği: `packages/web/server/lib/fs/DOCUMENTATION.md`