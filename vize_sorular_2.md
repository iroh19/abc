# Veri İletişimi ve Bilgisayar Ağları — Vize Soruları (2. Set)

**Ders:** Veri İletişimi ve Bilgisayar Ağları  
**Kaynak:** Kurose & Ross — Computer Networking: A Top-Down Approach (8. Baskı)  
**Kapsam:** Bölüm 1 · Bölüm 2 · Bölüm 3 — İlk sınav setinde geçilmeyen / az işlenen konular  
**Toplam:** 25 Soru · Her soru 4 puan

---

## SORULAR

---

### SORU 1
**Sakla-ve-yolla (store-and-forward)** ilkesine göre, 3 Mb boyutunda bir paket 1 Mb/s kapasiteli iki bağ üzerinden (1 ara yönlendirici ile) iletilmektedir. Yayılma gecikmesi sıfır kabul edilirse toplam iletim gecikmesi ne kadardır?

- A) 3 saniye
- B) 6 saniye
- C) 1.5 saniye
- D) 9 saniye

---

### SORU 2
**DSL (Digital Subscriber Line)** ve **HFC (Kablo/Hibrit Fiber-Koaksiyel)** erişim teknolojileri arasındaki en temel mimari fark nedir?

- A) DSL fiber optik kullanırken HFC bakır kablo kullanır.
- B) DSL'de her evin merkezi ofise ayrılmış bağlantısı varken, HFC'de evler kablo başucuna erişim ağını paylaşır.
- C) DSL kablosuz erişim sağlarken HFC kablolu erişim sağlar.
- D) HFC simetrik hız sunarken DSL asimetrik hız sunar.

---

### SORU 3
**Fiber optik kablo**nun bükümlü çift (twisted pair) ve koaksiyel kablodan üstün olduğu temel özellikler nelerdir?

- A) Düşük maliyetli ve bükmesi kolaydır.
- B) Çok yüksek iletim hızı, çok düşük hata oranı ve elektromanyetik gürültüden etkilenmemesi.
- C) Kısa mesafeli iletim için idealdir.
- D) Kablosuz bağlantı kurulumunu destekler.

---

### SORU 4
Aşağıdakilerden hangisi **DoS (Denial of Service)** saldırısının doğru tanımıdır?

- A) Saldırgan ağ üzerinden geçen paketleri sessizce dinler ve kaydeder.
- B) Saldırgan sahte IP adresi kullanarak farklı bir cihaz gibi görünür.
- C) Saldırgan, aşırı sahte trafik göndererek hedef kaynağa erişimi engeller.
- D) Saldırgan, zararlı yazılımı e-posta eki olarak yayar.

---

### SORU 5
**IP yanıltma (IP spoofing)** saldırısında saldırgan ne yapar?

- A) DNS sunucusuna sahte kayıtlar ekler.
- B) Ağ üzerindeki paketleri dinleyerek şifreleri çalar.
- C) Sahte gönderici IP adresi içeren paketler göndererek başka bir cihaz gibi görünür.
- D) Yönlendiricinin yönlendirme tablosunu bozar.

---

### SORU 6
Bir HTTP yanıtında **"304 Not Modified"** durum kodu ne anlama gelir?

- A) İstek başarıyla tamamlandı, nesne yanıt içinde.
- B) İstenen nesne sunucuda bulunamadı.
- C) Önbellekteki kopya hâlâ güncel; sunucu nesneyi tekrar göndermedi.
- D) HTTP versiyonu desteklenmiyor.

---

### SORU 7
**Koşullu GET (Conditional GET)** mekanizması hangi amaca hizmet eder ve hangi başlık alanını kullanır?

- A) Sunucunun istemci kimliğini doğrulaması; `Authorization` başlığı.
- B) Önbellekteki nesne güncel ise tekrar gönderilmemesi; `If-Modified-Since` başlığı.
- C) İstemcinin tercih ettiği dil bilgisini bildirmesi; `Accept-Language` başlığı.
- D) Bağlantının kalıcı tutulması; `Keep-Alive` başlığı.

---

### SORU 8
**POP3** ve **IMAP** protokolleri arasındaki en önemli fark nedir?

- A) POP3 TCP, IMAP UDP kullanır.
- B) POP3 mesajları sunucudan indirip (genellikle) siler; IMAP mesajları sunucuda saklar ve oturumlar arası klasör durumunu korur.
- C) IMAP yalnızca web tarayıcısı üzerinden kullanılabilir.
- D) POP3 şifrelenmiş iletişim sağlarken IMAP sağlamaz.

---

### SORU 9
DNS'te **TTL (Time To Live — Yaşam Süresi)** değerinin önemi nedir?

- A) Paketin ağda kaç yönlendirici geçebileceğini sınırlar.
- B) Önbelleklenmiş DNS kaydının ne kadar süre geçerli kalacağını belirler; süre dolunca kayıt önbellekten silinir.
- C) DNS sorgusunun cevap vermesi için beklenen maksimum süreyi tanımlar.
- D) DNS sunucusunun ne kadar süreyle çevrimiçi kalacağını gösterir.

