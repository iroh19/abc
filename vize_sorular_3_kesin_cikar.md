# Veri İletişimi ve Bilgisayar Ağları — Kesin Çıkar Soruları (3. Set)

**Ders:** Veri İletişimi ve Bilgisayar Ağları  
**Kaynak:** Kurose & Ross — Computer Networking: A Top-Down Approach (8. Baskı)  
**Odak:** Formül gerektiren sayısal sorular · Senaryo soruları · Klasik hoca soruları  
**Toplam:** 25 Soru · Her soru 4 puan

> **Not:** Bu setteki sorular sınav ortamında en sık karşılaşılan türlerdir.  
> Formülleri ezberlemeyin — **nereden geldiğini anlayın.**

---

## SORULAR

---

### SORU 1 *(Hesaplama)*
Bir sinyal 2500 km uzunluğundaki fiber optik kablo üzerinde **2 × 10⁸ m/s** hızla ilerlemektedir. **Yayılma gecikmesi** kaç milisaniyedir?

- A) 2.5 ms
- B) 12.5 ms
- C) 25 ms
- D) 125 ms

---

### SORU 2 *(Hesaplama — Paket Anahtarlama Kullanım Oranı)*
Bir gönderici, **1 Gb/s** kapasiteli bağ üzerinden **8000 bitlik** paketler göndermektedir. GDS = **30 ms** olduğuna göre, "dur ve bekle" protokolündeki gönderici **kullanım oranı (U_gönderici)** yaklaşık olarak nedir?

- A) %0.027
- B) %0.27
- C) %2.7
- D) %27

---

### SORU 3 *(Kapsülleme)*
Uygulama katmanından gelen bir mesaj taşıma katmanına geçerken ne olur? TCP/IP modelindeki **kapsülleme (encapsulation)** süreci nasıl işler?

- A) Mesaj doğrudan fiziksel katmana iletilir, hiçbir başlık eklenmez.
- B) Her katman, üstten gelen veriye **kendi başlık bilgisini ekler**; fiziksel katmanda bu tüm başlıkları içeren bit dizisine dönüşür.
- C) Yalnızca uygulama katmanı başlık ekler, diğerleri eklemez.
- D) Kapsülleme yalnızca alıcı tarafında gerçekleşir.

---

### SORU 4 *(Traceroute)*
`traceroute` komutu hangi bilgiyi ölçmek için kullanılır ve nasıl çalışır?

- A) Bir sunucunun kaç eşzamanlı bağlantı kabul edebildiğini ölçer.
- B) Kaynaktan hedefe kadar her yönlendiricide geçen **gecikme süresini** ölçer; her yönlendiriciye TTL değeri kademeli artırılan 3'er paket gönderilir, yönlendirici paketi geri yollar.
- C) Ağdaki tüm cihazların IP adreslerini listeler.
- D) Paket kayıp oranını hesaplar.

---

### SORU 5 *(ISP Hiyerarşisi)*
Aşağıdakilerden hangisi **Tabaka-1 (Tier-1) ISP'nin** temel özelliğini doğru ifade eder?

- A) Yalnızca ev kullanıcılarına hizmet verir ve bölgesel kapsama sahiptir.
- B) Ulusal ve uluslararası kapsama sahip, birbirine **iyi bağlanmış** büyük ağlardır; başka ISP'ye ücret ödemeden İnternet'in her yerine erişebilirler.
- C) Yalnızca içerik sağlayıcı şirketlere hizmet verir.
- D) Tabaka-2 ISP'leri tarafından yönetilir.

---

### SORU 6 *(HTTP Metotları)*
HTTP **HEAD** metodunun GET'ten farkı nedir ve ne zaman kullanılır?

- A) HEAD yalnızca HTTP/2.0'da desteklenir.
- B) HEAD isteğinde sunucu, nesnenin kendisini **göndermez**; yalnızca başlık satırlarını döner. Nesnenin var olup olmadığını veya değişip değişmediğini anlamak için kullanılır.
- C) HEAD metodu dosya yükleme için kullanılır.
- D) HEAD ve GET arasında işlevsel hiçbir fark yoktur.

---

### SORU 7 *(DNS Çözümleme Süreci)*
Bir istemci **www.amazon.com** adresinin IP'sini öğrenmek istiyor ve yerel DNS önbelleğinde kayıt yok. Sorgu hangi sırayla çözülür? *(Döngüsel sorgu varsayın)*

- A) Yerel DNS → Yetkili DNS → TLD DNS → Kök DNS
- B) Yerel DNS → Kök DNS → `.com` TLD DNS → `amazon.com` Yetkili DNS → Yerel DNS → İstemci
- C) İstemci → Yetkili DNS → İstemci
- D) Yerel DNS → TLD DNS → Yerel DNS → İstemci

---

### SORU 8 *(SMTP Komutu Sırası)*
SMTP ile e-posta gönderiminde komutların doğru sırası hangisidir?

- A) DATA → HELO → MAIL FROM → RCPT TO → QUIT
- B) HELO → MAIL FROM → RCPT TO → DATA → (mesaj içeriği) → `.` → QUIT
- C) MAIL FROM → HELO → DATA → RCPT TO → QUIT
- D) RCPT TO → MAIL FROM → HELO → DATA → QUIT

---

