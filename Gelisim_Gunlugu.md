# Gelişim günlüğü

Yeniden eskiye. "Test aşamasında" yazan işler kodda bitmiştir; oyun içi doğrulaması sürüyor.

---

## 22 Kasım 2026

**Sürüm 1.0.2: yüzler, GM yetkisi ve tek programla sunucu** · *test aşamasında*
- **Yüzler:** kurulan oyunda karakterlerin yüzü görünmüyordu. Yüz, göz ve canlı ifade verileri pakete eklendi; her paket artık
  yayından önce eksik varlık için denetleniyor. Timex'in bıyığındaki düz beyaz alan da giderildi.
- **GM yetkisi:** yalnız kurucu hesapta. Kurucu, F8 menüsündeki yeni **GM** sekmesinden GM ekleyip çıkarabiliyor; değişiklik
  bağlı oyuncuya birkaç saniyede geçiyor. Yetki alınınca ölümsüzlük, hız ve görünmezlik de geri alınıyor. Karar sunucuda,
  doğrulanmış giriş biletine göre veriliyor.
- **Sunucu güvenliği:** ağ üzerinden gelen geliştirici komutları kapatıldı; hız hilesine karşı hareket zamanı denetimi eklendi
  (bağlantısı takılan oyuncu cezalanmıyor).
- **Xalasco Sunucu:** ev sahibi için tek program. Çift tıklayınca hesap sunucusunu ve oyun sunucusunu doğru sırayla açıyor;
  durum, hesaplar, GM'ler, ayarlar ve günlük tek pencerede.
- **Sesli sohbet:** `/sustur` komutları, Sosyal penceresinde ses listesi. Konuşanın kimliği sunucuda doğrulanıyor.
- Paketli oyunla uçtan uca denendi: gerçek giriş biletiyle kurucu GM oldu, ikinci oyuncu olmadı; canlı GM verme ve alma çalıştı.

**Sosyal sistemler** · *test aşamasında*
- **Sohbet:** yeni Bölge, Grup ve Fısıltı kanalları; `/f`, `/c`, `/g`, `/davet`, `/arkadas`, `/engelle` gibi komutlar.
  Boşluklu adlar da yazılabiliyor.
- **Grup:** beş kişi, ekranda grup çerçeveleri. Yakındaki grup üyeleri mob öldürünce deneyim, görev ilerlemesi ve kendi
  ganimetlerini alıyor.
- **Arkadaş ve engel listesi:** **O** tuşuyla açılan Sosyal penceresi; engellenen oyuncunun mesajları ve istekleri hiç
  görünmüyor.
- Bir oyuncunun adına ya da çerçevesine sağ tıklayınca açılan menü; grup, takas ve düello istekleri ekranda kart olarak geliyor.
- **Doğrudan takas:** sekiz yuva ve altın; iki adımlı onay (kilitle, sonra onayla). Herhangi bir değişiklik iki onayı da
  sıfırlıyor. Takas ya bütünüyle gerçekleşiyor ya da hiç: yarıda bir şey olursa iki çanta da eski hâline dönüyor.
- **Düello:** iki oyuncunun arasına dikilen bayrak, "3, 2, 1, Başla!", 40 m'lik alan. Öldürücü vuruş canı 1'de bırakıyor,
  kimse ölmüyor; bitince can ve mana geri geliyor. Dışarıdan kimse karışamıyor.
- **Ekipman inceleme:** oyuncunun kuşandıkları, seviyesi ve sınıfı.
- Hepsi sunucu otoriteli. Her istek sunucuda denetleniyor ve hızı sınırlı.

**Sesli sohbet** · *test aşamasında*
- İki kanal: **Yakın** (30 m içindekiler, uzaklaştıkça kısılıyor) ve **Grup** (uzaklık sınırı yok).
- Bas-konuş (Fare 4 / Fare 5 ya da Sol / Sağ Ctrl) ya da açık mikrofon.
- Konuşanın isminde halka, grup çerçevesinde nokta; oyuncuya sağ tıklayıp **Sesini kapat**.
- Ayarlar > Ses: sesli sohbet açık / kapalı, kip, ses düzeyi, mikrofon kazancı ve eşiği, **Mikrofonu Dene**.
- Ses oyunun kendi bağlantısından gidiyor, ek bir ayar gerekmiyor.

