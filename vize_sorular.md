# Veri İletişimi ve Bilgisayar Ağları — Vize Soruları

**Ders:** Veri İletişimi ve Bilgisayar Ağları  
**Kaynak:** Kurose & Ross — Computer Networking: A Top-Down Approach (8. Baskı)  
**Kapsam:** Bölüm 1 (Tanıtım) · Bölüm 2 (Uygulama Katmanı) · Bölüm 3 (Taşıma Katmanı)  
**Toplam:** 25 Soru · Her soru 4 puan

---

## SORULAR

---

### SORU 1
Aşağıdakilerden hangisi **paket anahtarlamanın** devre anahtarlamaya göre en önemli avantajını ifade eder?

- A) Uçtan uca gecikme garantisi sağlar.
- B) Kaynaklar önceden rezerv edildiğinden performans sabittir.
- C) Ağ kaynaklarını paylaşarak daha fazla kullanıcıya hizmet verebilir.
- D) Ses ve görüntü uygulamaları için daha uygundur.

---

### SORU 2
Bir paket iletim gecikmesi hesaplanırken kullanılan formül hangisidir?  
*(L = paket boyutu bit, R = bağ kapasitesi bps)*

- A) d_iletim = R / L
- B) d_iletim = L × R
- C) d_iletim = L / R
- D) d_iletim = L + R

---

### SORU 3
Trafik yoğunluğu **La/R > 1** olduğunda ne gerçekleşir?

- A) Sıralanma gecikmesi sıfıra yaklaşır.
- B) Ortalama sıralanma gecikmesi sonsuza gider; sisteme giren iş miktarı servis edilebilecekten fazladır.
- C) Paket iletim hızı maksimuma ulaşır.
- D) Yönlendirici otomatik olarak yük dengelemesi yapar.

---

### SORU 4
Bir paketteki toplam uçtan uca gecikme dört bileşenden oluşur. Aşağıdakilerden hangisi **bu dört bileşenden biri değildir**?

- A) İşlem gecikmesi (d_işlem)
- B) Sıralanma gecikmesi (d_sıralanma)
- C) Şifreleme gecikmesi (d_şifreleme)
- D) Yayılma gecikmesi (d_yayılma)

---

### SORU 5
**Darboğaz bağ (bottleneck link)** kavramı ne anlama gelir?

- A) En yüksek bant genişliğine sahip bağlantı.
- B) Uçtan uca yol üzerinde iş hacmini kısıtlayan bağlantı.
- C) Yalnızca kablosuz ağlarda oluşan tıkanma noktası.
- D) Yönlendiricinin hafızasının dolduğu andaki bağlantı durumu.

---

### SORU 6
TCP/IP modelinde **taşıma katmanının** görevi nedir?

- A) Paketleri kaynaktan hedefe fiziksel olarak taşımak.
- B) Farklı cihazlar üzerindeki uygulamalar (işlemler) arasında uçtan uca mantıksal iletişim sağlamak.
- C) Bitleri elektrik sinyaline çevirerek kablo üzerinden iletmek.
- D) IP adreslerini MAC adreslerine dönüştürmek.

---

### SORU 7
OSI referans modelinde **İnternet modelinde yer almayan** iki katman hangisidir?

- A) Fiziksel ve Veri Bağlantı katmanları
- B) Sunum ve Oturum katmanları
- C) Ağ ve Taşıma katmanları
- D) Uygulama ve Fiziksel katmanlar

---

### SORU 8
**HTTP protokolü** ile ilgili aşağıdaki ifadelerden hangisi **yanlıştır**?

- A) HTTP, TCP üzerinde çalışır ve varsayılan port numarası 80'dir.
- B) HTTP durum bilgisi saklayan (stateful) bir protokoldür.
- C) Kalıcı olmayan HTTP'de her nesne için ayrı bir TCP bağlantısı açılır.
- D) HTTP, istemci-sunucu mimarisini kullanır.

---

### SORU 9
Kalıcı olmayan HTTP kullanıldığında, bir nesneyi almak için gereken süre yaklaşık olarak nedir?  
*(GDS = Gidiş-Dönüş Süresi, dosya iletim süresi = T)*

