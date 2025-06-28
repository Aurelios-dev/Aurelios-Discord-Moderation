# 🤖 Aurelios-Discord-Moderation Botu

Modern Discord sunucuları için geliştirilmiş kapsamlı Aurelios-Discord-Moderation. Gelişmiş güvenlik özellikleri, otomatik rol sistemi ve kullanıcı dostu arayüzü ile sunucunuzu güvende tutar.

## ✨ Özellikler

### 🔐 Moderasyon Sistemi
- **Kullanıcı Yönetimi**: Kick, ban, unban, timeout işlemleri
- **Uyarı Sistemi**: Kullanıcılara uyarı verme ve takip etme
- **Mesaj Yönetimi**: Toplu mesaj silme (1-100 arası)
- **Yetki Kontrolü**: Otomatik yetki doğrulama

### 🛡️ Güvenlik Özellikleri
- **Kelime Filtresi**: Özelleştirilebilir yasaklı kelimeler
- **Spam Koruması**: Otomatik spam tespiti ve engelleme
- **Anti-Raid Sistemi**: Toplu saldırı koruması
- **Şiddet Seviyeleri**: Uyarı, susturma, atma (1-3 seviye)

### 🎭 Otomatik Rol Sistemi
- **Katılım Rolleri**: Yeni üyelere otomatik rol verme
- **Reaksiyon Rolleri**: Emoji ile rol alma/verme
- **Esnek Konfigürasyon**: Çoklu rol desteği

### 📊 Loglama ve İzleme
- **Detaylı Loglar**: Tüm moderasyon işlemlerini kaydetme
- **Hoşgeldin/Veda**: Özelleştirilebilir mesajlar
- **Kullanıcı İstatistikleri**: Aktivite takibi
- **Sunucu Analitikleri**: Kapsamlı raporlama

### 🔧 Yardımcı Özellikler
- **Slash Commands**: Modern Discord komut sistemi
- **Çoklu Dil**: Tam Türkçe arayüz
- **Gerçek Zamanlı**: Hızlı yanıt süreleri
- **Kolay Kurulum**: Basit setup süreci

## 📋 Komut Listesi

### Moderasyon
```
/kick <kullanıcı> [sebep]        - Kullanıcıyı sunucudan atar
/ban <kullanıcı> [sebep]         - Kullanıcıyı yasaklar
/unban <kullanıcı_id> [sebep]    - Yasağı kaldırır
/uyar <kullanıcı> <sebep>        - Kullanıcıya uyarı verir
/timeout <kullanıcı> <süre>      - Kullanıcıyı susturur
/uyarilar <kullanıcı>            - Uyarı geçmişini gösterir
/temizle <sayı> [kullanıcı]      - Mesajları toplu siler
```

### Otomatik Rol
```
/otorol-ekle <rol> <tür>         - Otomatik rol ekler
/otorol-sil <rol>                - Otomatik rol siler
/otorol-liste                    - Otomatik rolleri listeler
```

### Yönetim
```
/ayarlar                         - Sunucu ayarlarını gösterir
/prefix <yeni_prefix>            - Bot prefixini değiştirir
/kelime-filtresi <işlem>         - Kelime filtresini yönetir
/spam-koruması                   - Spam korumasını aç/kapat
/anti-raid                       - Anti-raid korumasını aç/kapat
```

### Loglama
```
/log-kanal <kanal>               - Log kanalını ayarlar
/hosgeldin-ayarla <kanal>        - Hoşgeldin sistemini ayarlar
/veda-ayarla <kanal>             - Veda sistemini ayarlar
```

### Yardımcı
```
/yardım                          - Komut rehberini gösterir
/kullanıcı-bilgi [kullanıcı]     - Kullanıcı bilgilerini gösterir
/sunucu-bilgi                    - Sunucu detaylarını gösterir
/bot-bilgi                       - Bot istatistiklerini gösterir
/ping                            - Bot durumunu kontrol eder
/davet                           - Bot davet linkini gösterir
```

## 🚀 Kurulum

### Gereksinimler
- Python 3.11+
- Discord.py 2.5+
- SQLite/PostgreSQL
- Discord Bot Token

### 1. Projeyi İndirin
```bash
git clone https://github.com/Aurelios-dev/Aurelios-Discord-Moderation.git
cd Aurelios-Discord-Moderation
```

### 2. Bağımlılıkları Yükleyin
```bash
pip install discord.py aiosqlite psutil
```

### 3. Bot Token'ını Ayarlayın
`.env` dosyası oluşturun:
```env
DISCORD_BOT_TOKEN=your_bot_token_here
```

### 4. Botu Başlatın
```bash
python main.py
```

## ⚙️ Konfigürasyon

### Bot Ayarları (`config.json`)
```json
{
    "default_prefix": "/",
    "default_language": "tr",
    "auto_sync_commands": true,
    "debug_mode": false,
    "owners": [123456789],
    "blacklisted_users": []
}
```

### Veritabanı Ayarları
Bot otomatik olarak SQLite veritabanı oluşturur. PostgreSQL kullanmak için `DATABASE_URL` environment variable'ını ayarlayın.