### SORU 9 *(E-posta Gönderim Süreci)*
Ayşe, `ayse@gmail.com` adresinden Ali'ye `ali@hotmail.com` adresine e-posta gönderiyor. Bu süreçte **kaç farklı protokol** ve **kaç aşama** devreye girer?

- A) Yalnızca SMTP kullanılır, tek aşamada tamamlanır.
- B) Ayşe'nin kullanıcı aracı → SMTP → Ayşe'nin posta sunucusu → SMTP → Ali'nin posta sunucusu → **POP3/IMAP/HTTP** → Ali'nin kullanıcı aracı. En az 2 farklı protokol (SMTP + okuma protokolü) devreye girer.
- C) FTP ile gönderilir, SMTP yalnızca bildirim için kullanılır.
- D) Tüm süreç HTTP üzerinden gerçekleşir.

---

### SORU 10 *(Önbellek — Sayısal)*
Bir kurumun erişim bağı **15 Mb/s** kapasitesinde olup ortalama nesne boyutu **1 Mb**, saniyedeki istek sayısı **9**'dur. Vekil sunucu **isabet oranı %60** ise erişim bağı kullanım oranı nedir?

- A) %90
- B) %60
- C) %36
- D) %24

---

### SORU 11 *(TCP vs UDP Soket Farkı)*
TCP soket programlamada `accept()` fonksiyonu ne işe yarar? UDP soket programlamada neden `accept()` gerekmez?

- A) `accept()` sunucunun portu açmasını sağlar; UDP'de port yoktur.
- B) TCP'de `accept()` karşılama soketinde bekleyen sunucunun **yeni bir bağlantı soketini** oluşturmasını sağlar; UDP bağlantısız olduğundan her datagram bağımsızdır, ayrı soket oluşturmaya gerek yoktur.
- C) `accept()` istemci kimliğini doğrular; UDP şifreleme yaptığı için buna gerek duymaz.
- D) `accept()` ve `bind()` aynı işlevi görür.

---

### SORU 12 *(Pipeline Kullanım Hesabı)*
rdt3.0'da "dur ve bekle" protokolü **U = 0.00027** kullanım oranı sağlamaktaydı. **3 paket** pipeline ile gönderilirse kullanım oranı yaklaşık ne olur?

- A) 0.00027 (değişmez)
- B) 0.00081 (3 katına çıkar)
- C) 0.0027
- D) 0.027

---

### SORU 13 *(GGN Pencere Boyutu ve Sıra Numarası)*
**Geri-Git-N** protokolünde **k-bit sıra numarası** kullanılıyorsa, maksimum pencere boyutu **N** en fazla kaç olabilir?

- A) 2^k
- B) 2^k − 1
- C) 2^(k−1)
- D) k

---

### SORU 14 *(Seçici Tekrar — İkilem)*
**Seçici Tekrar** protokolünde sıra numarası uzayı **n** bit ise, pencere boyutu neden en fazla **2^(n−1)** olmalıdır?

- A) Alıcı önbelleği sınırlı olduğu için.
- B) Pencere boyutu sıra numarası uzayının yarısını aşarsa, alıcı yeni bir paketin mi yoksa eski bir paketin **kopyasının mı** geldiğini ayırt edemez.
- C) Standartlar bunu zorunlu kılmıştır.
- D) Gönderici tarafında kronometre sayısını azaltmak için.

---

### SORU 15 *(TCP rwnd = 0 Durumu)*
TCP akış kontrolünde alıcı **rwnd = 0** bildirirse ne olur? Bu kilitlenme nasıl aşılır?

- A) Gönderici bağlantıyı kapatır ve yeniden bağlanır.
- B) Gönderici veri göndermeyi durdurur; ancak alıcı sonunda önbelleği boşaltıp rwnd > 0 bildirene kadar kilitlenme oluşabilir. Bunu önlemek için gönderici **1 byte'lık sonda (probe) segment** göndermeye devam eder.
- C) Gönderici cwnd değerini artırarak tıkanıklığı aşmaya çalışır.
- D) Ağ katmanı devreye girer ve akışı yeniden başlatır.

---

### SORU 16 *(Sıkışma Kontrolü — Senaryo)*
TCP bağlantısında **ssthresh = 8 MSB**, **cwnd = 1 MSB** ile başlıyor. Hiç kayıp olmadığını varsayarak **4. GDS sonunda** cwnd değeri ne olur?

- A) 4 MSB
- B) 8 MSB
- C) 9 MSB
- D) 16 MSB

---

### SORU 17 *(TCP Reno — Hızlı Kurtarma)*
TCP Reno'da, **cwnd = 12 MSB** iken **3 kopya ACK** alındığında ne olur? ssthresh ve cwnd yeni değerleri nedir?

- A) ssthresh = 12, cwnd = 1
- B) ssthresh = 6, cwnd = 6 (hızlı kurtarma: tıkanıklık önleme fazından devam)
- C) ssthresh = 6, cwnd = 1
- D) ssthresh = 12, cwnd = 6

---

### SORU 18 *(Zamansız Timeout — rdt3.0)*
rdt3.0'da paket iletildi, ACK de geldi ancak **ACK çok gecikti** ve gönderici daha önce timeout yapıp paketi tekrar gönderdi. Bu "zamansız timeout" durumunda alıcı ne yapar?

