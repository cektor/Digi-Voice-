# Privacy Policy — Digi Voice

**Last Updated:** June 26, 2026  
**Application:** Digi Voice (`com.alg.dmrvoice`)  
**Developer:** ALG Soft — [algsoft.net.tr](https://algsoft.net.tr)  
**Contact:** [fatih@radio.org.tr](mailto:fatih@radio.org.tr)

---

## 🇬🇧 English

---

### 1 · Digi Voice Does NOT Collect Any Data

> **Digi Voice does not operate any servers, databases, or backend services of its own. It does not collect, store, transmit, sell, or share any personally identifiable information with its developer.**

Digi Voice **never**:

- ✗ Sends your data to the developer or any Digi Voice-owned server  
- ✗ Uses analytics, crash-reporting, or advertising SDKs  
- ✗ Tracks your behaviour, usage patterns, or location history  
- ✗ Creates or manages user accounts  
- ✗ Processes or stores payments  
- ✗ Shares data with advertisers or data brokers  

---

### 2 · How the App Works — Data Flows

Digi Voice is a Push-to-Talk (PTT) radio client that connects to publicly-operated amateur radio networks. All data flows described below are **directly between your device and those third-party radio infrastructure servers** — not through or to Digi Voice.

#### 2.1 · Radio Network Connections (BrandMeister, TGIF, etc.)

When you connect to a radio network, the app sends your **callsign**, **DMR ID**, and real-time **voice audio** directly to the server you selected. This is the fundamental mechanism of every amateur radio digital network protocol (DMR, D-STAR, M17, YSF, P25, NXDN).

> Your callsign and DMR ID are **public information** within the amateur radio community and are voluntarily registered by you on third-party platforms such as **BrandMeister** and **RadioID.net**. Digi Voice does not register, hold, or manage these credentials.

#### 2.2 · RadioID.net Database Lookups

Digi Voice may query the public [RadioID.net](https://radioid.net) API to resolve a callsign to a DMR ID (or vice versa) for display purposes. This query sends only the callsign or DMR ID — both publicly available in the global amateur radio registry. No other personal information is transmitted. RadioID.net is an independent service with its own privacy policy at [radioid.net](https://radioid.net).

#### 2.3 · GPS / Location

Location access is **optional**. If you grant the Location permission, the app determines your GPS coordinates to calculate your *Maidenhead QTH grid locator* — a standard identifier used by ham radio operators worldwide. The grid locator may be transmitted to the connected radio server as part of the protocol. It is **not** transmitted to Digi Voice, stored in any remote database, or shared with any advertising service.

#### 2.4 · Microphone

The microphone is used solely to capture your voice during PTT transmissions. Audio is encoded and streamed in real-time to the selected radio server. Digi Voice does not record, store, or upload audio to any service.

#### 2.5 · Server List Downloads

Digi Voice downloads publicly available server host lists (e.g. from *pistar.uk*, *m17project.org*) to populate the server selection menu. These are plain-text files maintained by the amateur radio community. No personal data is included in these requests.

#### 2.6 · Log Files (Device-Only)

The application writes diagnostic logs **only to your device's local storage**. These files are never uploaded anywhere. You can view and delete them from the *Log* tab inside the app.

#### 2.7 · Settings Export / Import

Digi Voice provides an optional feature that lets you export all your application settings to a `.config` file and import them on any other device or platform that supports the same format. This feature:

- Is triggered **only by you** via the Settings screen — never runs automatically.
- Uses Android's **Storage Access Framework** (system file picker); no additional storage permissions are required.
- Saves the file **exactly where you choose** — the app has no access to any other location on your device.
- Does **not** upload the file to any server or cloud service.

> **Important:** The exported `.config` file contains your callsign, DMR ID, network passwords (BrandMeister, TGIF, AllStar), talk-group preferences, and all other application settings in plain JSON format. **Store this file securely** and do not share it with untrusted parties.

---

### 3 · Android Permissions

| Permission | Why it is needed |
|---|---|
| `RECORD_AUDIO` | Capture your voice for PTT radio transmission. |
| `INTERNET` | Connect to radio servers and download server host lists. |
| `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION` | Optional. Calculate your Maidenhead QTH grid square. |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MICROPHONE`, `FOREGROUND_SERVICE_PHONE_CALL` | Keep the radio connection active in the background with a visible notification. |
| `POST_NOTIFICATIONS` | Show the foreground-service notification (required on Android 13+). |
| `WAKE_LOCK` | Prevent the device from sleeping during an active connection. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Optionally exempt the app from Doze Mode for stable radio links. |
| `ACCESS_NETWORK_STATE` | Detect network availability before connecting. |
| `MEDIA_CONTENT_CONTROL` | Handle hardware PTT buttons (volume keys, headset buttons). |
| `WRITE_EXTERNAL_STORAGE` | Write diagnostic log files on Android 9 and below. |

> **Settings export/import** uses Android's Storage Access Framework (SAF) and requires **no additional permissions**. The system file picker handles all storage access on behalf of the user.

---

### 4 · Third-Party Services

| Service | Purpose | Data Sent |
|---|---|---|
| **BrandMeister** (`brandmeister.network`) | DMR radio network | Callsign, DMR ID, voice audio, optional GPS grid |
| **RadioID.net** (`radioid.net`) | Public callsign/DMR ID registry lookup | Callsign or DMR ID (public data) |
| **Other Reflectors** (TGIF, M17, D-STAR, YSF, P25, NXDN, FCS) | Radio network connections | Callsign, radio ID, voice audio, optional GPS grid |
| **Server Host Lists** (pistar.uk, m17project.org, etc.) | Download lists of available reflectors | None — anonymous requests only |

---

### 5 · Managing Your Data on Third-Party Platforms

> **Important:** Your callsign, DMR ID, name, and other personal information associated with amateur radio registration are held exclusively by **BrandMeister**, **RadioID.net**, and other radio network operators — *not by Digi Voice*.

If you wish to view, edit, or delete your personal data:

- **BrandMeister:** Log in at [brandmeister.network](https://brandmeister.network) and manage your profile or contact their support team.  
- **RadioID.net:** Log in at [radioid.net](https://radioid.net) and use their account management tools.

Because Digi Voice holds **no copy** of your personal information, you **cannot request data deletion from Digi Voice** — all such requests must be directed to the respective platform where your data resides.

---

### 6 · Data Stored on Your Device

Digi Voice stores the following **only on your device** (Android's encrypted DataStore):

- Your callsign and radio ID (used only to connect to radio servers)  
- Selected server and talk-group preferences  
- Application settings (audio levels, PTT key, mode, favourite talk groups, etc.)  
- Diagnostic log files (viewable and deletable from within the app)  

None of this data is backed up to the developer's servers. Uninstalling the app removes all locally stored data.

You may optionally export all settings to a `.config` file stored in a location of your choosing. The exported file remains entirely under your control — Digi Voice does not retain a copy and cannot access it after export.

---

### 7 · Children's Privacy

Digi Voice is intended for licensed amateur radio operators. It is not directed at children under 13 years of age and does not knowingly collect personal information from children.

---

### 8 · Security

All communication with RadioID.net uses HTTPS. Radio server connections use the UDP/TCP protocols defined by the respective digital radio standards. The app contains no advertising libraries, analytics SDKs, or third-party tracking code.

---

### 9 · Changes to This Policy

We may update this Privacy Policy from time to time. The revised policy will be posted at the same URL with an updated "Last Updated" date. Continued use of the application after changes constitutes acceptance of the new policy.

---

### 10 · Contact

- **Developer:** ALG Soft  
- **Website:** [algsoft.net.tr](https://algsoft.net.tr)  
- **E-mail:** [fatih@radio.org.tr](mailto:fatih@radio.org.tr)  

---
---

## 🇹🇷 Türkçe

---

### 1 · Digi Voice Hiçbir Veri Toplamaz

> **Digi Voice'un hiçbir sunucusu, veritabanı veya arka uç hizmeti yoktur. Kişisel olarak tanımlanabilir hiçbir bilgiyi toplamamakta, depolamamakta, iletmemekte, satmamakta veya paylaşmamaktadır.**

Digi Voice kesinlikle:

- ✗ Verilerinizi geliştirici veya Digi Voice'a ait herhangi bir sunucuya göndermez  
- ✗ Analitik, kilitlenme bildirimi veya reklam SDK'sı kullanmaz  
- ✗ Davranışlarınızı, kullanım kalıplarınızı veya konum geçmişinizi takip etmez  
- ✗ Kullanıcı hesabı oluşturmaz veya yönetmez  
- ✗ Ödeme işlemi yapmaz veya depolamaz  
- ✗ Reklamcılarla veya veri komisyoncularıyla veri paylaşmaz  

---

### 2 · Uygulamanın Çalışma Şekli — Veri Akışları

Digi Voice, kamuya açık amatör telsiz ağlarına bağlanan bir PTT (bas-konuş) telsiz istemcisidir. Aşağıda açıklanan tüm veri akışları, doğrudan **cihazınız ile söz konusu üçüncü taraf telsiz altyapı sunucuları arasında** gerçekleşir — Digi Voice üzerinden veya Digi Voice'a değil.

#### 2.1 · Telsiz Ağı Bağlantıları (BrandMeister, TGIF vb.)

Bir telsiz ağına bağlanmayı tercih ettiğinizde uygulama, **çağrı işaretinizi**, **DMR ID'nizi** ve gerçek zamanlı **ses verisini** doğrudan seçtiğiniz sunucuya iletir. Bu, her amatör telsiz dijital ağ protokolünün (DMR, D-STAR, M17, YSF, P25, NXDN) temel mekanizmasıdır.

> Çağrı işaretiniz ve DMR ID'niz, amatör telsiz topluluğunda kamuya açık bilgilerdir ve **BrandMeister** ile **RadioID.net** gibi üçüncü taraf platformlara sizin tarafınızdan gönüllü olarak kaydettirilmiştir. Digi Voice bu kimlik bilgilerini kaydetmez, tutmaz veya yönetmez.

#### 2.2 · RadioID.net Veritabanı Sorguları

Digi Voice, görüntüleme amacıyla bir çağrı işaretini DMR ID ile eşleştirmek için [RadioID.net](https://radioid.net) genel API'sini sorgulayabilir. Bu sorgu yalnızca çağrı işareti veya DMR ID'yi içerir; bunların ikisi de küresel amatör telsiz sicilinde kamuya açık bilgilerdir. Başka hiçbir kişisel bilgi iletilmez. RadioID.net, kendi gizlilik politikasına sahip bağımsız bir hizmettir.

#### 2.3 · GPS / Konum

Konum erişimi **isteğe bağlıdır**. Konum iznini verirseniz uygulama, *Maidenhead QTH grid locator*'ı hesaplamak için GPS koordinatlarınızı kullanır. Grid locator, protokolün bir parçası olarak bağlı telsiz sunucusuna iletilebilir. Digi Voice'a, uzak bir veritabanına veya herhangi bir reklam hizmetine **gönderilmez**.

#### 2.4 · Mikrofon

Mikrofon yalnızca PTT iletimi sırasında sesinizi yakalamak için kullanılır. Ses, gerçek zamanlı olarak seçilen telsiz sunucusuna kodlanıp akıtılır. Digi Voice herhangi bir hizmete ses kaydetmez, depolamaz veya yüklemez.

#### 2.5 · Sunucu Listesi İndirmeleri

Digi Voice, sunucu seçim menüsünü doldurmak için kamuya açık sunucu listelerini (*pistar.uk*, *m17project.org* vb.) indirir. Bunlar amatör telsiz topluluğu tarafından yönetilen düz metin dosyalarıdır. Bu isteklere hiçbir kişisel veri dahil edilmez.

#### 2.6 · Günlük Dosyaları (Yalnızca Cihaz)

Uygulama, tanı günlüklerini **yalnızca cihazınızın yerel depolama alanına** yazar. Bu dosyalar hiçbir yere yüklenmez. Uygulama içindeki *Günlük* sekmesinden görüntüleyebilir ve silebilirsiniz.

#### 2.7 · Ayarları Dışa Aktar / İçe Aktar

Digi Voice, tüm uygulama ayarlarınızı `.config` dosyası olarak dışa aktarmanıza ve aynı formatı destekleyen farklı bir cihaz ya da platforma aktarmanıza olanak tanıyan isteğe bağlı bir özellik sunar. Bu özellik:

- Yalnızca **siz başlatırsanız** çalışır — hiçbir zaman otomatik çalışmaz.
- Android'in **Storage Access Framework** (sistem dosya seçici) altyapısını kullanır; ek depolama izni gerekmez.
- Dosyayı **yalnızca sizin seçtiğiniz konuma** kaydeder; uygulama cihazınızdaki başka hiçbir konuma erişemez.
- Dosyayı herhangi bir sunucuya veya bulut hizmetine **yüklemez**.

> **Önemli:** Dışa aktarılan `.config` dosyası çağrı işaretinizi, DMR ID'nizi, ağ şifrelerinizi (BrandMeister, TGIF, AllStar), konuşma grubu tercihlerinizi ve diğer tüm uygulama ayarlarınızı düz JSON formatında içerir. Bu dosyayı **güvenli bir yerde saklayınız** ve güvenmediğiniz kişilerle paylaşmayınız.

---

### 3 · Android İzinleri

| İzin | Gerekçe |
|---|---|
| `RECORD_AUDIO` | PTT telsiz iletimi için sesinizi yakalar. |
| `INTERNET` | Telsiz sunucularına bağlanır ve sunucu listelerini indirir. |
| `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION` | İsteğe bağlı. Maidenhead QTH grid karesini hesaplar. |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MICROPHONE`, `FOREGROUND_SERVICE_PHONE_CALL` | Uygulama arka plandayken telsiz bağlantısını etkin tutar. |
| `POST_NOTIFICATIONS` | Ön plan hizmet bildirimini gösterir (Android 13+ zorunlu). |
| `WAKE_LOCK` | Aktif bağlantı sırasında cihazın uyku moduna geçmesini engeller. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | İsteğe bağlı Doze Modu muafiyeti. |
| `ACCESS_NETWORK_STATE` | Bağlantıdan önce ağ kullanılabilirliğini kontrol eder. |
| `MEDIA_CONTENT_CONTROL` | Donanım PTT düğmelerini yönetir. |
| `WRITE_EXTERNAL_STORAGE` | Android 9 ve altında tanı günlüğü yazar. |

> **Ayar dışa/içe aktarma** özelliği Android'in Storage Access Framework (SAF) altyapısını kullanır ve **ek izin gerektirmez**. Depolama erişimi, sistem dosya seçicisi aracılığıyla kullanıcı adına yönetilir.

---

### 4 · Üçüncü Taraf Hizmetler

| Hizmet | Amaç | Gönderilen Veri |
|---|---|---|
| **BrandMeister** (`brandmeister.network`) | DMR telsiz ağı | Çağrı işareti, DMR ID, ses verisi, isteğe bağlı GPS grid |
| **RadioID.net** (`radioid.net`) | Kamuya açık çağrı işareti/DMR ID sicil sorgusu | Çağrı işareti veya DMR ID (kamuya açık bilgi) |
| **Diğer Yansıtıcılar** (TGIF, M17, D-STAR, YSF, P25, NXDN, FCS) | Telsiz ağı bağlantıları | Çağrı işareti, telsiz ID, ses verisi, isteğe bağlı GPS grid |
| **Sunucu Listeleri** (pistar.uk, m17project.org vb.) | Yansıtıcı listelerini indirir | Hiçbiri — yalnızca anonim istekler |

---

### 5 · Üçüncü Taraf Platformlardaki Verilerinizi Yönetme

> **Önemli:** Çağrı işaretiniz, DMR ID'niz, adınız ve amatör telsiz kaydıyla ilişkili diğer kişisel bilgiler, yalnızca **BrandMeister**, **RadioID.net** ve diğer telsiz ağı operatörleri tarafından tutulmaktadır — *Digi Voice tarafından değil*.

Kişisel verilerinizi görüntülemek, düzenlemek veya silmek istiyorsanız:

- **BrandMeister:** [brandmeister.network](https://brandmeister.network) adresinden giriş yapın ve profilinizi yönetin ya da destek ekibiyle iletişime geçin.  
- **RadioID.net:** [radioid.net](https://radioid.net) adresinden giriş yapın ve hesap yönetim araçlarını kullanın.  

Digi Voice kişisel bilgilerinizin hiçbir kopyasını tutmadığından, **Digi Voice'tan veri silme talebinde bulunamazsınız** — bu tür talepler, verilerinizin bulunduğu ilgili platforma yönlendirilmelidir.

---

### 6 · Cihazınızda Depolanan Veriler

Digi Voice, aşağıdakileri **yalnızca cihazınızda** (Android şifreli DataStore) saklar:

- Çağrı işaretiniz ve telsiz ID'niz (yalnızca telsiz sunucularına bağlanmak için)  
- Seçili sunucu ve talk-group tercihleri  
- Uygulama ayarları (ses seviyeleri, PTT tuşu, mod, favori konuşma grupları vb.)  
- Tanı günlük dosyaları (uygulama içinden görüntülenebilir ve silinebilir)  

Bu verilerin hiçbiri geliştiricinin sunucularına yedeklenmez. Uygulamayı kaldırmak, yerel olarak depolanan tüm verileri siler.

Tüm ayarları isteğe bağlı olarak seçtiğiniz bir konumdaki `.config` dosyasına dışa aktarabilirsiniz. Dışa aktarılan dosya tamamen sizin kontrolünüzdedir; Digi Voice dışa aktarma sonrasında bu dosyayı saklamamakta ve erişememektedir.

---

### 7 · Çocuk Gizliliği

Digi Voice, lisanslı amatör telsiz operatörleri için tasarlanmıştır. 13 yaş altındaki çocuklara yönelik değildir ve bu kişilerden bilerek kişisel bilgi toplamamaktadır.

---

### 8 · Güvenlik

RadioID.net ile tüm iletişim HTTPS üzerinden gerçekleşir. Telsiz sunucu bağlantıları, ilgili dijital telsiz standartlarının belirlediği UDP/TCP protokollerini kullanır. Uygulama herhangi bir reklam kütüphanesi, analitik SDK veya üçüncü taraf izleme kodu içermemektedir.

---

### 9 · Politika Değişiklikleri

Bu Gizlilik Politikası'nı zaman zaman güncelleyebiliriz. Revize edilmiş politika, güncellenmiş bir "Son Güncelleme" tarihiyle aynı URL'de yayınlanacaktır. Değişikliklerin ardından uygulamayı kullanmaya devam etmeniz yeni politikayı kabul ettiğiniz anlamına gelir.

---

### 10 · İletişim

- **Geliştirici:** ALG Soft  
- **Web sitesi:** [algsoft.net.tr](https://algsoft.net.tr)  
- **E-posta:** [fatih@radio.org.tr](mailto:fatih@radio.org.tr)  

---

*© 2026 ALG Soft · Digi Voice · com.alg.dmrvoice*
