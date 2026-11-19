# Gelişim günlüğü

Yeniden eskiye. "Test aşamasında" yazan işler kodda bitmiştir; oyun içi doğrulaması sürüyor.

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