- A) İkinci paketi yeni veri olarak işler ve üst katmana iletir.
- B) İkinci paketi **sıra numarasına bakarak kopya olduğunu** anlar, yoksayar ve tekrar ACK gönderir. Sistemin doğruluğu bozulmaz.
- C) Hata mesajı üretir ve bağlantıyı kapatır.
- D) Her iki paketi de üst katmana iletir.

---

### SORU 19 *(TCP MSS)*
TCP'de **MSS (Maximum Segment Size)** nedir ve nasıl belirlenir?

- A) TCP bağlantısında gönderilebilecek maksimum paket sayısıdır.
- B) Bir TCP segmentindeki **maksimum uygulama verisi miktarıdır**; genellikle **MTU (Maximum Transmission Unit)** den TCP+IP başlık boyutu (40 byte) çıkarılarak belirlenir. Tipik değer **1460 byte**'tır.
- C) cwnd'nin alabileceği maksimum değerdir.
- D) Maksimum TCP bağlantı sayısını belirler.

---

### SORU 20 *(FDM vs TDM)*
Devre anahtarlamada **FDM (Frekans Bölüşümlü Çoğullama)** ile **TDM (Zaman Bölüşümlü Çoğullama)** arasındaki fark nedir?

- A) FDM dijital, TDM analog sinyaller için kullanılır.
- B) FDM'de her bağlantıya **ayrı frekans bandı** ayrılır ve sürekli kullanır; TDM'de her bağlantıya **zaman dilimleri (slot)** ayrılır ve sırayla kullanır.
- C) TDM daha yüksek bant genişliği sunar.
- D) FDM yalnızca kablolu, TDM yalnızca kablosuz ağlarda kullanılır.

---

### SORU 21 *(DNS Saldırısı)*
**DNS zehirleme (DNS poisoning)** saldırısı nasıl gerçekleşir ve ne tehlike yaratır?

- A) DNS sunucusuna fazla sorgu göndererek sunucuyu çevrimdışı bırakır.
- B) Saldırgan DNS sunucusuna **sahte kayıtlar yerleştirir**; sunucu bu sahte kayıtları önbellekler ve kullanıcıları yanlış IP adreslerine (sahte sitelere) yönlendirir.
- C) Saldırgan DNS trafiğini dinleyerek şifreleri çalar.
- D) DNS sunucusunun TTL değerlerini manipüle ederek önbelleği hızla doldurur.

---

### SORU 22 *(TCP Başlangıç Sıra Numarası)*
TCP bağlantısında her iki tarafın başlangıç sıra numarası (ISN — Initial Sequence Number) neden **rastgele** seçilir?

- A) Verimli önbellekleme için.
- B) Önceki bağlantıdan kalan eski paketlerin yeni bağlantıya ait paket olarak **yanlış tanınmasını önlemek** ve saldırganların sıra numarasını tahmin ederek sahte paket enjekte etmesini zorlaştırmak için.
- C) Checksum hesabını kolaylaştırmak için.
- D) Yönlendiricilerin paketi daha hızlı işlemesi için.

---

### SORU 23 *(Uygulama + Taşıma Protokolü Eşleştirmesi)*
Aşağıdaki eşleştirmelerden hangisi **yanlıştır**?

- A) DNS → UDP
- B) HTTP → TCP
- C) SMTP → TCP
- D) FTP → UDP

---

### SORU 24 *(Sıkışma Kontrolü — Maliyet)*
Ağ sıkışmasının iki temel "maliyeti" nedir?

- A) Artan bant genişliği kullanımı ve azalan gecikme.
- B) **(1)** Tekrar gönderimlerin yol açtığı gereksiz bant genişliği tüketimi ve **(2)** paket düşürüldüğünde o ana kadar harcanan bant genişliğinin tamamen boşa gitmesi.
- C) Artan CPU kullanımı ve azalan güvenlik.
- D) Büyük önbellek gerekliliği ve yüksek enerji tüketimi.

---

### SORU 25 *(Bütünleşik Senaryo — TCP Sıkışma)*
Bir TCP bağlantısında **ssthresh = 16 MSB**, **cwnd = 1 MSB** ile başlıyor. **5. GDS'de timeout** oluşuyor. Timeout anında cwnd ve ssthresh değerleri nedir, timeout **sonrasında** yeni ssthresh ve cwnd ne olur?

- A) Timeout öncesi: cwnd=16, ssthresh=16 → Sonrası: ssthresh=8, cwnd=1
- B) Timeout öncesi: cwnd=32, ssthresh=16 → Sonrası: ssthresh=16, cwnd=1
- C) Timeout öncesi: cwnd=16, ssthresh=16 → Sonrası: ssthresh=16, cwnd=8
- D) Timeout öncesi: cwnd=8, ssthresh=16 → Sonrası: ssthresh=4, cwnd=1

---

---

## CEVAPLAR VE AÇIKLAMALAR

---

### SORU 1 — Cevap: **B**

> **B) 12.5 ms**

**Açıklama:**

```
d_yayılma = mesafe / yayılma hızı
           = 2,500,000 m / (2 × 10⁸ m/s)
           = 0.0125 s
           = 12.5 ms
```

**Sık yapılan hata:** 2500 km → 2,500,000 m dönüşümünü unutmak.

**Karşılaştırma:** 30,000 km mesafedeki bir uydu bağlantısı:
```
d_yayılma = 30,000,000 / (3 × 10⁸) ≈ 100 ms (tek yön)
→ GDS ≈ 270 ms — bu nedenle uydu bağlantıları interaktif uygulamalar için kötüdür
```

