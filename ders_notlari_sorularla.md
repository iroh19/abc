# Veri İletişimi ve Bilgisayar Ağları — Ders Notları ve Sorular

**Kaynak:** Kurose & Ross — Computer Networking: A Top-Down Approach (8. Baskı)  
**Hazırlayan:** Doç. Dr. Mehmet Dinçer Erbaş · Bolu Abant İzzet Baysal Üniversitesi  
**Kapsam:** Bölüm 1 · Bölüm 2 · Bölüm 3 + 75 Soru (3 Set)

---

> **Nasıl kullanılır?**  
> Her konu bittikten sonra o konunun soruları gelir.  
> Önce soruyu kendiniz çözün, sonra ✅ ile işaretli cevabı açıklayın.

---

# BÖLÜM 1: TANITIM

---

## 1.1 İnternet Nedir?

### İçerik Açısından

- **Milyarlarca** birbirine bağlı cihaz → **uç sistemler**
- Uç sistemler ağ uygulaması çalıştırır
- **İletişim bağları:** fiber, bakır, radyo, uydu → Bant genişliği ile ölçülür
- **Paket anahtarlama:** veriler paketlere bölünür, yönlendiriciler ve anahtarlayıcılar aracılığıyla iletilir

### Genel Yapısı (Altyapı Açısından)

- **İnternet = "ağların ağı"** → birbirine bağlı ISP'ler
- **Protokoller** mesaj gönderimini/alımını kontrol eder: TCP, IP, HTTP, 802.11
- **İnternet standartları:**
  - **RFC** (Request for Comments): standartları tanımlar
  - **IETF** (Internet Engineering Task Force): standartları belirler

### Verdiği Hizmet

- Uygulamalara hizmet veren altyapı: Web, VoIP, e-posta, oyunlar, e-ticaret…
- Uygulamalara **programlama arayüzü** sağlar (soket API)

### Protokol Nedir?

> *Protokoller ağ birimleri arasında gönderilen ve alınan mesajların yapısı ve sıralaması ile bu mesajların iletimi esnasında uygulanan aksiyonları tanımlar.*

---

## 1.2 Ağ Kenarı

**Ağ yapısı:**
- **Ağ kenarı:** cihazlar (istemci ve sunucu), veri merkezlerindeki sunucular
- **Erişim ağları / fiziksel bağlar:** kablolu, kablosuz iletişim bağları
- **Ağ çekirdeği:** birbirine bağlı yönlendiriciler

### Erişim Ağı Türleri

#### DSL (Digital Subscriber Line)
- Mevcut **telefon hattı** üzerinden bağlantı
- Her evin merkezi ofise **ayrılmış** bağlantısı
- **24–52 Mb/s** indirme, **3.5–16 Mb/s** yükleme

#### Kablo Ağı — HFC (Hibrit Fiber-Koaksiyel)
- Evler **kablo başucuna erişim ağını paylaşır**
- Frekans bölüşümlü çoğullama (FDM)
- **40 Mb/s – 1.2 Gb/s** indirme, **30–100 Mb/s** yükleme

#### Ethernet (Firma Erişim Ağı)
- Şirketler, üniversiteler
- **100 Mb/s, 1 Gb/s, 10 Gb/s**

#### Kablosuz (WiFi / Hücresel)
- WiFi (802.11b/g): 11–450 Mb/s, 30 m
- 4G/4.5G hücresel: 10'larca Mb/s, 10 km

### Fiziksel Ortam

| Ortam | Özellik |
|-------|---------|
| **Bükümlü çift** | Kat.5: 100 Mb/s–1 Gb/s; Kat.6: 10 Gb/s |
| **Koaksiyel** | Çift yönlü, geniş bant, HFC'de kullanılır |
| **Fiber optik** | 10–100'lerce Gb/s, düşük hata, EMI'dan etkilenmez |
| **Radyo** | Kablosuz, yansıma/engellemeden etkilenir |

---

### 📝 Bölüm 1.2 Soruları

**S1.** **DSL** ve **HFC** erişim teknolojileri arasındaki en temel mimari fark nedir?

- A) DSL fiber optik kullanırken HFC bakır kablo kullanır.
- B) DSL'de her evin merkezi ofise ayrılmış bağlantısı varken, HFC'de evler kablo başucuna erişim ağını paylaşır.
- C) DSL kablosuz erişim sağlarken HFC kablolu erişim sağlar.
- D) HFC simetrik hız sunarken DSL asimetrik hız sunar.

✅ **Cevap: B** — DSL "dedicated" (ayrılmış), HFC "shared" (paylaşımlı) bağlantı mimarisi kullanır. HFC'de komşular yoğun kullandığında hız düşer.

---

**S2.** **Fiber optik kablo**nun bükümlü çift ve koaksiyele göre üstünlükleri nelerdir?

- A) Düşük maliyetli ve bükmesi kolaydır.
- B) Çok yüksek iletim hızı, çok düşük hata oranı ve elektromanyetik gürültüden etkilenmemesi.
- C) Kısa mesafeli iletim için idealdir.
- D) Kablosuz bağlantı kurulumunu destekler.

✅ **Cevap: B** — Fiber ışık atımları taşır; 10–100'lerce Gb/s, EMI'dan bağışık, çoklayıcılar uzağa konulabilir. Dezavantajı: kırılgan ve pahalı.

---

## 1.3 Ağ Çekirdeği

### Paket Anahtarlama

- Mesajlar **paketlere** bölünür, yönlendiriciden yönlendiriciye iletilir
- **Sakla-ve-yolla:** paket tamamen gelene kadar iletilmez
  - **d_iletim = L/R** (L bit, R bps)
  - N bağ → toplam iletim = N × L/R

### Paket Anahtarlama: Sıralanma ve Kayıp

- Geliş hızı > çıkış hızı → **kuyruk** oluşur
- Önbellek (buffer) dolarsa → **paket düşürülür (kayıp)**

### İki Temel Çekirdek Fonksiyon

- **Yönlendirme (Routing):** kaynaktan hedefe giden yolu belirler → yönlendirme algoritması
- **Yollama (Forwarding):** paketi giriş porttan doğru çıkış porta taşır

### Devre Anahtarlama

- Uçtan uca kaynaklar **önceden rezerv edilir**
- **Garanti** edilen performans, ama boşa giden kapasite
- Telefon ağlarında kullanılır

### FDM vs TDM

| | FDM | TDM |
|-|-----|-----|
| Paylaşım | Frekans bantları | Zaman dilimleri |
| Kullanım | Sürekli, kendi bandında | Sırayla, tam band |
| Ortak sorun | Boş kaynak başkasına verilemez |

### Paket Anahtarlama vs Devre Anahtarlama

- **Örnek:** 1 Mb/s bağ, kullanıcı aktifken 100 kb/s, %10 aktif
  - Devre anahtarlama: **max 10 kullanıcı**
  - Paket anahtarlama (35 kullanıcı): 11+ aktif olma ihtimali < 0.0004

### ISP Hiyerarşisi

```
Tabaka-1 ISP (Level 3, Sprint, AT&T, NTT) — ulusal/uluslararası
    └── Bölgesel ISP
            └── Erişim ISP
                    └── Uç Sistemler
```
- İçerik sağlayıcı ağları (Google, Akamai): Tabaka-1/bölgesel ISP'leri atlayabilir

---

### 📝 Bölüm 1.3 Soruları

**S3.** **Paket anahtarlamanın** devre anahtarlamaya göre en önemli avantajı nedir?

- A) Uçtan uca gecikme garantisi sağlar.
- B) Kaynaklar önceden rezerv edilir.
- C) Ağ kaynaklarını paylaşarak daha fazla kullanıcıya hizmet verebilir.
- D) Ses ve görüntü için daha uygundur.

✅ **Cevap: C** — İstatistiksel çoğullama sayesinde aynı bağı çok daha fazla kullanıcı paylaşabilir. Devre anahtarlamada kaynak boşta bile başkasına verilemez.

---

**S4.** Bir paket, **1 Mb/s** kapasiteli **2 bağ** üzerinden **3 Mb** boyutunda ve **1 ara yönlendirici** ile iletilmektedir (yayılma gecikmesi sıfır). Toplam iletim gecikmesi kaçtır? *(Sakla-ve-yolla)*

- A) 3 saniye
- B) 6 saniye
- C) 1.5 saniye
- D) 9 saniye

✅ **Cevap: B** — d = N × L/R = 2 × (3 Mb / 1 Mb/s) = **6 saniye**. Her bağda paketin tamamı iletilmeli.

---

**S5.** **Tabaka-1 (Tier-1) ISP**'nin temel özelliği nedir?

- A) Yalnızca ev kullanıcılarına hizmet verir.
- B) Ulusal ve uluslararası kapsama sahip; başka ISP'ye ücret ödemeden her yere ulaşır.
- C) Yalnızca içerik sağlayıcılara hizmet verir.
- D) Tabaka-2 ISP'leri tarafından yönetilir.

✅ **Cevap: B** — Tier-1 ISP'ler peering anlaşmalarıyla birbirine bağlıdır ve transit ücret ödemezler. Örnek: Level 3, Sprint, AT&T, NTT.

---

**S6.** Devre anahtarlamada **FDM** ile **TDM** arasındaki fark nedir?

- A) FDM dijital, TDM analog sinyaller için kullanılır.
- B) FDM'de ayrı frekans bandı; TDM'de ayrı zaman dilimleri ayrılır.
- C) TDM daha yüksek bant genişliği sunar.
- D) FDM yalnızca kablolu, TDM yalnızca kablosuz ağlarda kullanılır.

✅ **Cevap: B** — FDM: her bağlantı sürekli kendi frekans bandını kullanır. TDM: her bağlantı periyodik zaman dilimleriyle tam bant genişliğini kullanır.

