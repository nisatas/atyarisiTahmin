# 🏇 Beygir Mühendisi - At Yarışı Tahminleri

Bu proje, Netlify CMS kullanarak at yarışı tahminlerini yönetmek için oluşturulmuştur.

## 🚀 Netlify CMS Kurulumu

### 1. Netlify'da Site Oluşturma

1. [Netlify](https://netlify.com)'a gidin ve hesabınızla giriş yapın
2. "New site from Git" butonuna tıklayın
3. GitHub/GitLab/Bitbucket hesabınızı bağlayın
4. Bu repository'yi seçin
5. Build settings:
   - **Build command**: Boş bırakın
   - **Publish directory**: `.` (nokta)
6. "Deploy site" butonuna tıklayın

### 2. Netlify Identity Ayarları

1. Netlify dashboard'da sitenize gidin
2. **Site settings** > **Identity** sekmesine gidin
3. **Enable Identity** butonuna tıklayın
4. **Registration preferences**'ı "Invite only" olarak ayarlayın
5. **Invite users** bölümünden kendinizi davet edin

### 3. Git Gateway Ayarları

1. **Site settings** > **Identity** > **Services** sekmesine gidin
2. **Git Gateway**'i etkinleştirin
3. **Generate access token** butonuna tıklayın

### 4. Admin Paneli Erişimi

1. Sitenizin URL'sine `/admin` ekleyerek admin paneline erişin
2. Netlify Identity ile giriş yapın
3. Artık yeni tahminler ekleyebilir ve mevcut olanları düzenleyebilirsiniz

## 📝 Yeni Tahmin Ekleme

### Admin Panelinden:

1. `/admin` sayfasına gidin
2. **At Yarışı Tahminleri** bölümüne tıklayın
3. **New At Yarışı Tahminleri** butonuna tıklayın
4. Gerekli bilgileri doldurun:
   - **Tarih**: YYYY-MM-DD formatında (örn: 2025-07-15)
   - **Başlık**: Tahmin başlığı
   - **Pist**: İstanbul, Ankara, İzmir vb.
   - **Gün**: Haftanın günü
   - **Tür**: Altılı Ganyan, Beşli Ganyan vb.
   - **Açıklama**: Tahmin açıklaması
   - **Google Sheets URL**: Yayınlanmış Google Sheets URL'si
   - **Öne Çıkan Resim**: Tahmin için resim
   - **Aktif**: Tahminin aktif olup olmadığı
   - **Tutan Tahmin**: Tahminin tutup tutmadığı
   - **İçerik**: Ek açıklamalar (markdown formatında)

5. **Publish** butonuna tıklayın

### Manuel Olarak:

1. `tahminler/` klasöründe yeni bir `.html` dosyası oluşturun
2. Dosya adı: `YYYY-MM-DD.html` formatında olmalı
3. `tahminler/template.html` dosyasını kopyalayın
4. Front matter bölümündeki değerleri güncelleyin

## 🔧 Özellikler

- ✅ Netlify CMS ile kolay içerik yönetimi
- ✅ Otomatik tarih formatı
- ✅ Google Sheets entegrasyonu
- ✅ Responsive tasarım
- ✅ Mobil uyumlu menü
- ✅ Tutan tahminler listesi
- ✅ Medya yönetimi

## 📁 Dosya Yapısı

```
AtYarisiTahmin/
├── admin/
│   ├── index.html          # Netlify CMS admin paneli
│   └── config.yml          # CMS konfigürasyonu
├── assets/
│   ├── logo.png
│   ├── atyarisitahminleri.jpg
│   └── uploads/            # CMS'den yüklenen dosyalar
├── tahminler/
│   ├── template.html       # Tahmin sayfası şablonu
│   ├── 2025-07-10.html    # Mevcut tahminler
│   └── ...
├── index.html              # Ana sayfa
├── netlify.toml           # Netlify konfigürasyonu
└── README.md              # Bu dosya
```

## 🎯 Kullanım İpuçları

1. **Google Sheets URL'si**: Google Sheets'i "Publish to web" olarak yayınlayın
2. **Resimler**: Admin panelinden yükleyebilir veya `assets/` klasörüne manuel ekleyebilirsiniz
3. **Tarih Formatı**: Her zaman YYYY-MM-DD formatını kullanın
4. **Slug**: Otomatik olarak tarihten oluşturulur
5. **Değişiklikler**: Otomatik olarak yayınlanır

## 🔒 Güvenlik

- Admin paneline erişim sadece davet edilen kullanıcılar için
- Git Gateway ile güvenli değişiklik yönetimi
- HTTPS zorunlu

## 📞 Destek

Herhangi bir sorun yaşarsanız:
- Netlify dokümantasyonunu kontrol edin
- GitHub Issues'da sorun bildirin
- E-posta: info@beygirmuhendisi.com

---

**Not**: Bu sistem Netlify'ın ücretsiz planında çalışır. Daha fazla özellik için ücretli planlara geçebilirsiniz. #   a t y a r i s i T a h m i n  
 