- A) GDS + T
- B) 2 × GDS + T
- C) 3 × GDS + T
- D) T

---

### SORU 10
Bir HTTP isteğinde **GET metodu** ile **POST metodu** arasındaki temel fark nedir?

- A) GET yalnızca HTTP/1.1'de, POST ise HTTP/1.0'da kullanılır.
- B) GET ile veri URL'ye eklenerek gönderilir; POST ile veri mesaj gövdesinde (body) gönderilir.
- C) GET güvenli bağlantı gerektirir, POST gerektirmez.
- D) GET sunucudan dosya siler, POST dosya yükler.

---

### SORU 11
HTTP **çerez (cookie)** mekanizması kaç bileşenden oluşur?

- A) 2
- B) 3
- C) 4
- D) 5

---

### SORU 12
Web **vekil sunucusu (proxy server)** kullanımının temel amacı nedir?

- A) Sunucu kimlik doğrulamasını güçlendirmek.
- B) İstemci isteklerini hedef sunucuya iletmeden karşılamak; böylece yanıt süresini kısaltmak ve erişim bağı trafiğini azaltmak.
- C) HTTP bağlantılarını şifrelemek.
- D) DNS sorgularını hızlandırmak.

---

### SORU 13
**FTP protokolü** ile ilgili aşağıdaki ifadelerden hangisi **doğrudur**?

- A) FTP kontrol ve veri transferi için tek bir TCP bağlantısı kullanır.
- B) FTP kontrol bağlantısını port 21, veri bağlantısını ayrı bir port üzerinden sağlar ve durum bilgisi saklar.
- C) FTP UDP tabanlı bir protokoldür.
- D) FTP durumsuz (stateless) bir protokoldür.

---

### SORU 14
**SMTP** ile **HTTP** arasındaki en temel fark nedir?

- A) SMTP güvenilir, HTTP güvenilmez veri transferi sağlar.
- B) SMTP bir **itme (push)** protokolüdür; HTTP ise **çekme (pull)** protokolüdür.
- C) HTTP port 25, SMTP port 80 kullanır.
- D) SMTP UDP, HTTP TCP kullanır.

---

### SORU 15
**DNS** sistemi neden merkezi tek bir sunucu yerine dağınık hiyerarşik yapı kullanır?

- A) Merkezi yapı kurulumu çok pahalıdır.
- B) Merkezi yapıda tek nokta arızası tüm sistemi durdurur, trafik hacmi yönetilemez ve bakım zorlaşır.
- C) Hiyerarşik yapı şifrelemeyi kolaylaştırır.
- D) Merkezi DNS yasal düzenlemeler nedeniyle yasaktır.

---

### SORU 16
DNS kayıt türü **MX** ne anlama gelir?

- A) Cihaz adını IP adresine eşler.
- B) Bir alan adı için yetkili isim sunucusunu gösterir.
- C) Bir alan adına karşılık gelen **posta sunucusunun** cihaz adını tutar.
- D) Takma adı (alias) kanonik isme eşler.

---

### SORU 17
BitTorrent'te **tit-for-tat** mekanizması nasıl çalışır?

- A) Bir üye yalnızca izleyiciden (tracker) parça alır, diğer üyelerle paylaşmaz.
- B) Bir üye kendisine en yüksek hızda parça gönderen 4 üyeye parça gönderir; her 30 saniyede rastgele bir üye de "iyimser" olarak beslenir.
- C) Üyeler parçaları alfabetik sıraya göre paylaşır.
- D) Sunucu tüm parçaları eşit hızda tüm üyelere dağıtır.

---

### SORU 18
**UDP** ile **TCP** arasındaki en temel fark nedir?

- A) UDP daha büyük başlık alanına sahipken TCP daha küçük başlık kullanır.
- B) UDP bağlantısız ve güvenilmez; TCP bağlantı odaklı, güvenilir ve akış/sıkışma kontrolü sağlar.
- C) UDP yalnızca yerel ağlarda kullanılabilir.
- D) TCP şifreleme sağlar, UDP sağlamaz.

---

### SORU 19
**rdt3.0** protokolünde, ACK mesajının kaybolması durumunda gönderici nasıl davranır?

