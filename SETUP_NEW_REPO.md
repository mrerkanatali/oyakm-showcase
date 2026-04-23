# Showcase repository setup

This file helps initialize or refresh a public showcase repository.

## 1) Create a new empty GitHub repository

1. Create a new **empty** repository (for example, `oyakm-showcase`, public).
2. Do not pre-add README, license, or gitignore.

## 2) Local setup and first push

```bash
# Example local flow
mkdir oyakm-showcase
cd oyakm-showcase

git init
git branch -M main
git add .
git status
git commit -m "docs(showcase): initial public sanitized pack (EN+TR, no secrets)"

git remote add origin git@github.com:<YOUR_USER>/oyakm-showcase.git
git push -u origin main
```

Use your own GitHub account and remote URL.

## 3) Optional screenshot update

```bash
git add assets/screenshots/
git commit -m "docs(showcase): add sanitized showcase screenshots"
git push
```

## 4) Ongoing showcase update flow

```bash
# In showcase repository
git checkout main
git pull

# Update only docs and safe assets
git add README.md docs/ assets/screenshots/ .gitignore
git status
git commit -m "docs(showcase): refresh sanitized capabilities and architecture"
git push
```

Never include: source code, `.env`, service accounts, keystores, endpoint internals, formula or algorithm details.

## 5) Quick leak checks before push

```bash
# Suspicious key patterns
rg -n "AIza|BEGIN PRIVATE KEY|password|secret|token|firebase|keystore|GoogleService-Info|google-services" .

# Optional check for accidental code snippets
rg -n "class |function |import |package " docs README.md
```

## 6) Release cadence

- Preferred rhythm: weekly showcase update.
- Acceptable rhythm: bi-weekly if no major capability change.
- Commit message standard: `docs(showcase): ...`

---

## Turkce

Bu dosya, public showcase reposunu ilk kez kurmak veya guncellemek icin hizli kilavuzdur.

## 1) Bos GitHub reposu olustur

1. Yeni **bos** bir repo olustur (ornek: `oyakm-showcase`, public).
2. README, license veya gitignore onceden ekleme.

## 2) Yerel kurulum ve ilk push

```bash
# Ornek yerel akis
mkdir oyakm-showcase
cd oyakm-showcase

git init
git branch -M main
git add .
git status
git commit -m "docs(showcase): initial public sanitized pack (EN+TR, no secrets)"

git remote add origin git@github.com:<YOUR_USER>/oyakm-showcase.git
git push -u origin main
```

Remote URL'yi kendi GitHub hesabina gore duzenle.

## 3) Opsiyonel screenshot guncellemesi

```bash
git add assets/screenshots/
git commit -m "docs(showcase): add sanitized showcase screenshots"
git push
```

## 4) Surekli showcase guncelleme akisi

```bash
# Showcase repo icinde
git checkout main
git pull

# Sadece docs ve guvenli varliklari guncelle
git add README.md docs/ assets/screenshots/ .gitignore
git status
git commit -m "docs(showcase): refresh sanitized capabilities and architecture"
git push
```

Asla dahil etme: kaynak kod, `.env`, servis hesabi dosyalari, keystore, endpoint ic detaylari, formul/algoritma detaylari.

## 5) Push oncesi hizli sizinti kontrolu

```bash
# Supheli anahtar desenleri
rg -n "AIza|BEGIN PRIVATE KEY|password|secret|token|firebase|keystore|GoogleService-Info|google-services" .

# Yanlislikla kod parcasi eklendi mi kontrolu
rg -n "class |function |import |package " docs README.md
```

## 6) Guncelleme periyodu

- Tercih edilen ritim: haftalik showcase guncellemesi.
- Kabul edilen ritim: buyuk capability degisikligi yoksa iki haftada bir.
- Commit mesaji standardi: `docs(showcase): ...`
