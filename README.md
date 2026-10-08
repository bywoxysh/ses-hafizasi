# Ses Hafızası 🎧
### YouTube sesini kulaklığın ve OBS yayının için ayrı ayrı kontrol et

Ses Hafızası, Brave/Chromium tarayıcısındaki seçtiğin YouTube sekmesinin sesini **kulaklığın ve OBS yayının için bağımsız olarak ayarlamanı** sağlar.

Müziği kendin kısık dinlerken izleyicilerine daha yüksek bir seviyede gönderebilir veya yayını susturup kulaklığında dinlemeye devam edebilirsin.

Uygulama bir tarayıcı uzantısı ve bilgisayarında çalışan yerel yardımcı programdan oluşur.

---

## Ne işe yarar?

Normal kullanımda YouTube veya bilgisayar sesini kıstığında yayına giden ses de etkilenebilir. Ses Hafızası, seçtiğin sekmenin sesini iki ayrı kontrol üzerinden yönetir:

- **Kulaklığım:** Senin duyduğun ses seviyesini ayarlar.
- **Yayın:** OBS’ye gönderilen ses seviyesini ayarlar.

Örneğin kulaklık sesini %1 seviyesinde tutarken yayına gönderilen sesi −20 dB olarak ayarlayabilirsin.

Yalnızca **Başlat** düğmesine bastığın sekme aktarılır. Diğer açık YouTube sekmeleri otomatik olarak yayına eklenmez.

## Özellikler

- Kulaklık ve yayın için bağımsız ses kontrolü.
- Yayın sesinde −60 ile 0 dB arasında, 0,1 dB adımlarla ayarlama.
- Sayı yazarak yayın seviyesini belirleme.
- Yayın sesini susturma ve önceki seviyeye geri dönme.
- Siteye göre ses ayarlarını kaydetme.
- OBS’de gerekli Browser Source bağlantısını otomatik hazırlama.
- Sekmeler arasında geçişte mevcut OBS bağlantısını yeniden kullanma.
- Kaydedilmiş OBS susturma ayarlarını geri yükleme.
- Bilgisayar üzerinde yerel ses işleme ve aktarımı.

## Gereksinimler

- Windows 10 veya Windows 11, 64 bit.
- Standart OBS Studio 28 veya üzeri.
- Brave veya Chromium tabanlı, sürüm 116 veya üzeri bir tarayıcı.

Windows Brave/OBS üzerinde önceki yardımcı programla başarılı bir gerçek yayın denemesi bildirilmiştir. Taşınabilir OBS ve diğer tarayıcılar ayrıca doğrulanmamıştır.

---

## Kurulum

### 1. Uygulama paketini indir

Hazır Windows paketi yayımlandığında bu deponun **Releases** bölümündeki Windows ZIP dosyasını indir.

> **Code → Download ZIP** seçeneği kaynak kodunu indirir. Hazır Windows EXE dosyası içermez.

ZIP dosyasını bilgisayarında kalıcı bir klasöre çıkar. Uygulama ve uzantı dosyalarını bu klasörde tut.

### 2. Tarayıcı uzantısını yükle

Brave kullanıyorsan:

1. Adres çubuğuna `brave://extensions` yaz.
2. **Geliştirici modu** seçeneğini aç.
3. **Paketlenmemiş öğe yükle** düğmesine bas.
4. İndirdiğin paketin içindeki `uzanti` klasörünü seç.

Chrome kullanıyorsan uzantı sayfasına `chrome://extensions` adresinden ulaşabilirsin.

### 3. Yardımcı programı ve OBS’yi aç

1. Paketin içindeki `SesHafizasi.exe` dosyasını çalıştır.
2. OBS Studio’yu aç.
3. Mevcut OBS bağlantısı etkinse uygulama bunu otomatik kullanır.
4. Bağlantı etkin değilse uygulamanın açtığı kurulum sayfasındaki bir defalık adımları tamamla.

Windows’un varsayılan ses çıkışının kullandığın kulaklık olduğundan emin ol.

### 4. YouTube sekmesini seç

1. Yayına göndermek istediğin YouTube videosunu veya müziğini aç.
2. İçeriği oynat.
3. O sekmedeyken Ses Hafızası uzantısına tıkla.
4. **Başlat** düğmesine bas.

Seçtiğin sekmenin sesi artık kulaklık ve yayın kontrolleri üzerinden yönetilir.

---

## Nasıl kullanılır?

### Kulaklık sesini ayarlama

**Kulaklığım** kontrolünü kullanarak yalnızca senin duyduğun sesi değiştir.

Bu kontrol, OBS’ye gönderilen yayın seviyesini bağımsız bırakır.

### Yayın sesini ayarlama

**Yayın** kontrolü OBS’ye gönderilen sesi ayarlar.

Kaydırıcıyı kullanabilir veya dB değerini sayı olarak yazıp **Enter** tuşuna basabilirsin.

- **0 dB:** Kaynak sesine bu kontrol üzerinden azaltma uygulanmaz.
- **−20 dB:** Ses azaltılır.
- **−26 dB:** −20 dB’ye göre daha düşük bir seviyedir.
- Değer daha negatif oldukça yayın sesi azalır.

Bu kontrol otomatik ses normalizasyonu yapmaz. Farklı videoların kaynak ses seviyeleri farklı olabilir.

### Yayını susturma

**Sustur** düğmesi yayına gönderilen sesi keser.