---

### SORU 10
DNS **döngüsel (iterative) sorgu** ile **yinelenmeli (recursive) sorgu** arasındaki fark nedir?

- A) Döngüsel sorguda yerel DNS tüm çözümleme işini yaparak nihai cevabı döner; yinelenmeli sorguda her sunucu bir sonraki sunucunun adresini söyler.
- B) Yinelenmeli sorguda yerel DNS tüm çözümleme işini yaparak nihai cevabı döner; döngüsel sorguda her sunucu bir sonraki sunucunun adresini söyler.
- C) İkisi arasında işlevsel hiçbir fark yoktur.
- D) Döngüsel sorgu yalnızca kök sunucular tarafından kullanılır.

---

### SORU 11
**SSL (Secure Sockets Layer)** ile ilgili aşağıdaki ifadelerden hangisi doğrudur?

- A) SSL, TCP'nin yerini alan yeni bir taşıma katmanı protokolüdür.
- B) SSL uygulama katmanında çalışır; uygulamalar SSL kütüphaneleri aracılığıyla şifrelenmiş TCP bağlantısı kurar.
- C) SSL yalnızca UDP üzerinde çalışabilir.
- D) SSL, şifreleme yerine yalnızca veri sıkıştırma sağlar.

---

### SORU 12
Bir işlemi benzersiz biçimde tanımlamak için **IP adresi yeterli midir?** Değilse ne gerekmektedir?

- A) Evet, IP adresi tek başına yeterlidir.
- B) Hayır; hem IP adresi hem de **port numarası** birlikte gereklidir — çünkü aynı cihazda birden fazla işlem çalışabilir.
- C) Hayır; IP adresi yerine yalnızca MAC adresi kullanılmalıdır.
- D) Hayır; IP adresi, port numarası ve protokol adı üçü birlikte gereklidir.

---

### SORU 13
**P2P dosya dağıtım süresi** istemci-sunucu mimarisine kıyasla kullanıcı sayısı N arttıkça nasıl değişir?

- A) P2P dağıtım süresi N ile doğrusal artar, istemci-sunucu sabit kalır.
- B) İstemci-sunucu dağıtım süresi N ile doğrusal artarken, P2P dağıtım süresi her yeni üye yeni kapasite getirdiğinden çok daha yavaş büyür.
- C) Her iki mimari de N'den bağımsızdır.
- D) P2P dağıtım süresi her zaman istemci-sunucudan daha uzundur.

---

### SORU 14
**UDP checksum** hesaplamasında hangi yöntem kullanılır ve hata tespit edildiğinde ne yapılır?

- A) CRC (Döngüsel Artıklık Kodu) kullanılır; hata tespit edilince paket otomatik düzeltilir.
- B) 16-bit birin tamamlayıcısı (one's complement) toplamı kullanılır; hata tespit edilince UDP paketi sessizce atılır — düzeltme UDP'nin görevi değildir.
- C) MD5 özet algoritması kullanılır; hata tespit edilince paket yeniden istenir.
- D) Checksum hesaplanmaz; hata kontrolü tamamen ağ katmanına bırakılmıştır.

---

### SORU 15
UDP'de **bağlantısız çoklama çözme (connectionless demultiplexing)** hangi bilgilere göre yapılır? TCP'den farkı nedir?

- A) UDP: kaynak IP + kaynak port (2 bilgi); TCP: yalnızca hedef port (1 bilgi)
- B) UDP: yalnızca **hedef port numarası** (2-tuple); TCP: kaynak IP, kaynak port, hedef IP, hedef port **(4-tuple)**
- C) UDP ve TCP her ikisi de 4-tuple kullanır.
- D) UDP: hedef IP + hedef port; TCP: yalnızca kaynak port

---

### SORU 16
**rdt2.1** protokolü rdt2.0'a göre hangi sorunu çözmek için geliştirilmiştir ve çözüm olarak ne eklenmiştir?

- A) Paket kaybı sorununu çözmek için zamanlayıcı eklenmiştir.
- B) ACK/NAK mesajlarının bozulabileceği sorununu çözmek için paketlere **sıra numarası (0 ve 1)** eklenmiştir.
- C) Büyük veri transferlerini hızlandırmak için pipeline mekanizması eklenmiştir.
- D) Alıcı tarafında önbellekleme eklenmiştir.

---

### SORU 17
TCP segment başlığındaki **SYN, FIN ve RST** bayraklarının işlevleri nelerdir?

- A) SYN: veri gönder, FIN: hata bildir, RST: bağlantıyı yeniden başlat
- B) SYN: bağlantı **kurma** isteği, FIN: bağlantıyı **kapatma** isteği, RST: bağlantıyı **anında sıfırlama**
- C) SYN: sıkışma kontrolü, FIN: akış kontrolü, RST: tekrar gönderme
- D) Üçü de yalnızca UDP'de kullanılır.

---

### SORU 18
TCP'de **sıra numarası (sequence number)** ve **ACK numarası** ne anlama gelir?