---

**S7.** **Paket anahtarlama** her zaman devre anahtarlamadan iyi midir?

- A) Evet, her koşulda daha iyidir.
- B) Hayır; patlamalı veri akışı için üstündür, ama ses/görüntü gibi bant genişliği garantisi gerektiren uygulamalar için zayıf kalabilir.
- C) Hayır; devre anahtarlama her zaman daha iyidir.
- D) Evet, sıkışma kontrolü ile her durumda daha iyidir.

✅ **Cevap: B** — Paket anahtarlama patlamalı trafikte çok verimli; ama gerçek zamanlı ses/video için gecikme garantisi vermez (hâlâ çözülmemiş bir problem).

---

## 1.4 Ağlarda Gecikme, Kayıp, İş Hacmi

### Dört Gecikme Kaynağı

```
d_düğüm = d_işlem + d_sıralanma + d_iletim + d_yayılma
```

| Bileşen | Açıklama | Formül |
|---------|----------|--------|
| **d_işlem** | Bit hata kontrolü, çıkış bağına karar | < msec |
| **d_sıralanma** | Çıkış bağını bekleme | Yük bağlı |
| **d_iletim** | Tüm bitleri bağa basmak | L/R |
| **d_yayılma** | Bitin fiziksel ortamda ilerlemesi | d/v |

### Sıralanma Gecikmesi ve Trafik Yoğunluğu

- **La/R** = trafik yoğunluğu (L: bit, a: varış hızı, R: kapasite)
  - La/R ≈ 0 → gecikme küçük
  - La/R → 1 → gecikme büyür
  - **La/R > 1 → sonsuz gecikme, paket kaybı**

### Traceroute

- Kaynaktan hedefe her yönlendiricinin gecikmesini ölçer
- Her yönlendiriciye TTL değeri artırılmış 3 paket gönderilir
- `* * *` → yönlendirici yanıt vermiyor

### Paket Kaybı

- Önbellek (buffer) dolarsa gelen paketler **düşürülür**
- Kayıp olan paket kaynak tarafından tekrar iletilebilir

### İş Hacmi (Throughput)

- **Anlık:** belirli zamandaki bit/sn
- **Ortalama:** uzun süredeki bit/sn
- **Darboğaz bağ:** uçtan uca iş hacmini kısıtlayan bağlantı
  - Uçtan uca iş hacmi = **min(R_c, R_s, R/N)**

---

### 📝 Bölüm 1.4 Soruları

**S8.** Paket iletim gecikmesi formülü hangisidir? *(L = paket boyutu bit, R = kapasite bps)*

- A) d = R / L
- B) d = L × R
- C) d = L / R
- D) d = L + R

✅ **Cevap: C** — d_iletim = L(bit) / R(bit/sn) = saniye. Örnek: 8000 bit / 10⁹ bps = 8 μs.

---

**S9.** Trafik yoğunluğu **La/R > 1** olduğunda ne gerçekleşir?

- A) Sıralanma gecikmesi sıfıra yaklaşır.
- B) Ortalama sıralanma gecikmesi sonsuza gider; sisteme giren iş miktarı servis edilebilecekten fazladır.
- C) Paket iletim hızı maksimuma ulaşır.
- D) Yönlendirici otomatik yük dengelemesi yapar.

✅ **Cevap: B** — Gelen > giden → kuyruk sonsuza büyür. La/R=1'e yaklaştıkça gecikme hızla artar; La/R>1'de sistem doyuma ulaşır.

---

**S10.** Aşağıdakilerden hangisi dört gecikme bileşeninden **biri değildir**?

- A) İşlem gecikmesi
- B) Sıralanma gecikmesi
- C) Şifreleme gecikmesi
- D) Yayılma gecikmesi

✅ **Cevap: C** — Dört bileşen: d_işlem + d_sıralanma + d_iletim + d_yayılma. Şifreleme ayrı bir bileşen olarak tanımlanmaz.

---

**S11.** **Darboğaz bağ** ne anlama gelir?

- A) En yüksek bant genişliğine sahip bağlantı.
- B) Uçtan uca yol üzerinde iş hacmini kısıtlayan bağlantı.
- C) Yalnızca kablosuz ağlarda oluşan tıkanma noktası.
- D) Yönlendiricinin hafızasının dolduğu andaki bağlantı durumu.

✅ **Cevap: B** — min(R_c, R_s, R/N) — en küçük kapasite darboğazı oluşturur ve tüm uçtan uca iş hacmini sınırlar.

---

**S12.** Bir sinyal **2500 km** fiber optik üzerinde **2×10⁸ m/s** hızla ilerliyor. Yayılma gecikmesi kaçtır?

- A) 2.5 ms
- B) 12.5 ms
- C) 25 ms
- D) 125 ms

✅ **Cevap: B** — d_yayılma = 2,500,000 m / (2×10⁸ m/s) = 0.0125 s = **12.5 ms**. Birim dönüşümüne dikkat: km → m.

---

**S13.** `traceroute` komutu ne ölçer ve nasıl çalışır?

- A) Sunucunun eşzamanlı bağlantı kapasitesini ölçer.
- B) Kaynaktan hedefe her yönlendiricideki gecikmeyi ölçer; TTL değeri kademeli artırılmış 3'er paket gönderilir.
- C) Ağdaki tüm cihazların IP adreslerini listeler.
- D) Paket kayıp oranını hesaplar.

✅ **Cevap: B** — Her yönlendirici TTL=0 olan paketi düşürüp ICMP hata mesajı döner; gönderici gidiş-dönüş süresini hesaplar.

---

## 1.5 Protokol Katmanları ve Hizmet Modelleri

### Neden Katmanlama?

- Karmaşık sistemi yönetmek için
- **Modüler yapı:** bir katmandaki değişiklik diğerini etkilemez
- Belirgin yapı → parçaların ilişkilerini tanımlar

### TCP/IP 5 Katman Modeli

| Katman | Protokol | Birim |
|--------|----------|-------|
| **Uygulama** | FTP, SMTP, HTTP | Mesaj |
| **Taşıma** | TCP, UDP | Segment |
| **Ağ** | IP, yönlendirme protokolleri | Datagram |
| **Veri Bağlantı** | Ethernet, WiFi, PPP | Çerçeve |
| **Fiziksel** | — | Bit |

### OSI 7 Katman Modeli

TCP/IP'ye ek olarak:
- **Sunum katmanı:** şifreleme, sıkıştırma, format çevirisi
- **Oturum katmanı:** senkronizasyon, denetim noktası

→ İnternet modelinde bu iki katman **uygulama katmanına dahil edilmiştir.**

### Kapsülleme (Encapsulation)

```
Uygulama:     [Mesaj]
Taşıma:       [Th | Mesaj]          → Segment
Ağ:           [Nh | Th | Mesaj]     → Datagram
Veri Bağlantı:[Dh | Nh | Th | Mesaj]→ Çerçeve
Fiziksel:     010101...             → Bit dizisi
```

---

### 📝 Bölüm 1.5 Soruları

**S14.** **Taşıma katmanının** görevi nedir?

- A) Paketleri fiziksel olarak taşımak.
- B) Farklı cihazlardaki uygulamalar (işlemler) arasında uçtan uca mantıksal iletişim sağlamak.
- C) Bitleri elektrik sinyaline çevirmek.
- D) IP adreslerini MAC adreslerine dönüştürmek.

✅ **Cevap: B** — Taşıma: işlem↔işlem (uçtan uca). Ağ: cihaz↔cihaz. Fiziksel: bit iletimi. Ev benzetmesi: ağ=posta servisi, taşıma=ev içinde mektup dağıtımı.

---

**S15.** OSI modelinde **İnternet modelinde yer almayan** iki katman hangisidir?

- A) Fiziksel ve Veri Bağlantı
- B) Sunum ve Oturum
- C) Ağ ve Taşıma
- D) Uygulama ve Fiziksel

✅ **Cevap: B** — OSI'nin Sunum ve Oturum katmanları TCP/IP'de uygulama katmanına gömülüdür. Gerekirse uygulama kendisi bu hizmetleri sağlar.

---

**S16.** **Kapsülleme (encapsulation)** sürecini doğru tanımlayan ifade hangisidir?

- A) Mesaj doğrudan fiziksel katmana iletilir.
- B) Her katman üstten gelen veriye kendi başlık bilgisini ekler; fiziksel katmanda bit dizisine dönüşür.
- C) Yalnızca uygulama katmanı başlık ekler.
- D) Kapsülleme yalnızca alıcı tarafında gerçekleşir.

✅ **Cevap: B** — Gönderici: her katman başlık ekler (kapsüller). Alıcı: her katman kendi başlığını söker (decapsulation). Modülerlik sayesinde her katman yalnızca kendi başlığını görür.

---

## 1.6 Ağ Güvenliği

### Temel Saldırı Türleri

#### Zararlı Yazılım (Malware)
- **Virüs:** zararlı nesneyi alma/çalıştırma ile bulaşır (kendini çoklar)
- **Worm:** kendi kendini çalıştıran nesneyi alarak yayılır
- **Botnet:** enfekte cihazlar spam/DDoS için kullanılır

#### DoS / DDoS Saldırısı
1. Hedef seç
2. Ağdaki cihazlara sız (botnet oluştur)
3. Hedef üzerine yoğun sahte trafik gönder → kaynak tükenir

#### Paket Yoklayıcı (Sniffer)
- Paylaşımlı ortamda geçen paketleri dinler/kaydeder (şifreler dahil)
- **Wireshark** ücretsiz bir sniffer aracıdır