**Sesi aç** düğmesi önceki yayın seviyesine geri döner.

### Gönderilen ses göstergesi

“Gönderilen ses” satırı gerçek sinyalin tepe seviyesini **dBFS** olarak gösterir. Bu değer müziğin veya videonun o andaki sesine göre değişir; yayın kaydırıcısındaki dB ayarıyla aynı ölçüm değildir.

### Başka bir sekmeye geçme

1. Mevcut kontrol penceresinde **Durdur** düğmesine bas.
2. Yeni YouTube sekmesine geç.
3. O sekmede uzantıyı açıp **Başlat** düğmesine bas.

OBS bağlantısını yeniden kurman gerekmez. Seçili sekmeyi kapatırsan o sekmenin aktarımı ve kontrol penceresi kapanır.

## Kullanım sırasında açık kalması gerekenler

- `SesHafizasi.exe` çalışır durumda kalmalıdır.
- Uzantının kontrol penceresi açık kalmalıdır; küçültebilirsin.
- Sesini aktardığın YouTube sekmesi açık kalmalıdır.
- Kurulum tamamlandıktan sonra uygulamanın kurulum web sayfasını kapatabilirsin.

Uzantıyı yükledikten sonra `uzanti` klasörünü taşıma veya silme.

YouTube’un kendi ses düğmesi yerine Ses Hafızası kontrollerini kullan. Yakalama sırasında YouTube medya sesi tam kaynak seviyesinde tutulur; aktarım durdurulunca önceki medya ayarları geri yüklenir.

---

## OBS ses kaynakları hakkında

Aynı sesin iki kez yayına gitmesini veya diğer sekmelerin duyulmasını önlemek için yardımcı program, çakışan **Masaüstü Sesi / Brave uygulama yakalama** kaynaklarını susturabilir. Mikrofon kaynakları korunur.

Oyun sesini de yayına vermek istiyorsan oyun için ayrı bir uygulama sesi yakalama kaynağı kullanman gerekebilir.

Kaydedilmiş önceki susturma durumlarına dönmek için uygulamadaki **Eski OBS ses ayarlarını geri al** düğmesini kullanabilirsin.

## Sorun giderme

### Yayında ses duyulmuyor

- OBS ve `SesHafizasi.exe` açık mı?
- Doğru YouTube sekmesinde **Başlat** düğmesine bastın mı?
- Video veya müzik oynuyor mu?
- Yayın kontrolü susturulmuş mu?
- OBS bağlantısı için bir defalık kurulum tamamlandı mı?

### Diğer sekmelerin sesi de yayına gidiyor

OBS’de Masaüstü Sesi veya tarayıcının tamamını yakalayan başka bir kaynak olup olmadığını kontrol et. Bu kaynaklar, seçili sekmenin dışında kalan sesleri de yakalayabilir.

### Kulaklıkta ses duyulmuyor

Windows’un varsayılan ses çıkışını ve **Kulaklığım** seviyesini kontrol et.

### Uzantı yüklenmiyor

Geliştirici modunun açık olduğundan ve `manifest.json` dosyasının bulunduğu `uzanti` klasörünü seçtiğinden emin ol.

---

## Kaynak kodunu çalıştırma

Geliştirme ve kaynak kodundan çalıştırma için **Node.js 24 veya üzeri** gerekir.

Proje klasöründe:

    npm ci
    npm start

Testleri çalıştırmak için:

    npm test
    npm run test:audio
    npm run test:browser

Tarayıcı testleri yerel bağlantı noktaları ve bir OBS protokol simülatörü kullanır. Testleri çalıştırmadan önce gerçek yardımcı programı kapat.

Derleme adımları: [docs/BUILD.md](docs/BUILD.md)  
Test kapsamı: [docs/TESTING.md](docs/TESTING.md)

Otomatik OBS testleri bir simülatör kullanır; gerçek Windows OBS ses çıkışının tamamını doğrulamaz.

## Gizlilik

Ses bilgisayarında işlenir ve yerel bağlantı üzerinden aktarılır. Uzak bir ses sunucusuna yüklenmez.

- Hesap gerektirmez.
- Telemetri içermez.
- Sanal ses kablosu gerektirmez.
- Yerel sunucu yalnızca `127.0.0.1` adresinde çalışır.
- OBS bağlantı bilgileri tarayıcı uzantısına gönderilmez.

## Sürüm

**7.3.0**, uzantının görünür adını ve proje belgelerini günceller; MIT lisanslı kaynak kodu, testler ve Windows derleme betiğini sunar.

Ses davranışı incelenmiş 7.2.1 sürümüyle aynıdır. Paket içindeki yardımcı program 7.2.0 sürümünü kullanır.

## Katkıda bulunma

Hata bildirimlerini ve geliştirme önerilerini GitHub **Issues** bölümünden paylaşabilirsin.

Katkı rehberi: [CONTRIBUTING.md](CONTRIBUTING.md)

## Lisans

Uygulamanın kaynak kodu [MIT lisansı](LICENSE) ile sunulmaktadır.

Hazır EXE, Node.js ve üçüncü taraf bileşenlerini içerir. Bunların lisans bildirimleri [NODE-LISANS.txt](NODE-LISANS.txt) dosyasındadır.

Bu proje OBS, Brave veya YouTube ile bağlantılı olmayan bağımsız bir topluluk projesidir.