- A) Sıra numarası segmentin kaçıncı segment olduğunu, ACK numarası toplam gönderilen byte sayısını gösterir.
- B) Sıra numarası segmentteki **ilk byte'ın byte-akışı numarasını**; ACK numarası karşı taraftan **bir sonraki beklenen byte'ın numarasını** gösterir.
- C) Her ikisi de yalnızca bağlantı kurulum aşamasında kullanılır.
- D) Sıra numarası port numarasıyla aynıdır.

---

### SORU 19
TCP **RTT tahmini** için kullanılan **Üstel Ağırlıklı Hareketli Ortalama (EWMA)** formülü hangisidir ve α değeri genellikle ne olarak seçilir?

- A) TahminiGDS = α × TahminiGDS + (1−α) × ÖrnekGDS ; α = 0.5
- B) TahminiGDS = (1−α) × TahminiGDS + α × ÖrnekGDS ; α = 0.125
- C) TahminiGDS = ÖrnekGDS / α ; α = 0.25
- D) TahminiGDS = TahminiGDS + ÖrnekGDS ; α = 1

---

### SORU 20
TCP **timeout süresi** nasıl hesaplanır? DevGDS (RTT sapması) bu hesapta nasıl kullanılır?

- A) TimeoutSüresi = TahminiGDS
- B) TimeoutSüresi = 2 × TahminiGDS
- C) TimeoutSüresi = TahminiGDS + 4 × DevGDS
- D) TimeoutSüresi = TahminiGDS − DevGDS

---

### SORU 21
TCP **hızlı tekrar gönderim (fast retransmit)** ne zaman tetiklenir ve neden timeout'tan daha iyi bir yöntemdir?

- A) Herhangi bir ACK geldiğinde tetiklenir; timeout'tan daha basittir.
- B) Gönderici **aynı sıra numarası için 3 kopya ACK** aldığında tetiklenir; timeout süresi dolmadan harekete geçildiği için gecikme çok daha azdır.
- C) Alıcı NAK gönderdiğinde tetiklenir.
- D) cwnd değeri ssthresh'e ulaştığında tetiklenir.

---

### SORU 22
TCP **bağlantı sonlandırma** süreci nasıl işler?

- A) Yalnızca istemci FIN gönderebilir; sunucu sadece ACK ile karşılık verir.
- B) Her iki taraf da FIN gönderebilir; FIN gönderen taraf bağlantının kendi yönündeki akışını kapatır, karşı taraf ACK gönderir. Her iki taraf da FIN gönderdikten sonra bağlantı tamamen kapanır.
- C) Bağlantı sonlandırmak için SYN bayrağı kullanılır.
- D) TCP bağlantıları otomatik olarak timeout ile kapanır, FIN mesajına gerek yoktur.

---

### SORU 23
TCP sıkışma kontrolünde **ssthresh (slow start threshold)** değişkeni ne işe yarar ve kayıp durumunda nasıl güncellenir?

- A) Akış kontrolü penceresi (rwnd) ile aynıdır; kayıptan etkilenmez.
- B) Yavaş başlangıçtan tıkanıklık önleme fazına geçiş eşiğidir; kayıp durumunda **kayıp anındaki cwnd değerinin yarısına** ayarlanır.
- C) Maksimum segment boyutunu (MSS) belirler.
- D) ssthresh her zaman sabit tutulur, güncellenmez.

---

### SORU 24
TCP **ortalama iş hacmi (throughput)** W (kayıp anındaki pencere boyutu) ve GDS cinsinden nasıl ifade edilir?

- A) İş hacmi = W / GDS
- B) İş hacmi = W / (2 × GDS)
- C) İş hacmi ≈ (3/4) × W / GDS
- D) İş hacmi = 2W / GDS

---

### SORU 25
**TCP adaleti (TCP fairness)** bağlamında, aynı bağı paylaşan K TCP oturumu için ideal durum nedir? UDP uygulamaları bu dengeyi nasıl bozar?

- A) Her TCP oturumu R/2 bant genişliği almalıdır; UDP hiçbir etkisi yoktur.
- B) Her TCP oturumu R/K bant genişliği almalıdır; ancak UDP sıkışma kontrolü uygulamadığı için sabit hızda gönderim yapar ve TCP oturumlarının payını azaltır.
- C) TCP oturumları arasında herhangi bir adalet garantisi yoktur.
- D) UDP uygulamaları TCP'den daha az bant genişliği kullandığı için adaleti bozmazlar.

---

---

## CEVAPLAR VE AÇIKLAMALAR

---

### SORU 1 — Cevap: **B**

> **B) 6 saniye**

**Açıklama:**  
Sakla-ve-yolla ilkesi: bir yönlendirici paketi bir sonraki bağa iletmeden önce paketin **tamamının** gelmesini bekler.

```
Bağ 1: 3 Mb / 1 Mb/s = 3 saniye  (kaynak → yönlendirici)
Bağ 2: 3 Mb / 1 Mb/s = 3 saniye  (yönlendirici → hedef)
──────────────────────────────────
Toplam: 6 saniye
```