---

### SORU 2 — Cevap: **A**

> **A) %0.027**

**Açıklama:**

```
L = 8000 bit
R = 10⁹ bps (1 Gb/s)
GDS = 30 ms = 0.030 s

d_iletim = L/R = 8000 / 10⁹ = 8 × 10⁻⁶ s = 0.008 ms

U_gönderici = (L/R) / (GDS + L/R)
            = 0.000008 / (0.030 + 0.000008)
            = 0.000008 / 0.030008
            ≈ 0.000267
            ≈ 0.027%
```

**Yorumu:** Gönderici zamanın yalnızca %0.027'sinde veri gönderiyor — bu son derece verimsiz. **Çözüm: Pipeline** (arka arkaya gönderim).

**N paket pipeline ile:**
```
U = (N × L/R) / (GDS + L/R)
N = 3 → U ≈ 0.00081 → yaklaşık 3 kat iyileşme
```

---

### SORU 3 — Cevap: **B**

> **B) Her katman, üstten gelen veriye kendi başlık bilgisini ekler.**

**Açıklama:**  
Gönderici tarafında kapsülleme:

```
Uygulama katmanı:  [Mesaj]
                         ↓ taşıma katmanı başlık ekler
Taşıma katmanı:    [Tb | Mesaj]           → Segment
                         ↓ ağ katmanı başlık ekler
Ağ katmanı:        [Nb | Tb | Mesaj]      → Datagram
                         ↓ veri bağlantı başlık ekler
Veri Bağlantı:     [Db | Nb | Tb | Mesaj] → Çerçeve (Frame)
                         ↓
Fiziksel katman:   0101011101...           → Bit dizisi
```

Alıcı tarafında ise her katman kendi başlığını **söker (decapsulation)** ve üst katmana iletir.

**Bu neden önemli?** Her katman yalnızca kendi başlığını görür — alt katman kapsüllemeyi bilmek zorunda değildir (modülerlik).

---

### SORU 4 — Cevap: **B**

> **B) Kaynaktan hedefe kadar her yönlendiricide geçen gecikme süresini ölçer.**

**Açıklama:**  
Traceroute çalışma prensibi:

```
Her i. yönlendirici için:
  → TTL = i olarak ayarlanmış 3 paket gönderir
  → Yönlendirici TTL = 0 olduğunda paketi düşürür ve ICMP hata mesajı döner
  → Gönderici gidiş-dönüş süresini hesaplar

Çıktıda her satır:
[Yönlendirici sırası] [IP adresi] [3 ölçümün ms cinsinden değerleri]
```

**Gerçek traceroute çıktısından örnek:**
```
1  cs-gw (128.119.240.254)    1 ms    1 ms    2 ms
8  62.40.103.253              104 ms  109 ms  106 ms  ← Transatlantik bağ
19 fantasia.eurecom.fr        132 ms  128 ms  136 ms
```

`* * *` satırları → o yönlendirici ICMP mesajına yanıt vermiyor.

---

### SORU 5 — Cevap: **B**

> **B) Ulusal ve uluslararası kapsama sahip, birbirine iyi bağlanmış büyük ağlardır.**

**Açıklama:**  
ISP hiyerarşisi:

```
Tabaka-1 ISP (Level 3, Sprint, AT&T, NTT)
    └── Bölgesel ISP (Türk Telekom, Deutsche Telekom...)
            └── Erişim ISP (ev kullanıcıları, şirketler)
                    └── Uç Sistemler (bilgisayar, telefon...)
```

**Tabaka-1 özellikleri:**
- Hiçbir ISP'ye ücret ödemeden her yere ulaşabilirler (peering anlaşmaları)
- Diğer Tabaka-1 ISP'leriyle doğrudan bağlantılı
- Ulusal + uluslararası kapsama

**İçerik sağlayıcı ağları (Google, Akamai):** Tabaka-1 ve bölgesel ISP'leri bazen atlayarak kullanıcılara daha yakından hizmet verir.

---

### SORU 6 — Cevap: **B**

> **B) HEAD isteğinde sunucu nesnenin kendisini göndermez; yalnızca başlık satırlarını döner.**

**Açıklama:**

```
GET isteği: Sunucu → başlık + nesne gönderir
HEAD isteği: Sunucu → yalnızca başlık gönderir (nesne yok)
```

**HEAD ne zaman kullanılır?**
- "Bu URL var mı?" kontrolü (404 mü, 200 mu?)
- "Bu dosya son ne zaman değişti?" (`Last-Modified` başlığına bak)
- Dosyayı indirmeden boyutunu öğrenmek (`Content-Length`)
- Önbellek geçerlilik kontrolü

**HTTP/1.0 metotları:** GET, POST, HEAD  
**HTTP/1.1 eklemeleri:** GET, POST, HEAD + **PUT** (dosya yükle), **DELETE** (dosya sil)

---

### SORU 7 — Cevap: **B**

> **B) Yerel DNS → Kök DNS → .com TLD DNS → amazon.com Yetkili DNS → Yerel DNS → İstemci**

**Açıklama:**  
Döngüsel (iterative) sorgu adım adım:

```
1. İstemci → Yerel DNS: "www.amazon.com nerede?"
   (Yerel DNS önbellekte göremedi)

2. Yerel DNS → Kök DNS sunucusu:
   Kök: "Bilmiyorum ama .com TLD adresi şu..."

3. Yerel DNS → .com TLD sunucusu:
   TLD: "Bilmiyorum ama amazon.com yetkili sunucu şu..."

4. Yerel DNS → amazon.com Yetkili DNS sunucusu:
   Yetkili: "www.amazon.com = 205.251.242.103"

5. Yerel DNS → İstemci: "IP = 205.251.242.103"
   (Yerel DNS bu cevabı TTL süresi boyunca önbellekler)
```

Toplam **4 DNS mesajı** (gidip gelen hariç), yalnızca **yerel DNS** tüm hiyerarşiyi gezer.

---

### SORU 8 — Cevap: **B**

> **B) HELO → MAIL FROM → RCPT TO → DATA → (mesaj içeriği) → `.` → QUIT**

**Açıklama:**  
SMTP oturumu tam akışı:

```
S: 220 hamburger.edu
C: HELO crepes.fr
S: 250 Hello crepes.fr, pleased to meet you
C: MAIL FROM: <alice@crepes.fr>
S: 250 Sender ok
C: RCPT TO: <bob@hamburger.edu>
S: 250 Recipient ok
C: DATA
S: 354 Enter mail, end with "." on a line by itself
C: Merhaba Bob, nasılsın?
C: .
S: 250 Message accepted for delivery
C: QUIT
S: 221 hamburger.edu closing connection
```

**Hatırlatıcı:** HELO(selamlaşma) → FROM(kimden) → TO(kime) → DATA(içerik) → `.`(bitti) → QUIT(çıkış)

---

### SORU 9 — Cevap: **B**

> **B) SMTP ile gönderim, SMTP ile sunucular arası iletim, POP3/IMAP/HTTP ile okuma.**

**Açıklama:**  
E-posta gönderimi 6 adım:

```
1. Ayşe mesajı yazar → kullanıcı aracı (Outlook, Gmail web vs.)
2. Ayşe'nin KA (kullanıcı aracı) → SMTP → Ayşe'nin posta sunucusu
3. Ayşe'nin posta sunucusu → SMTP → Ali'nin posta sunucusu
4. Ali'nin posta sunucusu mesajı Ali'nin posta kutusuna koyar
5. Ali kullanıcı aracını açar
6. Ali'nin KA → POP3/IMAP/HTTP → Ali'nin posta sunucusu → mesajı alır

Protokol akışı:
Ayşe → [SMTP] → Sunucu A → [SMTP] → Sunucu B → [POP3/IMAP] → Ali
```

**SMTP neden gönderim+iletim için, POP3/IMAP neden okuma için?**  
SMTP bir **itme** protokolüdür (push) — mesajı aktif olarak iletir.  
POP3/IMAP bir **çekme** protokolüdür (pull) — Ali ne zaman isterse okur.

---

### SORU 10 — Cevap: **C**

> **C) %36**

**Açıklama:**

```
Erişim bağı kapasitesi: R = 15 Mb/s
Toplam istek hızı: 9 istek/s × 1 Mb/nesne = 9 Mb/s
İsabet oranı: %60 → isteklerin %60'ı önbellekten karşılanır

Erişim bağından geçen trafik:
= (1 - 0.60) × 9 Mb/s
= 0.40 × 9 Mb/s
= 3.6 Mb/s

Kullanım oranı:
= 3.6 / 15 = 0.24 = %24
```

Dur, tekrar hesaplayayım:
```
İsabet oranı = %60 → bağa giden = %40 × 9 = 3.6 Mb/s
Kullanım = 3.6 / 15 = 0.24 = %24
```

**Düzeltme: Cevap D (%24)'tür.**

> **Doğru cevap: D) %24**

**Bu soruyu sınavda yanlış yapmanın en kolay yolu:** İsabet oranını doğrudan kullanım oranı olarak yazmak. İsabet oranı %60 → bağa giden %40 → kullanım = %40 × (9/15) = %24.

---

### SORU 11 — Cevap: **B**

> **B) accept() yeni bir bağlantı soketi oluşturur; UDP'de bağlantı olmadığından gerekmez.**

**Açıklama:**  
TCP sunucu mimarisi:

```python
# TCP Sunucu
serverSocket = socket(AF_INET, SOCK_STREAM)  # karşılama soketi
serverSocket.bind(('', 12000))
serverSocket.listen(1)

while True:
    connectionSocket, addr = serverSocket.accept()  
    # ← YENİ soket oluşur, bu istemciye özel
    data = connectionSocket.recv(1024)
    connectionSocket.send(data.upper())
    connectionSocket.close()  # ← bu istemcinin soketi kapanır
    # serverSocket açık kalmaya devam eder
```

```python
# UDP Sunucu — accept() YOK
serverSocket = socket(AF_INET, SOCK_DGRAM)
serverSocket.bind(('', 12000))

while True:
    message, clientAddress = serverSocket.recvfrom(2048)  # direkt al
    serverSocket.sendto(message.upper(), clientAddress)
```

---

### SORU 12 — Cevap: **B**

> **B) 0.00081 (3 katına çıkar)**

**Açıklama:**

