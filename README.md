# 🤖 Rolmatik - Discord Sunucu Yönetim Botu

**Aurelios-Discord-Moderation**, Discord sunucularınızı daha düzenli, güvenli ve kullanıcı dostu hale getirmek için geliştirilmiş, kolay kullanımlı bir moderasyon botudur.  
Python ile yazılmıştır ve `discord.py` kütüphanesini temel alır.

---

## 🔧 Özellikler

- 🛡️ **Moderasyon Komutları**  
  Kullanıcıları kickleme, banlama, uyarma gibi temel yönetim işlemleri.

- 🧾 **Oto Rol Sistemi**  
  Yeni katılan üyelere otomatik olarak rol atama.

- 👋 **Hoş Geldin Mesajı**  
  Sunucuya yeni biri katıldığında özel mesaj ya da kanal bildirimi gönderir.

- 🧹 **Temel Temizlik Komutları** *(isteğe bağlı)*  
  Belirli sayıda mesajı silme gibi işlemler.

- ⚙️ **Kolay Geliştirilebilir Yapı**  
  Yeni özellikler eklemeye uygun sade kod yapısı.

---

## 📦 Kurulum

```bash
git clone https://github.com/Aurelios-dev/Aurelios-Discord-Moderation.git
cd Aurelios-Discord-Moderation
```

## 🔑 Bot Token Ayarları

Bot token’ınızı `config.json` veya `.env` gibi güvenli bir şekilde saklamayı unutmayın. Örnek `.env` içeriği:

```
DISCORD_TOKEN=senin-bot-tokenin
```

Kodda `os.getenv("DISCORD_TOKEN")` kullanarak çağırabilirsiniz.

---

## 🚀 Botu Başlatmak

```bash
python bot.py
```

---

## 📌 Gerekli İzinler

- Üyeleri Yönetme
- Mesajları Görüntüleme ve Silme
- Roller Atama
- Sunucuya Katılanları Görme (Intents ayarlarından `Server Members Intent` aktif olmalı)

---

## 💡 Katkıda Bulun

Rolmatik açık kaynak bir projedir.  
Yeni özellikler eklemek, hata düzeltmek veya öneri sunmak için `Issue` açabilir veya `Pull Request` gönderebilirsiniz.

---

## 📝 Lisans

Bu proje MIT lisansı ile lisanslanmıştır.  
Dilediğiniz gibi kullanabilir, dağıtabilir ve geliştirebilirsiniz.

---

## ✨ Destek

Herhangi bir soru, hata bildirimi veya öneriniz varsa GitHub üzerinden iletişime geçebilirsiniz.  
İyi sunucular, düzenli topluluklar! 🚀