#### IP Yanıltma (IP Spoofing)
- Sahte gönderici IP adresi içeren paketler gönderilir
- Kimlik gizleme veya yansıma saldırıları için kullanılır

---

### 📝 Bölüm 1.6 Soruları

**S17.** **DoS (Denial of Service)** saldırısının doğru tanımı hangisidir?

- A) Saldırgan ağ üzerinden geçen paketleri sessizce dinler.
- B) Saldırgan sahte IP adresi kullanarak farklı bir cihaz gibi görünür.
- C) Saldırgan aşırı sahte trafik göndererek hedef kaynağa erişimi engeller.
- D) Saldırgan zararlı yazılımı e-posta eki olarak yayar.

✅ **Cevap: C** — DoS: botnet üzerinden hedefe yoğun trafik → kaynak tükenir → meşru kullanıcılar erişemez. DDoS, dağıtık kaynaktan aynı saldırıdır.

---

**S18.** **IP yanıltma (IP spoofing)** saldırısında ne yapılır?

- A) DNS sunucusuna sahte kayıtlar eklenir.
- B) Ağ üzerindeki paketler dinlenerek şifreler çalınır.
- C) Sahte gönderici IP adresi içeren paketler gönderilerek başka bir cihaz gibi görünülür.
- D) Yönlendiricinin yönlendirme tablosu bozulur.

✅ **Cevap: C** — IP Spoofing: paket başlığındaki kaynak IP manipüle edilir. Savunma: ingress filtering (giriş filtreleme).

---

## 1.7 İnternetin Kısa Tarihçesi

| Dönem | Gelişme |
|-------|---------|
| 1961–1972 | Kleinrock sıralanma teorisi; ARPAnet; ilk e-posta |
| 1972–1980 | Cerf & Kahn TCP/IP mimarisi; Ethernet (Xerox PARC) |
| 1980–1990 | TCP/IP geçişi (1983); DNS (1983); SMTP (1982) |
| 1990–2000 | ARPAnet kapandı; Web (HTML/HTTP, Berners-Lee); Mosaic/Netscape |
| 2005–günümüz | Milyarlarca cihaz; 4G/5G; sosyal ağlar; bulut bilişim |

---

# BÖLÜM 2: UYGULAMA KATMANI

---

## 2.1 Ağ Uygulamalarının Prensipleri

### Uygulama Mimarileri

#### İstemci-Sunucu
- **Sunucu:** her zaman açık, sabit IP, veri merkezi
- **İstemci:** aralıklı bağlantı, dinamik IP, birbirleriyle direk iletişim kurmaz

#### P2P (Peer-to-Peer)
- Her zaman açık sunucu yok
- Uç sistemler direk haberleşir
- **Öz ölçeklenebilirlik:** her yeni üye hem kapasite tüketir hem kapasite ekler

### Soketler ve Adresleme

- **Soket:** işlemler arası kapı — gönderici mesajı sokete yollar, altta TCP/UDP taşır
- İşlemi tanımlamak için: **IP adresi + Port numarası**
  - HTTP: 80 · HTTPS: 443 · SMTP: 25 · FTP: 21 · DNS: 53

### Taşıma Hizmeti İhtiyaçları

| Uygulama | Kayıp | İş Hacmi | Zamanlama |
|----------|-------|----------|-----------|
| Dosya transferi | Yok | Elastik | Hayır |
| Gerçek-zaman ses/video | Tolere | 5 kbps–5 Mbps | Evet (<100 ms) |
| İnteraktif oyunlar | Tolere | Birkaç kbps | Evet (<100 ms) |
| E-posta | Yok | Elastik | Hayır |

### TCP ve UDP

| | TCP | UDP |
|-|-----|-----|
| Güvenilirlik | **Var** | Yok |
| Akış kontrolü | **Var** | Yok |
| Sıkışma kontrolü | **Var** | Yok |
| Bağlantı | **Gerekli** (3-yönlü) | Yok |
| Hız | Daha yavaş | **Daha hızlı** |

### SSL/TLS

- TCP ve UDP başlı başına şifreleme sağlamaz
- **SSL:** uygulama katmanında çalışır → şifrelenmiş TCP bağlantısı
- HTTPS = HTTP + SSL (port 443)

---

### 📝 Bölüm 2.1 Soruları

**S19.** Bir işlemi benzersiz tanımlamak için **IP adresi yeterli midir?**

- A) Evet, IP adresi tek başına yeterlidir.
- B) Hayır; hem IP adresi hem de **port numarası** gereklidir — aynı cihazda birden fazla işlem çalışabilir.
- C) Hayır; IP adresi yerine yalnızca MAC adresi kullanılmalıdır.
- D) Hayır; IP, port ve protokol adı üçü birlikte gereklidir.

✅ **Cevap: B** — IP adresi cihazı, port numarası cihaz üzerindeki işlemi tanımlar. Soket = IP + Port.

---

**S20.** **SSL** ile ilgili doğru ifade hangisidir?

- A) SSL, TCP'nin yerini alan yeni bir taşıma protokolüdür.
- B) SSL uygulama katmanında çalışır; uygulamalar SSL kütüphaneleri aracılığıyla şifrelenmiş TCP bağlantısı kurar.
- C) SSL yalnızca UDP üzerinde çalışabilir.
- D) SSL şifreleme yerine yalnızca veri sıkıştırma sağlar.

✅ **Cevap: B** — SSL/TLS uygulama katmanı kütüphanesidir. TCP değişmez; SSL TCP üstüne şifreleme, bütünlük ve kimlik doğrulama ekler.

---

**S21.** Aşağıdaki uygulama-protokol eşleştirmelerinden hangisi **yanlıştır?**

- A) DNS → UDP
- B) HTTP → TCP
- C) SMTP → TCP
- D) FTP → UDP

✅ **Cevap: D** — FTP dosya transferi için güvenilirlik gerektirir, bu yüzden **TCP** kullanır (port 21 kontrol, port 20 veri). DNS küçük sorgular için UDP kullanır.

---

## 2.2 Web ve HTTP

### HTTP Genel Bakış

- **HTTP:** HyperText Transfer Protocol — Web'in uygulama katmanı protokolü
- **TCP** üzerinde çalışır, port **80**
- **Durumsuz (stateless):** sunucu önceki istekleri hatırlamaz
- Web sayfası = nesnelerden oluşur; her nesne URL ile erişilir

### Kalıcı Olmayan vs Kalıcı HTTP

| | Kalıcı Olmayan | Kalıcı |
|-|---------------|--------|
| TCP bağlantısı | Her nesne için yeni | Aynı bağlantı devam |
| Yanıt süresi | **2 GDS + T** (her nesne) | ~**1 GDS** (ilk hariç) |
| Sorun | Her bağlantı için OS yükü | — |

### HTTP İstek Mesajı

```
GET /index.html HTTP/1.1\r\n
Host: www.example.com\r\n
\r\n
```

#### Metotlar

| HTTP/1.0 | HTTP/1.1 ekleri |
|---------|----------------|
| GET, POST, HEAD | + PUT (yükle), DELETE (sil) |

- **GET:** veri URL'ye eklenir
- **POST:** veri mesaj gövdesinde
- **HEAD:** yanıtta nesne gönderilmez; yalnızca başlık

### HTTP Yanıt Durum Kodları

| Kod | Anlam |
|-----|-------|
| **200 OK** | Başarılı |
| **301 Moved Permanently** | Taşındı |
| **304 Not Modified** | Önbellek güncel, nesne gönderilmedi |
| **400 Bad Request** | Anlaşılamadı |
| **404 Not Found** | Nesne yok |
| **505 HTTP Version Not Supported** | |

### Çerezler (Cookies)

4 bileşen:
1. HTTP **yanıt** mesajındaki `Set-Cookie` başlığı
2. HTTP **istek** mesajındaki `Cookie` başlığı
3. İstemcideki **çerez dosyası**
4. Sunucudaki **geri-uç veritabanı**

### Web Önbelleği (Proxy/Vekil Sunucu)

- Amaç: istemci isteğini hedef sunucuya iletmeden karşılamak
- **Koşullu GET:** `If-Modified-Since` başlığı ile önbellek güncelliği kontrol edilir
  - Güncel → **304 Not Modified** (nesne gönderilmez)

---

### 📝 Bölüm 2.2 Soruları

**S22.** **HTTP** ile ilgili hangisi **yanlıştır?**

- A) HTTP TCP üzerinde çalışır, port 80.
- B) HTTP durum bilgisi saklayan (stateful) bir protokoldür.
- C) Kalıcı olmayan HTTP'de her nesne için ayrı TCP bağlantısı açılır.
- D) HTTP istemci-sunucu mimarisini kullanır.

✅ **Cevap: B** — HTTP **durumsuz (stateless)**'tır. Sunucu önceki istekleri hatırlamaz. Durum takibi için çerezler kullanılır — ama bu HTTP'yi stateful yapmaz.

---

**S23.** Kalıcı olmayan HTTP ile **bir nesne** almak için gereken süre?

- A) GDS + T
- B) 2 × GDS + T
- C) 3 × GDS + T
- D) T

✅ **Cevap: B** — 1. GDS: TCP bağlantı kurulumu, 2. GDS: HTTP istek/yanıt, T: dosya iletimi. Kalıcı HTTP'de sonraki nesneler ~1 GDS.

---

**S24.** **GET** ile **POST** arasındaki fark nedir?

- A) GET yalnızca HTTP/1.1'de, POST HTTP/1.0'da kullanılır.
- B) GET ile veri URL'ye eklenir; POST ile veri mesaj gövdesinde gönderilir.
- C) GET güvenli bağlantı gerektirir.
- D) GET sunucudan dosya siler, POST yükler.