- A) Bağlantıyı kapatır ve yeniden başlatır.
- B) Geri sayım zamanlayıcısı dolunca paketi tekrar gönderir; sıra numarası sayesinde alıcı kopya paketi tespit edip yoksayar.
- C) NAK göndererek alıcıyı uyarır.
- D) Paketi bir sonraki paketle birleştirerek yeniden gönderir.

---

### SORU 20
**Geri-Git-N (Go-Back-N)** ile **Seçici Tekrar (Selective Repeat)** arasındaki en önemli fark nedir?

- A) GGN daha büyük pencere boyutu kullanır.
- B) GGN'de timeout olduğunda penceredeki tüm paketler yeniden gönderilir; Seçici Tekrar'da sadece ACK alınmayan paket yeniden gönderilir.
- C) Seçici Tekrar UDP tabanlıdır.
- D) GGN alıcıda önbellekleme yaparken Seçici Tekrar yapmaz.

---

### SORU 21
TCP'de **3-yönlü elsıkışma (three-way handshake)** hangi sırayla gerçekleşir?

- A) SYN → ACK → FIN
- B) SYN → SYN-ACK → ACK
- C) ACK → SYN → SYN-ACK
- D) FIN → ACK → SYN

---

### SORU 22
TCP **akış kontrolü (flow control)** ne amaçla kullanılır?

- A) Ağdaki yönlendirici önbelleklerinin taşmasını önlemek.
- B) Göndericinin alıcının önbelleğini aşırı veri göndererek taşırmasını engellemek; **rwnd** alanı ile boş önbellek miktarı bildirilir.
- C) Paketlerin doğru sırada iletilmesini garantilemek.
- D) Bağlantı kurulum süresini kısaltmak.

---

### SORU 23
TCP sıkışma kontrolünde **AIMD (Additive Increase Multiplicative Decrease)** ne anlama gelir?

- A) Her GDS'de cwnd değerini ikiyle çarp; kayıp olunca sıfırla.
- B) Her GDS'de cwnd değerini 1 MSB artır (toplamalı artış); kayıp olunca cwnd değerini yarıya indir (çarpmalı azalış).
- C) cwnd değerini sabit tut, sadece ssthresh değerini değiştir.
- D) Kayıp olmasa da cwnd değerini düzenli aralıklarla yarıya indir.

---

### SORU 24
TCP **yavaş başlangıç (slow start)** aşamasında cwnd nasıl artırılır?

- A) Her GDS'de cwnd 1 MSB artırılır (doğrusal artış).
- B) cwnd sabit tutulur, ssthresh aşılana kadar beklenir.
- C) Her ACK alındığında cwnd 1 MSB artırılır; bu da her GDS'de cwnd'nin ikiye katlanmasına yol açar (üstel artış).
- D) cwnd değeri rastgele belirlenir.

---

### SORU 25
**TCP Tahoe** ve **TCP Reno** arasındaki fark nedir?

- A) TCP Tahoe UDP tabanlıdır, TCP Reno TCP tabanlıdır.
- B) Her ikisinde de timeout durumunda cwnd = 1 MSB yapılır; ancak **3 kopya ACK** geldiğinde TCP Tahoe cwnd'yi 1 MSB'ye düşürürken, TCP Reno cwnd'yi yarıya indirir (hızlı kurtarma).
- C) TCP Reno akış kontrolü yaparken TCP Tahoe yapmaz.
- D) TCP Tahoe daha yeni bir sürümdür.

---

---

## CEVAPLAR VE AÇIKLAMALAR

---

### SORU 1 — Cevap: **C**

> **C) Ağ kaynaklarını paylaşarak daha fazla kullanıcıya hizmet verebilir.**

**Açıklama:**  
Devre anahtarlamada kaynaklar çağrı boyunca rezerv edilir — kullanılmasa da boşa gider. Paket anahtarlamada ise kaynaklar tüm kullanıcılar tarafından paylaşılır; istatistiksel çoğullama sayesinde çok daha fazla kullanıcı aynı bağı kullanabilir.

