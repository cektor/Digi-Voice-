# Privacy Policy — Digi Voice

**Last Updated:** August 18, 2026  
**Application:** Digi Voice (`com.alg.dmrvoice`)  
**Platforms:** Android phone & tablet · Android Auto · Android TV  
**Developer:** ALG Soft — [algsoft.net.tr](https://algsoft.net.tr)  
**Contact:** [fatih@radio.org.tr](mailto:fatih@radio.org.tr)

---

## 🇬🇧 English

---

### 1 · Data Digi Voice Does NOT Collect

> **Other than the basic usage statistics described in Section 9, Digi Voice does not operate any other servers, databases, or backend services of its own, and does not otherwise collect, store, transmit, sell, or share any personally identifiable information with its developer.**

Beyond the usage statistics described in Section 9, Digi Voice **never**:

- ✗ Sends your other data to the developer or any Digi Voice-owned server  
- ✗ Uses third-party analytics, crash-reporting, or advertising SDKs  
- ✗ Tracks your behaviour, usage patterns, or location history  
- ✗ Creates or manages user accounts  
- ✗ Processes or stores payments  
- ✗ Shares data with advertisers or data brokers  

---

### 2 · How the App Works — Data Flows

Digi Voice is a Push-to-Talk (PTT) radio client that connects to publicly-operated amateur radio networks. All data flows described below are **directly between your device and those third-party radio infrastructure servers** — not through or to Digi Voice.

#### 2.1 · Radio Network Connections (BrandMeister, TGIF, etc.)

When you connect to a radio network, the app sends your **callsign**, **DMR ID**, and real-time **voice audio** directly to the server you selected. This is the fundamental mechanism of every amateur radio digital network protocol (DMR, M17, YSF, P25, NXDN).

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

### 3 · Android Auto

Digi Voice supports **Android Auto** so a licensed operator can listen and use Push-to-Talk without handling the phone while driving.

- Android Auto is **not a separate app**. It is a projected interface of the phone app; the connection, settings and audio all keep running on your phone. It therefore introduces **no new data collection** and sends no statistics of its own.
- The car interface is **template-based** (Google's Car App Library). Digi Voice only supplies text and list content to templates that Android Auto itself renders. The app receives no camera feed, no contacts, no messages and no vehicle telemetry.
- The app is declared under the **IOT** category, not the CALLING category. It is not registered with Android's telephony/Telecom framework and does not access call logs, phone numbers, or contacts.
- The **microphone** is used only while you press PTT, exactly as on the phone; audio is streamed to your selected radio server and never recorded.
- Talk-group and server names shown on the car screen come from your own device settings and the public reflector lists.

---

### 4 · Android TV

Digi Voice for Android TV is a separate, TV-optimised (leanback) build of the same application. It stores its configuration **only on the television or TV box** and communicates with radio networks exactly as described in Section 2.

#### 4.1 · Microphone is optional — receive-only devices are supported

Many televisions and TV boxes have no microphone. The app therefore declares the microphone as **not required**: on a device without a microphone Digi Voice works fully in **receive (RX)** mode and only transmission (TX) is disabled. The app explains this on screen.

#### 4.2 · Transferring settings from your phone (local network, encrypted)

Typing a callsign, DMR ID and network passwords with a TV remote is impractical, so the TV app can import these settings from the Digi Voice app on your phone. This transfer:

- Is **strictly local** — your phone finds the TV on the same Wi-Fi using Android **NSD/mDNS** (service type `_digivoicesync._tcp`) and sends the data directly over TCP. It **never** passes through the internet or any server of ours.
- Is **end-to-end encrypted with AES-GCM**, using a key derived through **HKDF-SHA256** from a **6-digit code** displayed on your TV and typed on your phone. Another device on the same network cannot decrypt the packet without that code.
- Carries the same `.config` payload as the Export/Import feature — **including your network passwords**. Treat the 6-digit code as a one-time secret and use it only with a device you own.

Because a 6-digit code is short, the protection comes from the channel rather than the key length. The receiver on the TV therefore listens **only while the pairing screen is open**, **shuts down after the first successful transfer**, and **regenerates the code after 5 incorrect attempts**.

The wire format is identical to the Apple version, so transferring from an iPhone to an Android TV (and vice versa) also works. In every case the data travels only between your own two devices.

#### 4.3 · No additional permissions

The TV build uses the same permissions as the phone build (see Section 5); local discovery works with `INTERNET` and `ACCESS_NETWORK_STATE` and needs no extra permission.

---

### 5 · Android Permissions

| Permission | Why it is needed |
|---|---|
| `RECORD_AUDIO` | Capture your voice for PTT radio transmission. On Android TV this is optional — without a microphone the app runs receive-only. |
| `INTERNET` | Connect to radio servers, download server host lists, send the Section 9 statistics, and perform the local phone-to-TV settings transfer. |
| `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION` | Optional. Calculate your Maidenhead QTH grid square. |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MICROPHONE`, `FOREGROUND_SERVICE_PHONE_CALL` | Keep the radio connection active in the background with a visible notification. |
| `POST_NOTIFICATIONS` | Show the foreground-service notification (required on Android 13+). |
| `WAKE_LOCK` | Prevent the device from sleeping during an active connection. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Optionally exempt the app from Doze Mode for stable radio links. |
| `ACCESS_NETWORK_STATE` | Detect network availability, and discover your TV for the local settings transfer. |
| `MEDIA_CONTENT_CONTROL` | Handle hardware PTT buttons (volume keys, headset buttons). |
| `BLUETOOTH_CONNECT` | Use Bluetooth headsets / PTT accessories for audio. |
| `MODIFY_AUDIO_SETTINGS`, `VIBRATE` | Audio routing for PTT and haptic feedback. |
| `WRITE_EXTERNAL_STORAGE` | Write diagnostic log files on Android 9 and below. |

> **Settings export/import** uses Android's Storage Access Framework (SAF) and requires **no additional permissions**. The system file picker handles all storage access on behalf of the user.

---

### 6 · Third-Party Services

| Service | Purpose | Data Sent |
|---|---|---|
| **BrandMeister** (`brandmeister.network`) | DMR radio network | Callsign, DMR ID, voice audio, optional GPS grid |
| **RadioID.net** (`radioid.net`) | Public callsign/DMR ID registry lookup | Callsign or DMR ID (public data) |
| **Other Reflectors** (TGIF, M17, YSF, P25, NXDN, FCS) | Radio network connections | Callsign, radio ID, voice audio, optional GPS grid |
| **Server Host Lists** (pistar.uk, m17project.org, etc.) | Download lists of available reflectors | None — anonymous requests only |

---

### 7 · Managing Your Data on Third-Party Platforms

> **Important:** Your callsign, DMR ID, name, and other personal information associated with amateur radio registration are held exclusively by **BrandMeister**, **RadioID.net**, and other radio network operators — *not by Digi Voice*.

If you wish to view, edit, or delete your personal data:

- **BrandMeister:** Log in at [brandmeister.network](https://brandmeister.network) and manage your profile or contact their support team.  
- **RadioID.net:** Log in at [radioid.net](https://radioid.net) and use their account management tools.

Because Digi Voice holds **no copy** of your personal information, you **cannot request data deletion from Digi Voice** — all such requests must be directed to the respective platform where your data resides.

---

### 8 · Data Stored on Your Device

Digi Voice stores the following **only on your device** (Android's encrypted DataStore) — on phones, tablets and Android TV alike:

- Your callsign and radio ID (used only to connect to radio servers)  
- Selected server and talk-group preferences  
- Application settings (audio levels, PTT key, mode, favourite talk groups, etc.)  
- Diagnostic log files (viewable and deletable from within the app)  

None of this data is backed up to the developer's servers. Uninstalling the app removes all locally stored data.

You may optionally export all settings to a `.config` file stored in a location of your choosing. The exported file remains entirely under your control — Digi Voice does not retain a copy and cannot access it after export.

---

### 9 · Usage Statistics We Send

Digi Voice collects basic usage statistics so we can see how many people use the app and on which platforms. On launch (and whenever you change your callsign), the following is sent to our servers:

- Device model and operating system version
- App version and device language
- Your configured callsign (from Settings)
- An approximate country and city, resolved at that moment from the IP address the request came from

This check-in is sent by the phone/tablet app **and by the Android TV app**. Android Auto runs on your phone, so it is covered by the phone app's check-in — the car interface sends nothing of its own.

Your raw IP address is never logged or stored — it is used only momentarily to look up the country/city and is discarded immediately afterward. This data is not shared with or sold to third parties; it is used only to view aggregate usage statistics (how many users, on which platform, in which country). No third-party analytics or crash-reporting SDK is used (e.g. Firebase, Crashlytics) — this data goes directly to Digi Voice's own server. If you'd like this data deleted, contact us at [fatih@radio.org.tr](mailto:fatih@radio.org.tr).

---

### 10 · Children's Privacy

Digi Voice is intended for licensed amateur radio operators. It is not directed at children under 13 years of age and does not knowingly collect personal information from children.

---

### 11 · Security

All communication with RadioID.net and with our statistics endpoint uses HTTPS. The phone-to-TV settings transfer described in Section 4 is encrypted with AES-GCM under a key derived from your 6-digit pairing code. Radio server connections use the UDP/TCP protocols defined by the respective digital radio standards. The app contains no advertising libraries, third-party analytics SDKs, or third-party tracking code.

---

### 12 · Changes to This Policy

We may update this Privacy Policy from time to time. The revised policy will be posted at the same URL with an updated "Last Updated" date. Continued use of the application after changes constitutes acceptance of the new policy.

---

### 13 · Contact

- **Developer:** ALG Soft  
- **Website:** [algsoft.net.tr](https://algsoft.net.tr)  
- **E-mail:** [fatih@radio.org.tr](mailto:fatih@radio.org.tr)  

---
---

## 🇹🇷 Türkçe

---

### 1 · Digi Voice'un Toplamadığı Veriler

> **Bölüm 9'da açıklanan temel kullanım istatistikleri dışında, Digi Voice'un başka bir sunucusu, veritabanı veya arka uç hizmeti yoktur ve kişisel olarak tanımlanabilir başka hiçbir bilgiyi toplamamakta, depolamamakta, iletmemekte, satmamakta veya paylaşmamaktadır.**

Bölüm 9'da açıklanan kullanım istatistikleri dışında, Digi Voice kesinlikle:

- ✗ Diğer verilerinizi geliştirici veya Digi Voice'a ait herhangi bir sunucuya göndermez  
- ✗ Üçüncü taraf analitik, kilitlenme bildirimi veya reklam SDK'sı kullanmaz  
- ✗ Davranışlarınızı, kullanım kalıplarınızı veya konum geçmişinizi takip etmez  
- ✗ Kullanıcı hesabı oluşturmaz veya yönetmez  
- ✗ Ödeme işlemi yapmaz veya depolamaz  
- ✗ Reklamcılarla veya veri komisyoncularıyla veri paylaşmaz  

---

### 2 · Uygulamanın Çalışma Şekli — Veri Akışları

Digi Voice, kamuya açık amatör telsiz ağlarına bağlanan bir PTT (bas-konuş) telsiz istemcisidir. Aşağıda açıklanan tüm veri akışları, doğrudan **cihazınız ile söz konusu üçüncü taraf telsiz altyapı sunucuları arasında** gerçekleşir — Digi Voice üzerinden veya Digi Voice'a değil.

#### 2.1 · Telsiz Ağı Bağlantıları (BrandMeister, TGIF vb.)

Bir telsiz ağına bağlanmayı tercih ettiğinizde uygulama, **çağrı işaretinizi**, **DMR ID'nizi** ve gerçek zamanlı **ses verisini** doğrudan seçtiğiniz sunucuya iletir. Bu, her amatör telsiz dijital ağ protokolünün (DMR, M17, YSF, P25, NXDN) temel mekanizmasıdır.

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

### 3 · Android Auto

Digi Voice, lisanslı operatörün araç kullanırken telefona dokunmadan dinleyip bas-konuş yapabilmesi için **Android Auto** desteği sunar.

- Android Auto **ayrı bir uygulama değildir**. Telefon uygulamasının araca yansıtılan arayüzüdür; bağlantı, ayarlar ve ses telefonda çalışmaya devam eder. Bu nedenle **yeni bir veri toplama** doğurmaz ve kendi başına istatistik göndermez.
- Araç arayüzü **şablon tabanlıdır** (Google Car App Library). Digi Voice yalnızca metin ve liste içeriği sağlar; şablonları Android Auto'nun kendisi çizer. Uygulama kamera görüntüsü, rehber, mesaj veya araç telemetrisi almaz.
- Uygulama **IOT** kategorisinde beyan edilmiştir, CALLING kategorisinde değil. Android'in telefon/Telecom çerçevesine kaydolmaz; arama kayıtlarına, telefon numaralarına veya rehbere erişmez.
- **Mikrofon** yalnızca PTT'ye bastığınız sürece kullanılır; ses seçtiğiniz telsiz sunucusuna akıtılır, kaydedilmez.
- Araç ekranında görünen konuşma grubu ve sunucu adları kendi cihaz ayarlarınızdan ve kamuya açık yansıtıcı listelerinden gelir.

---

### 4 · Android TV

Android TV için Digi Voice, aynı uygulamanın televizyona uyarlanmış (leanback) ayrı bir sürümüdür. Yapılandırmasını **yalnızca televizyonda veya TV kutusunda** saklar ve telsiz ağlarıyla Bölüm 2'de anlatıldığı gibi iletişim kurar.

#### 4.1 · Mikrofon isteğe bağlıdır — yalnızca dinleyen cihazlar desteklenir

Pek çok televizyon ve TV kutusunda mikrofon yoktur. Bu nedenle uygulama mikrofonu **zorunlu olmayan** bir donanım olarak beyan eder: mikrofonsuz bir cihazda Digi Voice **alma (RX)** modunda tam olarak çalışır, yalnızca yayın (TX) devre dışı kalır. Uygulama bu durumu ekranda açıklar.

#### 4.2 · Telefondan ayar aktarımı (yerel ağ, şifreli)

Çağrı işareti, DMR ID ve ağ şifrelerini TV kumandasıyla yazmak pratik olmadığından, TV uygulaması bu ayarları telefonunuzdaki Digi Voice uygulamasından içe aktarabilir. Bu aktarım:

- **Tamamen yereldir** — telefonunuz TV'yi aynı Wi-Fi ağında Android **NSD/mDNS** ile (`_digivoicesync._tcp` servis tipi) bulur ve veriyi doğrudan TCP ile gönderir. İnternetten veya bize ait herhangi bir sunucudan **geçmez**.
- **AES-GCM ile uçtan uca şifrelenir**; anahtar, TV ekranında gösterilip telefonunuza yazdığınız **6 haneli koddan** **HKDF-SHA256** ile türetilir. Aynı ağdaki başka bir cihaz paketi yakalasa bile kodu bilmeden açamaz.
- Dışa/İçe Aktarma ile aynı `.config` içeriğini taşır — **ağ şifreleriniz dahil**. 6 haneli kodu tek kullanımlık bir sır olarak görün ve yalnızca kendi cihazınızla kullanın.

6 haneli kod kısa olduğundan koruma, anahtar uzunluğundan değil kanalın kendisinden gelir. Bu yüzden TV'deki alıcı **yalnızca eşleme ekranı açıkken** dinler, **ilk başarılı aktarımdan sonra kapanır** ve **5 hatalı denemeden sonra kodu yeniler**.

Tel biçimi Apple sürümüyle birebir aynı olduğundan iPhone'dan Android TV'ye (ve tersine) aktarım da çalışır. Her durumda veri yalnızca sizin iki cihazınız arasında gider.

#### 4.3 · Ek izin yok

TV sürümü telefon sürümüyle aynı izinleri kullanır (bkz. Bölüm 5); yerel keşif `INTERNET` ve `ACCESS_NETWORK_STATE` ile çalışır, ek izin gerektirmez.

---

### 5 · Android İzinleri

| İzin | Gerekçe |
|---|---|
| `RECORD_AUDIO` | PTT telsiz iletimi için sesinizi yakalar. Android TV'de isteğe bağlıdır; mikrofon yoksa uygulama yalnızca dinleme modunda çalışır. |
| `INTERNET` | Telsiz sunucularına bağlanır, sunucu listelerini indirir, Bölüm 9 istatistiklerini gönderir ve telefondan TV'ye yerel ayar aktarımını yapar. |
| `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION` | İsteğe bağlı. Maidenhead QTH grid karesini hesaplar. |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MICROPHONE`, `FOREGROUND_SERVICE_PHONE_CALL` | Uygulama arka plandayken telsiz bağlantısını etkin tutar. |
| `POST_NOTIFICATIONS` | Ön plan hizmet bildirimini gösterir (Android 13+ zorunlu). |
| `WAKE_LOCK` | Aktif bağlantı sırasında cihazın uyku moduna geçmesini engeller. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | İsteğe bağlı Doze Modu muafiyeti. |
| `ACCESS_NETWORK_STATE` | Ağ durumunu denetler ve yerel ayar aktarımı için TV'yi bulur. |
| `MEDIA_CONTENT_CONTROL` | Donanım PTT düğmelerini yönetir. |
| `BLUETOOTH_CONNECT` | Bluetooth kulaklık / PTT aksesuarlarını kullanır. |
| `MODIFY_AUDIO_SETTINGS`, `VIBRATE` | PTT ses yönlendirmesi ve dokunsal geri bildirim. |
| `WRITE_EXTERNAL_STORAGE` | Android 9 ve altında tanı günlüğü yazar. |

> **Ayar dışa/içe aktarma** özelliği Android'in Storage Access Framework (SAF) altyapısını kullanır ve **ek izin gerektirmez**. Depolama erişimi, sistem dosya seçicisi aracılığıyla kullanıcı adına yönetilir.

---

### 6 · Üçüncü Taraf Hizmetler

| Hizmet | Amaç | Gönderilen Veri |
|---|---|---|
| **BrandMeister** (`brandmeister.network`) | DMR telsiz ağı | Çağrı işareti, DMR ID, ses verisi, isteğe bağlı GPS grid |
| **RadioID.net** (`radioid.net`) | Kamuya açık çağrı işareti/DMR ID sicil sorgusu | Çağrı işareti veya DMR ID (kamuya açık bilgi) |
| **Diğer Yansıtıcılar** (TGIF, M17, YSF, P25, NXDN, FCS) | Telsiz ağı bağlantıları | Çağrı işareti, telsiz ID, ses verisi, isteğe bağlı GPS grid |
| **Sunucu Listeleri** (pistar.uk, m17project.org vb.) | Yansıtıcı listelerini indirir | Hiçbiri — yalnızca anonim istekler |

---

### 7 · Üçüncü Taraf Platformlardaki Verilerinizi Yönetme

> **Önemli:** Çağrı işaretiniz, DMR ID'niz, adınız ve amatör telsiz kaydıyla ilişkili diğer kişisel bilgiler, yalnızca **BrandMeister**, **RadioID.net** ve diğer telsiz ağı operatörleri tarafından tutulmaktadır — *Digi Voice tarafından değil*.

Kişisel verilerinizi görüntülemek, düzenlemek veya silmek istiyorsanız:

- **BrandMeister:** [brandmeister.network](https://brandmeister.network) adresinden giriş yapın ve profilinizi yönetin ya da destek ekibiyle iletişime geçin.  
- **RadioID.net:** [radioid.net](https://radioid.net) adresinden giriş yapın ve hesap yönetim araçlarını kullanın.  

Digi Voice kişisel bilgilerinizin hiçbir kopyasını tutmadığından, **Digi Voice'tan veri silme talebinde bulunamazsınız** — bu tür talepler, verilerinizin bulunduğu ilgili platforma yönlendirilmelidir.

---

### 8 · Cihazınızda Depolanan Veriler

Digi Voice, aşağıdakileri **yalnızca cihazınızda** (Android şifreli DataStore) saklar — telefon, tablet ve Android TV için aynı şekilde:

- Çağrı işaretiniz ve telsiz ID'niz (yalnızca telsiz sunucularına bağlanmak için)  
- Seçili sunucu ve talk-group tercihleri  
- Uygulama ayarları (ses seviyeleri, PTT tuşu, mod, favori konuşma grupları vb.)  
- Tanı günlük dosyaları (uygulama içinden görüntülenebilir ve silinebilir)  

Bu verilerin hiçbiri geliştiricinin sunucularına yedeklenmez. Uygulamayı kaldırmak, yerel olarak depolanan tüm verileri siler.

Tüm ayarları isteğe bağlı olarak seçtiğiniz bir konumdaki `.config` dosyasına dışa aktarabilirsiniz. Dışa aktarılan dosya tamamen sizin kontrolünüzdedir; Digi Voice dışa aktarma sonrasında bu dosyayı saklamamakta ve erişememektedir.

---

### 9 · Gönderdiğimiz Kullanım İstatistikleri

Digi Voice, kaç kişinin uygulamayı hangi platformda kullandığını görebilmek için basit kullanım istatistikleri toplar. Uygulama açılışında (ve çağrı işaretinizi değiştirdiğinizde), aşağıdaki bilgiler sunucularımıza gönderilir:

- Cihaz modeli ve işletim sistemi sürümü
- Uygulama sürümü ve cihaz dili
- Çağrı işaretiniz (Ayarlar'da girdiğiniz)
- İsteğin geldiği IP adresinden o an çözümlenen yaklaşık ülke ve şehir bilgisi

Bu bildirim telefon/tablet uygulaması **ve Android TV uygulaması** tarafından gönderilir. Android Auto telefonunuzda çalıştığından telefon uygulamasının bildirimi kapsamındadır — araç arayüzü kendi başına hiçbir şey göndermez.

Ham IP adresiniz hiçbir zaman kaydedilmez veya saklanmaz — yalnızca ülke/şehir bilgisini bulmak için anlık olarak kullanılır ve hemen atılır. Bu veriler üçüncü taraflarla paylaşılmaz veya satılmaz; yalnızca toplu kullanım istatistiklerini (kaç kullanıcı, hangi platformda, hangi ülkede) görmek için kullanılır. Üçüncü taraf analitik veya çökme raporlama SDK'sı (ör. Firebase, Crashlytics) kullanılmaz — bu veriler doğrudan Digi Voice'un kendi sunucusuna gider. Bu veriyi silmemizi istiyorsanız [fatih@radio.org.tr](mailto:fatih@radio.org.tr) adresinden bize ulaşabilirsiniz.

---

### 10 · Çocuk Gizliliği

Digi Voice, lisanslı amatör telsiz operatörleri için tasarlanmıştır. 13 yaş altındaki çocuklara yönelik değildir ve bu kişilerden bilerek kişisel bilgi toplamamaktadır.

---

### 11 · Güvenlik

RadioID.net ile ve istatistik adresimizle tüm iletişim HTTPS üzerinden gerçekleşir. Bölüm 4'te anlatılan telefondan TV'ye ayar aktarımı, 6 haneli eşleme kodunuzdan türetilen anahtarla AES-GCM ile şifrelenir. Telsiz sunucu bağlantıları, ilgili dijital telsiz standartlarının belirlediği UDP/TCP protokollerini kullanır. Uygulama herhangi bir reklam kütüphanesi, üçüncü taraf analitik SDK'sı veya üçüncü taraf izleme kodu içermemektedir.

---

### 12 · Politika Değişiklikleri

Bu Gizlilik Politikası'nı zaman zaman güncelleyebiliriz. Revize edilmiş politika, güncellenmiş bir "Son Güncelleme" tarihiyle aynı URL'de yayınlanacaktır. Değişikliklerin ardından uygulamayı kullanmaya devam etmeniz yeni politikayı kabul ettiğiniz anlamına gelir.

---

### 13 · İletişim

- **Geliştirici:** ALG Soft  
- **Web sitesi:** [algsoft.net.tr](https://algsoft.net.tr)  
- **E-posta:** [fatih@radio.org.tr](mailto:fatih@radio.org.tr)  

---

*© 2026 ALG Soft · Digi Voice · com.alg.dmrvoice*