✅ **Cevap: B** — GET: `?q=ağlar` şeklinde URL'de görünür, önbelleklenebilir. POST: gövdede taşınır, form verileri ve yüklemeler için kullanılır.

---

**S25.** HTTP **çerez mekanizması** kaç bileşenden oluşur?

- A) 2  B) 3  **C) 4**  D) 5

✅ **Cevap: C** — (1) yanıt mesajında Set-Cookie, (2) istek mesajında Cookie, (3) istemcideki çerez dosyası, (4) sunucudaki veritabanı.

---

**S26.** **Vekil sunucu (proxy)** kullanımının temel amacı nedir?

- A) HTTP bağlantılarını şifrelemek.
- B) İstemci isteklerini hedef sunucuya iletmeden karşılamak; yanıt süresini kısaltmak ve erişim bağı trafiğini azaltmak.
- C) DNS sorgularını hızlandırmak.
- D) Sunucu kimlik doğrulamasını güçlendirmek.

✅ **Cevap: B** — %40 isabet oranıyla bile önbellek olmadan 10 kat hızlı internet almaktan daha ucuz ve hızlı sonuç verebilir.

---

**S27.** HTTP **304 Not Modified** durum kodu ne anlama gelir?

- A) İstek başarılı, nesne yanıt içinde.
- B) İstenen nesne bulunamadı.
- C) Önbellekteki kopya güncel; sunucu nesneyi tekrar göndermedi.
- D) HTTP versiyonu desteklenmiyor.

✅ **Cevap: C** — Koşullu GET mekanizmasının çıktısıdır. `If-Modified-Since` başlığı gönderilir; nesne değişmemişse sunucu 304 döner, bant genişliği tasarruf edilir.

---

**S28.** **Koşullu GET** hangi başlık alanını kullanır?

- A) Authorization
- B) If-Modified-Since
- C) Accept-Language
- D) Keep-Alive

✅ **Cevap: B** — `If-Modified-Since: <tarih>` ile önbelleğin tarihi bildirilir. Nesne değişmişse 200+nesne, değişmemişse 304 (nesne yok) yanıtı gelir.

---

**S29.** HTTP **HEAD** metodunun amacı nedir?

- A) HEAD yalnızca HTTP/2.0'da desteklenir.
- B) Sunucu nesnenin kendisini göndermez; yalnızca başlık satırlarını döner. Nesnenin varlığını/değişimini kontrol etmek için kullanılır.
- C) HEAD dosya yüklemek için kullanılır.
- D) HEAD ve GET arasında fark yoktur.

✅ **Cevap: B** — HEAD ile nesne boyutu, son değişim tarihi veya varlığı öğrenilebilir. Nesneyi indirmeden meta bilgi alınır.

---

**S30.** Erişim bağı **15 Mb/s**, ort. nesne **1 Mb**, saniyedeki istek **9**, vekil sunucu isabet oranı **%60**. Erişim bağı kullanım oranı nedir?

- A) %90  B) %60  C) %36  **D) %24**

✅ **Cevap: D** — Bağa giden trafik = (1−0.60) × 9 Mb/s = 3.6 Mb/s. Kullanım = 3.6 / 15 = **%24**. İsabet oranını ≠ kullanım oranı! Önce kalan trafiği hesapla.

---

## 2.3 FTP

### Temel Özellikler

- Uzak cihaza dosya transferi; port **21** (kontrol), ayrı port (veri)
- **İki ayrı bağlantı:**
  - **Kontrol bağlantısı (port 21):** komutlar — "bant dışı"
  - **Veri bağlantısı:** her transfer için yeni bağlantı açılır
- **Durum bilgisi saklar:** mevcut klasör, kullanıcı oturumu

### FTP Komutları

| Komut | Açıklama |
|-------|----------|
| USER | Kullanıcı adı |
| PASS | Şifre |
| LIST | Dosya listesi |
| RETR | Dosya al |
| STOR | Dosya gönder |

### FTP Dönüş Kodları

- 331: Username OK, password required
- 125: Transfer başlıyor
- 425: Veri bağlantısı açılamadı
- 452: Dosya yazma hatası

---

### 📝 Bölüm 2.3 Sorusu

**S31.** **FTP** ile ilgili doğru ifade hangisidir?

- A) FTP kontrol ve veri için tek TCP bağlantısı kullanır.
- B) FTP kontrol bağlantısını port 21, veri bağlantısını ayrı bir port üzerinden sağlar ve durum bilgisi saklar.
- C) FTP UDP tabanlıdır.
- D) FTP durumsuz bir protokoldür.

✅ **Cevap: B** — FTP iki bağlantılıdır. HTTP'den farkı: FTP durum bilgisi saklar (mevcut klasör, oturum). HTTP durumsuz, FTP durum bilgili.

---

## 2.4 Elektronik Posta

### Üç Ana Parça

1. **Kullanıcı Aracı (UA):** posta okuyucu (Outlook, Thunderbird…)
2. **Posta Sunucusu:** posta kutusu, mesaj sırası
3. **SMTP:** posta sunucuları arası aktarım protokolü

### SMTP

- TCP kullanır, port **25**
- **İtme (push)** protokolü — gönderici sunucuya aktarır
- 7-bit ASCII mesaj formatı
- Mesaj sonu: `CRLF.CRLF`

**Komut sırası:**
```
HELO → MAIL FROM → RCPT TO → DATA → (içerik) → . → QUIT
```

### SMTP vs HTTP

| | SMTP | HTTP |
|-|------|------|
| Yön | **İtme** (push) | **Çekme** (pull) |
| Port | 25 | 80 |
| Format | 7-bit ASCII zorunlu | Her şey |
| Nesne | Çok-parçalı mesajda | Her nesne ayrı yanıtta |

### E-posta Alım Protokolleri

| Protokol | Özellik |
|----------|---------|
| **POP3** | İndir-ve-sil; durumsuz; port 110 |
| **IMAP** | Sunucuda sakla; klasörler; oturumlar arası durum; port 143 |
| **HTTP** | Gmail, Hotmail gibi web tabanlı |

---

### 📝 Bölüm 2.4 Soruları

**S32.** **SMTP** ile **HTTP** arasındaki en temel fark nedir?

- A) SMTP güvenilir, HTTP güvenilmez.
- B) SMTP bir itme (push) protokolüdür; HTTP çekme (pull) protokolüdür.
- C) HTTP port 25, SMTP port 80 kullanır.
- D) SMTP UDP, HTTP TCP kullanır.

✅ **Cevap: B** — SMTP: gönderici aktif olarak sunucuya iter. HTTP: istemci sunucudan çeker. İkisi de TCP, ikisi de ASCII komut/yanıt, ikisi de durum kodları kullanır.

---

**S33.** SMTP komutlarının doğru sırası hangisidir?

- A) DATA → HELO → MAIL FROM → RCPT TO → QUIT
- B) HELO → MAIL FROM → RCPT TO → DATA → (içerik) → `.` → QUIT
- C) MAIL FROM → HELO → DATA → RCPT TO → QUIT
- D) RCPT TO → MAIL FROM → HELO → DATA → QUIT

✅ **Cevap: B** — Hatırlatıcı: Selamlama(HELO) → Kimden(MAIL FROM) → Kime(RCPT TO) → İçerik(DATA) → Bitti(.) → Çıkış(QUIT).

---

**S34.** Ayşe `ayse@gmail.com`'dan Ali'ye `ali@hotmail.com`'a mail gönderiyor. Süreçte hangi protokoller devreye girer?

- A) Yalnızca SMTP, tek aşamada.
- B) UA → SMTP → Ayşe sunucusu → SMTP → Ali sunucusu → POP3/IMAP/HTTP → Ali UA. En az 2 farklı protokol devreye girer.
- C) FTP ile gönderilir, SMTP bildirim içindir.
- D) Tüm süreç HTTP üzerinden gerçekleşir.

✅ **Cevap: B** — SMTP itme yönünde (gönderme), POP3/IMAP/HTTP çekme yönünde (okuma) çalışır. Gönderici sunucudan alıcı sunucuya da SMTP kullanılır.

---

**S35.** **POP3** ile **IMAP** arasındaki en önemli fark nedir?

- A) POP3 TCP, IMAP UDP kullanır.
- B) POP3 mesajları sunucudan indirip siler; IMAP mesajları sunucuda saklar ve klasör durumunu korur.
- C) IMAP yalnızca web tarayıcısıyla kullanılabilir.
- D) POP3 şifrelenmiş iletişim sağlar, IMAP sağlamaz.

✅ **Cevap: B** — IMAP birden fazla cihazda aynı e-posta kutusuna erişimi sağlar. POP3 "indir-sil" ile cihaza bağımlı. Modern kullanımda IMAP/HTTP tercih edilir.

---

## 2.5 DNS — Domain Name System

### Neden DNS?

- İnsanlar isim kullanır (`www.google.com`), makineler IP kullanır
- DNS: **dağınık, hiyerarşik** isim→IP çeviri veritabanı

### Hiyerarşi

```
Kök sunucular (13 küme, dünya genelinde dağıtık)
    └── TLD sunucuları (.com, .org, .edu, .tr …)
            └── Yetkili DNS sunucuları (google.com, amazon.com …)
                    └── Yerel DNS sunucuları (ISP, üniversite)
```

### DNS Hizmetleri

- Cihaz adı → IP adresi çevirisi
- Cihaz paylaşımlama (alias): kanonik ↔ takma isim
- Posta sunucusu paylaşımlama
- Yük dağıtımı (bir isme birden fazla IP)

### DNS Kayıt Türleri (KK formatı: isim, değer, tip, ys)

| Tip | isim | değer |
|-----|------|-------|
| **A** | Cihaz adı | IP adresi |
| **NS** | Alan adı | Yetkili isim sunucusunun adı |
| **CNAME** | Takma ad | Kanonik (gerçek) isim |
| **MX** | Alan adı | Posta sunucusunun cihaz adı |