**Örnek:** 1 Mb/s bağ, her kullanıcı aktifken 100 kb/s kullansın ve zamanın %10'unda aktif olsun:
- Devre anahtarlama: max 10 kullanıcı
- Paket anahtarlama: 35 kullanıcı ile 11'inden fazlasının aynı anda aktif olma ihtimali < 0.0004

**Yanlış şıklar neden yanlış?**
- A ve B: Bunlar devre anahtarlamanın özelliğidir.
- D: Ses/görüntü için gecikme garantisi gerekir; bu devre anahtarlamanın avantajıdır.

---

### SORU 2 — Cevap: **C**

> **C) d_iletim = L / R**

**Açıklama:**  
İletim gecikmesi, paketin tüm bitlerinin bağa "basılması" için geçen süredir.

```
d_iletim = L (bit) / R (bit/sn) = saniye
```

**Örnek:** L = 8000 bit, R = 1 Gb/sn = 10⁹ bps
```
d_iletim = 8000 / 10⁹ = 8 mikrosaniye
```

**Dikkat:** İletim gecikmesi ≠ yayılma gecikmesi. Yayılma gecikmesi paketin fiziksel ortamda ilerlemesi için geçen süredir (d_yayılma = mesafe / yayılma hızı).

---

### SORU 3 — Cevap: **B**

> **B) Ortalama sıralanma gecikmesi sonsuza gider; sisteme giren iş miktarı servis edilebilecekten fazladır.**

**Açıklama:**  
La/R trafik yoğunluğunu ifade eder:
- La/R ≈ 0 → sıra yok, gecikme küçük
- La/R → 1 → sıra oluşur, gecikme büyür
- La/R > 1 → gelen iş > giden iş → sıra sonsuza büyür → paket kaybı başlar

Burada L paket boyutu, a ortalama paket varış hızı, R bağ kapasitesidir.

---

### SORU 4 — Cevap: **C**

> **C) Şifreleme gecikmesi (d_şifreleme)**

**Açıklama:**  
Düğüm (node) gecikmesinin dört bileşeni şunlardır:

```
d_düğüm = d_işlem + d_sıralanma + d_iletim + d_yayılma
```

| Bileşen | Açıklama |
|---------|----------|
| d_işlem | Bit hata kontrolü, çıkış bağına karar (genelde < msec) |
| d_sıralanma | Çıkış bağını bekleme süresi |
| d_iletim | Tüm bitleri bağa basmak için gereken süre (L/R) |
| d_yayılma | Bitin bağ boyunca ilerlemesi için gereken süre |

Şifreleme gecikmesi bu modelde ayrı bir bileşen olarak tanımlanmamıştır.

---

### SORU 5 — Cevap: **B**

> **B) Uçtan uca yol üzerinde iş hacmini kısıtlayan bağlantı.**

**Açıklama:**  
Uçtan uca iş hacmi şu formülle hesaplanır:

```
İş hacmi = min(R_c, R_s, R/N)
```

- R_c: istemci erişim bağı kapasitesi
- R_s: sunucu erişim bağı kapasitesi
- R/N: N bağlantının paylaştığı omurga kapasitesi

Bu üçünden en küçük olanı darboğaz oluşturur ve tüm transferi sınırlar.

---

### SORU 6 — Cevap: **B**

> **B) Farklı cihazlar üzerindeki uygulamalar (işlemler) arasında uçtan uca mantıksal iletişim sağlamak.**

**Açıklama:**  
Katman karşılaştırması:

| Katman | Görevi | Birim |
|--------|--------|-------|
| Fiziksel | Bit iletimi | Bit |
| Veri Bağlantı | Komşu düğümler arası | Çerçeve |
| Ağ | Cihaz-cihaz (kaynak→hedef) | Datagram |
| **Taşıma** | **İşlem-işlem (uçtan uca)** | **Segment** |
| Uygulama | Ağ uygulamaları | Mesaj |

Ev benzetmesi: Ağ katmanı = posta servisi (evden eve), Taşıma katmanı = ev içinde mektupları çocuklara dağıtan kişi (işlemden işleme).

---

### SORU 7 — Cevap: **B**

> **B) Sunum ve Oturum katmanları**

