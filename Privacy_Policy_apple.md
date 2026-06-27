# Privacy Policy — Digi Voice

**App Name:** Digi Voice  
**Bundle ID:** com.alg.dmrvoice  
**Developer:** ALGSoft Inc. / Fatih ÖNDER (TB1TFO)  
**Platforms:** iOS · macOS · watchOS  
**Last Updated:** June 28, 2026  
**Effective Date:** June 26, 2026

---

> This document is written in both **English** (Section 1–12) and **Turkish** (Bölüm 1–12).  
> Her iki dil de hukuki açıdan geçerlidir / Both language versions are legally valid.

---

## ENGLISH VERSION

---

### 1. Introduction

ALGSoft Inc. ("we," "our," or "us") built **Digi Voice** as a commercial amateur radio digital voice communication application. This Privacy Policy explains how we handle information in connection with your use of the Digi Voice app on iOS, macOS, and watchOS devices.

Digi Voice is designed for **licensed amateur radio operators**. Use of this application requires a valid amateur radio license issued by your country's telecommunications authority.

By using Digi Voice, you agree to the terms of this Privacy Policy. If you do not agree, please discontinue use of the application.

---

### 2. Digi Voice Does Not Collect Your Data

> **Plain-language summary:** Digi Voice collects **nothing**. It has no backend, no database, no analytics, and no crash reporting. It is a radio protocol client — a pipe between your device and the radio network server you choose to connect to. No data ever reaches ALGSoft Inc. or any server we operate.

#### 2.1 Your Callsign, DMR ID, and Passwords Belong to Third-Party Platforms

Your amateur radio callsign and DMR/NXDN ID are credentials that you registered directly with **RadioID.net**, **BrandMeister**, **TGIF**, or another radio network — independently of Digi Voice. Digi Voice does not issue, register, store, or manage these credentials on its own servers.

When you enter your callsign and password in the Digi Voice Settings screen, that information is:

- Saved **only on your local device** (iOS/macOS `UserDefaults`, protected by device encryption and your passcode/biometrics).
- **Never transmitted to ALGSoft Inc. or any server we control.**
- Sent directly from your device to the **third-party radio network server you select**, using the protocol that server requires.

Digi Voice is the messenger. The accounts, the credentials, and the user data all belong to those third-party platforms — not to us.

#### 2.2 Configuration Stored Locally on Your Device

The following fields are stored only on your device. They are not "collected" by us — we never receive them:

| Field | Purpose | Where It Goes |
|---|---|---|
| Amateur Radio Callsign | Protocol identification | Your device → radio server you connect to |
| Digital Radio ID (DMR / NXDN) | Protocol-level identification | Your device → radio server you connect to |
| ESSID | Hotspot subscriber ID suffix | Your device → radio server you connect to |
| Network Passwords (BrandMeister, TGIF, AllStar…) | Authentication on third-party networks | Your device → that network's server |
| GPS Coordinates | Position reporting in protocol packets | Your device → radio server (if location reporting enabled) |
| QTH Grid Locator | Amateur radio grid reference | Your device → radio server (if configured) |
| Location Name & Description | Optional protocol metadata | Your device → radio server (if configured) |
| Personal URL | Optional protocol packet field | Your device → radio server (if configured) |
| Protocol & Server Preferences | Session settings | Stays on your device |
| Audio Settings (mic level, AGC, VOX, RX Volume) | Audio configuration | Stays on your device |
| Favorite Talk Groups | Quick-access talk group list | Stays on your device; synced to paired Apple Watch locally |

#### 2.3 Diagnostic Log Files

The app writes session logs to the device's **Caches directory** (not iCloud-synced). Log files contain connection events, protocol handshake results, audio engine status, GPS acquisition status, and error messages. Logs are stored locally and are **never transmitted to us or any third party automatically**. You may share log content manually from the Logs tab for self-diagnosis or community support.

#### 2.4 No Analytics, No Crash SDK, No Telemetry

Digi Voice does **not** integrate Firebase, Mixpanel, Amplitude, Sentry, Crashlytics, or any equivalent SDK. ALGSoft Inc. receives zero telemetry from your device.

#### 2.5 Apple Watch — Local Data Synchronization

When you use Digi Voice with a paired Apple Watch, the app uses Apple's **WatchConnectivity** framework to synchronize configuration between your iPhone and your Watch. This synchronization is:

- **Local only** — data travels over Bluetooth or local Wi-Fi directly between your iPhone and your Apple Watch. It is not routed through Apple's servers or any server operated by ALGSoft Inc.
- **One-way from iPhone to Watch** for configuration: callsign, Digital ID, selected server, selected talk group, favorite talk groups list, and connection status.
- **One-way from Watch to iPhone** for settings changes: talk group selection, callsign, ESSID, Digital ID, Hotspot Security password, server selection, and private call mode. These values are received by the iPhone app and stored in local `UserDefaults` — they are never forwarded to a third party except as part of the radio protocol connection described in Sections 3 and 4.

No WatchConnectivity data is transmitted to ALGSoft Inc. or any external server by the Watch layer itself.

---

### 3. How We Use Your Information

Your information is used exclusively to operate the application's core radio communication features:

1. **Protocol Authentication** — Your callsign, digital ID, ESSID, and password are included in protocol handshake packets sent to the radio network server you select.
2. **Position Reporting** — When you tap "Get GPS Location" or enter coordinates manually, those coordinates are included in the protocol configuration packet sent to the network server. This is a standard feature of amateur radio digital protocols (BrandMeister, TGIF, HBLink, etc.).
3. **Callsign / ID Lookup** — When you tap the Digital ID lookup button, your callsign is sent to **radioid.net** to retrieve your registered DMR or NXDN ID. This request is initiated solely by you.
4. **Voice Transmission** — Your microphone audio is encoded and transmitted in real time to the radio network server for the duration of PTT (Push-To-Talk) activation.
5. **Local Persistence** — Settings are persisted locally so your configuration survives app restarts.
6. **Apple Watch Synchronization** — Your configuration (callsign, talk group, favorites, server selection) is synchronized to your paired Apple Watch via WatchConnectivity for use in the Watch companion app. This transfer is purely local and device-to-device.

---

### 4. Information Shared with Third Parties

We do not sell, rent, or commercially share your personal information. The following limited sharing occurs as a direct result of the application's radio network functionality:

#### 4.1 Radio Network Servers

When you connect to a network server, the following data is transmitted directly **from your device to the server operator** you choose:

- Callsign, Digital ID, ESSID
- Password (for authenticated networks)
- GPS coordinates / location metadata (if configured)
- Encoded voice audio (during PTT)

Network servers operated by third parties include, but are not limited to:

| Network | Operator | Privacy Information |
|---|---|---|
| BrandMeister | BrandMeister Network | [brandmeister.network](https://brandmeister.network) |
| TGIF | TGIF Network | [tgif.network](https://tgif.network) |
| FreeDMR | FreeDMR Project | [freedmr.cymru](https://freedmr.cymru) |
| HBLink / US Digital | US Digital Network | [usdigitalnetwork.com](https://usdigitalnetwork.com) |
| D-STAR Reflectors | Various operators | Varies |
| YSF / FCS Reflectors | Various operators | Varies |
| AllStar / IAX2 | Various operators | Varies |

We have no control over and are not responsible for the data practices of these third-party network operators.

#### 4.2 RadioID.net

When you use the Digital ID lookup feature, your callsign is transmitted to `https://radioid.net` via HTTPS. RadioID.net is an independent amateur radio identification registry. Please refer to their privacy policy at [radioid.net](https://radioid.net) for details on how they handle lookup requests.

---

### 5. Device Permissions

The following device permissions are requested:

| Permission | Platform | When Requested | Purpose |
|---|---|---|---|
| **Microphone** | iOS / macOS / watchOS | First PTT attempt | Capture voice audio for transmission |
| **Location (When In Use)** | iOS / macOS | When "Get GPS Location" is tapped | Obtain GPS coordinates for position reporting |
| **Local Network** | iOS / macOS | On connection attempt to a local server | Connect to DMR hotspot servers on the local network |

#### Permission Details

**Microphone:**  
Audio is captured only while PTT is active. The app does not record audio to a file and does not transmit audio except to the radio network server you are connected to. Background audio capture uses `UIBackgroundModes: audio` to maintain an uninterrupted connection. On Apple Watch, microphone access is used when the Watch serves as the PTT input device; audio is relayed to the iPhone via WatchConnectivity for encoding and transmission.

**Location:**  
Location is accessed only when you explicitly tap "Get GPS Location." The app uses `requestWhenInUseAuthorization()`; background location access is never requested. Once coordinates are retrieved, the location service is stopped immediately. Coordinates are stored locally in your settings and included in protocol packets only if you have configured location reporting.

**Local Network:**  
Required to allow UDP connections to DMR hotspot devices operating on your local Wi-Fi network. This permission does not grant access to files or data on other devices.

**Apple Watch — No Additional Permissions:**  
The Digi Voice Watch companion app does not request any permissions beyond those already granted to the paired iPhone app. Microphone access on the Watch is governed by watchOS and granted automatically for paired apps that have microphone permission on iPhone.

---

### 6. App Store Privacy Nutrition Label

Digi Voice's App Store privacy disclosure declares **No Data Collected** from users by ALGSoft Inc. The following table reflects the App Privacy label accurately:

| Data Category | Collected by ALGSoft Inc. | Notes |
|---|---|---|
| Contact Info | No | Not collected |
| Health & Fitness | No | Not collected |
| Financial Info | No | Not collected |
| Location | No | Used only on-device; not sent to us |
| Sensitive Info | No | Not collected |
| Contacts | No | Not collected |
| User Content (Audio) | No | Transmitted to third-party radio servers only; not collected by us |
| Browsing History | No | Not collected |
| Search History | No | Not collected |
| Identifiers | No | Not collected |
| Usage Data | No | Not collected |
| Diagnostics | No | No crash SDKs; no telemetry |

Data transmitted to **third-party radio network servers** (callsign, voice audio) is governed by those networks' own privacy policies, not by ALGSoft Inc.

---

### 7. Data Security

All settings, including passwords, are stored using `UserDefaults` on your local device, protected by iOS/macOS Data Protection and your device's passcode / biometrics. We recommend using strong, unique passwords for each radio network.

Passwords are transmitted to network servers in the format required by the protocol (DMR uses a SHA-256 hash; other protocols may transmit in plaintext within the UDP payload). We recommend using network-specific hotspot security keys rather than primary account credentials.

When Hotspot Security passwords are entered via the Apple Watch Settings screen and relayed to the iPhone, the transfer occurs locally over WatchConnectivity (Bluetooth / local Wi-Fi). The password is stored in `UserDefaults` on the iPhone only and is not retained on the Watch.

---

### 8. Data Retention and Deletion

**Settings:** Stored indefinitely until you reset the app or delete it. To remove all settings, delete the Digi Voice app from your device.

**Log Files:** Stored in the device's Caches directory. The OS may delete cache files under storage pressure. You can clear logs manually from the Logs tab. Logs are removed when the app is deleted.

**Apple Watch Data:** Configuration synced to the Apple Watch via WatchConnectivity is stored only in the Watch companion app's local storage. Uninstalling the Watch app removes this data. No backup of Watch-side data is retained on iPhone.

We do not retain any data on our servers because we do not receive any data from your device in our infrastructure.

---

### 9. Children's Privacy

Digi Voice is intended for **licensed amateur radio operators** and is **not directed at persons under the age of 13** (or the applicable minimum age in your jurisdiction). We do not knowingly collect personal information from children. If you believe a child has used this application without appropriate supervision, please contact us and we will take appropriate steps.

---

### 10. International Users

Digi Voice is developed in Türkiye and the data you enter is stored locally on your device. If you connect to radio network servers, your data is transmitted to servers operated by third parties in various countries. By using network features, you consent to this cross-border transmission as part of the radio network operation.

---

### 11. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. When we do, we will update the "Last Updated" date at the top of this document and, where appropriate, provide notice within the application. Continued use of Digi Voice after the effective date of a revised policy constitutes your acceptance of the changes.

---

### 12. Your Rights and How to Exercise Them

Because Digi Voice holds no personal data on its own servers, the way you exercise data rights depends entirely on **where the data actually lives**.

#### 12.1 Data Inside the Digi Voice App (on your device)

All app settings — callsign, ID, passwords, coordinates, RX volume, favorite talk groups — are stored locally on your device and are fully under your control:

- **Access / Export:** Read settings directly in the Digi Voice Settings screen.
- **Rectify:** Edit any field in the Settings screen at any time.
- **Erase:** Delete the Digi Voice app from your device. All UserDefaults and cached log files are permanently removed. There is nothing to request from us — we hold no copy.

#### 12.2 Data on Third-Party Radio Network Platforms

Your callsign, DMR ID, account profile, and transmission history are held by the platforms you registered with. **Digi Voice has no access to this data and cannot modify or delete it on your behalf.**

To exercise data rights on those platforms, contact them directly:

| Platform | Data Rights Contact |
|---|---|
| **RadioID.net** | [radioid.net](https://radioid.net) — contact via the website |
| **BrandMeister** | [brandmeister.network](https://brandmeister.network) — contact your regional admin |
| **TGIF Network** | [tgif.network](https://tgif.network) |
| **FreeDMR** | [freedmr.cymru](https://freedmr.cymru) |
| **HBLink / US Digital** | [usdigitalnetwork.com](https://usdigitalnetwork.com) |
| D-STAR / YSF / AllStar reflectors | Contact the individual reflector operator |

ALGSoft Inc. cannot fulfill data access, correction, or deletion requests for data held by these platforms. Any such request directed to us will be forwarded to the relevant platform or returned to you with the appropriate contact information.

---

### 13. Contact Us

If you have questions, concerns, or requests regarding this Privacy Policy, please contact:

**ALGSoft Inc.**  
📧 info@algsoft.net.tr  
🌐 [https://algsoft.net.tr](https://algsoft.net.tr)

**Developer**  
Fatih ÖNDER (TB1TFO)  
📧 info@fatihonder.org.tr  
🌐 [https://fatihonder.org.tr](https://fatihonder.org.tr)

---
---

## TÜRKÇE VERSİYON

---

### 1. Giriş

ALGSoft Inc. ("biz", "bizim") tarafından **Digi Voice**, ticari bir amatör radyo dijital ses iletişim uygulaması olarak geliştirilmiştir. Bu Gizlilik Politikası, Digi Voice uygulamasını iOS, macOS ve watchOS cihazlarda kullanımınız kapsamında bilgilerin nasıl işlendiğini açıklamaktadır.

Digi Voice, **lisanslı amatör radyo operatörleri** için tasarlanmıştır. Bu uygulamanın kullanımı, ülkenizin telekomünikasyon otoritesi tarafından verilen geçerli bir amatör radyo lisansı gerektirmektedir.

Digi Voice'u kullanarak bu Gizlilik Politikası'nın koşullarını kabul etmiş olursunuz. Kabul etmiyorsanız lütfen uygulamayı kullanmayı bırakınız.

---

### 2. Digi Voice Verilerinizi Toplamaz

> **Özet:** Digi Voice **hiçbir şey toplamaz**. Arka ucu, veritabanı, analitiği ve kilitlenme raporu yoktur. Uygulama bir radyo protokol istemcisidir — cihazınız ile bağlanmayı seçtiğiniz radyo ağı sunucusu arasındaki bir köprüdür. ALGSoft Inc.'in işlettiği hiçbir sunucuya hiçbir veri ulaşmaz.

#### 2.1 Çağrı İşaretiniz, DMR ID'niz ve Şifreleriniz Üçüncü Taraf Platformlara Aittir

Amatör radyo çağrı işaretiniz ve DMR/NXDN ID'niz, Digi Voice'tan bağımsız olarak doğrudan **RadioID.net**, **BrandMeister**, **TGIF** veya başka bir radyo ağına kayıt yaptırdığınızda oluşturulan kimlik bilgileridir. Digi Voice bu kimlik bilgilerini kendi sunucularında oluşturmaz, kaydetmez, saklamaz veya yönetmez.

Digi Voice Ayarlar ekranına çağrı işaretinizi ve şifrenizi girdiğinizde bu bilgiler:

- Yalnızca **yerel cihazınızda** saklanır (iOS/macOS `UserDefaults`, cihaz şifrelemesi ve parolanız/biyometrinizle korunur).
- **ALGSoft Inc.'e veya bizim kontrolümüzdeki herhangi bir sunucuya iletilmez.**
- Cihazınızdan, protokolün gerektirdiği şekilde **seçtiğiniz üçüncü taraf radyo ağı sunucusuna** doğrudan gönderilir.

Digi Voice yalnızca bir aracıdır. Hesaplar, kimlik bilgileri ve kullanıcı verileri bu üçüncü taraf platformlara aittir — bize değil.

#### 2.2 Cihazınızda Yerel Olarak Saklanan Yapılandırma

Aşağıdaki alanlar yalnızca cihazınızda saklanır. Bunlar tarafımızca "toplanmaz" — biz hiçbir zaman almayız:

| Alan | Amaç | Nereye Gider |
|---|---|---|
| Amatör Radyo Çağrı İşareti | Protokol kimliği | Cihazınız → bağlandığınız radyo sunucusu |
| Dijital Radyo ID (DMR / NXDN) | Protokol düzeyinde kimlik | Cihazınız → bağlandığınız radyo sunucusu |
| ESSID | Hotspot abone ID son eki | Cihazınız → bağlandığınız radyo sunucusu |
| Ağ Şifreleri (BrandMeister, TGIF, AllStar…) | Üçüncü taraf ağlarda kimlik doğrulama | Cihazınız → ilgili ağın sunucusu |
| GPS Koordinatları | Protokol paketlerine konum bildirimi | Cihazınız → radyo sunucusu (etkinse) |
| QTH Kare Konumu | Amatör radyo ızgara referansı | Cihazınız → radyo sunucusu (yapılandırılmışsa) |
| Konum Adı & Açıklama | İsteğe bağlı protokol meta verisi | Cihazınız → radyo sunucusu (yapılandırılmışsa) |
| Kişisel URL | İsteğe bağlı protokol paketi alanı | Cihazınız → radyo sunucusu (yapılandırılmışsa) |
| Protokol & Sunucu Tercihleri | Oturum ayarları | Cihazınızda kalır |
| Ses Ayarları (mikrofon seviyesi, AGC, VOX, RX Ses Seviyesi) | Ses yapılandırması | Cihazınızda kalır |
| Favori Konuşma Grupları | Hızlı erişim konuşma grubu listesi | Cihazınızda kalır; eşleşik Apple Watch'a yerel olarak senkronize edilir |

#### 2.3 Tanı Log Dosyaları

Uygulama, oturum günlüklerini cihazın **Caches dizinine** yazar (iCloud ile senkronize edilmez). Log dosyaları bağlantı olayları, protokol el sıkışma sonuçları, ses motoru durumu, GPS alım durumu ve hata mesajlarını içerir. Günlükler yerel olarak saklanır ve **bize veya herhangi bir üçüncü tarafa otomatik olarak iletilmez**. Kayıtlar sekmesinden log içeriğini kendi teşhisiniz veya topluluk desteği için manuel olarak paylaşabilirsiniz.

#### 2.4 Analitik, Kilitlenme SDK'sı veya Telemetri Yok

Digi Voice Firebase, Mixpanel, Amplitude, Sentry, Crashlytics veya eşdeğer herhangi bir SDK entegre **etmemektedir**. ALGSoft Inc., cihazınızdan sıfır telemetri almaktadır.

#### 2.5 Apple Watch — Yerel Veri Senkronizasyonu

Digi Voice'u eşleşik bir Apple Watch ile kullandığınızda, uygulama iPhone ile Watch arasındaki yapılandırmayı senkronize etmek için Apple'ın **WatchConnectivity** çerçevesini kullanır. Bu senkronizasyon:

- **Yalnızca yereldir** — veriler, iPhone'unuz ile Apple Watch'unuz arasında doğrudan Bluetooth veya yerel Wi-Fi üzerinden aktarılır. Apple'ın sunucuları veya ALGSoft Inc. tarafından işletilen herhangi bir sunucu üzerinden yönlendirilmez.
- **iPhone'dan Watch'a tek yönlüdür** (yapılandırma için): çağrı işareti, Dijital ID, seçili sunucu, seçili konuşma grubu, favori konuşma grupları listesi ve bağlantı durumu.
- **Watch'tan iPhone'a tek yönlüdür** (ayar değişiklikleri için): konuşma grubu seçimi, çağrı işareti, ESSID, Dijital ID, Hotspot Security şifresi, sunucu seçimi ve özel çağrı modu. Bu değerler iPhone uygulaması tarafından alınır ve yerel `UserDefaults`'a kaydedilir; Bölüm 3 ve 4'te açıklanan radyo protokolü bağlantısının bir parçası dışında hiçbir üçüncü tarafa iletilmez.

WatchConnectivity verilerinin hiçbiri, Watch katmanı tarafından ALGSoft Inc.'e veya herhangi bir harici sunucuya iletilmez.

---

### 3. Bilgilerinizi Nasıl Kullanırız

Bilgileriniz yalnızca uygulamanın temel radyo iletişim özelliklerini işletmek amacıyla kullanılır:

1. **Protokol Kimlik Doğrulaması** — Çağrı işaretiniz, dijital ID'niz, ESSID'niz ve şifreniz, seçtiğiniz radyo ağ sunucusuna gönderilen protokol el sıkışma paketlerine dahil edilir.
2. **Konum Bildirimi** — "GPS Konumunu Al" düğmesine dokunduğunuzda veya koordinatları manuel girdiğinizde, bu koordinatlar ağ sunucusuna gönderilen protokol yapılandırma paketine eklenir. Bu, amatör radyo dijital protokollerinin (BrandMeister, TGIF, HBLink vb.) standart bir özelliğidir.
3. **Çağrı İşareti / ID Arama** — Dijital ID arama düğmesine dokunduğunuzda, kayıtlı DMR veya NXDN ID'nizi almak için çağrı işaretiniz HTTPS üzerinden **radioid.net**'e gönderilir. Bu istek yalnızca sizin tarafınızdan başlatılır.
4. **Ses İletimi** — PTT (Bastır-Konuş) aktif olduğu sürece mikrofon sesiniz gerçek zamanlı olarak kodlanır ve bağlı olduğunuz radyo ağı sunucusuna iletilir.
5. **Yerel Kalıcılık** — Ayarlar, yapılandırmanızın uygulama yeniden başlatmalarını atlatması için yerel olarak saklanır.
6. **Apple Watch Senkronizasyonu** — Yapılandırmanız (çağrı işareti, konuşma grubu, favoriler, sunucu seçimi) Watch yardımcı uygulamasında kullanılmak üzere WatchConnectivity aracılığıyla eşleşik Apple Watch'unuza senkronize edilir. Bu aktarım tamamen yereldir ve cihazdan cihazadır.

---

### 4. Üçüncü Taraflarla Paylaşılan Bilgiler

Kişisel bilgilerinizi satmıyor, kiralayıp paylaşmıyor veya ticari amaçla kullanmıyoruz. Aşağıdaki sınırlı paylaşım, uygulamanın radyo ağı işlevselliğinin doğrudan bir sonucu olarak gerçekleşmektedir:

#### 4.1 Radyo Ağı Sunucuları

Bir ağ sunucusuna bağlandığınızda, aşağıdaki veriler **cihazınızdan, seçtiğiniz sunucu operatörüne** doğrudan iletilir:

- Çağrı işareti, Dijital ID, ESSID
- Şifre (kimlik doğrulamalı ağlar için)
- GPS koordinatları / konum meta verisi (yapılandırılmışsa)
- Kodlanmış ses (PTT sırasında)

Üçüncü taraflarca işletilen ağ sunucuları şunları kapsar ancak bunlarla sınırlı değildir:

| Ağ | Operatör | Gizlilik Bilgisi |
|---|---|---|
| BrandMeister | BrandMeister Network | [brandmeister.network](https://brandmeister.network) |
| TGIF | TGIF Network | [tgif.network](https://tgif.network) |
| FreeDMR | FreeDMR Projesi | [freedmr.cymru](https://freedmr.cymru) |
| HBLink / US Digital | US Digital Network | [usdigitalnetwork.com](https://usdigitalnetwork.com) |
| D-STAR Reflektörler | Çeşitli operatörler | Değişken |
| YSF / FCS Reflektörler | Çeşitli operatörler | Değişken |
| AllStar / IAX2 | Çeşitli operatörler | Değişken |

Bu üçüncü taraf ağ operatörlerinin veri uygulamaları üzerinde kontrolümüz bulunmamakta ve bunlar için sorumluluk kabul etmemekteyiz.

#### 4.2 RadioID.net

Dijital ID arama özelliğini kullandığınızda, çağrı işaretiniz HTTPS üzerinden `https://radioid.net`'e iletilir. RadioID.net, bağımsız bir amatör radyo kimlik kayıt servisidir. Arama isteklerini nasıl işledikleri hakkında [radioid.net](https://radioid.net) adresindeki gizlilik politikalarına başvurunuz.

---

### 5. Cihaz İzinleri

Aşağıdaki cihaz izinleri talep edilmektedir:

| İzin | Platform | Ne Zaman Talep Edilir | Amaç |
|---|---|---|---|
| **Mikrofon** | iOS / macOS / watchOS | İlk PTT denemesinde | İletim için ses yakalanması |
| **Konum (Kullanımdayken)** | iOS / macOS | "GPS Konumunu Al" düğmesine dokunulduğunda | Konum bildirimi için GPS koordinatlarının alınması |
| **Yerel Ağ** | iOS / macOS | Yerel bir sunucuya bağlantı denemesinde | Yerel ağdaki DMR hotspot sunucularına bağlantı |

#### İzin Detayları

**Mikrofon:**  
Ses yalnızca PTT aktifken yakalanır. Uygulama, sesi bir dosyaya kaydetmez ve sesi yalnızca bağlı olduğunuz radyo ağı sunucusuna iletir. Arka plan ses yakalama, kesintisiz bağlantıyı sürdürmek için `UIBackgroundModes: audio` kullanır. Apple Watch'ta mikrofon erişimi, Watch'un PTT giriş cihazı olarak işlev gördüğünde kullanılır; ses, kodlama ve iletim için WatchConnectivity aracılığıyla iPhone'a iletilir.

**Konum:**  
Konuma yalnızca "GPS Konumunu Al" düğmesine açıkça dokunduğunuzda erişilir. Uygulama `requestWhenInUseAuthorization()` kullanır; arka plan konum erişimi hiçbir zaman talep edilmez. Koordinatlar alındıktan sonra konum servisi hemen durdurulur. Koordinatlar, ayarlarınızda yerel olarak saklanır ve yalnızca konum bildirimini yapılandırdıysanız protokol paketlerine dahil edilir.

**Yerel Ağ:**  
Yerel Wi-Fi ağınızda çalışan DMR hotspot cihazlarına UDP bağlantısına izin vermek için gereklidir. Bu izin, diğer cihazlardaki dosya veya verilere erişim sağlamaz.

**Apple Watch — Ek İzin Yok:**  
Digi Voice Watch yardımcı uygulaması, eşleşik iPhone uygulamasına halihazırda tanınan izinlerin ötesinde herhangi bir izin talep etmez. Watch'taki mikrofon erişimi watchOS tarafından yönetilir ve iPhone'da mikrofon iznine sahip eşleşik uygulamalar için otomatik olarak tanınır.

---

### 6. App Store Gizlilik Beslenme Etiketi

Digi Voice'un App Store gizlilik açıklaması, ALGSoft Inc. tarafından kullanıcılardan **Veri Toplanmadığını** beyan etmektedir. Aşağıdaki tablo App Privacy etiketini doğru şekilde yansıtmaktadır:

| Veri Kategorisi | ALGSoft Inc. Tarafından Toplanıyor mu | Notlar |
|---|---|---|
| İletişim Bilgisi | Hayır | Toplanmıyor |
| Sağlık & Fitness | Hayır | Toplanmıyor |
| Finansal Bilgi | Hayır | Toplanmıyor |
| Konum | Hayır | Yalnızca cihazda kullanılır; bize gönderilmez |
| Hassas Bilgi | Hayır | Toplanmıyor |
| Kişiler | Hayır | Toplanmıyor |
| Kullanıcı İçeriği (Ses) | Hayır | Yalnızca üçüncü taraf radyo sunucularına iletilir; biz toplamayız |
| Tarama Geçmişi | Hayır | Toplanmıyor |
| Arama Geçmişi | Hayır | Toplanmıyor |
| Tanımlayıcılar | Hayır | Toplanmıyor |
| Kullanım Verisi | Hayır | Toplanmıyor |
| Tanı | Hayır | Kilitlenme SDK'sı yok; telemetri yok |

**Üçüncü taraf radyo ağı sunucularına** iletilen veriler (çağrı işareti, ses) bu ağların kendi gizlilik politikaları kapsamındadır; ALGSoft Inc. kapsamında değildir.

---

### 7. Veri Güvenliği

Şifreler dahil tüm ayarlar, iOS/macOS Veri Koruması ile cihaz parolanız/biyometriniz tarafından korunan yerel cihazınızda `UserDefaults` kullanılarak saklanır. Her radyo ağı için güçlü ve benzersiz şifreler kullanmanızı öneririz.

Şifreler, protokolün gerektirdiği biçimde ağ sunucularına iletilir (DMR, SHA-256 hash kullanır; diğer protokoller UDP yükü içinde düz metin iletebilir). Birincil hesap kimlik bilgileri yerine ağa özgü hotspot güvenlik anahtarları kullanmanızı öneririz.

Apple Watch Ayarlar ekranı üzerinden girilen Hotspot Security şifreleri iPhone'a iletildiğinde, aktarım WatchConnectivity üzerinden (Bluetooth / yerel Wi-Fi) yerel olarak gerçekleşir. Şifre yalnızca iPhone'daki `UserDefaults`'a kaydedilir; Watch'ta saklanmaz.

---

### 8. Veri Saklama ve Silme

**Ayarlar:** Uygulamayı sıfırlayıncaya veya silene kadar süresiz olarak saklanır. Tüm ayarları kaldırmak için Digi Voice uygulamasını cihazınızdan silin.

**Log Dosyaları:** Cihazın Caches dizininde saklanır. İşletim sistemi, depolama baskısı altında önbellek dosyalarını silebilir. Kayıtlar sekmesinden günlükleri manuel olarak temizleyebilirsiniz. Uygulama silindiğinde günlükler de kaldırılır.

**Apple Watch Verisi:** WatchConnectivity aracılığıyla Apple Watch'a senkronize edilen yapılandırma yalnızca Watch yardımcı uygulamasının yerel deposunda saklanır. Watch uygulamasının kaldırılması bu veriyi siler. Watch tarafındaki verinin iPhone'da hiçbir yedeği saklanmaz.

Altyapımızda cihazınızdan herhangi bir veri almadığımız için sunucularımızda hiçbir veri tutmuyoruz.

---

### 9. Çocukların Gizliliği

Digi Voice, **lisanslı amatör radyo operatörleri** için tasarlanmış olup **13 yaşın altındaki kişilere** (veya yargı bölgenizdeki geçerli asgari yaşa) **yönelik değildir**. Bilerek çocuklardan kişisel bilgi toplamıyoruz. Bir çocuğun bu uygulamayı uygun denetim olmaksızın kullandığına inanıyorsanız lütfen bizimle iletişime geçin; gerekli adımları atacağız.

---

### 10. Uluslararası Kullanıcılar

Digi Voice Türkiye'de geliştirilmiştir ve girdiğiniz veriler cihazınızda yerel olarak saklanır. Radyo ağı sunucularına bağlandığınızda, verileriniz çeşitli ülkelerdeki üçüncü taraflarca işletilen sunuculara iletilir. Ağ özelliklerini kullanarak, radyo ağı operasyonunun bir parçası olarak bu sınır ötesi iletimi kabul etmiş olursunuz.

---

### 11. Bu Gizlilik Politikasındaki Değişiklikler

Bu Gizlilik Politikasını zaman zaman güncelleyebiliriz. Güncelleme yaptığımızda bu belgenin başındaki "Son Güncelleme" tarihini revize edecek ve uygun olduğu hallerde uygulama içinde bildirim sağlayacağız. Revize edilmiş bir politikanın yürürlük tarihinden sonra Digi Voice'u kullanmaya devam etmeniz, değişiklikleri kabul ettiğiniz anlamına gelir.

---

### 12. Haklarınız ve Nasıl Kullanacağınız

Digi Voice kendi sunucularında hiçbir kişisel veri tutmadığından, veri haklarını kullanma şekliniz tamamen **verinin gerçekte nerede bulunduğuna** bağlıdır.

#### 12.1 Digi Voice Uygulaması İçindeki Veriler (cihazınızda)

Tüm uygulama ayarları — çağrı işareti, ID, şifreler, koordinatlar, RX ses seviyesi, favori konuşma grupları — cihazınızda yerel olarak saklanır ve tamamen sizin kontrolünüzdedir:

- **Erişim / Dışa Aktarım:** Ayarları Digi Voice Ayarlar ekranında doğrudan okuyun.
- **Düzeltme:** Herhangi bir alanı Ayarlar ekranından istediğiniz zaman düzenleyin.
- **Silme:** Digi Voice uygulamasını cihazınızdan silin. Tüm UserDefaults ve önbelleğe alınan log dosyaları kalıcı olarak kaldırılır. Bizden talep edilecek bir şey yoktur — elimizde hiçbir kopya bulunmamaktadır.

#### 12.2 Üçüncü Taraf Radyo Ağı Platformlarındaki Veriler

Çağrı işaretiniz, DMR ID'niz, hesap profiliniz ve iletim geçmişiniz, kayıt yaptırdığınız platformlarda tutulmaktadır. **Digi Voice bu verilere erişemez; sizin adınıza bu verileri değiştiremez veya silemez.**

Bu platformlardaki veri haklarınızı kullanmak için doğrudan ilgili platformla iletişime geçin:

| Platform | Veri Hakları İletişimi |
|---|---|
| **RadioID.net** | [radioid.net](https://radioid.net) — web sitesi üzerinden iletişim |
| **BrandMeister** | [brandmeister.network](https://brandmeister.network) — bölgesel yöneticinizle iletişim |
| **TGIF Network** | [tgif.network](https://tgif.network) |
| **FreeDMR** | [freedmr.cymru](https://freedmr.cymru) |
| **HBLink / US Digital** | [usdigitalnetwork.com](https://usdigitalnetwork.com) |
| D-STAR / YSF / AllStar reflektörler | İlgili reflektör operatörüyle iletişim |

ALGSoft Inc., bu platformların elinde bulunan veriler için veri erişim, düzeltme veya silme taleplerini yerine getiremez. Bize yöneltilen bu tür talepler, ilgili platforma yönlendirilecek veya size uygun iletişim bilgileriyle iade edilecektir.

---

### 13. Bize Ulaşın

Bu Gizlilik Politikası hakkında sorularınız, endişeleriniz veya talepleriniz varsa lütfen aşağıdaki kanallardan iletişime geçin:

**ALGSoft Inc.**  
📧 info@algsoft.net.tr  
🌐 [https://algsoft.net.tr](https://algsoft.net.tr)

**Geliştirici**  
Fatih ÖNDER (TB1TFO)  
📧 info@fatihonder.org.tr  
🌐 [https://fatihonder.org.tr](https://fatihonder.org.tr)

---

*© 2026 ALGSoft Inc. — All rights reserved / Tüm hakları saklıdır.*