Genel formül: **N bağ, L bit paket, R bps → toplam = N × L/R** (yayılma gecikmesi sıfır varsayımıyla)

**Dikkat:** Pipeline (boru hattı) gönderiminde birden fazla paket aynı anda farklı bağlarda ilerleyebilir — bu durumda toplam süre farklı hesaplanır.

---

### SORU 2 — Cevap: **B**

> **B) DSL'de her evin merkezi ofise ayrılmış bağlantısı varken, HFC'de evler kablo başucuna erişim ağını paylaşır.**

**Açıklama:**

| Özellik | DSL | HFC (Kablo) |
|---------|-----|------------|
| Fiziksel hat | Mevcut telefon hattı (bakır) | Koaksiyel + fiber (hibrit) |
| Bağlantı yapısı | **Ayrılmış** (her eve özel) | **Paylaşımlı** (komşular aynı ağı paylaşır) |
| İndirme hızı | 24–52 Mb/s | 40 Mb/s – 1.2 Gb/s |
| Yükleme hızı | 3.5–16 Mb/s | 30–100 Mb/s |
| Merkez nokta | DSLAM (merkezi ofis) | Kablo başucu (cable headend) |

**Paylaşımlı olmanın dezavantajı:** Komşular yoğun kullandığında HFC hızı düşebilir. DSL'de bu sorun yoktur.

---

### SORU 3 — Cevap: **B**

> **B) Çok yüksek iletim hızı, çok düşük hata oranı ve elektromanyetik gürültüden etkilenmemesi.**

**Açıklama:**  
Fiber optik, cam fiber içinde ışık atımları taşır — her atım bir bit.

**Avantajları:**
- **Hız:** 10'larca – 100'lerce Gb/s iletim hızı
- **Hata oranı:** Son derece düşük (çoklayıcılar birbirinden çok uzağa konulabilir)
- **EMI bağışıklığı:** Elektromanyetik gürültüden etkilenmez
- **Uzun mesafe:** Zayıflama çok az

**Dezavantajları:** Maliyetli, kırılgan, kurulumu zordur.

Karşılaştırma:
- Bükümlü çift: Kategori 5 → 100 Mb/s – 1 Gb/s; Kategori 6 → 10 Gb/s
- Koaksiyel: HFC'de kullanılır, çift yönlü, geniş bant
- Radyo: Kablosuz, çevresel etkilerden (yansıma, engelleme) etkilenir

---

### SORU 4 — Cevap: **C**

> **C) Saldırgan, aşırı sahte trafik göndererek hedef kaynağa erişimi engeller.**

**Açıklama:**  
DoS saldırısı üç aşamada gerçekleşir:
1. Hedef seç (sunucu veya ağ altyapısı)
2. Ele geçirilmiş cihazlara (botnet) gir
3. Bu cihazlardan hedefe yoğun paket gönder → kaynak tükenir → meşru kullanıcılar erişemez

**DDoS (Distributed DoS):** Çok sayıda ele geçirilmiş cihazdan (botnet) eşzamanlı saldırı.

**Diğer saldırı türleri:**
- A → Sniffer (paket dinleme)
- B → IP Spoofing
- D → Virus/Worm ile malware yayma

---

### SORU 5 — Cevap: **C**

> **C) Sahte gönderici IP adresi içeren paketler göndererek başka bir cihaz gibi görünür.**

**Açıklama:**  
IP Spoofing'de saldırgan paketlerin kaynak IP adresini taklit eder:
- Kimliğini gizleyebilir
- Başka bir sunucuyu kaynak gibi göstererek yansıma (reflection) saldırısı yapabilir
- Güven ilişkisine dayalı sistemleri kandırabilir

**Çözüm:** Giriş filtreleme (ingress filtering) — ağa giren paketlerin kaynak IP'si o ağa ait olmalı.

---

### SORU 6 — Cevap: **C**

> **C) Önbellekteki kopya hâlâ güncel; sunucu nesneyi tekrar göndermedi.**

**Açıklama:**  
Önemli HTTP durum kodları:

| Kod | Anlamı |
|-----|--------|
| **200 OK** | Başarılı, nesne yanıt içinde |
| **301 Moved Permanently** | Nesne taşındı, yeni adres `Location` başlığında |
| **304 Not Modified** | Önbellekteki kopya güncel, nesne gönderilmedi |
| **400 Bad Request** | İstek anlaşılamadı |
| **404 Not Found** | Nesne sunucuda yok |
| **505 HTTP Version Not Supported** | HTTP versiyonu desteklenmiyor |

304 yanıtı Koşullu GET mekanizmasının sonucudur — gereksiz veri transferini önler.

---

### SORU 7 — Cevap: **B**

> **B) Önbellekteki nesne güncel ise tekrar gönderilmemesi; `If-Modified-Since` başlığı.**

**Açıklama:**  
Koşullu GET'in işleyişi:

```
1. Önbellek HTTP isteğine şunu ekler:
   If-Modified-Since: Wed, 16 Apr 2025 10:00:00 GMT

2a. Nesne değişmişse → Sunucu: 200 OK + nesneyi gönderir
2b. Nesne değişmemişse → Sunucu: 304 Not Modified (nesne gönderilmez)
```

**Faydaları:**
- Nesne iletim gecikmesi ortadan kalkar
- Bağ kullanımı azalır
- Gereksiz bant genişliği harcanmaz

---

### SORU 8 — Cevap: **B**

> **B) POP3 mesajları sunucudan indirip (genellikle) siler; IMAP mesajları sunucuda saklar ve oturumlar arası klasör durumunu korur.**

**Açıklama:**

| Özellik | POP3 | IMAP |
|---------|------|------|
| Port | 110 | 143 |
| Mesaj yeri | İndirilir, sunucudan silinebilir | Sunucuda saklanır |
| Klasör desteği | Yok | Var |
| Oturumlar arası durum | **Yok** (durumsuz) | **Var** (durum saklar) |
| Çoklu cihaz | Sorunlu (farklı cihazda göremezsin) | Sorunsuz |

**POP3 modları:**
- **İndir-ve-sil:** Bir cihazda indirince diğerinde göremezsin
- **İndir-ve-sakla:** Farklı cihazlarda kopyalar oluşur

**IMAP'ın avantajı:** Telefon, tablet, bilgisayarda aynı e-postayı görebilirsin — mesajlar sunucuda tek yerde durur.

---

### SORU 9 — Cevap: **B**

> **B) Önbelleklenmiş DNS kaydının ne kadar süre geçerli kalacağını belirler; süre dolunca kayıt önbellekten silinir.**

**Açıklama:**  
DNS önbellekleme mekanizması:

```
Yerel DNS sunucusu bir eşlemeyi öğrenince → önbellekler
TTL süresi dolunca → önbellekten silinir → tekrar sorgu yapılır
```

**Sorun:** Eğer bir sunucunun IP adresi değişirse, eski TTL süresi dolmadan İnternet'in geri kalanı bu değişikliği bilemez.

**IP değişimi senaryosu:** Bir web sunucusu IP adresini değiştirdi. TTL = 24 saat ise, 24 saat boyunca bazı kullanıcılar eski IP'ye gitmeye devam edebilir.

**Not:** TTL değeri DNS kaydında (KK formatında) şöyle tutulur: **(isim, değer, tip, ys)** — ys = yaşam süresi (TTL).

---

### SORU 10 — Cevap: **B**

> **B) Yinelenmeli sorguda yerel DNS tüm çözümleme işini yaparak nihai cevabı döner; döngüsel sorguda her sunucu bir sonraki sunucunun adresini söyler.**

**Açıklama:**

**Döngüsel (Iterative) Sorgu:**
```
İstemci → Yerel DNS: "www.amazon.com nerede?"
Yerel DNS → Kök sunucu: "bilmiyorum, .com sunucusuna sor"
Yerel DNS → .com TLD sunucu: "bilmiyorum, amazon.com sunucusuna sor"
Yerel DNS → amazon.com sunucusu: "IP = 1.2.3.4"
Yerel DNS → İstemci: "IP = 1.2.3.4"
```

**Yinelenmeli (Recursive) Sorgu:**
```
İstemci → Yerel DNS: "www.amazon.com nerede?"
Yerel DNS → Kök sunucu: "sen bul ve bana söyle"
Kök sunucu → .com TLD: "sen bul ve bana söyle"
.com TLD → amazon.com: "IP nedir?"
Cevap zinciri geri döner
```

Yinelenmeli sorgu üst sunuculara fazla yük bindirdiği için pratikte genellikle döngüsel sorgu kullanılır.

---

### SORU 11 — Cevap: **B**

> **B) SSL uygulama katmanında çalışır; uygulamalar SSL kütüphaneleri aracılığıyla şifrelenmiş TCP bağlantısı kurar.**

**Açıklama:**  
SSL/TLS mimarisi:

```
Uygulama Katmanı → SSL kütüphanesi kullanır
Taşıma Katmanı   → TCP (değişmez)
```

TCP ve UDP başlı başına **şifreleme sağlamaz**. Şifreler açık metin olarak soketten geçerse İnternet üzerinde okunabilir.

**SSL şunları sağlar:**
- Şifrelenmiş TCP bağlantısı
- Veri bütünlüğü
- Uç-nokta kimlik doğrulama

**HTTPS = HTTP + SSL/TLS** (port 443)

---

### SORU 12 — Cevap: **B**

> **B) Hayır; hem IP adresi hem de port numarası birlikte gereklidir.**

**Açıklama:**  
IP adresi bir **cihazı** tanımlar, port numarası ise o cihazdaki **işlemi** tanımlar.

```
Örnek:
IP: 128.119.245.12 → gaia.cs.umass.edu cihazı
Port 80            → HTTP sunucu işlemi
Port 25            → SMTP posta sunucu işlemi
Port 443           → HTTPS işlemi
```