**Açıklama:**  
OSI 7 katman: Fiziksel, Veri Bağlantı, Ağ, Taşıma, **Oturum, Sunum**, Uygulama  
TCP/IP 5 katman: Fiziksel, Veri Bağlantı, Ağ, Taşıma, Uygulama

Sunum ve Oturum katmanları TCP/IP modelinde **uygulama katmanına dahil edilmiştir** — bu hizmetler gerekiyorsa uygulama kendisi sağlar.

---

### SORU 8 — Cevap: **B**

> **B) HTTP durum bilgisi saklayan (stateful) bir protokoldür.**

**Açıklama:**  
HTTP **durumsuz (stateless)** bir protokoldür. Sunucu, önceki istemci isteklerine dair hiçbir bilgi saklamaz. Her istek bağımsız olarak işlenir.

**Neden durumsuz?** Durum bilgisi saklamak karmaşıklık yaratır: sunucu veya istemci çökerse durum bilgilerinin senkronizasyonu gerekir.

**Durum nasıl taklit edilir?** Çerezler (cookies) HTTP'nin durumsuzluğunu aşmak için kullanılan bir mekanizmadır — ama bu HTTP'yi stateful yapmaz, çerez istemcide saklanır.

---

### SORU 9 — Cevap: **B**

> **B) 2 × GDS + T**

**Açıklama:**  
Kalıcı olmayan HTTP'de her nesne için ayrı TCP bağlantısı kurulur:

```
1. TCP bağlantı isteği gönder         → 1 GDS
2. HTTP isteği gönder + ilk yanıt gel → 1 GDS  
3. Dosyanın tamamı iletilir            → T (dosya iletim süresi)
─────────────────────────────────────────
Toplam: 2 × GDS + T
```

**Kalıcı HTTP'de:** Bağlantı açık kalır, her sonraki nesne için yaklaşık **1 GDS** yeterlidir.

---

### SORU 10 — Cevap: **B**

> **B) GET ile veri URL'ye eklenerek gönderilir; POST ile veri mesaj gövdesinde (body) gönderilir.**

**Açıklama:**

```
GET örneği:
GET /search?q=bilgisayar+ağları HTTP/1.1

POST örneği:
POST /login HTTP/1.1
Host: example.com

username=ayse&password=1234
```

GET: veriyi URL'e ekler → tarayıcı geçmişinde görünür, önbelleklenebilir  
POST: veriyi gövdede taşır → form verisi, dosya yükleme için uygundur

HTTP/1.0'da GET ve POST bulunur. HTTP/1.1 bunlara ek olarak PUT ve DELETE ekler.

---

### SORU 11 — Cevap: **C**

> **C) 4**

**Açıklama:**  
Çerez mekanizmasının 4 bileşeni:

1. **HTTP yanıt mesajındaki** `Set-Cookie` başlık satırı
2. **HTTP istek mesajındaki** `Cookie` başlık satırı
3. **İstemcide** tarayıcı tarafından yönetilen çerez dosyası
4. **Sunucuda** geri-uç veritabanı

**Ne için kullanılır?** Yetkilendirme, alışveriş sepeti, kişisel tavsiyeler, kullanıcı oturum durumu (web e-posta).

---

### SORU 12 — Cevap: **B**

> **B) İstemci isteklerini hedef sunucuya iletmeden karşılamak; böylece yanıt süresini kısaltmak ve erişim bağı trafiğini azaltmak.**

**Açıklama:**  
Vekil sunucu aynı anda hem istemci hem sunucu gibi davranır.

**Sayısal örnek:** İsabet oranı %40 olan vekil sunucu:
```
Toplam gecikme = 0.6 × (hedef sunucu gecikmesi) + 0.4 × (vekil önbelleği)
              = 0.6 × 2.01 sn + 0.4 × (milisaniyeler)
              ≈ 1.2 sn
```
10 kat hızlı internet almaktan hem daha hızlı hem de daha ucuz!

---

### SORU 13 — Cevap: **B**

> **B) FTP kontrol bağlantısını port 21, veri bağlantısını ayrı bir port üzerinden sağlar ve durum bilgisi saklar.**

