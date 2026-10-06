# PayTR Pazaryeri — Ödeme Bölüştürme Demosu

PayTR pazaryeri (marketplace) entegrasyonundaki ödeme akışını uçtan uca gösteren, tek dosyalık bir tarayıcı demosu.

## Ne gösteriyor

- Rezervasyon tutarının tesis ve platform arasında oranla bölüştürülmesi (canlı hesaplayıcı)
- iFrame ödeme token isteğinin **gerçek HMAC-SHA256** ile imzalanması (Web Crypto API)
- Bildirim (callback) hash'inin yeniden hesaplanıp doğrulanması. Doğrulanmayan bildirim "ödendi" sayılmaz.
- Sonuçta tesis bazlı ödeme (ledger) tablosu

## Notlar

- Tüm anahtarlar (`merchant_id`, `merchant_key`, `merchant_salt`) **TEST amaçlı sahte değerlerdir**. Gerçek bir PayTR hesabına bağlanmaz, gerçek ödeme yapılmaz.
- Hash alan sıraları yaygın bilinen iFrame API desenine göre yazılmıştır. Canlıya almadan önce güncel PayTR geliştirici dokümanıyla doğrulanmalıdır.
- Bağımlılık yok; `index.html` dosyasını tarayıcıda açmak yeterli.