Aynı cihazda aynı anda çalışan işlemler:
- Web sunucusu (80)
- Posta sunucusu (25)
- DNS sunucusu (53)
- FTP sunucusu (21)

**Soket adresi = IP + Port** → işlemi dünya genelinde benzersiz tanımlar.

---

### SORU 13 — Cevap: **B**

> **B) İstemci-sunucu dağıtım süresi N ile doğrusal artarken, P2P dağıtım süresi her yeni üye yeni kapasite getirdiğinden çok daha yavaş büyür.**

**Açıklama:**  
Dağıtım süresi formülleri:

**İstemci-Sunucu:**
```
D(c-s) = max { NF/u_s , F/d_min }
N büyüdükçe NF/u_s doğrusal artar → sunucu darboğaz olur
```

**P2P:**
```
D(P2P) = max { F/u_s , F/d_min , NF/(u_s + Σu_i) }
N büyüdükçe hem payda (NF) hem bölen (u_s + Σu_i) büyür
→ her yeni üye yeni yükleme kapasitesi getirdiğinden süre çok daha yavaş artar
```

Grafik: İstemci-sunucu süresi N ile sınırsız artar; P2P süresi büyük N için neredeyse sabitlenir. Bu P2P'nin **öz ölçeklenebilirliğidir**.

---

### SORU 14 — Cevap: **B**

> **B) 16-bit birin tamamlayıcısı toplamı kullanılır; hata tespit edilince UDP paketi sessizce atılır.**

**Açıklama:**  
UDP Checksum hesaplama:

```
Gönderici:
1. Segment içeriğini 16-bit'lik parçalara böl
2. Tüm parçaları topla (birin tamamlayıcısı ile)
3. Toplama 1'in tamamlayıcısını al → checksum
4. Checksum'ı UDP başlığına yaz

Alıcı:
1. Aynı hesaplamayı yap
2. Gelen checksum + hesaplanan değer = 1111...1 olmalı
   → Değilse hata var → paket atılır (sessizce)
   → Eşitse hata yok (ama %100 garanti değil!)
```

**Sayısal örnek:**
```
Sözcük 1: 0110011001100000
Sözcük 2: 0101010101010101
Toplam:   1011101110110101
Tamamlayıcı: 0100010001001010 ← checksum
```

---

### SORU 15 — Cevap: **B**

> **B) UDP: yalnızca hedef port numarası (2-tuple); TCP: kaynak IP, kaynak port, hedef IP, hedef port (4-tuple)**

**Açıklama:**

**UDP çoklama çözme:**
```
Paket geldi → hedef port numarasına bak → o porta bağlı sokete yolla
Farklı kaynaklardan gelen, aynı hedef IP+port'u taşıyan paketler → AYNI sokete gider
```

**TCP çoklama çözme:**
```
Paket geldi → 4-tuple'ın tamamına bak
(kaynak IP, kaynak port, hedef IP, hedef port) → ÖZGÜN sokete gider
```

Bu fark neden önemli?
- Bir web sunucusu (port 80) aynı anda binlerce istemciye hizmet verebilir
- Her istemci için farklı bir TCP soketi → her bağlantı bağımsız yönetilir
- UDP'de ise tüm istemciler aynı soketi paylaşır

---

### SORU 16 — Cevap: **B**

> **B) ACK/NAK mesajlarının bozulabileceği sorununu çözmek için paketlere sıra numarası (0 ve 1) eklenmiştir.**

**Açıklama:**  
rdt versiyonlarının evrimi:

| Versiyon | Varsayım | Eklenen |
|----------|----------|---------|
| rdt1.0 | Kanal mükemmel | — |
| rdt2.0 | Bit hatası var | ACK/NAK |
| **rdt2.1** | ACK/NAK da bozulabilir | **Sıra numarası (0,1)** |
| rdt2.2 | ACK/NAK bozulabilir | NAK kaldırıldı, sadece ACK |
| rdt3.0 | Bit hatası + kayıp var | Zamanlayıcı |

**rdt2.0'ın sorunu:** ACK bozulursa gönderici ne yapacağını bilemez. Yeniden gönderirse alıcı bunu yeni veri mi kopya mı diye ayırt edemez.

**rdt2.1'in çözümü:** 0 ve 1 sıra numarası → alıcı kopya paketi tanıyıp yoksayar. Yalnızca 2 sıra numarası yeterlidir çünkü "dur ve bekle" protokolde her seferinde tek paket gönderilir.

---

### SORU 17 — Cevap: **B**

> **B) SYN: bağlantı kurma isteği, FIN: bağlantıyı kapatma isteği, RST: bağlantıyı anında sıfırlama**

**Açıklama:**  
TCP segment başlığındaki bayraklar (6 bit):

| Bayrak | İşlev |
|--------|-------|
| **URG** | Acil veri var (genellikle kullanılmaz) |
| **ACK** | ACK numarası geçerli |
| **PSH** | Veriyi hemen uygulamaya ilet |
| **RST** | Bağlantıyı anında sıfırla (hata durumu) |
| **SYN** | Bağlantı kurma isteği (3-yönlü elsıkışmada) |
| **FIN** | Bağlantı kapatma isteği |