**Açıklama:**  
FTP iki ayrı bağlantı kullanır:
- **Kontrol bağlantısı (port 21):** Komutlar gönderilir (USER, PASS, LIST, RETR, STOR) — "bant dışı" kontrol
- **Veri bağlantısı (ayrı port):** Gerçek dosya transferi gerçekleşir; her transfer için yeni bağlantı açılır

FTP ayrıca **durum bilgisi saklar:** mevcut klasör, kullanıcı oturumu vb.

Bu özellik FTP'yi HTTP'den ayırır — HTTP durumsuz, FTP durum bilgisi tutan bir protokoldür.

---

### SORU 14 — Cevap: **B**

> **B) SMTP bir itme (push) protokolüdür; HTTP ise çekme (pull) protokolüdür.**

**Açıklama:**

| Özellik | SMTP | HTTP |
|---------|------|------|
| Yön | **İtme** (push): gönderici sunucuya aktarır | **Çekme** (pull): istemci sunucudan çeker |
| Port | 25 | 80 |
| Taşıma | TCP | TCP |
| Format | 7-bit ASCII | Binary dahil her şey |
| Mesaj | Birden fazla nesne tek mesajda | Her nesne ayrı yanıtta |

E-posta akışı: Gönderici → SMTP → Alıcı sunucu → POP3/IMAP → Alıcı

---

### SORU 15 — Cevap: **B**

> **B) Merkezi yapıda tek nokta arızası tüm sistemi durdurur, trafik hacmi yönetilemez ve bakım zorlaşır.**

**Açıklama:**  
Merkezi DNS'nin sorunları:
1. **Tek nokta arızası:** Sunucu çökerse İnternet çöker
2. **Trafik hacmi:** Tüm DNS sorguları tek noktaya gelir
3. **Uzak merkezi veritabanı:** Dünya genelinde gecikme farklılıkları
4. **Bakım:** Milyarlarca kayıt tek yerde güncellenmeli

**Çözüm — Hiyerarşik yapı:**
```
Kök sunucular (13 adet, dünya genelinde dağıtık)
    └── TLD sunucuları (.com, .org, .edu, .tr …)
            └── Yetkili DNS sunucuları (amazon.com, google.com …)
                    └── Yerel DNS sunucuları (ISP, üniversite)
```

---

### SORU 16 — Cevap: **C**

> **C) Bir alan adına karşılık gelen posta sunucusunun cihaz adını tutar.**

**Açıklama:**  
DNS kayıt türleri:

| Tür | isim | değer |
|-----|------|-------|
| **A** | Cihaz adı | IP adresi |
| **NS** | Alan adı (foo.com) | Yetkili isim sunucusunun adı |
| **CNAME** | Takma ad (alias) | Kanonik (gerçek) isim |
| **MX** | Alan adı | **Posta sunucusunun** cihaz adı |

**Örnek:** `google.com` için MX kaydı → `mail.google.com` → A kaydı → IP adresi

---

### SORU 17 — Cevap: **B**

> **B) Bir üye kendisine en yüksek hızda parça gönderen 4 üyeye parça gönderir; her 30 saniyede rastgele bir üye de "iyimser" olarak beslenir.**

**Açıklama:**  
BitTorrent tit-for-tat mekanizması:

```
Her 10 saniyede → En yüksek hızda parça gönderen 4 üye belirlenir
                  (Bu 4'ü "unchoked" — aktif ortaklar)
                  Diğerleri "choked" — geçici olarak engellenir

Her 30 saniyede → Rastgele 1 üye "iyimserçe" seçilir
                  Bu üyeye parça gönderilir
                  Bu üye bir süre sonra en iyi 4'e girebilir
```

Bu mekanizma "bedavacılığı" (free-riding) önler ve karşılıklı paylaşımı teşvik eder.

---

### SORU 18 — Cevap: **B**

> **B) UDP bağlantısız ve güvenilmez; TCP bağlantı odaklı, güvenilir ve akış/sıkışma kontrolü sağlar.**

**Açıklama:**