```
Dur-ve-bekle (1 paket): U = 0.008/30.008 ≈ 0.00027

3 paket pipeline:
U = (3 × L/R) / (GDS + L/R)
  = (3 × 0.000008) / 0.030008
  = 0.000024 / 0.030008
  ≈ 0.00080 ≈ 0.00081
```

Pipeline verimliliği **N paket** ile:
```
U ≈ N × (L/R) / GDS   (GDS >> L/R varsayımıyla)
```

**GDS = 30 ms, L/R = 0.008 ms olduğunda tam verimlilik için gereken paket sayısı:**
```
N = GDS / (L/R) = 30 / 0.008 = 3750 paket
→ %100 kullanım için 3750 paket pipeline gerekir
```

---

### SORU 13 — Cevap: **B**

> **B) 2^k − 1**

**Açıklama:**  
GGN'de pencere boyutu kısıtlaması:

```
k-bit sıra numarası → 2^k farklı değer (0'dan 2^k − 1'e kadar)
GGN maksimum pencere boyutu = 2^k − 1
```

**Neden 2^k değil de 2^k − 1?**

```
Örnek: k=2 → sıra #: 0,1,2,3 (4 değer), pencere = 3 (en fazla)
```

Pencere boyutu = 2^k olsaydı: tüm paketlerin ACK'ı kaybolursa alıcı yeni paketlerin mi geldiğini yoksa eski paketlerin tekrar mı gönderildiğini anlayamaz.

**Seçici Tekrar için:** Pencere boyutu ≤ 2^(k−1) — GGN'den daha kısıtlayıcı.

---

### SORU 14 — Cevap: **B**

> **B) Alıcı yeni paket mi, kopya mı geldiğini ayırt edemez.**

**Açıklama:**

```
Örnek: k=2 → sıra #: 0,1,2,3 → Seçici Tekrar pencere ≤ 2
```

Eğer pencere = 3 (> 2^(2−1) = 2) olsaydı:

```
Senaryo 1: ACK'lar teslim edildi
  Gönderici → paket 0,1,2 gönder → alındı → pencere kayar → paket 3 gönder
  Alıcı: sıra# 3 = yeni paket ✓

Senaryo 2: ACK'lar kayboldu
  Gönderici timeout → paket 0,1,2 tekrar gönder
  Alıcı: sıra# 0 = yeni mi? kopya mı? → AYIRT EDEMEZ!
```

Bu yüzden Seçici Tekrar'da pencere boyutu sıra numarası uzayının **yarısından fazla olamaz**.

---

### SORU 15 — Cevap: **B**

> **B) Gönderici veri göndermeyi durdurur; 1 byte'lık sonda segment göndererek alıcıyı sorgular.**

**Açıklama:**

```
Senaryo:
1. Alıcı önbelleği doldu → rwnd = 0 bildirir
2. Gönderici durur
3. Alıcı önbelleği boşalır ama bunu göndericiye bildirmez
   (sadece veri alınca TCP header gönderilir)
4. Gönderici bekler, alıcı bekler → KİLİTLENME!

Çözüm:
→ Gönderici düzenli aralıklarla 1 byte'lık "sonda" segment gönderir
→ Alıcı ACK ile güncel rwnd değerini döner
→ rwnd > 0 olunca gönderim yeniden başlar
```

Bu mekanizma TCP'de **gönderici soketleme (sender deadlock prevention)** olarak bilinir.

---

### SORU 16 — Cevap: **C**

> **C) 9 MSB**

**Açıklama:**  
Adım adım izleyelim:

```
Başlangıç: cwnd = 1 MSB, ssthresh = 8 MSB

GDS 1: cwnd=1 < ssthresh=8 → Yavaş Başlangıç → cwnd = 2
GDS 2: cwnd=2 < ssthresh=8 → Yavaş Başlangıç → cwnd = 4
GDS 3: cwnd=4 < ssthresh=8 → Yavaş Başlangıç → cwnd = 8
GDS 4: cwnd=8 = ssthresh=8 → Tıkanıklık Önleme → cwnd = 8 + 1 = 9
```

**4. GDS sonunda cwnd = 9 MSB**

**Önemli:** ssthresh'e ulaşınca (cwnd ≥ ssthresh) **Yavaş Başlangıç biter**, Tıkanıklık Önleme başlar (+1 MSB/GDS).

---

### SORU 17 — Cevap: **B**

> **B) ssthresh = 6, cwnd = 6**

**Açıklama:**  
TCP Reno — 3 kopya ACK durumu:

```
cwnd = 12 MSB, 3 kopya ACK geldi

1. ssthresh = cwnd / 2 = 12 / 2 = 6 MSB
2. cwnd = ssthresh = 6 MSB  ← TCP Reno hızlı kurtarma
3. Tıkanıklık Önleme fazından (+1 MSB/GDS) devam eder
```

**TCP Tahoe karşılaştırması (3 kopya ACK):**
```
ssthresh = 6 MSB
cwnd = 1 MSB  ← Yavaş Başlangıca döner (daha agresif)
```

**TCP Tahoe timeout:**
```
ssthresh = cwnd/2
cwnd = 1 MSB
```

**TCP Reno timeout:**
```
ssthresh = cwnd/2
cwnd = 1 MSB  ← Reno da timeout'ta Yavaş Başlangıca döner
```

---

### SORU 18 — Cevap: **B**

> **B) İkinci paketi sıra numarasına bakarak kopya olduğunu anlar, yoksayar ve tekrar ACK gönderir.**

