# AdımRota — Gizlilik Politikası / Privacy Policy

**Son Güncelleme:** 27 Mart 2026
**Geliştirici:** Yunus Emre Sevindik
**İletişim:** yunpels@icloud.com

---

## 1. Giriş

AdımRota ("Uygulama"), kullanıcıların yürüyüş aktivitelerini takip etmelerine, rotalarını harita üzerinde görüntülemelerine, uyku sürelerini kaydetmelerine, topluluk akışında paylaşım yapmalarına ve yürüyüş başarılarına dayalı uygulama içi koleksiyon kartları kazanmalarına olanak tanıyan bir sağlık ve fitness uygulamasıdır.

Bu Gizlilik Politikası, hangi verilerin toplandığını, nasıl kullanıldığını, kimlerle paylaşıldığını ve kullanıcıların verileri üzerindeki haklarını açıklar.

---

## 2. Toplanan Veriler

AdımRota, yalnızca uygulamanın temel özelliklerini sunmak için gerekli olan verileri toplar. Toplanan veri kategorileri aşağıda detaylı olarak açıklanmıştır:

### 2.1 Hesap Bilgileri (Kayıt Olduğunuzda)

Hesap oluşturduğunuzda aşağıdaki bilgiler toplanır:

| Veri | Amaç |
|------|-------|
| **E-posta adresi** | Hesap kimlik doğrulaması ve oturum açma |
| **Şifre** | Hesap güvenliği (Firebase Authentication tarafından şifrelenerek saklanır) |
| **Kullanıcı Kimliği (UID)** | Rota, paylaşım ve koleksiyon verilerinin hesabınızla ilişkilendirilmesi |

**İsteğe bağlı olarak** sağlayabileceğiniz bilgiler:

| Veri | Amaç |
|------|-------|
| **Boy (cm)** | BMI (Vücut Kitle İndeksi) hesaplaması ve daha doğru kalori tahmini |
| **Kilo (kg)** | Kalori yakım hesaplaması ve BMI analizi |
| **Biyografi** | Profil sayfanızda görünen kişisel tanıtım metni |

> **Not:** Telefon numarası toplanmaz. Kayıt için yalnızca e-posta ve şifre gereklidir.

### 2.2 Konum Verileri (İzninize Bağlı)

Konum verisi, yalnızca cihaz ayarlarından konum iznini verdiğinizde toplanır. Konum verileri şu amaçlarla kullanılır:

- **Yürüyüş rota takibi:** Yürüyüşünüzü harita üzerinde çizmek, mesafe hesaplamak ve rota geçmişinizi kaydetmek
- **Canlı konum paylaşımı:** Yalnızca siz manuel olarak başlattığınızda ve belirlediğiniz süre boyunca (15 dakika veya 1 saat) konumunuz paylaşılır. **Otomatik konum paylaşımı yapılmaz.** Her paylaşım için ayrı onay gerekir
- **Paylaşımlardaki konum etiketi:** Topluluk akışında paylaşım yaparken konum bilgisini dahil etmek isteğe bağlıdır ve varsayılan olarak **kapalıdır**
- **Ters coğrafi kodlama:** Koordinatlarınızın şehir/ilçe adına dönüştürülmesi (örn. "Kadıköy, İstanbul")

Toplanan konum bilgileri:

| Veri | Detay |
|------|-------|
| **GPS koordinatları (enlem/boylam)** | Rota çizimi ve mesafe hesabı |
| **Yatay doğruluk** | GPS sinyal kalitesi ölçümü |
| **Hız** | Anlık yürüyüş hızı |
| **Şehir/ilçe adı** | Ters coğrafi kodlama ile elde edilen konum adı |

### 2.3 Hareket ve Adım Verileri (İzninize Bağlı)

Cihazınızın hareket sensörleri aracılığıyla aşağıdaki veriler okunur:

| Veri | Kaynak | Amaç |
|------|--------|-------|
| **Adım sayısı** | Core Motion (CMPedometer) | Günlük adım takibi ve hedef izleme |
| **Yürüme mesafesi** | Core Motion (CMPedometer) | Mesafe hesaplama (km) |
| **Aktivite türü** | Core Motion (CMMotionActivity) | Yürüyüş/koşu/araç tespiti |
| **Tahmini kalori** | Uygulama içi hesaplama | Mesafe, süre ve kiloya dayalı kalori tahmini |

> **Önemli:** Bu veriler **Core Motion framework'ü** kullanılarak toplanır. HealthKit framework'ünden ayrı bir sistemdir.

### 2.4 Uyku Verileri — HealthKit (İzninize Bağlı)

Uygulamada iki farklı uyku takip yöntemi bulunur:

**a) Manuel Uyku Takibi:**
- "Uyudum" butonuna basarak uyku başlangıcını, "Uyandım" butonuna basarak bitiş zamanını kaydedersiniz
- Bu veriler Firestore veritabanında saklanır