**Paketli oyun ve kurulum paketi** · *test aşamasında*
- Oyun ilk kez dağıtılabilir biçimde paketlendi (1,3 GB). İlk denemede ortaya çıkan, yalnız paketli oyunda görülen bir çökme
  giderildi.
- Tam tur denendi: başlatıcının aldığı giriş biletiyle paketli oyun sunucuya bağlandı.
- Oynamak isteyenler için başlatıcı kurulum paketi bu depoya kondu: **[Nasıl oynanır](README.md#nasıl-oynanır)**.

---

## 21 Kasım 2026

**Online oyun: Xalasco Merkez, Xalasco Başlatıcı ve giriş bileti** · *test aşamasında*
- Oyun artık arkadaşlarla internet üzerinden oynanacak biçimde kuruldu. Ev sahibinin bilgisayarı sunucu oluyor. Bağlantı, yalnız davet edilen cihazların girebildiği şifreli özel bir ağ (Tailscale) üzerinden geçiyor; oyun herkese açık değil.
- **Xalasco Başlatıcı:**
  - Kullanıcı adı ve parolayla giriş, kayıt ve "şifremi unuttum".
  - Her yeni sürümde oyunu kendisi güncelliyor: yalnız değişen parçaları indiriyor ve yarıda kalan indirmeyi kaldığı yerden sürdürüyor. **Onar** bozuk dosyaları yeniden indiriyor.
  - Başlatıcı kendini de güncelliyor.
- **Xalasco Merkez:** hesapları, güncellemeleri ve haberleri dağıtan küçük sunucu. Parolalar hiçbir yerde düz yazılmıyor, tuzlanıp özetlenerek saklanıyor. Hatalı giriş denemeleri sınırlı.
- **Giriş bileti:**
  - **OYNA**'ya basınca başlatıcı tek kullanımlık, iki dakika geçerli, imzalı bir bilet alıyor.
  - Oyun sunucusu yalnız geçerli bileti olan oyuncuyu içeri alıyor.
  - Aynı hesapla ikinci bir yerden girilince eski oturum kapanıyor.
- Oyunda **Sunucuya Katıl** ve **Sunucu Kur** menüsü var. Sunucu pencere açmadan arka planda da çalışabiliyor.
- Giriş yolu uçtan uca denendi: geçerli bilet kabul edildi, kullanılmış ve eksik bilet reddedildi. Paketli oyunla tam tur sırada.

| Merkez'e bağlanma | Giriş |
|:---:|:---:|
| <img src="Ekran/90_baslatici_merkez.jpg" alt="Başlatıcı: Merkez adresi"> | <img src="Ekran/90_baslatici_giris.jpg" alt="Başlatıcı: giriş ekranı"> |
| **Güncelleme indiriliyor** | **Oyun güncel** |
| <img src="Ekran/90_baslatici_indirme.jpg" alt="Başlatıcı: yalnız değişen parçaları indiriyor"> | <img src="Ekran/90_baslatici_oyna.jpg" alt="Başlatıcı: OYNA"> |

**Kuvvetler ve alanlar (altyapı)** · *test aşamasında*
- Çekim kuyuları, itme dalgaları, savuran girdaplar ve yerçekimini değiştiren alanlar için ortak bir kuvvet sistemi yazıldı.
- Üst üste binen kuvvetler toplanıyor ve bir tavanla sınırlanıyor. Yerçekimi azaltılabiliyor, ters çevrilebiliyor; süzülme sağlanabiliyor.
- Yeni sınıfların yetenekleri bunun üstüne kurulacak. Otomatik testlerin hepsini geçti; oyunda açılması sırada.

**Sırada: sosyal sistemler ve sesli sohbet** · *yazılıyor*
- Beş kişilik grup, fısıltı, arkadaş ve engel listesi.
- Oyuncuya sağ tıklayınca açılan menü ve grup çerçeveleri.
- İki adımlı onaylı doğrudan takas.
- Her yerde düello ve ekipman inceleme.
- Yakındakiler ve grup için sesli sohbet.

## 20 Kasım 2026

**Hikâye genişledi: yedi bölüm ve sinematikler** · *test aşamasında*
- Ana hikâye yedi bölüme çıktı ve iki perdeye ayrıldı: **Perde I · Son Vuruş** ve **Perde II · Ayarsız Kalp**. Önsözden sonra karakola varış, ardından her bölümün açılışında ve dönüm noktasında anlatımlı kısa sinematikler geliyor: Ayna Gölü'ndeki görü, **Kristal Yankılar**, taçlı ismin açığa çıkışı, **Fırtınanın Gözü**, **Solgun Orman**, **Saatin Harabeleri**, **Kalp Saati**, yeni şafak, **Atlanan Tık** ve Arşiv Geçidi. Son sahne **Kadranis Eteği**'ne açılıyor.
- Ayna Gölü sahnesinde anlatılan görü artık ekranda: suyun üstünde mor gözlü, taçlı bir gölge ve ardında elinde yarım bir dişli tutan soluk bir kız beliriyor; anlatının son cümlesinde ikisi de incelip dağılıyor.
- Sinematik kamerası yere ve göle gömülmeden uçuyor. Yakın planlarda konuşan karakterin yüzüne yumuşak bir dolgu ışığı düşüyor (gece soğuk, gündüz sıcak), asa ve silah yüz kadrajına girmiyor.

| Uyanış | Komutan Vela | Ayna Gölü'ndeki görü |
|:---:|:---:|:---:|
| <img src="Ekran/80_cine_uyanis.jpg" alt="Uyanış sineması"> | <img src="Ekran/80_cine_vela.jpg" alt="Komutan Vela Orrin"> | <img src="Ekran/80_cine_ayna.jpg" alt="Ayna Gölü'nde taçlı gölge ve kız"> |
| **Kâhin Lio** | **Dev Kristal** | **Usta Bram** |
| <img src="Ekran/80_cine_lio.jpg" alt="Kâhin Lio"> | <img src="Ekran/80_cine_kristal.jpg" alt="Kristal Vadi'nin kalbi"> | <img src="Ekran/80_cine_bram.jpg" alt="Usta Bram Kızılörgü"> |
| **Yeni şafak** | **Arşivci Orin** | **Atlanan Tık** |
| <img src="Ekran/80_cine_safak.jpg" alt="Işıltı Havzası'nda şafak"> | <img src="Ekran/80_cine_orin.jpg" alt="Arşivci Orin"> | <img src="Ekran/80_cine_tik.jpg" alt="Kalp Saati'nin atladığı tık"> |

**Etkileşimli dünya** · *test aşamasında*
- Dünyadaki eşyaların çoğu artık kullanılabiliyor. Önüne gelince **[E]** istemi çıkıyor ve bakılan eşyanın kenarı hafifçe parlıyor.
- **Bank, devrik kütük, kesik kök:** oturulur. Kamera alçalır; herhangi bir hareket, zıplama, yetenek ya da tekrar E kaldırır. Savaşta oturulmaz, darbe alınca kalkılır.
- **Kamp ateşi:** başına oturunca 3 saniye sonra **Ateş Başı** gelir (10 dk, kışın 15 dk). Ayazı ve kış yavaşlamasını kaldırır; otururken can iki kat hızlı dolar.
- **Sandık, varil, konteyner, enkaz:** aranır. Karakter diz çöküp kurcalar, ganimet eşyadan fırlar. Aynı eşya oyuncu başına 30 dakikada bir aranabilir; kısa sürede çok arama yapılamaz.
- **Pano, totem, sınır taşı, tezgâh, anten:** okunur; köşede bölgenin hikâyesinden bir not çıkar. Çadır girişinde dinlenilir, sohbete **/otur** yazınca olduğun yere oturursun.

| Bankta oturmak | Kış akşamı ateş başı |
|:---:|:---:|
| <img src="Ekran/82_etk_bank.jpg" alt="Bankta oturan Speeder"> | <img src="Ekran/82_etk_ates.jpg" alt="Kamp ateşinin başında Ateş Başı"> |
| **Bakılan eşya parlar** | **Varil aramak** |
| <img src="Ekran/82_etk_odak.jpg" alt="Odaktaki varil ve Ara istemi"> | <img src="Ekran/82_etk_ara.jpg" alt="Varili arayan Panzer"> |

**Efsanevi silahlar** · *test aşamasında*
- On iki silah türünün her birine ayrı bir efsanevi model yapıldı: asa, değnek, küre, kitap, kılıç, hançer, teber, çakram, çekiç, balta, balyoz ve kol topu. Her birinin kendi silueti, parlayan bir çekirdeği, dönen bir hâlesi ve parçacık izi var.
- Tasarımlar MMORPG'lerin efsanevi silah anlayışından yola çıktı: uzaktan tanınan bir siluet, tek bir parlak odak noktası, sade bir sap ve hareketli bir süs.
- Sıradan silahlar da artık birbirine benzemiyor: altı ayrı asa stili var ve her silah türünün birden çok tasarımı oyunda.

| Asa | Küre | Kitap |
|:---:|:---:|:---:|
| <img src="Ekran/77_efsane_asa.jpg" alt="Efsanevi asa"> | <img src="Ekran/77_efsane_kure.jpg" alt="Efsanevi küre"> | <img src="Ekran/77_efsane_kitap.jpg" alt="Efsanevi kitap"> |
| **Çakram** | **Balyoz** | **Kılıç** |
| <img src="Ekran/77_efsane_cakram.jpg" alt="Efsanevi çakram"> | <img src="Ekran/77_efsane_balyoz.jpg" alt="Efsanevi balyoz"> | <img src="Ekran/77_efsane_kilic.jpg" alt="Efsanevi kılıç"> |

<p align="center"><img src="Ekran/76_asa_stilleri.jpg" alt="Altı asa stili" width="100%"><br><em>Altı asa stili</em></p>

**Gerçekçi kumaş ve pelerinler** · *test aşamasında*
- Kıyafetler metalik görünümden çıktı: keten, deri ve yırtık pelerinler gerçek kumaş dokusuyla, kumaş fiziğiyle dalgalanıyor. Eski parçalar eşya olarak oyunda kaldı.

| Speeder önden | Timex arkadan | Yırtık pelerin |
|:---:|:---:|:---:|
| <img src="Ekran/75_kumas_speeder_on.jpg" alt="Speeder kumaş kıyafet"> | <img src="Ekran/75_kumas_timex_arka.jpg" alt="Timex pelerin arkadan"> | <img src="Ekran/75_kumas_pelerin_yirtik.jpg" alt="Yırtık pelerin"> |

**Doğa: yapraklı ağaçlar ve uçan adalar** · *test aşamasında*
- Ağaç taçları tek bir küre yerine binlerce yapraktan oluşuyor; çamlar dal dal, iğne iğne yeniden yapıldı. Rüzgârda yaprak uçları sallanıyor, sonbaharda renk değiştiriyor.
- Uçan adaların alt yüzü kaya katmanlarıyla yontuldu; üstlerinde küçük ağaçlar, altlarında sarkan kökler var.

| Çayır | Uçan adalar |
|:---:|:---:|
| <img src="Ekran/81_agac_cayir.jpg" alt="Yapraklı çayır ağaçları"> | <img src="Ekran/81_agac_adalar.jpg" alt="Ağaçlı uçan adalar"> |
| **Çam ormanı** | **Sonbahar** |
| <img src="Ekran/81_agac_cam.jpg" alt="Çam ağaçları"> | <img src="Ekran/81_agac_sonbahar.jpg" alt="Sonbahar ağaçları"> |

**Yüzler, saçlar ve nişan** · *test aşamasında*
- Moblar artık boş boş bakmıyor: yakın planda gözleri açık ve dikkatli. Kukuletaları mat deri, altlarında saç var.
- Karakoldaki NPC'lere saç eklendi.
- Serbest nişan: sağ tıkla omuz kamerasına geçilip nişangâhla hedef alınabiliyor.

| Kukuletalı kâhin | Timex nişan alırken |
|:---:|:---:|
| <img src="Ekran/78_yuz_mob_gun.jpg" alt="Solgun Kâhin'in yüzü yakından"> | <img src="Ekran/79_nisan_timex.jpg" alt="Timex serbest nişan"> |

**Gerçek uçuşlu mermiler (altyapı)** · *test aşamasında*
- Oklar, cıvatalar ve büyü mermileri artık anında isabet etmek yerine gerçekten uçabiliyor. Yerçekimiyle düşüyor, yan rüzgârla sürükleniyor ve uzakta güç kaybediyor; Vael gecelerinde düşüş azalıyor.
- Çekim kuyuları ve zaman alanları mermiyi bükebiliyor, yavaşlatabiliyor ya da yörüngesine alabiliyor. Kalkanlar mermiyi durdurabiliyor ya da geri sektirebiliyor.
- Sunucu her atışı kendisi hesaplıyor; oyuncunun ekranındaki mermi aynı yolu izliyor. Gecikmeli oyuncu da hedefini gördüğü yerde vurabiliyor.
- Arbalist ve Gravitor bu altyapının üstüne kurulacak. Şimdilik oyunda açık değil; Kâhin'in büyü mermisi deneme ayarıyla bu yoldan uçabiliyor.

**Test altyapısı**
- Fotoğraf turuna hikâye sinematikleri, mob yüzleri, efsanevi silahlar ve etkileşim sahneleri eklendi. Etkileşim için 34 yeni otomatik denetim yazıldı; hepsi geçti.
- Mermi altyapısı için 38 otomatik denetim yazıldı (düşüş ve rüzgâr sayıları, isabet, delme, kalkan, alan bükmesi, ağ eşitliği); hepsi geçti.

---

## 19 Kasım 2026

**Cryon: altı yetenek ve ilk ulti oyunda** · *test aşamasında*
- Cryon'un ilk yetenek seti tamamlandı: **Ayaz Kesiği**, **Termal Akış**, **Termal Şok**, **Donma Noktası**, **Ayaz Duvarı**, imza yeteneği **Isı Dalgası** ve Sv 10 ultisi **Ayaz Halkası**. Sv 5'te **Isı Kalbi** pasifi açılıyor.
- **Termal Merdiven:** düşman soğudukça adım adım yavaşlıyor. Önce *Serin* (hareket ve saldırı hızı −%15), sonra *Buzlu* (−%30), en sonunda 2 saniyeliğine buz kalıbında *Donmuş*. Bosslar donmuyor; onun yerine *Kırılgan* oluyor.
- Sınıfın döngüsü: **Soğut → Çek → Aktar → Şokla.** Termal Akış tek tuşta iki iş yapıyor: dokununca dosta ısı aktarıyor, basılı tutunca düşmandan ısı çekiyor (*Soğuk Avuç*). Termal Şok yalnız Buzlu ya da Donmuş düşmana (ya da kendi Ayaz Duvarı'na) çalışıyor.
- Termal Rezerv düşmanı soğuttukça doluyor, aktarım ve şokla harcanıyor; Isı Dalgası hepsini bir anda salıyor.
- Görünüm yenilendi: teber kalınlaştı; beyaz yalıtımlı zırh plakaları, yeni omuzluklar ve uyluk plakaları geldi. Yeteneklerin efektleri ve sesleri eklendi.
- **Teber zıplarken artık yüzün önünden geçmiyor.** Ağır teber kendi tutuşunu aldı: havada ve inişte yanda, dik taşınıyor; oyun kamerasında baş hep açık. Timex'in asası ve Speeder'ın teberi eskisi gibi.

| Zıplarken Teber yanda | Oyun kamerasından |
|:---:|:---:|
| <img src="Ekran/66_jump_cryon.jpg" alt="Cryon zıplarken, Teber yanda ve dik"> | <img src="Ekran/66_jump_cryon_gameplay.jpg" alt="Oyun kamerasından zıplayan Cryon"> |

| Önden | Arkadan | Ayaz Kesiği: Saplama ile donan düşman |
|:---:|:---:|:---:|
| <img src="Ekran/C13_cryon_hero.jpg" alt="Cryon önden"> | <img src="Ekran/C13_cryon_hero_back_2.jpg" alt="Cryon arkadan, soğutma tüpü ve omuzluklar"> | <img src="Ekran/C13_cryon_basic.jpg" alt="Ayaz Kesiği ile buz kalıbına giren düşman"> |
| **İmza: Isı Dalgası** | **Ulti: Ayaz Halkası** | **20 sınıflık seçim ekranı** |
| <img src="Ekran/C13_cryon_sig.jpg" alt="Isı Dalgası"> | <img src="Ekran/C13_cryon_ult1.jpg" alt="Ayaz Halkası"> | <img src="Ekran/C13_cryon_select_2.jpg" alt="20 sınıflık seçim ekranı"> |

**20 sınıfa hazırlık: çekirdek sistemler** · *test aşamasında*
- Karakter oluşturma ekranında artık 20 sınıfın tamamı var: rol süzgeçli (yakın, menzilli, tank, şifacı, destek, kontrol) bir rozet ızgarası. Henüz hazır olmayan sınıflar soluk görünüyor; Cryon "pilot" etiketiyle seçilebiliyor.
- Kayıt sistemi yeni sürüme geçti; eski karakterler korunarak yükleniyor.
- Ortak savaş kuralları tek yerde toplandı: oyuncuya karşı oyuncu katsayısı, art arda gelen kontrol etkilerinin azalması, kalkan kuralları.
- İtme, savrulma, atılma ve ışınlanma için yeni ortak hareket çekirdeği eklendi. Şimdilik eski yoldan çalışıyor; oyun içi karşılaştırmadan sonra açılacak.
- Haritanın büyümesi için bölge ve mob verisi altyapısı hazırlandı.

**Test altyapısı**
- Otomatik duman testi 600'ü aşkın denetimle koşuyor; son koşuda 617 denetimin 591'i geçti. Kalanların hepsi yeni eklenen ve ayarı süren silah aralığı ölçümleri ile bir kamera sahnesi. Testin bulduğu gerçek sorun (Cryon'un teberi zıplarken yüzün önünden geçiyordu) aynı akşam düzeltildi.
- Yeni test türleri: oynanış senaryoları (27/27 geçti), sunucu + istemci ile çok oyunculu testler ve performans ölçümü.

**Kararlılık**
- Dünkü ekran kartı çökmesi önleminin oyunda gerçekten uygulandığı doğrulandı; bu akşamki 161 karelik fotoğraf turunda çökme olmadı.

---

## 18 Kasım 2026

**İlk yeni sınıf: Cryon** · *test aşamasında*
- 20 sınıflık yolun ilk yeni sınıfı oyuna girdi. **Cryon**, ısıyı düşmandan çalıp dosta taşıyan buzul kalkanı: bir kontrol tankı.
- Silahı **Termal Teber**. Göğsünde turuncu **Isı Kalbi**, sırtında soğutma tüpü var.
- Mana yerine kendi kaynağı var: **Termal Rezerv** (0–100). Ekranda yeni bir bar ve dikey bir cam tüp görünüyor. Rezervi 40–80 arasındaki **Denge Bandı**'nda tutmak sınıfın temel ritmi.
- İlk yeteneği **Ayaz Kesiği** çalışıyor. Sırada kalan yetenekler, buz duvarı ve **Ayaz Halkası** ultisi var.
- Görünüm hâlâ işleniyor: teber kalınlaşacak, omuzluklar ve beyaz zırh plakası yenilenecek.
- Karakter oluşturma ekranı dört sınıfa göre yenilendi: seçili sınıfın kartı açılıp açıklamasını gösteriyor.

| Sınıf seçimi | Termal Rezerv ve Ayaz Kesiği | Sırttaki soğutma tüpü |
|:---:|:---:|:---:|
| <img src="Ekran/C13_cryon_select.jpg" alt="Cryon sınıf seçimi"> | <img src="Ekran/C13_cryon_hud.jpg" alt="Cryon savaşta, Termal Rezerv barı"> | <img src="Ekran/C13_cryon_hero_back.jpg" alt="Cryon arkadan"> |

**Yeni sınıflar için ortak altyapı** · *test aşamasında*
- Her sınıf kendi kaynağını ve kaynak barını taşıyabiliyor.
- Sınıfların dünyaya koyduğu yapılar (duvar, kule gibi) için ortak bir temel kuruldu.
- Sınıfların düşmana koyduğu yavaşlatma ve dondurma gibi durumlar için de ortak bir temel var.
- Speeder, Panzer ve Timex'in görünümü ve sayıları değişmedi. Bu, otomatik testlerle ve eski görüntülerle karşılaştırılarak doğrulandı.

**Kararlılık** · *test aşamasında*
- Oyun açılırken ara sıra yaşanan ekran kartı çökmesinin kaynağı bulundu: motorun gölge hesabındaki bir hata. Bir gölge ayarıyla önlendi; denemede 20 açılışın hiçbirinde çökme olmadı.

**Yeni ekran görüntüleri: kahramanlar en iyi ekipmanlarıyla**
- Üç sınıf da en güçlü setleri, mitik silahları ve efsanevi parçalarıyla oyun içinden yeniden fotoğraflandı (ana sayfada **Kahramanlar** bölümü).
- Oyun içi fotoğraf turu geliştirildi: kahraman kadrajda ortalanıyor, göğüs portresi ve sırttan çekim (kanat / pelerin) eklendi, çekim sırasında motor uyarıları kareye düşmüyor.

| Speeder | Panzer | Timex |
|:---:|:---:|:---:|
| <img src="Ekran/70_vitrin_speeder_dusk.jpg" alt="Speeder"> | <img src="Ekran/70_vitrin_panzer_snow.jpg" alt="Panzer"> | <img src="Ekran/70_vitrin_timex_vael.jpg" alt="Timex"> |

**Silah ve hareket cilası (2. tur)** · *test aşamasında*
- Timex'in asası zıplarken ve inerken artık yüzün önünden geçmiyor.
- Kalkan doğru yöne bakıyor; kola girmiyor, havada "tepsi" gibi yatmıyor.
- Panzer boştayken çekici öne uzatmak yerine bacağının yanında taşıyor.
- Zıplama ve inişteki ani silah sıçraması giderildi; geçişler tek ve yumuşak.
- Uzak karakterlerde de doğru tutuş; ön kol burulması ve havada boşta kalan kolun duruşu düzeltildi.

**Savaş kamerası (2. tur)** · *test aşamasında*
- Sevilen vuruş sarsıntısı korundu; boss ağır çekimindeki aşırı sallantı azaltıldı.
- Kamera ağaç, sütun, çit ve kemerlere girmiyor; en yakın boş noktaya yumuşakça kayıyor, engel kalkınca yavaşça geri açılıyor.
- Kahramanı örten düşmanlar yarı saydamlaşıyor; kamera dev bir bossun içine girerse boss tamamen soluyor.
- Yamaçlarda kamera yükseliyor, ışınlanmada yeniden ortalanıyor; dikey bakış ±80° ile sınırlandı.

**20 sınıf altyapısı başladı**
- Sınıfların tek bir kayıt sisteminden beslenmesi ve 17 yeni sınıfın iskeleti üzerinde çalışılıyor.

**Diğer**
- Yapımcılar ekranı güncellendi.
- Bu gelişim sayfası açıldı.

---

## 17 Kasım 2026

**Büyük tasarım belgesi tamamlandı**
- 17 yeni sınıf (toplam 20), her sınıf için uzmanlıklar, evrim ve uyanış sistemleri, denge kuralları.
- Dünya, hikâye ve görev planı: haritanın yaklaşık 4 katına çıkması, 6 yeni büyük bölge, 7 perdelik ana hikâye ("Yedi Kışın Borcu"), yaklaşık 285 yeni görev.

**Oyun içi odak efekti (alan derinliği)**
- Karakter keskin, arka plan yumuşak bulanık. Ayarlar'dan **Kapalı / Hafif / Sinematik** seçilebiliyor; savaşta otomatik hafifliyor.

| Kapalı | Sinematik |
|:---:|:---:|
| <img src="Ekran/67_focus_outpost_off.jpg" alt="Odak kapalı"> | <img src="Ekran/67_focus_outpost_sinematik.jpg" alt="Odak sinematik"> |

**Savaş kamerası ve silah aralığı (1. tur)**
- Silahların gövdeye, kafaya ve pelerine girmesini önleyen sistem; kamera yakınlaştırma ve sarsıntı düzenlemeleri.
- Otomatik test sayısı 391'e çıktı (391/391 geçti).

---

## Kasım 2026 öncesi (özet)

- 3 sınıf (Speeder, Panzer, Timex), Gameplay Ability System ile yetenekler ve Rezonans sinerjisi.
- 6 × 6 km dünya, 5 bölge, 29 mob kampı, Kronit Kapıları, hover-kızak binek.
- Önsöz sineması, 25 görevlik ana hikâye, 26 yan görev, final boss Morvax.
- Dört mevsim, gün/gece, gerçek 3B kar ve yağmur, donan göl, Zaman Fırtınası dünya olayı.
- Envanter, ganimet, + basma, üretim, yetenek ağacı, başarımlar, günlük görevler, dünya haritası.
- Gerçekçi karakter oluşturma, berber, kumaş pelerinler, set zırhları.
- Sunucu otoriteli çok oyunculu yapı; otomatik duman testleri ve fotoğraf turu.