### Sorgu Türleri

**Döngüsel (Iterative):** Her sunucu "bilmiyorum, şuna sor" der; yerel DNS hiyerarşide gezer.  
**Yinelenmeli (Recursive):** Sunucu tam çözümü yapıp döner; üst sunuculara yük bindirir.

### DNS Önbellekleme ve TTL

- Öğrenilen eşleme **TTL süresi** boyunca önbelleklenir
- TTL dolunca silinir; IP değişirse eski TTL dolana kadar bilinmeyebilir

### Neden Merkezi DNS Yok?

1. Tek nokta arızası tüm sistemi durdurur
2. Trafik hacmi yönetilemez
3. Uzak merkezi veritabanı → yüksek gecikme
4. Bakım zorluğu

---

### 📝 Bölüm 2.5 Soruları

**S36.** DNS **merkezi** tek sunucu yerine hiyerarşik yapı kullanır çünkü:

- A) Merkezi yapı kurulumu çok pahalıdır.
- B) Tek nokta arızası tüm sistemi durdurur, trafik yönetilemez, bakım zorlaşır.
- C) Hiyerarşik yapı şifrelemeyi kolaylaştırır.
- D) Merkezi DNS yasal düzenlemeler nedeniyle yasaktır.

✅ **Cevap: B** — 4 temel sorun: tek nokta arızası, trafik hacmi, uzak veri, bakım. Bu nedenle DNS dağıtık ve hiyerarşik tasarlanmıştır.

---

**S37.** DNS kayıt türü **MX** ne anlama gelir?

- A) Cihaz adını IP adresine eşler.
- B) Yetkili isim sunucusunu gösterir.
- C) Alan adına karşılık gelen posta sunucusunun cihaz adını tutar.
- D) Takma adı kanonik isme eşler.

✅ **Cevap: C** — MX: `google.com` → `mail.google.com` → A kaydı → IP. E-posta sistemi MX kaydına bakarak doğru posta sunucusunu bulur.

---

**S38.** DNS **TTL** değerinin önemi nedir?

- A) Paketin kaç yönlendirici geçebileceğini sınırlar.
- B) Önbelleklenmiş DNS kaydının ne kadar süre geçerli kalacağını belirler; süre dolunca kayıt silinir.
- C) DNS sorgusunun cevap vermesi için beklenen max süreyi tanımlar.
- D) DNS sunucusunun ne kadar çevrimiçi kalacağını gösterir.

✅ **Cevap: B** — TTL dolunca önbellek silinir ve yeni sorgu yapılır. IP değişimlerinde eski TTL boyunca eski IP erişilebilir kalabilir.

---

**S39.** **Döngüsel** ve **yinelenmeli** DNS sorgusu arasındaki fark nedir?

- A) Döngüsel sorguda yerel DNS tüm işi yapıp cevabı döner; yinelenmeli sorguda her sunucu sonrakinin adresini söyler.
- B) Yinelenmeli sorguda yerel DNS tüm çözümlemeyi yapıp cevabı döner; döngüsel sorguda her sunucu sonrakinin adresini söyler.
- C) İkisi arasında fark yoktur.
- D) Döngüsel sorgu yalnızca kök sunucular tarafından kullanılır.

✅ **Cevap: B** — Döngüsel (iterative): yerel DNS hiyerarşide dolaşır. Yinelenmeli (recursive): her sunucu tam çözümü bir alt sunucuya yaptırır → üst sunuculara yük.

---

**S40.** `www.amazon.com` için döngüsel DNS sorgusunun doğru sırası?

- A) Yerel DNS → Yetkili DNS → TLD → Kök
- B) Yerel DNS → Kök DNS → .com TLD → amazon.com Yetkili DNS → Yerel DNS → İstemci
- C) İstemci → Yetkili DNS → İstemci
- D) Yerel DNS → TLD → Yerel DNS → İstemci

✅ **Cevap: B** — Yerel DNS kök → TLD → yetkili sunucu sırasıyla sorar, cevabı önbellekler ve istemciye iletir.

---

**S41.** **DNS zehirleme (poisoning)** saldırısı nasıl gerçekleşir?

- A) DNS sunucusuna fazla sorgu gönderilerek çevrimdışı bırakılır.
- B) Saldırgan DNS sunucusuna sahte kayıtlar yerleştirir; sunucu önbellekler, kullanıcılar yanlış IP'ye yönlendirilir.
- C) DNS trafiği dinlenerek şifreler çalınır.
- D) TTL değerleri manipüle edilerek önbellek doldurulur.

✅ **Cevap: B** — DNS zehirleme → phishing siteleri için kullanılır. Savunma: DNSSEC (dijital imzalı kayıtlar).

---

## 2.6 P2P Uygulamaları

### İstemci-Sunucu vs P2P Dağıtım Süresi

**İstemci-Sunucu:**
```
D(c-s) = max { NF/u_s , F/d_min }
→ N büyüdükçe doğrusal artar
```

**P2P:**
```
D(P2P) = max { F/u_s , F/d_min , NF/(u_s + Σu_i) }
→ Her yeni üye kapasite ekler → çok daha yavaş büyür
```

### BitTorrent

- Dosya **256 Kb parçalara** bölünür
- İzleyici (tracker): üye listesini tutar
- **Tit-for-tat mekanizması:**
  - Her 10 saniyede en yüksek hızda parça gönderen **4 üye** aktif tutulur
  - Her 30 saniyede **rastgele 1 üye** "iyimserçe" beslenir → potansiyel yeni ortak

---

### 📝 Bölüm 2.6 Soruları

**S42.** **BitTorrent tit-for-tat** mekanizması nasıl çalışır?

- A) Üye yalnızca izleyiciden parça alır.
- B) En yüksek hızda parça gönderen 4 üyeye gönderilir; her 30 saniyede rastgele 1 üye "iyimserçe" beslenir.
- C) Parçalar alfabetik sıraya göre paylaşılır.
- D) Sunucu tüm parçaları eşit hızda dağıtır.

✅ **Cevap: B** — Tit-for-tat bedavacılığı önler. 10 sn'de en iyi 4 seçilir; 30 sn'de rastgele 1 seçilerek yeni ortaklar keşfedilir.

---

**S43.** P2P'nin kullanıcı sayısı N arttıkça **dağıtım süresi** istemci-sunucuya kıyasla nasıl değişir?

- A) P2P süresi N ile doğrusal artar, istemci-sunucu sabit kalır.
- B) İstemci-sunucu süresi N ile doğrusal artarken, P2P süresi her yeni üye yeni kapasite getirdiğinden çok daha yavaş büyür.
- C) Her iki mimari de N'den bağımsızdır.
- D) P2P süresi her zaman daha uzundur.

✅ **Cevap: B** — P2P'nin **öz ölçeklenebilirliği** budur: N arttıkça hem talep hem kapasite artar. İstemci-sunucuda yalnızca sunucu kapasitesi sabit kalır.

---

## 2.7 Soket Programlama

### UDP Soketi
- Bağlantısız, `sendto`/`recvfrom` ile her datagram hedef adres içerir
- `accept()` gerekmez

### TCP Soketi
- Bağlantılı: `connect()` → `accept()` → yeni bağlantı soketi
- Her istemci için ayrı soket oluşturulur
- `send()`/`recv()` ile byte akışı

---

### 📝 Bölüm 2.7 Sorusu

**S44.** TCP'de `accept()` ne işe yarar? UDP'de neden gerekmez?

- A) `accept()` sunucunun portu açmasını sağlar; UDP'de port yoktur.
- B) TCP'de `accept()` yeni gelen bağlantı için **yeni soket oluşturur**; UDP bağlantısız olduğundan datagramlar bağımsız işlenir, ayrı soket gerekmez.
- C) `accept()` istemci kimliğini doğrular.
- D) `accept()` ile `bind()` aynı işlevi görür.

✅ **Cevap: B** — Karşılama soketi (serverSocket) her zaman dinler; `accept()` ile her istemciye özel yeni soket açılır. UDP'de datagram gelince `recvfrom()` ile doğrudan alınır.

---

# BÖLÜM 3: TAŞIMA KATMANI

---

## 3.1 Taşıma Katmanı Hizmetleri

- **Ağ katmanı:** cihaz↔cihaz mantıksal bağlantı
- **Taşıma katmanı:** işlem↔işlem mantıksal bağlantı (ağ katmanı üstüne inşa edilir)
- Gönderici: mesajı **segmentlere** böler, ağ katmanına verir
- Alıcı: segmentleri birleştirerek mesajı oluşturur, uygulamaya iletir

### İnternet Taşıma Protokolleri

- **TCP:** güvenilir, sıralı, sıkışma kontrolü, akış kontrolü, bağlantı kurulumu
- **UDP:** güvenilir olmayan, sırasız, hızlı
- **Sağlanmayan:** gecikme garantisi, bant genişliği garantisi

---

## 3.2 Çoklama ve Çoklama Çözme

- **Çoklama (Mux):** farklı soketlerden gelen verileri başlık bilgisiyle paketleyip ağa vermek
- **Çoklama Çözme (Demux):** gelen segmenti doğru sokete yönlendirmek

### UDP — Bağlantısız Demux (2-tuple)
- Yalnızca **hedef IP + hedef port** kullanılır
- Farklı kaynaklardan gelen, aynı hedef port'lu paketler **aynı sokete** gider

### TCP — Bağlantı-Odaklı Demux (4-tuple)
- **Kaynak IP + Kaynak Port + Hedef IP + Hedef Port**
- Her istemci için **ayrı soket** oluşturulur

---