**Kullanım senaryoları:**
- Normal bağlantı: SYN → SYN+ACK → ACK
- Normal kapanış: FIN → ACK → FIN → ACK
- Hatalı kapanış: RST (anında, karşı tarafı beklemeden)

---

### SORU 18 — Cevap: **B**

> **B) Sıra numarası segmentteki ilk byte'ın byte-akışı numarasını; ACK numarası karşı taraftan bir sonraki beklenen byte'ın numarasını gösterir.**

**Açıklama:**

```
Senaryo: İstemci "C" harfini gönderdi, sunucu "C" yi echo etti

İstemci → Sunucu:
  Sıra#=42, ACK#=79, Veri='C'
  (42: bu segmentteki ilk byte'ın numarası)
  (79: sunucudan sonraki beklenen byte)

Sunucu → İstemci:
  Sıra#=79, ACK#=43, Veri='C'
  (79: sunucu tarafında byte-akışı numarası)
  (43: istemciden 43. byte bekleniyor — 42+1)
```

**Toplu ACK:** ACK=43 demek "42 dahil tüm önceki byte'lar alındı, 43 bekliyorum" demektir.

---

### SORU 19 — Cevap: **B**

> **B) TahminiGDS = (1−α) × TahminiGDS + α × ÖrnekGDS ; α = 0.125**

**Açıklama:**  
EWMA (Exponential Weighted Moving Average):

```
TahminiGDS = (1 - 0.125) × TahminiGDS + 0.125 × ÖrnekGDS
           = 0.875 × TahminiGDS + 0.125 × ÖrnekGDS
```

**Neden EWMA?**
- Tek bir ölçüm çok değişken olabilir (ağ dalgalanmaları)
- Eski ölçümlerin ağırlığı üstel azalır: en son ölçüm %12.5, bir önceki %10.9, daha önceki %9.5...
- Sonuç: Değişimlere duyarlı ama gürültüye dirençli tahmin

**α = 0.125 (1/8) seçiminin sebebi:** Geçmiş geçmişe yeterince ağırlık verir, güncel değişimleri de yansıtır.

---

### SORU 20 — Cevap: **C**

> **C) TimeoutSüresi = TahminiGDS + 4 × DevGDS**

**Açıklama:**  
İki adımlı timeout hesabı:

**Adım 1 — Sapma hesapla:**
```
DevGDS = (1 - β) × DevGDS + β × |ÖrnekGDS - TahminiGDS|
         (genellikle β = 0.25)
```

**Adım 2 — Timeout belirle:**
```
TimeoutSüresi = TahminiGDS + 4 × DevGDS
```

**Neden 4 × DevGDS?**  
Güvenlik payı olarak çalışır. GDS çok değişkense (DevGDS büyük) → timeout süresi uzar. GDS kararlıysa (DevGDS küçük) → timeout ≈ TahminiGDS olur.

**Çok kısa timeout:** Gereksiz tekrar gönderim  
**Çok uzun timeout:** Kayıba geç tepki → bant genişliği israfı

---

### SORU 21 — Cevap: **B**

> **B) Gönderici aynı sıra numarası için 3 kopya ACK aldığında tetiklenir; timeout süresi dolmadan harekete geçildiği için gecikme çok daha azdır.**

**Açıklama:**

```
Gönderici: 1, 2, 3, 4, 5 numaralı segmentleri gönderir
Segment 2 kaybolur

Alıcı:
  Segment 1 geldi → ACK 2 gönder (2 bekliyorum)
  Segment 3 geldi → ACK 2 gönder (hâlâ 2 bekliyorum)
  Segment 4 geldi → ACK 2 gönder
  Segment 5 geldi → ACK 2 gönder

Gönderici 3 kopya ACK 2 aldı → HEMEN segment 2'yi tekrar gönder
(Timeout dolmasını BEKLEME)
```

**Neden 3?** 1 veya 2 kopya ACK sıra dışı teslimden kaynaklanıyor olabilir. 3 kopya ACK genellikle gerçek kayıpı işaret eder.

---

### SORU 22 — Cevap: **B**

> **B) Her iki taraf da FIN gönderebilir; FIN gönderen taraf bağlantının kendi yönündeki akışını kapatır...**

**Açıklama:**  
TCP bağlantı kapanışı (4 mesaj):

```
İstemci                    Sunucu
   |                          |
   |——— FIN ————————————————→|  "Ben göndermeyi bitirdim"
   |←——— ACK ————————————————|  "Anladım"
   |                          |  (Sunucu hâlâ gönderebilir)
   |←——— FIN ————————————————|  "Ben de bitirdim"
   |——— ACK ————————————————→|  "Anladım"
   |                          |
   [Bağlantı kapandı]
```

**Yarı kapalı bağlantı:** İstemci FIN gönderdi ama sunucu henüz göndermedi → istemci→sunucu kapalı, sunucu→istemci açık (HTTP yanıtı hâlâ gelebilir).

**Eşzamanlı FIN:** Her iki taraf da aynı anda FIN gönderebilir.