## 🔧 Discord Geliştirici Ayarları

### 1. Bot Oluşturma
1. [Discord Developer Portal](https://discord.com/developers/applications)'a gidin
2. "New Application" butonuna tıklayın
3. Uygulamanıza bir isim verin
4. "Bot" sekmesine gidin ve "Add Bot" butonuna tıklayın

### 2. Bot Yetkilerini Ayarlama
Aşağıdaki yetkileri etkinleştirin:
- **General Permissions**:
  - View Audit Log
  - Manage Webhooks
  - Read Messages
  - Send Messages
  - Embed Links
  - Attach Files
  - Read Message History
  - Add Reactions
  - Use Slash Commands

- **Membership Permissions**:
  - Kick Members
  - Ban Members
  - Moderate Members

- **Text Permissions**:
  - Manage Messages
  - Manage Threads

- **Voice Permissions**:
  - Connect
  - Move Members

### 3. Privileged Gateway Intents
Aşağıdaki intent'leri etkinleştirin:
- ✅ Server Members Intent
- ✅ Message Content Intent

### 4. OAuth2 URL Oluşturma
"OAuth2" > "URL Generator" sekmesinden:
- **Scopes**: `bot`, `applications.commands`
- **Bot Permissions**: Yukarıdaki yetkileri seçin

## 📁 Proje Yapısı

```
Aurelios-Discord-Moderation/
├── main.py                 # Ana başlatma dosyası
├── bot.py                  # Bot sınıfı ve temel yapı
├── database.py             # Veritabanı yönetimi
├── models.py               # Veri modelleri
├── config.json             # Bot konfigürasyonu
├── cogs/                   # Modüler komut grupları
│   ├── admin.py           # Yönetici komutları
│   ├── autorole.py        # Otomatik rol sistemi
│   ├── logging.py         # Loglama sistemi
│   ├── moderation.py      # Moderasyon komutları
│   └── utility.py         # Yardımcı komutlar
└── utils/                  # Yardımcı modüller
    ├── filters.py         # Filtreleme sistemleri
    └── helpers.py         # Genel yardımcılar
```

## 🔒 Güvenlik

### Veritabanı Güvenliği
- Parametreli sorgular kullanılır
- SQL injection koruması
- Otomatik sanitizasyon

### Bot Token Güvenliği
- Environment variables kullanın
- Token'ları asla kodda sabit yazmayın
- `.env` dosyasını `.gitignore`'a ekleyin

### Yetki Kontrolü
- Her komut için otomatik yetki kontrolü
- Kullanıcı rolleri doğrulanır
- Admin komutları korunur

## 📈 Performans

### Optimize Özellikler
- **Async/Await**: Non-blocking operasyonlar
- **Caching**: 5 dakikalık kelime filtresi cache'i
- **Connection Pooling**: Veritabanı bağlantı havuzu
- **Rate Limiting**: Discord API limitlerine uyum

### Sistem Gereksinimleri
- **RAM**: Minimum 512MB
- **CPU**: 1 vCPU
- **Disk**: 1GB boş alan
- **Network**: Stabil internet bağlantısı

## 🐛 Sorun Giderme

### Yaygın Hatalar

**Bot çevrimiçi görünmüyor**
- Bot token'ının doğru olduğunu kontrol edin
- Privileged intents'lerin etkin olduğunu doğrulayın

**Komutlar çalışmıyor**
- Bot'un gerekli yetkilere sahip olduğunu kontrol edin
- Slash command sync'in tamamlandığını bekleyin

**Veritabanı hataları**
- Dosya yazma yetkilerini kontrol edin
- SQLite dosyasının var olduğunu doğrulayın

### Debug Modu
```python
# config.json'da debug_mode'u true yapın
{
    "debug_mode": true
}
```

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/yeni-ozellik`)
3. Değişikliklerinizi commit edin (`git commit -am 'Yeni özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/yeni-ozellik`)
5. Pull Request açın

### Kod Standartları
- PEP 8 stilini takip edin
- Türkçe yorum ve docstring kullanın
- Type hints ekleyin
- Async/await tercih edin

## 📝 Lisans

Bu proje MIT Lisansı altında lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakın.

## 📞 Destek

- **Issues**: GitHub Issues sayfasını kullanın
- **Özellik İstekleri**: Feature request template'ini doldurun
- **Güvenlik**: Güvenlik açıklarını özel olarak bildirin

## 🙏 Teşekkürler

- [discord.py](https://github.com/Rapptz/discord.py) - Discord API wrapper
- [aiosqlite](https://github.com/omnilib/aiosqlite) - Async SQLite
- [psutil](https://github.com/giampaolo/psutil) - Sistem bilgileri

## 🔄 Güncellemeler

### v1.0.0 - İlk Sürüm
- ✅ Temel moderasyon komutları
- ✅ Otomatik rol sistemi
- ✅ Loglama ve güvenlik
- ✅ Slash command desteği
- ✅ Türkçe arayüz

---

**Türk Discord topluluğu için özel olarak geliştirilmiştir** 🇹🇷

Bot'u beğendiyseniz ⭐ vermeyi unutmayın!