### 📝 Bölüm 3.2 Sorusu

**S45.** UDP **bağlantısız çoklama çözme** ile TCP **bağlantı-odaklı çoklama çözme** arasındaki fark nedir?

- A) UDP: kaynak IP + kaynak port; TCP: yalnızca hedef port
- B) UDP: yalnızca **hedef port** (2-tuple); TCP: kaynak IP, kaynak port, hedef IP, hedef port **(4-tuple)**
- C) UDP ve TCP her ikisi de 4-tuple kullanır.
- D) UDP: hedef IP + hedef port; TCP: yalnızca kaynak port

✅ **Cevap: B** — TCP 4-tuple ile her istemciye özel soket açılır. UDP'de farklı kaynaklardan gelen aynı hedef portlu paketler aynı sokete düşer.

---

## 3.3 Bağlantısız Taşıma: UDP

### UDP Özellikleri

- "En iyi gayret" hizmet: kaybolabilir, sırası bozulabilir
- Bağlantısız: el sıkışma yok
- Başlık boyutu: **8 byte** (kaynak port, hedef port, uzunluk, checksum)
- **Neden UDP?** Bağlantı yok → gecikme yok; basit; küçük başlık; sıkışma kontrolü yok

### UDP Kullanım Alanları

- DNS, SNMP, canlı yayın (kayıp tolere edilebilir, hız önemli)

### UDP Checksum

- 16-bit **birin tamamlayıcısı** toplamı
- Hata tespit edilirse: UDP paketi sessizce atılır (düzeltme UDP'nin görevi değil)

---

### 📝 Bölüm 3.3 Soruları

**S46.** **UDP** ile **TCP** arasındaki en temel fark nedir?

- A) UDP daha büyük başlık kullanır.
- B) UDP bağlantısız ve güvenilmez; TCP bağlantı odaklı, güvenilir ve akış/sıkışma kontrolü sağlar.
- C) UDP yalnızca yerel ağlarda kullanılabilir.
- D) TCP şifreleme sağlar, UDP sağlamaz.

✅ **Cevap: B** — UDP: 8 byte başlık, hızlı, güvenilmez. TCP: 20+ byte başlık, güvenilir, yavaş. Her ikisi de taşıma katmanında işlemler arası iletişim sağlar.

---

**S47.** **UDP checksum** nasıl hesaplanır ve hata bulununca ne yapılır?

- A) CRC kullanılır; hata tespit edilince paket otomatik düzeltilir.
- B) 16-bit birin tamamlayıcısı toplamı kullanılır; hata tespit edilince UDP paketi sessizce atılır.
- C) MD5 özet algoritması kullanılır; paket yeniden istenir.
- D) Checksum hesaplanmaz; kontrol ağ katmanına bırakılmıştır.

✅ **Cevap: B** — Gönderici segment içeriğini 16-bit parçalara böler, toplar, tamamlayıcısını checksum alanına yazar. Alıcı kontrol eder; eşleşmezse atılır — düzeltme yoktur.

---

## 3.4 Güvenilir Veri Transferi Prensipleri

### rdt Protokollerinin Evrimi

| Versiyon | Kanal Varsayımı | Eklenen Mekanizma |
|----------|-----------------|-------------------|
| **rdt1.0** | Mükemmel kanal | — |
| **rdt2.0** | Bit hatası var | ACK / NAK |
| **rdt2.1** | ACK/NAK da bozulabilir | **Sıra numarası (0, 1)** |
| **rdt2.2** | ACK/NAK bozulabilir | NAK kaldırıldı, sadece ACK |
| **rdt3.0** | Bit hatası + **kayıp** var | **Zamanlayıcı (timeout)** |

### Pipeline Protokolleri

**Dur-ve-bekle:**
```
U = (L/R) / (GDS + L/R) — çok düşük verimlilik
```

**Pipeline:** gönderici çoklu ACK-almamış paket gönderebilir.

#### Geri-Git-N (GGN / Go-Back-N)
- Pencere boyutu: **N ≤ 2^k − 1** (k-bit sıra #)
- Timeout → penceredeki **tüm paketler** tekrar gönderilir
- Alıcı: **toplu ACK**, sıra dışı paketleri atar (önbellek yok)

#### Seçici Tekrar (ST)
- Pencere boyutu: **N ≤ 2^(k−1)**
- Timeout → **yalnızca ilgili paket** tekrar gönderilir
- Alıcı: bireysel ACK, sıra dışı paketleri **önbellekler**

---

### 📝 Bölüm 3.4 Soruları

**S48.** **rdt2.1** rdt2.0'a göre hangi sorunu çözmek için geliştirilmiştir?

- A) Paket kaybı için zamanlayıcı eklenmiştir.
- B) ACK/NAK mesajlarının bozulabileceği sorununu çözmek için paketlere **sıra numarası (0 ve 1)** eklenmiştir.
- C) Pipeline mekanizması eklenmiştir.
- D) Alıcıda önbellekleme eklenmiştir.

✅ **Cevap: B** — ACK bozulursa gönderici ne yapacağını bilemez; yeniden gönderirse alıcı kopya mu yeni mi ayırt edemez. Sıra numarası bu sorunu çözer.

---

**S49.** **GGN** ile **Seçici Tekrar** arasındaki en önemli fark nedir?

- A) GGN daha büyük pencere boyutu kullanır.
- B) GGN'de timeout olunca penceredeki **tüm paketler** tekrar gönderilir; ST'de yalnızca **ACK almayan paket**.
- C) Seçici Tekrar UDP tabanlıdır.
- D) GGN alıcıda önbellekleme yaparken ST yapmaz.

✅ **Cevap: B** — GGN: basit alıcı, israf tekrar gönderim. ST: karmaşık alıcı (önbellek var), verimli tekrar gönderim.

---

**S50.** **GGN** protokolünde **k-bit sıra numarası** kullanılıyorsa maksimum pencere boyutu nedir?

- A) 2^k
- B) 2^k − 1
- C) 2^(k−1)
- D) k

✅ **Cevap: B** — GGN: 2^k − 1. Seçici Tekrar: 2^(k−1). Örnek k=3: GGN pencere=7, ST pencere=4.

---

**S51.** **Seçici Tekrar**'da pencere boyutu neden 2^(k−1) ile sınırlandırılmıştır?

- A) Alıcı önbelleği sınırlıdır.
- B) Pencere boyutu sıra numarası uzayının yarısını aşarsa, alıcı yeni paket mi yoksa kopya mı geldiğini **ayırt edemez**.
- C) Standartlar zorunlu kılmıştır.
- D) Göndericide kronometre sayısını azaltmak için.

✅ **Cevap: B** — Sıra numarası uzayının yarısından büyük pencere = alıcı karışıklığı. Ör: k=2, sıra#={0,1,2,3}, pencere=3 → senaryo ikilemli.

---

**S52.** rdt3.0'da **zamansız timeout** (paket ulaştı, ACK de geldi, ama gönderici daha önce timeout yapıp tekrar gönderdi) durumunda alıcı ne yapar?

- A) İkinci paketi yeni veri olarak işler.
- B) İkinci paketi **sıra numarasına bakarak kopya** anlar, yoksayar, tekrar ACK gönderir.
- C) Hata mesajı üretir, bağlantıyı kapatır.
- D) Her iki paketi de üst katmana iletir.

✅ **Cevap: B** — Sıra numarası mekanizması tam olarak bu için var. Sistem doğruluğu korunur, yalnızca bant genişliği biraz israf edilir.

---

**S53.** **Pipeline** ile **3 paket** gönderildiğinde kullanım oranı "dur-ve-bekle"ye göre nasıl değişir? *(GDS=30ms, L/R=0.008ms)*

- A) Değişmez.
- B) 3 katına çıkar (~0.00081).
- C) 10 katına çıkar.
- D) 30 katına çıkar.

✅ **Cevap: B** — U = N × (L/R) / (GDS + L/R). N=1: ~0.00027, N=3: ~0.00081. Tam verimlilik için N≈GDS/(L/R)=3750 paket gerekir.

---

## 3.5 Bağlantı-Odaklı Taşıma: TCP

### TCP Genel Özellikleri

- Uçtan uca: bir gönderici, bir alıcı
- Güvenilir, sıralı byte yayını
- Pipeline (cwnd ile kontrol)
- Tam iki-yönlü veri akışı
- Bağlantı-odaklı: veri öncesi el sıkışma
- Akış kontrollü

### TCP Segment Yapısı

| Alan | Açıklama |
|------|----------|
| Kaynak/Hedef port | 16 bit |
| Sıra numarası | Segmentteki ilk byte'ın byte-akışı numarası |
| ACK numarası | Karşıdan beklenen sonraki byte'ın numarası |
| URG/ACK/PSH/RST/SYN/FIN | Bayraklar |
| rwnd | Alıcı pencere (akış kontrolü) |
| Checksum | |

### TCP RTT Tahmini

```
TahminiGDS = (1 − α) × TahminiGDS + α × ÖrnekGDS   (α = 0.125)
DevGDS = (1 − β) × DevGDS + β × |ÖrnekGDS − TahminiGDS|   (β = 0.25)
TimeoutSüresi = TahminiGDS + 4 × DevGDS
```

### TCP Güvenilir Veri Transferi

- Timeout → segment tekrar gönderilir
- **Hızlı tekrar gönderim:** 3 kopya ACK → timeout beklemeden tekrar gönder

### TCP ACK Oluşturma

- Sıralı segment gelirse: 500 ms bekle (sonraki segment için)
- İki sıralı segment bekliyorsa: hemen toplu ACK
- Sıra dışı (boşluk var): hemen kopya ACK
- Boşluk doluyorsa: hemen ACK

### TCP Akış Kontrolü