**b) HealthKit Entegrasyonu (İsteğe Bağlı):**
- "HealthKit'ten Getir" butonu ile Apple Sağlık uygulamasındaki uyku analizi verilerinizi içe aktarabilirsiniz
- Uygulama, HealthKit'ten yalnızca **uyku analizi (Sleep Analysis)** verisini **okuma** izni ister
- HealthKit'e herhangi bir veri **yazılmaz**
- İçe aktarılan bilgiler: uyku başlangıç saati, bitiş saati ve toplam uyku süresi

### 2.5 Fotoğraflar ve Medya (İsteğe Bağlı)

Topluluk akışında paylaşım oluştururken:

- Fotoğraf galerinizden seçtiğiniz fotoğraflar Firebase Storage'a yüklenir
- Paylaşımlarınıza isteğe bağlı metin açıklaması (caption) ekleyebilirsiniz
- Paylaşımlarınızı **herkese açık** veya **gizli** (sadece siz görebilirsiniz) olarak ayarlayabilirsiniz

### 2.6 Koleksiyon Kartları (NFT Ödülleri)

Koleksiyon kartları, yürüyüş aktivitelerinize dayalı olarak kazanılan **uygulama içi başarı ödülleridir**:

- **Normal:** Günlük yürüyüş hedefini tamamladığınızda kazanılır
- **Nadir:** 5 km üzeri günlük yürüyüş mesafesinde kazanılır
- **Efsanevi:** 10 km üzeri günlük yürüyüş mesafesinde kazanılır

> **Önemli:** Bu kartların blockchain, kripto para veya herhangi bir harici cüzdan ile **hiçbir ilgisi yoktur**. Satılamaz, takas edilemez ve uygulama dışında kullanılamaz. Tamamen uygulama içi dekoratif ödüllerdir.

### 2.7 Kullanıcı Etkileşim Verileri

| Veri | Amaç |
|------|-------|
| **Engellenen kullanıcılar listesi** | İstemediğiniz kullanıcıların paylaşımlarını filtreleme |
| **Paylaşım tercihleri** | Herkese açık/gizli, konum dahil etme tercihleri |
| **Günlük adım hedefi** | Kişisel hedef takibi (varsayılan: 8.000 adım) |
| **Gizlilik tercihleri** | Fiziksel veri, rota ve profil görünürlük ayarları |

---

## 3. Verilerin Kullanım Amaçları

Toplanan veriler yalnızca aşağıdaki amaçlarla kullanılır:

1. **Uygulama işlevselliği:** Rota takibi, adım sayma, mesafe ve kalori hesaplama, uyku takibi
2. **Topluluk özellikleri:** Post paylaşımı, topluluk akışı ve kullanıcı etkileşimi
3. **Kişiselleştirme:** Günlük hedef takibi, BMI analizi, seviye rozetleri ve koleksiyon kartları
4. **Güvenlik:** Kullanıcı engelleme, kötüye kullanım önleme ve hesap koruması
5. **Uygulama iyileştirmesi:** Performans optimizasyonu ve hata düzeltme

> **Bu uygulama, verileri reklam, pazarlama veya üçüncü taraf veri analizi amacıyla KULLANMAZ.**

---

## 4. Herkese Açık ve Gizli Paylaşım

### Topluluk Akışı Paylaşımları

- **Herkese Açık (Public):** Akışta tüm kullanıcılara görünür. Konum bilgisini dahil etme varsayılan olarak **kapalıdır**; yalnızca siz açtığınızda paylaşımda görünür
- **Gizli (Private):** Yalnızca "Paylaşımlarım" bölümünde size görünür, akışta gösterilmez

### Canlı Konum Paylaşımı

- Canlı konum paylaşımı **her seferinde manuel olarak başlatılmalıdır**
- Süreler: 15 dakika veya 1 saat
- Paylaşım başlamadan önce **konum izni onay uyarısı** gösterilir
- "Haritada görünür ol" seçeneği varsayılan olarak **kapalıdır**
- **Otomatik check-in özelliği yoktur**
- Yalnızca paylaşım kodunu bildiğiniz kişiler konumunuzu görebilir

### Kullanıcı Engelleme

- Topluluk akışındaki diğer kullanıcıları engelleyebilirsiniz
- Engellenen kullanıcıların paylaşımları akışınızda otomatik olarak filtrelenir
- Engelleri "Gizlilik ve Güvenlik" ayarlarından kaldırabilirsiniz

---

## 5. Veri Depolama ve Üçüncü Taraf Hizmetleri

AdımRota, aşağıdaki üçüncü taraf hizmetlerini kullanır:

| Hizmet | Sağlayıcı | Kullanım Amacı |
|--------|-----------|----------------|
| **Firebase Authentication** | Google | E-posta/şifre ile hesap yönetimi |
| **Cloud Firestore** | Google | Kullanıcı profilleri, rotalar, paylaşımlar, koleksiyon kartları, engellenen kullanıcılar ve uyku kayıtlarının saklanması |
| **Firebase Storage** | Google | Paylaşımlardaki fotoğrafların saklanması |

Bu hizmetler, verileri bizim adımıza işler. Kendi güvenlik ve gizlilik politikalarına tabidirler:
- Google Firebase Gizlilik Politikası: https://firebase.google.com/support/privacy

> **AdımRota, kullanıcı verilerini hiçbir üçüncü taraf veri komisyoncusuna (data broker) satmaz veya paylaşmaz.**