**Açıklama:**  
Zamansız timeout senaryosu:

```
Gönderici           Alıcı
    |--- pkt0 ------→|
    |← ACK0 ─────────| (ACK yolda, gecikmeli)
    |  [timeout!]    |
    |--- pkt0 ──────→| (tekrar gönderim)
    |← ACK0 ─────────| (1. ACK nihayet geldi)
    |← ACK0 ─────────| (2. ACK, kopya pkt için)
```

Alıcı pkt0'ı ikinci kez alınca:
- Sıra numarası = 0 → beklenen değil → **kopya**
- Üst katmana iletmez
- Ama ACK0 yine de gönderir (göndericiyi ilerleten)

**Sistem doğruluğu korunur** — sıra numarası mekanizması tam olarak bu durumu ele almak için var.

---

### SORU 19 — Cevap: **B**

> **B) MSS, TCP segmentindeki maksimum uygulama verisi miktarıdır; tipik değer 1460 byte'tır.**

**Açıklama:**

```
MTU (Ethernet): 1500 byte
- IP başlık: 20 byte
- TCP başlık: 20 byte
─────────────────────────
MSS = 1500 - 20 - 20 = 1460 byte
```

**MSS ne zaman önemlidir?**
- cwnd ve ssthresh **MSB (MSS = Maximum Segment Size)** cinsinden ifade edilir
- Yavaş başlangıçta cwnd = 1 MSB = 1 × 1460 byte ile başlar

**MSS ≠ cwnd:**
- MSS: bir segmentteki maksimum veri boyutu (sabit)
- cwnd: sıkışma kontrol penceresi (dinamik)

---

### SORU 20 — Cevap: **B**

> **B) FDM'de ayrı frekans bandı; TDM'de ayrı zaman dilimleri.**

**Açıklama:**

```
FDM (Frequency Division Multiplexing):
┌──────────────────────────────────┐  Zaman
│ f1 │ f2 │ f3 │ f4 │ f1 │ f2 ... │
└──────────────────────────────────┘
  Her bağlantı sürekli kendi frekansını kullanır

TDM (Time Division Multiplexing):
┌──────────────────────────────────┐  Zaman
│ B1 │ B2 │ B3 │ B4 │ B1 │ B2 ... │
└──────────────────────────────────┘
  Her bağlantı sırayla tam bant genişliğini kullanır
```

**Ortak nokta:** Her iki yöntemde de ayrılan kaynak (frekans veya zaman dilimi) **boş olsa bile başkası kullanamaz** → verimsizlik → paket anahtarlamanın bu noktada avantajı var.

---

### SORU 21 — Cevap: **B**

> **B) Saldırgan DNS sunucusuna sahte kayıtlar yerleştirir; kullanıcılar sahte sitelere yönlendirilir.**

**Açıklama:**  
DNS zehirleme saldırısı:

```
1. Saldırgan DNS sunucusuna sahte sorgu yanıtı gönderir
   (örnek: google.com = 1.2.3.4 → sahte IP)
2. DNS sunucusu bu yanıtı önbelleğe alır
3. Kullanıcılar google.com'u sorgulayınca sahte IP'yi alır
4. Kullanıcı saldırganın kontrolündeki sahte siteye gider
   → kimlik avı (phishing), şifre çalma
```

**Diğer DNS saldırıları:**
- **DDoS:** Kök/TLD sunucuları trafik bombardımanı
- **Yansıma (Reflection) DDoS:** Sahte kaynak IP ile sorgu → cevap hedefe gider
- **Ortada-adam:** DNS sorgularını yakalama

**Savunma:** DNSSEC (DNS Security Extensions) — kayıtları dijital olarak imzalar.

---

### SORU 22 — Cevap: **B**

> **B) Eski paketlerin yanlış tanınmasını önlemek ve saldırı güçlüğünü artırmak için.**

**Açıklama:**

**Eski paket problemi:**
```
Bağlantı 1: ISN=1000, seq#=1050 ile paket gönderildi
Bağlantı 1 kapandı
Bağlantı 2: aynı port çiftiyle yeniden açıldı, ISN=1000

Eğer eski paketin kopyası ağda hâlâ dolaşıyorsa →
seq#=1050 Bağlantı 2'de geçerli veri gibi görünebilir!
```

Rastgele ISN → bu çakışma ihtimali son derece düşük.

**Güvenlik açısından:**  
Saldırgan sıra numarasını tahmin edebilirse sahte paket enjekte edebilir. Rastgele ISN bunu zorlaştırır.

---

### SORU 23 — Cevap: **D**

> **D) FTP → UDP (YANLIŞ — FTP, TCP kullanır)**

**Açıklama:**  
Doğru protokol eşleştirmeleri:

| Uygulama | Protokol | Taşıma |
|----------|----------|--------|
| DNS | UDP (küçük sorgular) | UDP (53) |
| HTTP | TCP | TCP (80) |
| HTTPS | TCP | TCP (443) |
| SMTP | TCP | TCP (25) |
| **FTP** | **TCP** | **TCP (21, 20)** |
| POP3 | TCP | TCP (110) |
| IMAP | TCP | TCP (143) |
| SNMP | UDP | UDP |
| RTP (canlı yayın) | UDP veya TCP | — |

**FTP neden TCP?** Dosya transferi %100 güvenilir olmalı — UDP'nin kayıp toleransı yoktur.