| Özellik | UDP | TCP |
|---------|-----|-----|
| Bağlantı | Yok (connectionless) | Var (3-yönlü elsıkışma) |
| Güvenilirlik | Yok | Var (ACK, tekrar gönderim) |
| Sıra garantisi | Yok | Var |
| Akış kontrolü | Yok | Var (rwnd) |
| Sıkışma kontrolü | Yok | Var (cwnd, AIMD) |
| Başlık boyutu | 8 byte | 20 byte (minimum) |
| Hız | Daha hızlı | Daha yavaş |

**UDP ne zaman tercih edilir?** DNS, SNMP, canlı yayın, çevrimiçi oyunlar — gecikme hassas ve az kayıp tolere edilebilir uygulamalar.

---

### SORU 19 — Cevap: **B**

> **B) Geri sayım zamanlayıcısı dolunca paketi tekrar gönderir; sıra numarası sayesinde alıcı kopya paketi tespit edip yoksayar.**

**Açıklama:**  
rdt3.0, rdt2.2'yi şu şekilde geliştirir: kayıp paketler için **zamanlayıcı** ekler.

```
Senaryo: ACK kayboldu
─────────────────────────────
Gönderici paket 0 gönderir
Alıcı paket 0'ı alır, ACK 0 gönderir
ACK 0 kaybolur
Gönderici zamanlayıcı dolunca paket 0'ı tekrar gönderir
Alıcı paket 0'ı tekrar alır → sıra numarasına bakarak kopya olduğunu anlar → yoksayar → ACK 0 tekrar gönderir
```

**Sıra numarasının önemi:** Hangi paketin kopya olduğunu anlamak için şart — olmasa aynı paketin kopyasını yeni veri sanabiliriz.

---

### SORU 20 — Cevap: **B**

> **B) GGN'de timeout olduğunda penceredeki tüm paketler yeniden gönderilir; Seçici Tekrar'da sadece ACK alınmayan paket yeniden gönderilir.**

**Açıklama:**

| Özellik | Geri-Git-N | Seçici Tekrar |
|---------|-----------|---------------|
| Timeout davranışı | **Tüm pencere** tekrar gönderilir | **Sadece ilgili paket** tekrar gönderilir |
| ACK türü | Toplu (cumulative) ACK | Bireysel ACK |
| Alıcı önbellek | Yok — sıra dışı paketler atılır | Var — sıra dışı paketler önbelleklenir |
| Bant genişliği | Daha az verimli | Daha verimli |

**GGN örneği:** N=4 pencere, paket 2 kaybolursa → paket 2, 3, 4, 5 yeniden gönderilir  
**ST örneği:** N=4 pencere, paket 2 kaybolursa → sadece paket 2 yeniden gönderilir

---

### SORU 21 — Cevap: **B**

> **B) SYN → SYN-ACK → ACK**

**Açıklama:**

```
İstemci                          Sunucu
   |                                |
   |——— SYN (seq=x) ————————————→  |   1. İstemci bağlantı ister
   |                                |
   |  ←——— SYN-ACK (seq=y, ack=x+1)|   2. Sunucu kabul eder
   |                                |
   |——— ACK (ack=y+1) —————————→   |   3. İstemci onaylar
   |                                |
   |========= VERİ AKIŞI =========|   Bağlantı kuruldu!
```

**Neden 3-yönlü?** 2-yönlü elsıkışma değişken gecikme ve paket kaybı nedeniyle güvenilir değildir. 3-yönlü yapı her iki tarafın da gönderme ve alma kapasitesini doğrular.

---

### SORU 22 — Cevap: **B**

> **B) Göndericinin alıcının önbelleğini aşırı veri göndererek taşırmasını engellemek; rwnd alanı ile boş önbellek miktarı bildirilir.**

**Açıklama:**  
TCP akış kontrolü mekanizması:

```
Alıcı, TCP segment başlığındaki rwnd (receive window) alanında
boş önbellek miktarını göndericiye bildirir.

Gönderici: ACK almadan gönderilmiş veri ≤ rwnd
```

**Akış kontrolü ≠ Sıkışma kontrolü:**
- Akış kontrolü: alıcı önbelleğini korur (uçtan uca)
- Sıkışma kontrolü: ağ içindeki yönlendirici önbelleklerini korur

---