---

## 6. Kullanılan Cihaz Çerçeveleri (Frameworks)

| Framework | Kullanım |
|-----------|----------|
| **Core Motion** | Adım sayacı, mesafe, aktivite algılama |
| **Core Location** | GPS rota takibi, canlı konum, ters coğrafi kodlama |
| **HealthKit** | Uyku analizi verilerini okuma (yazma yapılmaz) |
| **PhotosUI** | Galeri erişimi (paylaşım fotoğrafı seçimi) |
| **MapKit** | Harita görüntüleme |

---

## 7. Kullanıcı Hakları ve Kontroller

Verileriniz üzerinde tam kontrole sahipsiniz:

| Kontrol | Açıklama |
|---------|----------|
| **Cihaz İzinleri** | Konum, hareket/fitness ve fotoğraf erişimini cihaz Ayarlar'ından açıp kapatabilirsiniz |
| **HealthKit İzni** | HealthKit uyku verisi okumayı Ayarlar → Sağlık → Veri Erişimi bölümünden yönetebilirsiniz |
| **Paylaşım Kontrolü** | Her paylaşımı herkese açık veya gizli yapabilirsiniz |
| **Konum Dahil Etme** | Paylaşımlara konum ekleme varsayılan olarak kapalıdır, her seferinde manuel açmanız gerekir |
| **Canlı Konum** | Her seferinde manuel başlatılır, otomatik paylaşım yoktur |
| **Kullanıcı Engelleme** | İstemediğiniz kullanıcıları engelleyebilir, engeli kaldırabilirsiniz |
| **Paylaşım Silme** | Paylaşımlarınızı istediğiniz zaman silebilirsiniz |
| **Görünürlük Ayarları** | Fiziksel veriler, rotalar ve profil görünürlüğünü "Herkes", "Takipçiler" veya "Sadece Ben" olarak ayarlayabilirsiniz |
| **Konum Geçmişi Temizleme** | Tüm yürüyüş konum geçmişinizi silebilirsiniz |
| **Hesaptan Çıkış** | İstediğiniz zaman hesabınızdan çıkış yapabilirsiniz |
| **Hesap Silme** | Hesabınızı ve tüm ilişkili verileri kalıcı olarak silebilirsiniz |

---

## 8. Veri Saklama Süresi

- Verileriniz, uygulama özelliklerini sunmak için gerekli olduğu sürece saklanır
- Sildiğiniz paylaşımlar, veritabanından ve depolama alanından kaldırılır (ağ senkronizasyonu nedeniyle kısa süreli önbellekte kalabilir)
- Hesabınızı sildiğinizde tüm ilişkili veriler kalıcı olarak silinir
- Yasal zorunluluklar gerektirmedikçe, veriler gereksinim ortadan kalktığında silinir

---

## 9. Veri Güvenliği

- Firebase Authentication, şifreleri endüstri standardı güvenlik protokolleriyle şifreler
- Tüm veri aktarımları HTTPS (TLS) üzerinden gerçekleştirilir
- Firebase güvenlik kuralları, kullanıcıların yalnızca kendi verilerine erişmesini sağlar
- Hiçbir güvenlik yöntemi %100 garantili olmamakla birlikte, verilerinizi korumak için endüstri standardı önlemler uygulanmaktadır

---

## 10. Kullanıcı Takibi (Tracking)

- AdımRota, kullanıcıları **reklam amacıyla takip etmez**
- Uygulama verileri, üçüncü taraf veri komisyoncuları ile **paylaşılmaz**
- AppTrackingTransparency (ATT) izni, uygulama tarafından **istenmez** çünkü kullanıcı takibi yapılmamaktadır

---

## 11. Çocukların Gizliliği

AdımRota, 13 yaşın altındaki çocuklara (veya yargı bölgesizin gerektirdiği asgari yaş) yönelik değildir. 13 yaşın altındaki bireylerden bilerek kişisel veri toplamayız. Böyle bir durumun farkına varırsak, ilgili verileri derhal sileriz.

---

## 12. Instagram Paylaşımı

Uygulama, rota istatistiklerinizi Instagram Hikâyeleri olarak paylaşmanıza olanak tanır. Bu özellik kullanıldığında:

- Paylaşım kartı cihazınızda oluşturulur
- Veri, Instagram uygulamasına **doğrudan cihazınız üzerinden** aktarılır
- AdımRota sunucuları üzerinden herhangi bir Instagram verisi geçmez

---

## 13. Politika Değişiklikleri

Bu Gizlilik Politikasını zaman zaman güncelleyebiliriz. Değişiklik yapıldığında "Son Güncelleme" tarihini revize edeceğiz. Önemli değişiklikler için uygulama içinden bildirim yapılabilir.

---

## 14. İletişim

Bu Gizlilik Politikası hakkında sorularınız, talepleriniz veya geri bildirimleriniz için:

- **E-posta:** yunusemresevindik@icloud.com
- **Geliştirici:** Yunus Emre Sevindik

---

*Bu gizlilik politikası, AdımRota uygulamasının 1.0 sürümü için geçerlidir.*
