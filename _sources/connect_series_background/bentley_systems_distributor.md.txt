# Bentley Systems Türkiye Distribütörü için Ürettiklerim
<div style="text-align: justify;">

## Ana başlıklar
Haziran 2023 - Şubat 2025 arasında, Bentley Systems Türkiye distribütöründe, connect serisi programlarının kullanılabilmesi için gerekli araç, ayar ve konfigürasyonları oluşturdum. Karayolu proje kökenli olmamdan kaynaklı olarak, ürettiklerim daha çok karayolu ile ilgili olsa da **Konfigürasyon** konusunda da oldukça kapsamlı bir çalışma yürüttüm.
Distribütör için çalışmaya başladığım Haziran 2023'te, Türkiye'de henüz bir çalışma var olmadığından, boş bir klasör ile başladığım serüvene yaklaşık 5400 saat mesai ayırdım. 
Bu sürecin ve "neler yapıldığının" farkına varılabilmesi ve yeni teknolojiye geçiş için gereksinimlere ait fikir edinilebilmesi için, yaptığım çalışmalara ait ana başlıklar ve bu başlıklara ayırdığım sürelerin yüzde olarak dağılımını aşağıdaki grafikten incelemek mümkün. Yalnızca bir **tasarım programı değişikliği değil, BIM 'in kaynak yönetimi** için oldukça farklı bir rotada seyreden çalışmalarım tüm aşamalarda "Deneme-Yanılma" metodu ile ilerledi çünkü konu ile ilgili herhangi bir konuda, programın **Help** dosyaları haricinde bir doküman bulmak hemen hemen imkansız.

<div style="text-align: center;">
    <img src="../_static/percentage_bs_time.png" alt="Percentage of Time" style="margin: 5px auto; padding: 0px; max-width: 75%; height: auto; display: block;">
</div>

## Kütüphaneler

Programın çalışabilmesi için gerekli olan **ana kütüphane**leri, "Türkçe" olarak, Türkiye ve AASHTO standartlarını dikkate alarak oluşturdum:

 - Tanım ve Semboloji Kütüphaneleri
 - Kesit Şablon Kütüphanesi
 - Dever Hesap Kütüphanesi
 - Tasarım Standartları Kütüphanesi
 - Görünüm Stili Kütüphanesi
 - Menü Kütüphanesi
 - Paftalama Kütüphaneleri
 - Bilgi Yazdırma Kütüphanesi
 - Civil Cell kütüphaneleri


## Konfigürasyon

Connect Serisi programları için hazırlanmış kütüphaneler, **kullanıcıların bilgisayarlarına kopyalanarak kullanılmıyor**. Kütüphaneler, her bir kullanıcıya "salt okunur" olarak iletiliyor. Programlar kütüphanelerin içeriklerini okuyabiliyor fakat kullanıcı kütüphaneleri değiştiremiyor.

Şöyle düşünün: InRoads'ta her bir projeye çeşitli dosyaları kopyalayarak başlıyorsunuz (örneğin itl, xin vb). Bilgisayarınızda ve çeşitli hardisk/flashdisk'lerinizde toplam kaç adet **itl** veya **xin** dosyanız var? Buna bir de firmanızda çalışan tüm arkadaşlarınızı ekleyin, toplam sayı nedir?

Connect serisinde, program çalıştırıldığında, önceden ayarlanmış olan kesit kütüphanesi tüm kullanıcıların önüne "salt okunur" olarak iletilen tek bir kütüphanedir.
Bunun gibi, tüm tabaka, çizim ayarları, hesap dosyaları da tek noktadan kullanıcıların önüne otomatik olarak ulaşır. Her kütüphaneden bir adet mevcuttur. Kullanıcılar bu kütüphaneleri değiştiremez ama kullanabilir.

Ayrıca programın ihtiyaç duyduğu onlarca ayar dosyasının da kullanıcıya yine "salt okunur" olarak iletilmesi gerekiyor.