### SORU 23 — Cevap: **B**

> **B) Her GDS'de cwnd değerini 1 MSB artır (toplamalı artış); kayıp olunca cwnd değerini yarıya indir (çarpmalı azalış).**

**Açıklama:**

```
Toplamalı Artış (Additive Increase):
cwnd = cwnd + 1 MSB (her GDS)
→ Yavaş, temkinli büyüme

Çarpmalı Azalış (Multiplicative Decrease):
cwnd = cwnd / 2 (kayıp tespit edilince)
→ Hızlı tepki
```

Bu asimetrik davranış "testere dişi" (sawtooth) grafiği oluşturur ve ağı çökmeden korurken bant genişliğini verimli kullanmayı sağlar.

---

### SORU 24 — Cevap: **C**

> **C) Her ACK alındığında cwnd 1 MSB artırılır; bu da her GDS'de cwnd'nin ikiye katlanmasına yol açar (üstel artış).**

**Açıklama:**

```
Yavaş Başlangıç:
GDS 1: cwnd = 1 MSB → 1 segment gönder → 1 ACK al → cwnd = 2
GDS 2: cwnd = 2 MSB → 2 segment gönder → 2 ACK al → cwnd = 4
GDS 3: cwnd = 4 MSB → 4 segment gönder → 4 ACK al → cwnd = 8
...
```

"Yavaş" başlangıç adına rağmen büyüme **üsteldir** — isim, başlangıç cwnd'sinin küçük (1 MSB) olmasından gelir.

**ssthresh'e ulaşınca:** Üstel artış biter, **Tıkanıklık Önleme** (Congestion Avoidance) fazına geçilir → her GDS'de +1 MSB (doğrusal artış).

---

### SORU 25 — Cevap: **B**

> **B) Her ikisinde de timeout durumunda cwnd = 1 MSB yapılır; ancak 3 kopya ACK geldiğinde TCP Tahoe cwnd'yi 1 MSB'ye düşürürken, TCP Reno cwnd'yi yarıya indirir (hızlı kurtarma).**

**Açıklama:**

| Durum | TCP Tahoe | TCP Reno |
|-------|-----------|----------|
| Timeout | cwnd = 1, yavaş başlangıç | cwnd = 1, yavaş başlangıç |
| 3 kopya ACK | cwnd = 1, yavaş başlangıç | cwnd = cwnd/2, **hızlı kurtarma** |

**Neden 3 kopya ACK farklı?**  
3 kopya ACK geliyorsa ağ hâlâ çalışıyor (ACK'lar iletiliyor) — bu hafif bir sıkışma işaretidir. TCP Reno bunu fark edip daha yumuşak tepki verir. Timeout ise daha ciddi bir sorundur.

---

## ÖZET TABLO

| # | Cevap | Konu |
|---|-------|------|
| 1 | C | Paket vs Devre Anahtarlama |
| 2 | C | İletim Gecikmesi Formülü |
| 3 | B | Trafik Yoğunluğu La/R |
| 4 | C | Gecikme Bileşenleri |
| 5 | B | Darboğaz Bağ |
| 6 | B | Taşıma Katmanı Görevi |
| 7 | B | OSI vs TCP/IP |
| 8 | B | HTTP Özellikleri |
| 9 | B | HTTP Yanıt Süresi (2GDS+T) |
| 10 | B | GET vs POST |
| 11 | C | Çerez Bileşenleri |
| 12 | B | Vekil Sunucu Amacı |
| 13 | B | FTP Özellikleri |
| 14 | B | SMTP vs HTTP |
| 15 | B | DNS Merkezi Olmama Nedeni |
| 16 | C | DNS MX Kaydı |
| 17 | B | BitTorrent Tit-for-Tat |
| 18 | B | UDP vs TCP |
| 19 | B | rdt3.0 ACK Kaybı |
| 20 | B | GGN vs Seçici Tekrar |
| 21 | B | TCP 3-Yönlü Elsıkışma |
| 22 | B | TCP Akış Kontrolü |
| 23 | B | AIMD |
| 24 | C | TCP Yavaş Başlangıç |
| 25 | B | TCP Tahoe vs Reno |