- Alıcı **rwnd** alanında boş önbellek miktarını bildirir
- Gönderici: ACK almadan gönderilen veri ≤ rwnd
- **rwnd = 0:** gönderici 1 byte'lık sonda segment göndererek kilitlenmeyi önler

### TCP Bağlantı Yönetimi

**3-Yönlü Elsıkışma:**
```
İstemci → SYN → Sunucu
Sunucu → SYN-ACK → İstemci
İstemci → ACK → Sunucu
[Bağlantı kuruldu]
```

**Bağlantı Sonlandırma:**
```
İstemci → FIN → Sunucu → ACK
Sunucu → FIN → İstemci → ACK
[Bağlantı kapandı]
```

### TCP MSS

```
MTU (Ethernet) = 1500 byte
MSS = 1500 − 20 (IP) − 20 (TCP) = 1460 byte
```

---

### 📝 Bölüm 3.5 Soruları

**S54.** TCP **3-yönlü elsıkışma** hangi sırayla gerçekleşir?

- A) SYN → ACK → FIN
- B) SYN → SYN-ACK → ACK
- C) ACK → SYN → SYN-ACK
- D) FIN → ACK → SYN

✅ **Cevap: B** — İstemci SYN gönderir (bağlanmak istiyorum), sunucu SYN-ACK ile kabul eder, istemci ACK ile onaylar. 2-yönlü yeterli değildir çünkü gecikmeler/kayıplar güvenilmez durum yaratır.

---

**S55.** TCP **akış kontrolü (flow control)** ne amaçla kullanılır?

- A) Yönlendirici önbelleklerinin taşmasını önler.
- B) Göndericinin alıcının önbelleğini taşırmasını önler; **rwnd** alanı ile boş alan bildirilir.
- C) Paketlerin doğru sırada iletilmesini sağlar.
- D) Bağlantı kurulum süresini kısaltır.

✅ **Cevap: B** — Akış kontrolü = alıcı koruması. Sıkışma kontrolü = ağ koruması. İkisi farklı! rwnd TCP başlığında 16 bit alan.

---

**S56.** TCP **bayrakları SYN, FIN, RST** ne anlama gelir?

- A) SYN: veri gönder, FIN: hata bildir, RST: yeniden başlat
- B) SYN: **bağlantı kurma**, FIN: **bağlantı kapatma**, RST: **anında sıfırlama**
- C) SYN: sıkışma, FIN: akış, RST: tekrar gönderme
- D) Üçü de yalnızca UDP'de kullanılır.

✅ **Cevap: B** — SYN: 3-yönlü elsıkışmada. FIN: nazik kapatma (4 mesaj). RST: hata durumunda anlık kapatma.

---

**S57.** TCP **sıra numarası** ve **ACK numarası** ne anlama gelir?

- A) Sıra#: segmentin kaçıncı olduğu; ACK#: toplam gönderilen byte
- B) Sıra#: segmentteki **ilk byte'ın byte-akışı numarası**; ACK#: karşıdan **beklenen sonraki byte'ın numarası**
- C) Her ikisi de yalnızca bağlantı kurulumunda kullanılır.
- D) Sıra numarası port numarasıyla aynıdır.

✅ **Cevap: B** — Sıra#=42: bu segmentin ilk byte'ı 42. byte. ACK#=43: 42 alındı, sıradaki 43'ü bekliyorum.

---

**S58.** TCP **RTT tahmini** için hangi formül ve α değeri kullanılır?

- A) TahminiGDS = α×TahminiGDS + (1−α)×ÖrnekGDS ; α=0.5
- B) TahminiGDS = (1−α)×TahminiGDS + α×ÖrnekGDS ; **α=0.125**
- C) TahminiGDS = ÖrnekGDS / α ; α=0.25
- D) TahminiGDS = TahminiGDS + ÖrnekGDS ; α=1

✅ **Cevap: B** — EWMA: eski geçmiş ağırlığı azalır, yeni ölçüm %12.5 katkı sağlar. α=1/8=0.125 standardize değer.

---

**S59.** TCP **timeout süresi** nasıl hesaplanır?

- A) TimeoutSüresi = TahminiGDS
- B) TimeoutSüresi = 2 × TahminiGDS
- C) TimeoutSüresi = TahminiGDS + 4 × DevGDS
- D) TimeoutSüresi = TahminiGDS − DevGDS

✅ **Cevap: C** — 4×DevGDS güvenlik payıdır. GDS değişkense (DevGDS büyük) → geniş timeout. Kararlıysa → timeout ≈ TahminiGDS.

---

**S60.** TCP **hızlı tekrar gönderim** ne zaman tetiklenir?

- A) Herhangi bir ACK geldiğinde.
- B) Gönderici aynı sıra numarası için **3 kopya ACK** aldığında; timeout beklemeden tekrar gönderilir.
- C) Alıcı NAK gönderdiğinde.
- D) cwnd ssthresh'e ulaştığında.

✅ **Cevap: B** — 3 kopya ACK: ağ hâlâ çalışıyor (paketler iletiliyor) demek → hafif kayıp. Timeout süresi dolmadan harekete geçilir, gecikme azalır.

---

**S61.** TCP **bağlantı sonlandırması** nasıl çalışır?

- A) Yalnızca istemci FIN gönderir.
- B) Her iki taraf da FIN gönderebilir; FIN gönderen taraf kendi yönündeki akışı kapatır, karşı ACK ile onaylar. İki taraf da FIN gönderince bağlantı tamamen kapanır.
- C) SYN bayrağı ile kapatılır.
- D) TCP bağlantıları otomatik timeout ile kapanır.

✅ **Cevap: B** — 4 mesaj: FIN→ACK→FIN→ACK. "Yarı kapalı" mümkün: bir yön kapanabilir, diğer yön hâlâ açık olabilir.

---

**S62.** TCP **rwnd = 0** bildirilince ne olur? Kilitlenme nasıl önlenir?

- A) Gönderici bağlantıyı kapatır.
- B) Gönderici veri göndermeyi durdurur; kilitlenmeyi önlemek için **1 byte sonda segment** göndermeye devam eder.
- C) Gönderici cwnd'yi artırır.
- D) Ağ katmanı devreye girer.

✅ **Cevap: B** — rwnd=0: alıcı önbelleği dolu. Gönderici durursa alıcı boşalınca nasıl bildirecek? Sonda segment ile alıcıyı sorgular → rwnd>0 gelince devam.

---

**S63.** TCP **MSS** nedir ve nasıl hesaplanır?

- A) TCP bağlantısında gönderilebilecek max paket sayısıdır.
- B) Bir TCP segmentindeki **max uygulama verisi miktarıdır**; MTU − IP başlık (20) − TCP başlık (20) = **1460 byte**.
- C) cwnd'nin alabileceği max değerdir.
- D) Max TCP bağlantı sayısını belirler.

✅ **Cevap: B** — MSS sabit (1460 byte), cwnd dinamik. cwnd ve ssthresh MSB cinsinden ifade edilir.

---

**S64.** TCP başlangıç sıra numarası (ISN) neden **rastgele** seçilir?

- A) Verimli önbellekleme için.
- B) Eski bağlantı paketlerinin yeni bağlantıya karışmasını önler ve saldırganın sıra numarasını tahmin ederek sahte paket enjekte etmesini zorlaştırır.
- C) Checksum hesabını kolaylaştırır.
- D) Yönlendiricilerin işlemini hızlandırır.

✅ **Cevap: B** — Tahmin edilebilir ISN = güvenlik açığı. Rastgele ISN hem eski paket çakışmasını hem saldırı riskini azaltır.

---

## 3.6 Sıkışma Kontrolü Prensipleri

### Sıkışma Tanımı

> "Aşırı kaynak aşırı veriyi aşırı hızda gönderiyor ve ağ bu durumu idare edemiyor."

**Akış kontrolünden farklıdır:**
- Akış kontrolü: alıcı önbelleğini korur
- Sıkışma kontrolü: ağ yönlendirici önbelleklerini korur

### Sıkışmanın İki Maliyeti

1. **Gereksiz tekrar gönderimler:** gecikmeli (kaybolmamış) paket için gönderilen kopya → bant genişliği israfı
2. **Düşürülen paketin yolculuğu:** paketi taşıyan tüm bağlardaki bant genişliği boşa gider

### Sıkışma Kontrolü Yöntemleri

| Yöntem | Açıklama |
|--------|----------|
| **Uçtan uca** | Ağdan doğrudan geribildirim yok; kayıp/gecikme gözlemlenir. **TCP bu yöntemi kullanır.** |
| **Ağ-destekli** | Yönlendiriciler uç sistemlere geribildirim yapar (1 bit: sıkışma var/yok) |

---

### 📝 Bölüm 3.6 Sorusu

**S65.** Ağ sıkışmasının iki temel "maliyeti" nedir?

- A) Artan bant genişliği ve azalan gecikme.
- B) **(1)** Tekrar gönderimlerin gereksiz bant genişliği tüketimi ve **(2)** düşürülen paketin tüm yolculuğu boyunca harcanan bant genişliğinin boşa gitmesi.
- C) Artan CPU kullanımı ve azalan güvenlik.
- D) Büyük önbellek gerekliliği ve yüksek enerji tüketimi.

✅ **Cevap: B** — Bu iki maliyet sıkışma kontrolünün neden kritik olduğunu açıklar. Kontrol olmasaydı pozitif geri besleme döngüsü: daha çok trafik → daha çok kayıp → daha çok tekrar gönderim.

---

## 3.7 TCP Sıkışma Kontrolü

### AIMD (Toplamalı Artış Çarpmalı Azalış)

- **Toplamalı artış:** her GDS'de cwnd += 1 MSB (doğrusal)
- **Çarpmalı azalış:** kayıp → cwnd /= 2

