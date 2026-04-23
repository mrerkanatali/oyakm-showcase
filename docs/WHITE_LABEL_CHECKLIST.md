# White-label deployment checklist

**EN** | **TR** sections combined for one buyer-facing list.

---

## 1. Identity and domains

- [ ] **EN:** Choose app name, logo, store listings (iOS / Android).  
- [ ] **TR:** Uygulama adı, logo, mağaza metinleri (iOS / Android).

- [ ] **EN:** DNS for API, admin, and public site (or single host with paths).  
- [ ] **TR:** API, admin ve kamu web için DNS (veya tek host + yol yapısı).

- [ ] **EN:** TLS certificates (Let’s Encrypt / provider).  
- [ ] **TR:** TLS sertifikaları.

---

## 2. Server

- [ ] **EN:** PHP version compatible with API and admin; Composer where used.  
- [ ] **TR:** API ve admin ile uyumlu PHP; gerekli Composer.

- [ ] **EN:** MySQL / MariaDB; database created; user with least privilege.  
- [ ] **TR:** MySQL; veritabanı ve yetkili kullanıcı.

- [ ] **EN:** Cron: notification worker (e.g. every minute); financial jobs if purchased.  
- [ ] **TR:** Cron: bildirim worker; satın alındıysa finans scriptleri.

- [ ] **EN:** Writable directories for uploads / logs (policy-defined).  
- [ ] **TR:** Yükleme ve log için yazılabilir dizinler.

---

## 3. Secrets (never in public repos)

- [ ] **EN:** Database credentials; admin auth; Firebase service account JSON on server only.  
- [ ] **TR:** Veritabanı; admin kimlik doğrulama; Firebase JSON yalnız sunucuda.

- [ ] **EN:** Mobile: `google-services.json` / `GoogleService-Info.plist` per Firebase project.  
- [ ] **TR:** Mobil Firebase proje dosyaları.

- [ ] **EN:** Android signing keystore (buyer or vendor process per contract).  
- [ ] **TR:** Android imza (sözleşmeye göre alıcı veya tedarikçi).

---

## 4. Showcase-safe publication controls

- [ ] **EN:** Public materials include capability-level explanations only; no source code or implementation detail.  
- [ ] **TR:** Public içerik yalnız yetenek seviyesinde olmalı; kaynak kod ve uygulama detayı olmamalı.

- [ ] **EN:** No real formulas/algorithm details are published for proprietary calculators.  
- [ ] **TR:** Ticari sır niteliğindeki hesaplama formülleri/algoritma detayları yayınlanmaz.

- [ ] **EN:** Screenshots are sanitized: no personal data, secrets, internal domains, or admin credentials.  
- [ ] **TR:** Görseller anonimleştirilmiş olmalı: kişisel veri, sır, iç domain, admin bilgisi yok.

- [ ] **EN:** Demo links/credentials are shared privately on request, never committed to git.  
- [ ] **TR:** Demo bağlantı/erişim bilgileri yalnız özel kanaldan paylaşılır, git’e yazılmaz.

---

## 5. Content and operations

- [ ] **EN:** Seed or migrate content (news, blog, announcements).  
- [ ] **TR:** İçerik girişi veya aktarım.

- [ ] **EN:** Admin training; test-device workflow for push QA.  
- [ ] **TR:** Admin eğitimi; push test cihazı akışı.

---

## 6. Optional static web

- [ ] **EN:** Deploy static bundle; configure `bridge.php` targets and server-side key.  
- [ ] **TR:** Statik paket; köprü hedefleri ve sunucu tarafı anahtar.

---

This checklist is illustrative; a formal statement of work should attach to the chosen commercial model (see [COMMERCIAL.md](COMMERCIAL.md)).
