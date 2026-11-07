# Eşini Bul

2–4 kişiyle oynanan, üç zorluk seviyeli bir hafıza kartı oyunu. Tarayıcıda çalışır, kurulum gerektirmez.

**Canlı sürüm:** https://fantastic-gumdrop-6f98a9.netlify.app

## Nasıl oynanır

1. Oyuncu sayısını (2, 3 veya 4) ve zorluk seviyesini seç, istersen oyuncu adlarını değiştir.
2. Sırası gelen oyuncu iki kart açar.
3. Kartlar eşleşirse çift o oyuncunun olur ve tekrar oynar.
4. Eşleşmezse kartlar kapanır, sıra sonraki oyuncuya geçer.
5. Tüm çiftler bulununca en çok çift toplayan kazanır.

| Seviye | Tahta | Çift sayısı |
|--------|-------|-------------|
| Kolay  | 4 × 4 | 8           |
| Orta   | 6 × 6 | 18          |
| Zor    | 8 × 8 | 32          |

## Özellikler

- 2, 3 veya 4 oyuncu, her oyuncuya ayrı renk
- 22 farklı şekil × 4 renk ile oluşturulan kart yüzleri (SVG)
- Kart çevirme animasyonu (CSS 3D transform)
- Skor tablosu, sıra göstergesi, hamle sayacı ve süre
- Oyun sonu sıralama ekranı, beraberlik desteği
- Telefon, tablet ve masaüstünde çalışır
- Açık ve koyu tema desteği

## Teknik notlar

Proje tek bir `index.html` dosyasından oluşur. Harici kütüphane kullanılmaz, yalnızca HTML, CSS ve JavaScript vardır.

- **Kart karıştırma:** Fisher–Yates algoritması
- **Deste oluşturma:** Her çift için benzersiz bir (şekil, renk) kombinasyonu seçilir. Önce farklı şekiller tercih edilir.
- **Sıra mantığı:** Eşleşmede aynı oyuncu devam eder, eşleşme olmazsa sıra `(sıra + 1) % oyuncuSayısı` ile ilerler.
- **Şekiller:** Her şekil 100×100'lük bir SVG `viewBox` içinde kodla çizilir. Yıldız ve çokgenler trigonometriyle hesaplanır.

## Yerelde çalıştırma

`index.html` dosyasını herhangi bir tarayıcıda açman yeterli.

## Geliştirme süreci

Bu proje, yapay zekâ asistanı **Claude** (Anthropic) ile birlikte geliştirildi.

## Yapılacaklar

- [ ] Tek kişilik mod ve en iyi süre rekoru
- [ ] Ses efektleri
- [ ] Bilgisayara karşı oynama
- [ ] Kodu ayrı HTML / CSS / JS dosyalarına bölme
