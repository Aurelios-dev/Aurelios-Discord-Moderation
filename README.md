
🤖 Aurelios-Discord-Moderation

Aurelios-Discord-Moderation, bir Discord sunucusunun yönetimini kolaylaştırmak amacıyla geliştirilmiş kapsamlı bir bot projesidir.
Sunucu içi denetim, otomatik rol atama, loglama ve faydalı yardımcı araçlar sunar.
Python ile yazılmış olup discord.py kütüphanesi kullanılarak modüler yapıda geliştirilmiştir.

---

🔧 Özellikler

- 🛡️ Moderasyon: Ban, kick, timeout, silme gibi komutlarla kullanıcı denetimi.
- 🧾 Otorol: Yeni katılan kullanıcılara otomatik rol atama sistemi.
- 📜 Loglama: Kick, ban, silme ve rol olaylarının kayıt altına alınması.
- ⚙️ Admin Komutları: Botu yeniden başlatma, ayarları yapılandırma.
- 🧰 Yardımcı Komutlar: Sunucu bilgisi, kullanıcı bilgisi, zamanlayıcı gibi araçlar.
- 🔌 Modüler Yapı: cogs/ klasöründeki modüllerle kolay genişletilebilir sistem.
- 🛢️ SQLite Veritabanı: Rol ve ayar kayıtları için dahili veri yönetimi.
- 💡 Yardım Sistemi: Komutlara özel açıklamalar ve yardım komutları.

---

🚀 Kurulum

git clone https://github.com/Aurelios-dev/Aurelios-Discord-Moderation.git
cd Aurelios-Discord-Moderation
pip install -r requirements.txt (Dosya yapısında yoksa oluştura bilirsiniz.)

Gerekirse discord.py v2+ yüklü olduğundan emin olun:
pip install -U discord.py

---

⚙️ Ayarlar

config.json

Bot ayarlarını buradan yapabilirsin:

{
  "token": "BOT_TOKENINIZ",
  "prefix": "!",
  "log_channel_id": 123456789012345678,
  "autorole_id": 123456789012345678
}

Not: Geliştirme sırasında token'ı asla herkese açık paylaşmayın!

---

🧠 Kullanım

Botu başlatmak için:

python main.py

---

🗃️ Yapı

- main.py — Botun başlangıç noktası.
- bot.py — Discord client ve olay yönetimi.
- cogs/ — Özelliklerin modüler olarak tutulduğu klasör.
- utils/ — Yardımcı işlevler ve filtreler.
- models.py — Veritabanı modelleri.
- database.py — SQLite işlemleri.
- config.json — Ayar dosyası.

---

🛠️ Geliştirici Notları

- Geliştirme ortamı: Python 3.10+
- Veritabanı: SQLite (bot_database.db)
- Kütüphaneler: discord.py, sqlite3, os, json, datetime, re

---

📌 Katkı

Pull Request'ler ve önerilere her zaman açığız.
Dilersen proje üzerinde sen de katkıda bulunabilirsin!

İletişim: aurelios_1
Discord: https://discord.gg/7sqkqRkY

---

📜 Lisans

Bu proje MIT Lisansı ile lisanslanmıştır.
Dilediğiniz gibi kullanabilir, değiştirebilir ve dağıtabilirsiniz.

---

💬 İletişim

Soru, öneri veya geri bildirim için GitHub üzerinden bizimle iletişime geçebilirsiniz.