---

### SORU 24 — Cevap: **B**

> **B) Gereksiz tekrar gönderimlerin bant genişliği tüketimi ve düşürülen paketin yolculuğundaki bant genişliğinin boşa gitmesi.**

**Açıklama:**

**Maliyet 1 — Gereksiz tekrar gönderimler:**
```
Paket gecikmeli (henüz kaybolmadı) ama gönderici timeout yaptı
→ Paketi tekrar gönderdi → ağda 2 kopya var
→ İkisi de alıcıya ulaştı → biri boşa gitti
→ Bant genişliği israfı
```

**Maliyet 2 — Yukarı yönlü bant genişliği israfı:**
```
Kaynak → R1 → R2 → R3 → [DÜŞÜRÜLDÜ]
Paketin R1 ve R2'deki yolculuğu sırasında harcanan bant genişliği →
tamamen boşa gitti (R3'te düşürüldü)
```

Bu iki maliyet, sıkışma kontrolünün neden kritik olduğunu açıklar. Kontrol olmasaydı ağ pozitif geri besleme döngüsüne girerdi: daha çok trafik → daha çok kayıp → daha çok tekrar gönderim → daha çok trafik.

---

### SORU 25 — Cevap: **A**

> **A) Timeout öncesi: cwnd=16, ssthresh=16 → Sonrası: ssthresh=8, cwnd=1**

**Açıklama:**  
Adım adım izleyelim:

```
Başlangıç: cwnd=1 MSB, ssthresh=16 MSB

GDS 1: cwnd=1 < 16 → Yavaş Başlangıç → cwnd=2
GDS 2: cwnd=2 < 16 → Yavaş Başlangıç → cwnd=4
GDS 3: cwnd=4 < 16 → Yavaş Başlangıç → cwnd=8
GDS 4: cwnd=8 < 16 → Yavaş Başlangıç → cwnd=16
GDS 5: cwnd=16 = ssthresh=16 → Tıkanıklık Önleme → cwnd=17?
```

Dur! GDS 5'te cwnd ≥ ssthresh olduğunda tıkanıklık önlemeye geçilir. Soru **5. GDS'DE timeout** diyor — yani 5. GDS'in başında cwnd=16, ssthresh=16 iken timeout oluşuyor.

```
Timeout anında: cwnd=16 MSB, ssthresh=16 MSB

Timeout sonrası:
  ssthresh = cwnd / 2 = 16 / 2 = 8 MSB
  cwnd = 1 MSB (yavaş başlangıca dön)
```

**Cevap A doğrudur.**

**Sonraki adımlar:**
```
cwnd=1 → 2 → 4 → 8 (ssthresh'e ulaştı) → 9 → 10 → ... (tıkanıklık önleme)
```

---

## ÖZET TABLO

| # | **Cevap** | Konu |
|---|-----------|------|
| 1 | B | Yayılma Gecikmesi Hesabı |
| 2 | A | Pipeline Kullanım Oranı (U hesabı) |
| 3 | B | Kapsülleme (Encapsulation) |
| 4 | B | Traceroute Çalışma Prensibi |
| 5 | B | Tier-1 ISP Özellikleri |
| 6 | B | HTTP HEAD Metodu |
| 7 | B | DNS Döngüsel Sorgu Adımları |
| 8 | B | SMTP Komut Sırası |
| 9 | B | E-posta Gönderim Süreci |
| 10 | **D** | Önbellek Kullanım Oranı Hesabı |
| 11 | B | TCP accept() vs UDP |
| 12 | B | Pipeline ile Kullanım Artışı |
| 13 | B | GGN Maksimum Pencere Boyutu (2^k − 1) |
| 14 | B | Seçici Tekrar Pencere Kısıtı (2^(n−1)) |
| 15 | B | rwnd=0 Kilitlenmesi ve Çözümü |
| 16 | C | cwnd Hesabı (4. GDS'de değer) |
| 17 | B | TCP Reno — 3 Kopya ACK Senaryosu |
| 18 | B | Zamansız Timeout — rdt3.0 |
| 19 | B | MSS Tanımı ve Hesabı |
| 20 | B | FDM vs TDM |
| 21 | B | DNS Zehirleme Saldırısı |
| 22 | B | Rastgele ISN Seçiminin Nedeni |
| 23 | D | Yanlış Protokol Eşleştirmesi (FTP→UDP) |
| 24 | B | Sıkışma Kontrolünün İki Maliyeti |
| 25 | A | TCP Sıkışma Kontrolü Bütünleşik Senaryo |

---

> **Sınav Öncesi Son Hatırlatmalar:**
> - Formüller: d_iletim=L/R · d_yayılma=d/v · U=(L/R)/(GDS+L/R) · TahminiGDS=0.875×eski+0.125×yeni · Timeout=TahminiGDS+4×DevGDS
> - TCP Reno: 3 kopya ACK → cwnd=ssthresh=cwnd/2 · Timeout → cwnd=1, ssthresh=cwnd/2
> - GGN pencere: 2^k−1 · Seçici Tekrar pencere: 2^(k−1)
> - SMTP komutları: HELO→MAIL FROM→RCPT TO→DATA→.→QUIT
> - DNS kayıtları: A (isim→IP) · NS (alan→yetkili sunucu) · CNAME (takma ad) · MX (posta sunucusu)