---

### SORU 23 — Cevap: **B**

> **B) Yavaş başlangıçtan tıkanıklık önleme fazına geçiş eşiğidir; kayıp durumunda kayıp anındaki cwnd değerinin yarısına ayarlanır.**

**Açıklama:**  
cwnd ve ssthresh ilişkisi:

```
Başlangıç: cwnd = 1 MSB, ssthresh = 64 KB (örnek)

Yavaş Başlangıç: cwnd < ssthresh → cwnd ikiye katlanır (üstel)
Tıkanıklık Önleme: cwnd ≥ ssthresh → cwnd her GDS'de +1 MSB (doğrusal)

Kayıp olunca:
  ssthresh = cwnd / 2   ← yeni eşik
  TCP Tahoe: cwnd = 1 MSB (yavaş başlangıca dön)
  TCP Reno:  cwnd = ssthresh (hızlı kurtarma)
```

**Örnek:**
```
cwnd = 12 MSB iken kayıp
→ ssthresh = 6 MSB
→ TCP Reno: cwnd = 6 MSB (doğrusal artışa devam)
→ TCP Tahoe: cwnd = 1 MSB (sıfırdan başla)
```

---

### SORU 24 — Cevap: **C**

> **C) İş hacmi ≈ (3/4) × W / GDS**

**Açıklama:**  
TCP iş hacmi analizi (yavaş başlangıç görmezden gelinirse):

```
W = kayıp olduğundaki pencere boyutu (byte)

Pencere büyümesi: W/2 → W arası (testere dişi)
Ortalama pencere = (W/2 + W) / 2 = 3W/4

Ortalama iş hacmi = (3/4 × W) / GDS bytes/sn
```

**Yüksek hız örneği:**
```
İstenilen iş hacmi: 10 Gb/sn
Segment boyutu: 1500 byte
GDS: 100 ms = 0.1 sn

Kayıp ihtimali L için:
İş hacmi = 1.22 × MSB / (GDS × √L)
10 × 10⁹ = 1.22 × 1500 / (0.1 × √L)
→ L ≈ 2 × 10⁻¹⁰ (son derece düşük kayıp gerekli!)
```

---

### SORU 25 — Cevap: **B**

> **B) Her TCP oturumu R/K bant genişliği almalıdır; ancak UDP sıkışma kontrolü uygulamadığı için sabit hızda gönderim yapar ve TCP oturumlarının payını azaltır.**

**Açıklama:**  
**TCP Adalet mekanizması:** AIMD sayesinde iki TCP oturumu aynı bağı paylaşırken zamanla eşit bant genişliğine yakınsarlar.

```
Oturum 1 ve 2 aynı bağı paylaşıyor:
Her ikisi de artırır → toplam bant genişliği aşılır
Her ikisi de azaltır → oran birbirine yaklaşır
→ Zamanla her biri R/2 alır
```

**UDP'nin adaleti bozması:**
- Çoklu-ortam uygulamaları TCP kullanmaz (sıkışma kontrolü gecikmeye neden olur)
- UDP sabit hızda gönderir, sıkışma olsa bile yavaşlamaz
- TCP oturumları sıkışma kontrolü nedeniyle yavaşlarken UDP yavaşlamaz
- Sonuç: UDP bant genişliğinin orantısız büyük kısmını alır

**Paralel TCP bağlantıları da adaleti bozar:**  
11 paralel TCP bağlantısı açan tarayıcı, 1 bağlantısı olan kullanıcıdan ~11 kat fazla bant genişliği alır.

---

## ÖZET TABLO

| # | Cevap | Konu |
|---|-------|------|
| 1 | B | Sakla-ve-Yolla Hesabı |
| 2 | B | DSL vs HFC Mimari Fark |
| 3 | B | Fiber Optik Özellikleri |
| 4 | C | DoS Saldırısı |
| 5 | C | IP Spoofing |
| 6 | C | HTTP 304 Not Modified |
| 7 | B | Koşullu GET |
| 8 | B | POP3 vs IMAP |
| 9 | B | DNS TTL |
| 10 | B | Döngüsel vs Yinelenmeli DNS Sorgusu |
| 11 | B | SSL/TLS |
| 12 | B | IP + Port Numarası |
| 13 | B | P2P vs İstemci-Sunucu Ölçeklenebilirlik |
| 14 | B | UDP Checksum |
| 15 | B | UDP 2-tuple vs TCP 4-tuple |
| 16 | B | rdt2.1 Sıra Numarası |
| 17 | B | TCP Bayrakları (SYN/FIN/RST) |
| 18 | B | TCP Sıra/ACK Numarası |
| 19 | B | EWMA RTT Tahmini |
| 20 | C | TCP Timeout Formülü |
| 21 | B | TCP Hızlı Tekrar Gönderim |
| 22 | B | TCP Bağlantı Sonlandırma |
| 23 | B | ssthresh Mekanizması |
| 24 | C | TCP İş Hacmi Formülü |
| 25 | B | TCP Adalet ve UDP |
