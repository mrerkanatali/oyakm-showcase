# Showcase Release Policy

Defines periodic update practice for `oyakm-showcase`.

## Cadence

- Preferred: weekly update window.
- Acceptable: bi-weekly if no major capability change occurred.

## Scope of each update

- Capability-level wording updates.
- Architecture diagram updates (high level only).
- White-label process and commercial draft refresh.
- Sanitized screenshots only.

## Required checks before push

1. Secret keyword scan:
   - `secret`
   - `token`
   - `password`
   - `private key`
2. URL/domain check:
   - No internal domains or private environment URLs.
   - Public examples stay placeholder or approved public domain.
3. Visual review:
   - No personal data in screenshots.
   - No admin credentials, internal IDs, or sensitive values.

## Commit message standard

Use:

`docs(showcase): <short update summary>`

Examples:

- `docs(showcase): update capabilities and architecture wording`
- `docs(showcase): refresh onboarding and whitelist checklist`

---

## Turkce

Bu politika, `oyakm-showcase` icin periyodik guncelleme pratigini tanimlar.

## Periyot

- Tercih edilen: Haftalik update penceresi.
- Kabul edilen: Buyuk capability degisikligi yoksa iki haftada bir.

## Her guncellemenin kapsami

- Capability seviyesinde metin guncellemeleri.
- Mimari diyagram guncellemeleri (yalnizca yuksek seviye).
- White-label surec ve ticari dokuman tazelemesi.
- Sadece sanitize screenshot eklemeleri.

## Push oncesi zorunlu kontroller

1. Secret anahtar kelime taramasi:
   - `secret`
   - `token`
   - `password`
   - `private key`
2. URL/domain kontrolu:
   - Internal domain veya private environment URL olmamali.
   - Public ornekler placeholder ya da onayli public domain olmali.
3. Gorsel kontrol:
   - Screenshot'larda kisisel veri bulunmamali.
   - Admin credential, internal ID veya hassas alan gorunmemeli.

## Commit mesaji standardi

Kullanim:

`docs(showcase): <short update summary>`

Ornekler:

- `docs(showcase): update capabilities and architecture wording`
- `docs(showcase): refresh onboarding and whitelist checklist`