Konfigürasyon sistemleri işte bu işe yarıyor, yani tüm ayar ve kütüphaneleri kullanıcılara iletmeye.
Peki bu nasıl bir düzen? Kütüphanelerde veya bir ayar değişikliği gereksiniminde bu değişiklik nasıl ve kim tarafından yapılır?
Connect Serisi programları, arka planda daima birkaç sorumlunun çalışmasını ve sistemi takip etmesini gerektirir.
Sorumlular geri planda gerekli eklentileri yapar, kullanıcıları ekler/çıkarır, tüm sistemi tüzel kişiliğin ihtiyaçları doğrultusunda, zaman içerisinde yapılandırır ve gereksinimler doğrultusunda modifiye eder. 

Distribütör firma'da **Onay Makamı** ve **Proje Firması** isimlerinde iki ana konfigürasyon sistemi oluşturdum.
Programın çalışması için gerekli ayarları ve kütüphaneleri bu iki konfigürasyon sistemi ile birleştirdim. Bu iki sistem, GoogleDrive üzerinde çalışan bir mekanizmaya sahip.
Modifiye edilebilir özellikteler ve birbirlerine de bağlanabilirler. Oluşturduğum kaynakları (kütüphane ve ayarlar) her iki konfigürasyon sistemi de faydalanıyor. Konfigürasyon sistemleri içerisinde tüzel kişiliğin kendisine ait kaynakları tutabileceği bölümleri de oluşturdum. Örneğin bir firmanın anteti, eğer uygun klasöre konulur ise, firmadaki tüm proje üreticilerinin önüne gelebiliyor.

<div style="text-align: center;">
    <img src="../_static/config_auth_1.png" alt="Config Auth" style="margin: 5px auto; padding: 0px; height: auto; display: block;">
</div>

Konfigürasyon yalnızca OpenRoads/OpenRail designer ile ilgili değil. Oluşturduğum sistemler tüm Bentley Systems programlarının bağlanabileceği nitelikteler. Örneğin bir firmanın Microstation kullanan mimari grubu, OpenBridge kullanan köprü grubu vb tüm ekipleri aynı anteti, tabakaları, hesap dosyalarını aynı noktadan alabilirler. **BIM** yalnızca dijital olarak projelerinizin onayı ile ilgili değil. Kurguladığım konfigürasyon sistemleri **proje yönetimi** konularıyla ilgili olmasa da **BIM** 'in en önemli gereksinimi olan **Single Source of Truth** 'u kaynak yönetiminde kullanıcılarının hayatına katabilecek yapıda, zaten olması gereken de bu.

Connect serisi programlarının içerisinde mevcut olan **Rol** kavramı da farklı şekillerde sistemlere katabildim. Her bir kullanıcı, kendine atanan bir rol ile programa ulaşıyor. Rollere henüz büyük görevler yüklemesem de konfigürasyonlar içerisinde kavram olarak yüzeye çıkarttım ki gelecekte birçok farklı amaçla kullanılabilirler: örneğin bir tasarımcı programı açtığında tasarım add-in'lerine, çizimle ilgili bir teknisyen programı çalıştırdığında çizim ile ilgili add-in'lere ulaşabilir.

## Metodoloji

Elbette sadece yukarıdakilere sahipseniz ve programın metotlarına hakim değilseniz proje üretmeniz de mümkün olmayacaktır. Bentley Systems, kullanıcılarına ücretsiz olarak "Learn" başlığı altında hemen hemen her konuda dersler sunuyor.
Tek bir konu olarak dikkate alırsanız dersler oldukça başarılı denebilir. Fakat tüm bir projeyi oluşturabilmeniz için birçok değişkeni bir araya getirmeniz, onlarca metodu kullanmanız ve **bir düzene** sahip olmanız gerekir.
Örneğin hemen hemen her tasarım biriminin birer grafik olarak karşınızda olduğu ve referanslama ile dosyalar arasında aktarılabildiği bir tasarım programında, **Dosya Yönetimi** büyük önem taşıyor.
Bunlara ilave olarak uzun ve yoğun bir yol modelinin ortalama bir bilgisayarda nasıl yönetilmesi gerektiğine ilişkin hazır bir cevap ta bulmanız mümkün değil.