→ "Testere dişi" davranışı

### Yavaş Başlangıç (Slow Start)

```
cwnd = 1 MSB ile başlar
Her ACK → cwnd += 1 MSB
Sonuç: Her GDS cwnd ikiye katlanır (ÜSTEL artış)
ssthresh'e ulaşınca → Tıkanıklık Önleme fazına geç
```

### Tıkanıklık Önleme (Congestion Avoidance)

```
cwnd >= ssthresh → her GDS cwnd += 1 MSB (DOĞRUSAL artış)
```

### Kayıp Reaksiyonu

| Durum | TCP Tahoe | TCP Reno |
|-------|-----------|----------|
| **Timeout** | cwnd=1, ssthresh=cwnd/2 | cwnd=1, ssthresh=cwnd/2 |
| **3 kopya ACK** | cwnd=1, ssthresh=cwnd/2 | cwnd=ssthresh=cwnd/2 (**hızlı kurtarma**) |

### TCP İş Hacmi

```
Ort. iş hacmi ≈ (3/4) × W / GDS   (W = kayıp anındaki pencere)
```

### TCP Adaleti

- K TCP oturumu R bant genişliğini paylaşırsa → her biri ideal olarak R/K almalı
- AIMD mekanizması bunu yakınsatır
- **UDP adaleti bozar:** sıkışma kontrolü yok → sabit hızda gönderir → TCP'nin payını azaltır

---

### 📝 Bölüm 3.7 Soruları

**S66.** **AIMD** ne anlama gelir?

- A) Her GDS cwnd ikiye katla; kayıpla sıfırla.
- B) Her GDS cwnd += 1 MSB (toplamalı artış); kayıpta cwnd /= 2 (çarpmalı azalış).
- C) cwnd sabit tut, ssthresh değiştir.
- D) Kayıp olmasa da cwnd'yi düzenli yarıya indir.

✅ **Cevap: B** — Asimetrik tepki: yavaş artış (bant genişliğini keşfet), hızlı azalış (ağı koru). Bu "testere dişi" grafiği oluşturur.

---

**S67.** **Yavaş başlangıç** fazında cwnd nasıl artar?

- A) Her GDS +1 MSB (doğrusal).
- B) cwnd sabit kalır, ssthresh aşılana kadar beklenir.
- C) Her ACK alınca +1 MSB → her GDS cwnd ikiye katlanır (üstel artış).
- D) Rastgele belirlenir.

✅ **Cevap: C** — "Yavaş" başlangıç adına rağmen artış üsteldir! İsim, cwnd=1 MSB ile başlamasından gelir. ssthresh'e ulaşınca tıkanıklık önlemeye geçilir.

---

**S68.** **ssthresh = 8 MSB, cwnd = 1 MSB** ile başlanıyor. Kayıp olmadığında **4. GDS sonunda** cwnd nedir?

- A) 4 MSB  B) 8 MSB  **C) 9 MSB**  D) 16 MSB

✅ **Cevap: C** — GDS1:1→2, GDS2:2→4, GDS3:4→8 (ssthresh'e ulaşıldı), GDS4: Tıkanıklık Önleme → 8+1=**9 MSB**.

---

**S69.** **TCP Reno'da cwnd = 12 MSB** iken **3 kopya ACK** alındı. ssthresh ve cwnd yeni değerleri?

- A) ssthresh=12, cwnd=1
- B) ssthresh=6, cwnd=6 (hızlı kurtarma, tıkanıklık önleme devam)
- C) ssthresh=6, cwnd=1
- D) ssthresh=12, cwnd=6

✅ **Cevap: B** — TCP Reno hızlı kurtarma: ssthresh=cwnd/2=6, cwnd=ssthresh=6 → Tıkanıklık Önleme fazından devam (+1/GDS). TCP Tahoe'da: cwnd=1 olurdu.

---

**S70.** **TCP Tahoe** ve **TCP Reno** arasındaki fark nedir?

- A) TCP Tahoe UDP tabanlıdır.
- B) Her ikisinde timeout → cwnd=1; ancak **3 kopya ACK**'ta Tahoe cwnd=1 yaparken, Reno cwnd=ssthresh=cwnd/2 yapar (hızlı kurtarma).
- C) TCP Reno akış kontrolü yaparken Tahoe yapmaz.
- D) TCP Tahoe daha yeni bir sürümdür.

✅ **Cevap: B** — 3 kopya ACK ağın hâlâ çalıştığını gösterir (hafif sorun). Reno bunu fark edip daha nazik tepki verir. Timeout daha ciddi sorundur → her ikisi cwnd=1 yapar.

---

**S71.** **ssthresh** değişkeni ne işe yarar ve kayıptan nasıl güncellenir?

- A) rwnd ile aynıdır, kayıptan etkilenmez.
- B) Yavaş başlangıç→tıkanıklık önleme geçiş eşiğidir; kayıpta **ssthresh = kayıp anındaki cwnd/2** yapılır.
- C) MSS'yi belirler.
- D) ssthresh her zaman sabittir.

✅ **Cevap: B** — ssthresh dinamik eşiktir. Kayıp → eşik düşürülür → daha erken tıkanıklık önlemeye geçilir → daha temkinli davranış.

---

**S72.** TCP ortalama **iş hacmi** W ve GDS cinsinden nasıl ifade edilir?

- A) İş hacmi = W / GDS
- B) İş hacmi = W / (2×GDS)
- C) İş hacmi ≈ **(3/4) × W / GDS**
- D) İş hacmi = 2W / GDS

✅ **Cevap: C** — Pencere W/2→W arası salınır, ortalama = 3W/4. Bu ortalama pencereyi GDS'ye bölerek iş hacmi elde edilir.

---

**S73.** **TCP adaleti** bağlamında K oturum için ideal hedef ve UDP'nin adaleti nasıl bozduğu?

- A) Her oturum R/2 almalı; UDP etkisizdir.
- B) Her oturum **R/K** almalı; UDP sıkışma kontrolü uygulamadığı için TCP'nin payını azaltır.
- C) TCP oturumları arası adalet garantisi yoktur.
- D) UDP daha az bant genişliği kullandığı için adaleti bozmaz.

✅ **Cevap: B** — TCP AIMD ile R/K'ya yakınsar. UDP yavaşlamaz → bant genişliğinin orantısız büyük kısmını alır.

---

**S74.** **ssthresh = 16 MSB, cwnd = 1 MSB** ile başlanıyor. **5. GDS'de timeout** oluşuyor. Timeout anında ve sonrasında cwnd ve ssthresh değerleri nedir?

- A) Timeout öncesi: cwnd=16, ssthresh=16 → Sonrası: **ssthresh=8, cwnd=1**
- B) Timeout öncesi: cwnd=32, ssthresh=16 → Sonrası: ssthresh=16, cwnd=1
- C) Timeout öncesi: cwnd=16, ssthresh=16 → Sonrası: ssthresh=16, cwnd=8
- D) Timeout öncesi: cwnd=8, ssthresh=16 → Sonrası: ssthresh=4, cwnd=1

✅ **Cevap: A** — GDS1:1→2, GDS2:2→4, GDS3:4→8, GDS4:8→16 (ssthresh=16'ya ulaşıldı → Tıkanıklık Önleme), GDS5: cwnd=16 iken timeout → **ssthresh=8, cwnd=1**.

---

**S75.** **1 Gb/s bağ**, **8000 bit paket**, **GDS = 30 ms** ile "dur-ve-bekle" protokolündeki gönderici **kullanım oranı** nedir?

- A) %0.027  B) %0.27  C) %2.7  D) %27

✅ **Cevap: A** — U = (L/R) / (GDS + L/R) = 0.000008 / 0.030008 ≈ **0.00027 = %0.027**. Bu son derece verimsiz. Pipeline ile N=3 → U≈%0.081, N=3750 → U≈%100.

---

# FORMÜL ÖZETİ

```
İletim gecikmesi:     d_iletim = L / R
Yayılma gecikmesi:    d_yayılma = mesafe / yayılma hızı
Toplam gecikme:       d = d_işlem + d_sıralanma + d_iletim + d_yayılma
Sakla-ve-yolla:       D = N × L / R   (N bağ, yayılma=0)
Trafik yoğunluğu:     La / R   (>1 → sonsuz gecikme)
Darboğaz iş hacmi:    min(R_c, R_s, R/N)
Kullanım oranı:       U = (L/R) / (GDS + L/R)
Pipeline U:           U = N × (L/R) / (GDS + L/R)
HTTP yanıt süresi:    2×GDS + T (kalıcı olmayan)

TahminiGDS:  (1−0.125)×TahminiGDS + 0.125×ÖrnekGDS
DevGDS:      (1−0.25)×DevGDS + 0.25×|ÖrnekGDS−TahminiGDS|
Timeout:     TahminiGDS + 4×DevGDS

MSS:         MTU − 20(IP) − 20(TCP) = 1460 byte
TCP iş hacmi: (3/4) × W / GDS

GGN pencere:  ≤ 2^k − 1
ST pencere:   ≤ 2^(k−1)

AIMD:        Artış: cwnd += 1/GDS   Azalış: cwnd /= 2
Yavaş Baş:  cwnd ikiye katla (üstel), ssthresh'e kadar
TCP Reno 3×ACK: ssthresh=cwnd/2, cwnd=ssthresh
TCP Tahoe 3×ACK: ssthresh=cwnd/2, cwnd=1
Her ikisi timeout: ssthresh=cwnd/2, cwnd=1
```

---

*Toplam: 75 Soru — Bölüm 1: S1–S18 · Bölüm 2: S19–S44 · Bölüm 3: S45–S75*
