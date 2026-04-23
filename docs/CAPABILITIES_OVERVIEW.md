# Platform Capabilities Overview (Sanitized)

This file presents platform capabilities without exposing proprietary implementation.

## Flutter (iOS + Android)

- Unified mobile experience for members.
- Structured content consumption flows (news, announcements, blog-like feeds).
- Notification-driven deep-link behavior by content type.
- Locale-aware UX patterns and Turkish-first content presentation.
- Calculation tool family at category level (details kept proprietary).

## API Layer (PHP REST-style)

- Serves content and app configuration to mobile clients.
- Handles device registration and push-target eligibility.
- Supports controlled content distribution across client surfaces.
- Provides operational boundaries for admin-originated actions.
- Uses server-side integration patterns to avoid exposing sensitive keys on clients.

## Backend and Operations

- MySQL-backed content and operational records.
- Background processing model for notification dispatch jobs.
- Role-separated components: API, admin interface, worker process.
- Deployment-ready separation for public site, admin area, and service endpoints.

## Admin Capabilities

- Content management workflows for publishing and updates.
- Operational controls for notification campaigns.
- Audience scoping patterns (for example, test-only vs broader targets).
- Editorial lifecycle support from draft-like preparation to publish actions.

## Static Public Web

- Visitor-facing static site delivery.
- Optional server-side bridge model for controlled data access.
- Branding and content can be tailored per white-label deployment.

## Security and IP posture

- Showcase repo contains no source code and no secret material.
- Implementation logic, formulas, and internals remain private.
- Demo credentials are never committed and are only shared privately on request.

---

## Turkce

Bu dokuman, ticari implementasyon detaylarini aciga cikarmadan platform yeteneklerini ozetler.

## Flutter (iOS + Android)

- Uyeler icin birlesik mobil deneyim.
- Icerik tuketimi icin yapilandirilmis akislar (haber, duyuru, blog benzeri).
- Icerik tipine gore bildirimden deep-link davranisi.
- Turkce odakli ve yerel ihtiyaca uygun UX yaklasimi.
- Hesaplama araclari kategori seviyesinde sunulur (detaylar gizli tutulur).

## API Katmani (PHP REST-style)

- Mobil istemcilere icerik ve uygulama konfigurasyonu saglar.
- Cihaz kaydi ve bildirim hedef uygunlugunu yonetir.
- Icerigin istemci yuzeylerine kontrollu dagitimini destekler.
- Admin tarafindan baslatilan islemler icin operasyonel sinirlar sunar.
- Hassas anahtarlarin istemciye sizmamasi icin sunucu tarafi entegrasyon deseni kullanir.

## Backend ve Operasyon

- MySQL tabanli icerik ve operasyonel kayitlar.
- Bildirim isleri icin arka plan isleme modeli.
- Rol bazli ayrim: API, admin arayuzu ve worker sureci.
- Public web, admin ve servis endpointleri icin dagitima hazir ayrik yapi.

## Admin Yetenekleri

- Icerik yayinlama ve guncelleme is akislari.
- Bildirim kampanyalari icin operasyonel kontrol paneli.
- Hedef kitle kapsamlandirma deseni (test-only veya daha genis hedefleme).
- Taslaktan yayina editor yasam dongusu destegi.

## Statik Public Web

- Ziyaretci odakli statik site sunumu.
- Kontrollu veri erisimi icin opsiyonel sunucu-kopru modeli.
- White-label kurulumlarda marka ve icerik uyarlanabilir.

## Guvenlik ve Fikri Mulkiyet

- Showcase reposu kaynak kod ve secret icermez.
- Implementasyon mantigi, formuller ve ic detaylar private kalir.
- Demo erisim bilgileri git'e yazilmaz, sadece ozel kanal ile paylasilir.