Mevcut örnekler, son ürün açısından yalnızca 3D tasarım çıkartan çok da alışık olmadığımız bir görüntü sergiliyor. Metodoloji çalışmalarımı yürütürken oluşturduğum civil cell'leri hem 3D modeli, hem de 2D modeli birbirlerine bağlı olacak şekilde tasarladım.
Bu sayede Türkiye ve çevre ülkelerde yıllardır ürettiğimiz proje görünümünü de yakalayabildim. InRoads'ta yıllardır kullandığım tasarım metotlarını civil cell haline getirerek yeni teknolojiye uyarlamaya çalıştım.

Bir [YouTube](https://www.youtube.com/@Kovan-Connect)  kanalı oluşturdum ve 2 kavşak içeren somut bir proje üzerinde, ürettiğim civil cell'leri kullanarak ilerledim. 
Süreç oldukça faydalıydı ve zaman içerisinde YouTube'da pek de örneği olmayan 24 videoluk bir seri meydana geldi. Bu kanalda yalnızca proje üretimine değil, süreçte karşılaştığım sorunlara ve bu sorunların çözümlerinde de değinmeye çalıştım.

YouTube için bir video hazırlamak oldukça emek isteyen bir iş, metodolojide geldiğim noktanın tamamını YouTube için


## Yazılımlar

### ORD Indexer

2023'te boş bir dgn içerisinde, program için gerekli tanım (f. definition, f. symbology, element template, levels) girişlerini yapmanın çok uzun süren bir iş olduğunu fark ettim.
Ayrıca, eğer tanımları tek tek oluşturursanız genel şemanızı iyi planlayamıyorsunuz ve anlaşılır bir klasör düzeni oluşturmak imkansız hale gelebiliyor.
Buradan yola çıkarak tanım kütüphanelerini excel ile etkileşimli olarak oluşturan ORD Indexer'ı yazdım.
Şemanızı excel'de kuruyorsunuz ve tanım girişlerinizi ORD Indexer arayüzüne yapıyorsunuz. Program size üç adet xml ve bir adet csv dosyası sunuyor.
Bu dosyalar OpenRoads/OpenRail içerisine import ile alınabiliyor.

<div style="position: relative; width: 100%; max-width: 800px; height: 450px; margin: 0 auto; min-height: 300px;">
  <iframe
    src="https://www.youtube.com/embed/UQRc8n_g_OE"
    frameborder="0"
    allowfullscreen
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
  ></iframe>
</div>

### Connector

Kullanıcıların sisteme ulaşmasını sağlamak için KULLANICI tarafında:

 - Connect Serisi programlarını kurduğum sisteme bağlar
 - Video izleme mekanizması içerir
 - Doküman okuma mekanizması içerir
 - Duyuruları ve üyeleri tablolaştırır ve kullanıcılara sunar

### Admin Panel

Sistemi yönetebilmek için Admin tarafında:

 - Uygun API'leri kullanarak kullanıcılar ile yapılan paylaşımları otomasyona ile yapan,
 - Her bir kullanıcı için üretilmesi gereken konfigürasyon dosyalarını otomatik oluşturan
   bir yazılımdır.

*Bir yönetim programı olduğundan buradan bir arayüz görüntüsü paylaşmam doğru olmaz*


## Sonuçlar

Distribütör için çalıştığım dönemde **Faz-1** ile belirttiğim noktaya ulaştım. 

**Faz-2**'ye ulaştığımda program ile proje üretebilmek mümkün olacak, fakat bu faza **Hibrit Dönem** denebilir çünkü bu fazda:
 - Şev Tarama
 - Some ve Eksen Bilgileri
konularını InRoads ve Select Serisi VBA kodları ile tamamlamak gerekecek.

**Faz-3**'e ulaştığımda ise artık InRoads'a ve eski teknolojiye ihtiyaç kalmadan proje üretilebilecek ve geçiş tamamlanmış olacak

Distribütör firmada çalıştığım dönemde, küçük parçaları birbirlerine entegre ederek büyük bir yapı oluşturdum. Burada yazılanları okuyarak, güncel teknoloji gereksinimleri konusunda az çok bir fikre sahip olmuşsunuzdur.

Distribütör firmanın, firma için yaptığım çalışmalarımı nasıl kullanacağı konusunda bir fikre sahip değilim. Şunu unutmamak gerekir: Bu çalışmalar arka planda sistemi canlı tutmaya, sorunlarını gidermeye ve eklentiler yapmaya çalışan kişiler kadar güçlüler.

</div>


