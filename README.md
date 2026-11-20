# arsa — web sitesi + QR menü

```
index.html      → web sitesi (TR / EN)
menu/           → QR menü (masadaki QR'ın açtığı sayfa, sitenin içine de gömülü)
assets/         → fotoğraflar, fontlar, logo
```

Hiçbir derleme adımı yok. Klasörün tamamı GitHub Pages'e (ya da Vercel / Netlify'a) olduğu gibi yüklenir.

## QR kodlar bozulmasın

Basılı QR şu an hangi adresi açıyorsa o adreste menü açılmaya devam etmeli.

**QR, mevcut reponun ana adresini açıyorsa** (ör. `kullanici.github.io/arsa-menu/`):

1. Bu klasörü **yeni bir repoya** yükle (ya da alan adına bağla), site orada yayınlansın.
2. Eski repodaki `index.html`'i `qr-yonlendirme.html` dosyasıyla değiştir, içindeki `YENI-ADRES` kısmına sitenin adresini yaz.
   QR okutan kişi doğrudan `.../menu/` sayfasına geçer. Menü tek yerden güncellenir.

**QR zaten `.../menu/` gibi bir alt adresi açıyorsa** bu klasörü o repoya yüklemek yeterli.

## Instagram akışı

Site en son 6 gönderiyi Behold üzerinden çeker (ücretsiz plan: 6 gönderi, günde bir güncelleme, ayda 1.200 görüntülenme).

1. behold.so'da ücretsiz hesap aç, @arsacoffeeco hesabını bağla.
2. **Add Feed → JSON** ile bir akış oluştur, akış adresini kopyala (`https://feeds.behold.so/...`).
3. `index.html` içinde `const BEHOLD_FEED_URL = "";` satırına bu adresi yapıştır.

Adres boşsa ya da limit dolarsa bölüm mekân fotoğraflarını Instagram profiline bağlı olarak gösterir; sayfa boş kalmaz.

## Menüyü güncellemek

Fiyatlar ve ürünler `menu/index.html` içindeki `categories` listesinde. Sitedeki kategori bağlantıları aynı id'leri kullanır (`menu/#hot-coffee` vb.).

## Fontlar

Eyesome Script, Eyesome Regular ve Boston Angel'da ğ, ş, İ yoktu; bu harfler fontlara eklendi (`*-TR.woff2`).
Boston Angel'daki "ı" noktalıydı, düzeltildi. "st" ve i'li süs bağlantıları (noktayı yutan) kapatıldı.
