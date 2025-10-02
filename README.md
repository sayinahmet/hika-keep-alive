# 🔔 Render Keep-Alive Service

Bu repo, Render üzerindeki backend servislerimi ücretsiz planda aktif tutar.

## 🎯 Nasıl Çalışır?

GitHub Actions kullanarak **her 10 dakikada bir** backend servisime ping atar. Bu sayede Render'ın 15 dakikalık inactivity sonrası uyku moduna girme özelliği engellenir.

## 🚀 Ping Edilen Servisler

- **Backend:** https://hika-backend-bigquery.onrender.com/ping

## ⚙️ Konfigürasyon

Workflow dosyası: `.github/workflows/keep-alive.yml`

### Ping Sıklığı
Varsayılan: **Her 10 dakikada bir**

İsterseniz değiştirebilirsiniz:
```yaml
# Her 5 dakikada (daha sık)
- cron: '*/5 * * * *'

# Her 14 dakikada (limit öncesi)
- cron: '*/14 * * * *'
```

## 📊 Monitoring

- GitHub repo'nuzun **Actions** sekmesinden logları kontrol edebilirsiniz
- Her ping'in başarılı olup olmadığını görebilirsiniz
- Manuel test için "Run workflow" butonu kullanabilirsiniz

## 🔒 Güvenlik

Bu repo sadece public erişime açık bir endpoint'e ping atar. Hiçbir hassas bilgi içermez.

---

*Son güncelleme: Ekim 2025*

