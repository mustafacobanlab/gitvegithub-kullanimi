---

### 📌 Git Nedir?

**Git**, proje dosyalarının geçmişini ve değişikliklerini takip etmeyi sağlayan dağıtık bir sürüm kontrol sistemidir.

**GitHub** ise bu Git projelerini çevrimiçi depolayabileceğin ve takım arkadaşlarınla paylaşabileceğin bir platformdur.

---

## 📌 Git Kurulumu ve Başlangıç

### Git Kurmak (Windows/macOS/Linux)

👉 https://git-scm.com/downloads

Kurulduktan sonra:
```bash
git --version
````

---

## 📌 Git Konfigürasyonu

### Kullanıcı Bilgilerini Tanımlama

```bash
git config --global user.name "Mustafa Çoban"
git config --global user.email "mustafa@example.com"
```

### Konfigürasyonları Görüntüleme

```bash
git config --list
```

---

## 📌 Git Komutları ve Açıklamaları

### Proje Başlatma

```bash
git init
```

Bulunduğun klasörü Git deposuna dönüştürür.

---

### Durum Kontrolü

```bash
git status
```

Değişen ve eklenmeyi bekleyen dosyaları listeler.

---

### Dosya Ekleme (Staging)

```bash
git add dosyaadı.txt
git add .        # Tüm dosyalar
```

---

### Commit (Değişiklikleri Kaydetme)

```bash
git commit -m "Açıklama mesajı"
```

---

### Geçmişi Görüntüleme

```bash
git log
```

---

### Değişiklikleri Geri Alma

**Staging’den Çıkarma**

```bash
git reset dosyaadı.txt
```

**Son commit’i geri almak**

```bash
git reset --soft HEAD~1
```

---

### Farkları Görme

```bash
git diff          # Çalışma alanı ve staging farkları
git diff --staged # Staging ve son commit farkları
```

---

## 📌 Branch (Dal) Kullanımı

### Branch Listeleme

```bash
git branch
```

### Yeni Branch Oluşturma

```bash
git branch yeni-ozellik
```

### Branch’e Geçiş

```bash
git checkout yeni-ozellik
```

**Branch oluşturup direkt geçmek**

```bash
git checkout -b yeni-ozellik
```

### Branch Birleştirme

```bash
git merge yeni-ozellik
```

### Branch Silme

```bash
git branch -d yeni-ozellik
```

---

## 📌 GitHub Kullanımı

### GitHub Repo'yu Local’e Çekme (Clone)

```bash
git clone https://github.com/kullaniciadi/repo-adi.git
```

---

### Mevcut Projeyi GitHub’a Göndermek

**1️⃣ Remote Adresi Tanımla**

```bash
git remote add origin https://github.com/kullaniciadi/repo-adi.git
```

**2️⃣ Remote Adresleri Görüntüle**

```bash
git remote -v
```

**3️⃣ Push İşlemi**

```bash
git push -u origin main
```

---

### Değişiklikleri GitHub’a Gönderme

```bash
git add .
git commit -m "Commit mesajı"
git push
```

---

### GitHub’dan Değişiklikleri Çekme

```bash
git pull
```

---

## 📌 .gitignore Dosyası

**Takibe alınmasını istemediğin dosya ve klasörleri tanımlar.**

```bash
node_modules/
*.log
.env
```

---

## 📌 Git Alias (Kısa Komutlar)

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.cm "commit -m"
```

Kullanımı:

```bash
git st
git co main
git cm "Mesaj"
```

---

## 📌 Git ve GitHub Kullanım Akışı

1. Proje klasörüne geç
2. `git init` ile başlat
3. `git add .` ile dosyaları ekle
4. `git commit -m "ilk commit"`
5. GitHub'da repo oluştur
6. `git remote add origin ...`
7. `git push -u origin main`

---

