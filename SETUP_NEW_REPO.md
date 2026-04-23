# Yeni boş GitHub reposuna aktarma — komutlar

Bu dosya yalnızca talimat içindir; ana `oyakm` reposuna commit etmeyin. Paketi **ayrı public repo**da yayınlayacaksınız.

## 1) GitHub’da

1. Yeni **boş** repository oluşturun (ör. `oyakm-showcase`, public).
2. README / .gitignore / license **eklemeyin** (repo tamamen boş kalsın).

## 2) Yerelde (paketi kopyalayıp ilk push)

```bash
# Örnek: üst klasörde yeni klasör
cd /Volumes/destek/projects
cp -R oyakm/showcase-public-pack oyakm-showcase
cd oyakm-showcase

git init
git branch -M main
git add .
git status   # kontrol: gizli dosya yok
git commit -m "docs(showcase): initial public sanitized pack (EN+TR, no secrets)"

git remote add origin git@github.com:KULLANICI/oyakm-showcase.git
git push -u origin main
```

`KULLANICI/oyakm-showcase` ve SSH/HTTPS URL’yi kendi GitHub hesabınıza göre değiştirin.

## 3) Ana oyakm reposunda (isteğe bağlı)

`showcase-public-pack/` klasörü `.gitignore` ile **izlenmiyor**. İsterseniz yalnızca `.gitignore` satırını `main`’e commit edersiniz (paket dosyaları commitlenmez):

```bash
cd /Volumes/destek/projects/oyakm
git add .gitignore
git commit -m "chore: ignore showcase-public-pack (ayrı repo)"
git push origin main
```

## 4) Ekran görüntüleri

PNG’leri `assets/screenshots/` içine koyduktan sonra **yeni repo**da:

```bash
git add assets/screenshots/
git commit -m "docs(showcase): add sanitized showcase screenshots"
git push
```

## 5) Asıl repo değiştikçe showcase güncelleme akışı

Asıl `oyakm` reposunda feature geliştirmeye devam edin. Showcase repo için sadece güvenli doküman/varlık güncellemesi taşıyın:

```bash
# showcase repo içinde
git checkout main
git pull

# sadece docs + güvenli görsel güncelle
git add README.md docs/ assets/screenshots/ .gitignore
git status
git commit -m "docs(showcase): refresh sanitized capabilities and architecture"
git push
```

Asla taşınmaması gerekenler: gerçek kod dosyaları, `.env`, Firebase servis hesapları, keystore, endpoint iç detayları, formül/algoritma detayları.

## 6) Push öncesi hızlı sızıntı kontrolü (showcase repo)

```bash
# şüpheli anahtar/desen taraması
rg -n "AIza|BEGIN PRIVATE KEY|password|secret|token|firebase|keystore|GoogleService-Info|google-services" .

# yanlışlıkla kod eklendi mi kontrolü
rg -n "class |function |import |package " docs README.md
```

## 7) Periyodik sürümleme pratiği

- Tercih edilen ritim: haftalık showcase güncellemesi.
- Kabul edilen ritim: büyük değişiklik yoksa iki haftada bir.
- Commit mesaj standardı: `docs(showcase): ...`
