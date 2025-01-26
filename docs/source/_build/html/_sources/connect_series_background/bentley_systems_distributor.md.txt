# Bentley Systems Türkiye Distribütörü için Ürettiklerim
<div style="text-align: justify;">

## Ana başlıklar

Haziran 2023 - Şubat 2025 arasında, Bentley Systems Türkiye distribütöründe, connect serisi programlarının kullanılabilmesi için gerekli araç, ayar ve konfigürasyonları oluşturdum. Karayolu proje kökenli olmamdan kaynaklı olarak, ürettiklerim daha çok karayolu ile ilgili olsa da **Konfigürasyon** konusunda da oldukça kapsamlı bir çalışma yürüttüm.
Distribütör için çalışmaya başladığım Haziran 2023'te, Türkiye'de henüz bir çalışma var olmadığından, boş klasör ile başladığım serüvene çok ciddi bir mesai ayırdım. 
Bu sürecin ve "neler yapıldığının" farkına varılabilmesi ve yeni teknolojiye geçiş için gereksinimlere ait fikir edinilebilmesi için, yaptığım çalışmalara ait ana başlıklar ve bu başlıklara ayırdığım sürelerin yüzde olarak dağılımını aşağıdaki grafikten incelemek mümkün. Yalnızca bir **tasarım programı değişikliği değil, BIM 'in kaynak yönetimi** için oldukça farklı bir rotada seyreden çalışmalarım tüm aşamalarda "Deneme-Yanılma" metodu ile ilerledi çünkü konu ile ilgili herhangi bir konuda, programın **Help** dosyaları haricinde bir doküman bulmak hemen hemen imkansız.

<div style="text-align: center;">
    <img src="../_static/percentage_bs_time.png" alt="Percentage of Time" style="margin: 5px auto; padding: 0px; max-width: 75%; height: auto; display: block;">
</div>

## Kütüphaneler ve Civil Cell'ler

<head>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
</head>

<details style="border: 0px solid #ccc; padding: 10px; border-radius: 0px; cursor: pointer;  ">
  <summary><b>Kütüphaneler konusunda bilgi edinin <i class="fas fa-arrow-right"></i></b></summary>

> Tasarımın gerçekleşebilmesi için gerekli kütüphaneler:
>
> **Tanım Kütüphaneleri** Inroads'tan farklı olarak, Connect Serisinde ne yarattığınızı, programa önceden tarif etmelisiniz. (Inroads'ta bir style vermeden güzergah oluşturamadığınızı düşünün) Güzergahınız nasıl görüneceği gibi görsel özellikleri ve otomatik kazanacağı bazı yetenekleri de feature definition'lardan alıyor. Üstten alta doğru dört temel tarif mevcut:
> 	- Feature Definition (Örneğin Alignment>Anahat)
> 	- Feature Symbology (Örneğin Linear>Guzergah>Anahat)
> 	- Element Template (Level'ların gruplanıp klasörlenebildiği yapı)
> 	- Level (herkes hakimdir-Select serisi ile aynı)
> Tanım kütüphaneleri bu tarifleri tutar ve bir eleman oluşturduğunuzda, eleman sergilediği özellikleri bu kütüphanelerden alır.
>
> **Kesit Şablon Kütüphanesi** InRoads'un itl kütüphanesinin biraz daha gelişmişi denebilir
>
> **Dever Hesap Kütüphanesi** xml formatındadır ve  mdl programlama diline benzer bir formülasyon yapısı vardır. Hemen her matematiksel formülün girilebileceği, döngülerin (loop) dolaylı yollar ile başarılabileceği bir yapıdadır. Her güzergah değişikliğinde, program bu dosyaya tekrar başvurur verilen parametrelere göre tekrar hesaplanır.
>
> **Tasarım Standartları Kütüphanesi** Minimum spiral boyu, minimum yatay kurp uzunluğu, düşey kurplarda gerekli "K" katsayısı gibi birçok parametrenin  kontrolünü sağlar
> 
> **Görünüm Stili Kütüphanesi** Tüm tasarım ekrana "çizdirilen" elemanlar ile yürütüldüğünden karmaşık bir çalışma ortamı oluşabilir. Bu kütüphaneler, gerektiğinde doğru tasarım elemanlarına odaklanabilmeyi sağlar ve verimliliği arttırır.
> 
> **Menü Kütüphanesi** Tasarımcıları, tasarım sırasında "Ribbon"'da komutları aramaktan kurtarır. Klavye tuşlarına iş gruplarına göre yapılan atamalar ile yalnıca bir-iki tuşa basarak komutlara ulaşılır
> 
> **Paftalama Kütüphaneleri** İhtiyaç duyulan pafta formatları bu dosyalarda saklanır. Daha sonra paftalama sırasında yerleştirilen çerçeveler (named boundry) pafta formatlarını okurlar bu dosyalardan okur
> 
> **Bilgi Yazdırma Kütüphanesi** Kesit, plan ve profil bilgileri de "Annotation Groups" adı verilen yapılarda bir kütüphane dosyasında tutulur ve programa bilgi yazdırması komutunu verdiğinizde, program bu dosyalara başvurur
> 
> **Civil Cell** Bir mühendislik çözümü civil cell şeklinde kapsüllenebilir. Bir antet "cell" dosyası nasıl her çizimde kullanılabiliyor ise bir "kavşak kolu-kot taşıma" civil cell'i de her oluşturulan farklı seviyeli kavşak için kot taşıma prosedürünüzü tekrarlayabilir. Civil cell'ler olmadan, programın tasarım gücünü tam olarak kullanabilmek imkansızdır.
>



</details>

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

<head>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
</head>

<details style="border: 0px solid #ccc; padding: 10px; border-radius: 0px; cursor: pointer;  ">
  <summary><b>Konfigürasyon konusunda bilgi edinin <i class="fas fa-arrow-right"></i></b></summary>


> Tüm Connect serisi programları birer **Network** programıdır. Programlarınız eğer gerekli ayar ve kütüphaneleri bir ağdan okumuyor ise durumunuz şöyle özetlenebilir: **Yeni bir telefon aldınız ama sim karta sahip değilsiniz**. Telefonunuzu kullanabilmek, Google veya Apple serverlarındaki ayar ve fotoğraflarınıza ulaşabilmek için bir simkart da satın almalısınız.
Eğer kütüphane ve ayarlarınızı tek kaynaktan kullanıcılarınıza ulaştıramıyorsanız sizin için **InRoads** birçok açıdan daha iyi sonuçlar verebilir. Fakat **gelecek açısından InRoads'da devam etmenin iyi sonuç vermeyeceği kesin**.
>
> Connect Serisi programları için hazırlanmış kütüphaneler, **kullanıcıların bilgisayarlarına kopyalanarak kullanılmıyor**. Kütüphaneler, her bir kullanıcıya "salt okunur" olarak bir paylaşım mekanizması ile iletiliyor. Programlar kütüphanelerin içeriklerini okuyabiliyor fakat kullanıcı kütüphaneleri değiştiremiyor. 
>
> Şöyle düşünün: InRoads'ta her bir projeye çeşitli dosyaları kopyalayarak başlıyorsunuz (örneğin itl, xin vb). Bilgisayarınızda ve çeşitli hardisk/flashdisk'lerinizde toplam kaç adet **itl** veya **xin** dosyanız var? Buna bir de firmanızda çalışan tüm arkadaşlarınızı ekleyin, toplam sayı nedir?
Connect serisinde, program çalıştırıldığında, önceden ayarlanmış olan kesit kütüphanesi tüm kullanıcıların önüne "salt okunur" olarak iletilen tek bir kütüphanedir.
Bunun gibi, tüm tabaka, çizim ayarları, hesap dosyaları da tek noktadan kullanıcıların önüne otomatik olarak ulaşır. Her kütüphaneden bir adet mevcuttur. Kullanıcılar bu kütüphaneleri değiştiremez ama kullanabilir.
>
> Ayrıca programın ihtiyaç duyduğu ayar dosyalarının da kullanıcıya yine "salt okunur" olarak iletilmesi gerekiyor çünkü yüzlerce ayar dosyasını her bir kullanıcının bilgisayarına kopyalarsanız revize edilemez ve yönetilemez bir yapı oluşturursunuz.
>
> Konfigürasyon sistemleri işte bu işe yarıyor, yani tüm ayar ve kütüphaneleri kullanıcılara iletmeye. Peki bu nasıl bir düzen? Kütüphanelerde veya bir ayar değişikliği gereksiniminde bu değişiklik nasıl ve kim tarafından yapılır? **Connect Serisi programları, arka planda, daima birkaç sorumlunun çalışmasını ve sistemi takip etmesini gerektirir.** Sorumlular geri planda gerekli eklentileri yapar, kullanıcıları ekler/çıkarır, tüm sistemi tüzel kişiliğin ihtiyaçları doğrultusunda, zaman içerisinde yapılandırır ve gereksinimler doğrultusunda modifiye eder. Connect Serisi programları, **Inroads** gibi kişilerin arşivlerinin ön planda olduğu bir yapıya sahip değildir. Bir add-in üretiliyor ise veya itl kütüphanesine bir eklenti yapılacaksa, çalışmalar kaynak noktada ve herkes için yapılır.


</details>


Distribütör firma'da **Onay Makamı** ve **Proje Firması** isimlerinde iki ana konfigürasyon sistemi oluşturdum.
Programın çalışması için gerekli ayarları ve kütüphaneleri bu iki konfigürasyon sistemi ile birleştirdim. Bu iki sistem, GoogleDrive üzerinde çalışan bir mekanizmaya sahip.
Modifiye edilebilir özellikteler ve birbirlerine de bağlanabilirler. Oluşturduğum kaynaklardan (kütüphane ve ayarlar) her iki konfigürasyon sistemi de faydalanıyor. Konfigürasyon sistemleri içerisinde **tüzel kişiliğin kendisine ait kaynakları** tutabileceği bölümleri de oluşturdum. Örneğin bir firmanın anteti, eğer uygun klasöre konulur ise, firmadaki tüm proje üreticilerinin önüne gelebiliyor.

Aşağıda, **Onay Makamı** için hazırladığım konfigürasyon sistemini görüyorsunuz. Karayolu-proje kökenli olduğumdan ve içerik hazırlığım da bu yönde olduğundan, **KGM** için bir örnek sistem hazırlamayı tercih ettim. Bu sistem elbette **Rol** tabanlı ve **İdare** 'nin de eğer isterlerse proje üretebileceği yapıda. 

<div style="text-align: center;">
    <img src="../_static/config_auth_1.png" alt="Config Auth" style="margin: 5px auto; padding: 0px; height: auto; display: block;">
</div>

Konfigürasyon yalnızca OpenRoads/OpenRail designer ile ilgili değil. Oluşturduğum sistemler **tüm Bentley Systems programlarının bağlanabileceği** nitelikteler. Örneğin bir firmanın Microstation kullanan mimari grubu, OpenBridge kullanan köprü grubu vb tüm ekipleri aynı anteti, tabakaları, hesap dosyalarını aynı noktadan alabilirler. **BIM** yalnızca dijital olarak projelerinizin onayı ile ilgili değil. Kurguladığım konfigürasyon sistemleri **proje yönetimi** konularıyla ilgili olmasa da **BIM** 'in en önemli gereksinimi olan **Single Source of Truth** 'u kaynak yönetiminde kullanıcılarının hayatına katabilecek yapıda, zaten olması gereken de bu.

Aşağıda, **Proje Firmaları** için hazırladığım konfigürasyon sistemini görüyorsunuz. Gördüğünüz gibi farklı Connect Serisi programlarını kullanan proje gruplarını tek bir çatıda toplamak mümkün.

<div style="text-align: center;">
    <img src="../_static/config_cont_1.png" alt="Config Cont" style="margin: 5px auto; padding: 0px; height: auto; display: block;">
</div>

Connect serisi programlarının içerisinde mevcut olan **Rol** kavramı da farklı şekillerde sistemlere katabildim. Her bir kullanıcı, kendine atanan bir rol ile programa ulaşıyor. Rollere henüz büyük görevler yüklemesem de konfigürasyonlar içerisinde kavram olarak yüzeye çıkarttım ki gelecekte birçok farklı amaçla kullanılabilirler: örneğin bir tasarımcı programı açtığında tasarım add-in'lerine, çizimle ilgili bir teknisyen programı çalıştırdığında çizim ile ilgili add-in'lere ulaşabilir.

## Metodoloji

<details style="border: 0px solid #ccc; padding: 10px; border-radius: 0px; cursor: pointer;  ">
  <summary><b>Metodoloji konusunda bilgi edinin <i class="fas fa-arrow-right"></i></b></summary>

> Sadece yukarıdakilere sahipseniz ve programın metotlarına hakim değilseniz proje üretmeniz de mümkün olmayacaktır. Bentley Systems, kullanıcılarına **ücretsiz olarak** "Learn" başlığı altında hemen hemen her konuda dersler sunuyor. Tek bir konu olarak dikkate alırsanız dersler oldukça başarılı denebilir. Fakat tüm bir projeyi oluşturabilmeniz için **birçok değişkeni bir araya getirmeniz**, onlarca metodu kullanmanız ve **bir düzene** sahip olmanız gerekir. Örneğin hemen hemen her tasarım biriminin birer grafik olarak karşınızda olduğu ve referanslama ile dosyalar arasında aktarılabildiği bir tasarım programında, **Dosya Yönetimi** büyük önem taşıyor. Ayrıca uzun ve yoğun bir yol modelinin ortalama bir bilgisayarda nasıl yönetilmesi gerektiğine ilişkin hazır bir cevap ta bulmanız mümkün değil.
> 
> Mevcut örnekler, son ürün açısından yalnızca 3D tasarım çıkartan çok da alışık olmadığımız bir görüntü sergiliyor. Metodoloji çalışmalarımı yürütürken oluşturduğum **civil cell'leri hem 3D modeli, hem de 2D modeli birbirlerine bağlı olacak şekilde tasarladım**.
Bu sayede Türkiye ve çevre ülkelerde yıllardır ürettiğimiz proje görünümünü de yakalayabildim. InRoads'ta yıllardır kullandığım tasarım metotlarını civil cell haline getirerek yeni teknolojiye uyarlamaya çalıştım.

</details>

Bir [YouTube](https://www.youtube.com/@Kovan-Connect)  kanalı oluşturdum ve 2 kavşak içeren **somut bir proje** üzerinde, ürettiğim civil cell'leri kullanarak ilerledim. 
Süreç oldukça faydalıydı ve zaman içerisinde YouTube'da pek de örneği olmayan 24 videoluk bir seri meydana geldi. Bu kanalda yalnızca proje üretimine değil, **süreçte karşılaştığım sorunlara ve bu sorunların çözümlerine** de değinmeye çalıştım. 

YouTube için bir video hazırlamak oldukça emek isteyen bir iş, metodolojide geldiğim noktanın tamamını, Distribütör'de görev aldığım süre aralığında YouTube için hazırlamam mümkün olmadı. Toprak işleri, enkesit çizimleri, plan profil paftalarının oluşturulması gibi konuları **dökümanlaştırdım** ve örnek olarak hazırladığım projenin içerisine bu dökümanları yerleştirdim.

Metodoloji konusunda çözdüğüm başlıklar:

- Tasarım
 	- **Anahat modelleri**nin civil cell'ler ile oluşturulması ve yönetimi
 	- **Kavşak eksenleri**nin civil cell'ler ile oluşturulması
 	- Farklı seviyeli kavşaklarda **kot taşıma prosedürü**nün civil cell'ler ile gerçekleştirilmesi
 	- Taş **iksa/istinat** duvarlarının civil cell'ler ile oluşturulması
 	- Türkiye'de yaygın kullanımı olan **eşdüzey kavşak modelinin tamamının** bir civil cell ile tasarımı
 	- **Kavşak adaları**nın civil cell'ler ile tasarımı
	- İki gözlü bir **altgeçit**in civil cell'ler ile modellenmesi
 	- Çalışmalar sonucunda bir **Proje Şablonu** 'nun oluşturulması (her proje bu şablondan kopyalanarak başlar)

 - Çizimler
 	- **Enkesit paftaları**nın hazırlanması (A0 ve Rulo A0)
 	- **Plan ve Profil-Rulo** paftaların oluşturulması
 	- KGM formatında **A1-plan&profil** paftalarının oluşturulması
 	- **Yapım formatı**nda (global) A1-plan&profil paftalarının oluşturulması
	- **Sheet Index** ile paftaların **otomatik olarak numaralandırılması**
	- Cell ve Text Field kullanarak **paftaların otomatik olarak isimlendirilmesi**
 
- Raporlamalar
	- **Toprak işleri hacimleri**ne ait xml raporlarının Power Quary ile otomatik olarak Excel'e aktarımı


## Yazılımlar

### ORD Indexer

2023'te program için gerekli tanım (f. definition, f. symbology, element template, levels) girişlerini bir dgn içerisinde yapmanın çok uzun süren bir iş olduğunu fark ettim.
Ayrıca, eğer tanımları tek tek oluşturursanız genel şemanızı iyi planlayamıyorsunuz ve anlaşılır bir klasör düzeni oluşturmak imkansız hale gelebiliyor.
Buradan yola çıkarak **tanım kütüphanelerini excel ile etkileşimli olarak oluşturan** ORD Indexer'ı yazdım.
Şemanızı excel'de kuruyorsunuz ve tanım girişlerinizi ORD Indexer arayüzüne yapıyorsunuz. ORD Indexer size üç adet xml ve bir adet csv dosyası sunuyor. Bu dosyalar OpenRoads/OpenRail içerisine import ile alınabiliyor. Distribütör firma için hazırladığım tanım kütüphanelerinin büyük çoğunluğunu bu yazılım ile oluşturdum.

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
 - Duyuruları ve üye listesini kullanıcılara sunar

<video controls style="width: 100%; height: auto;">
  <source src="../_static/connector.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Admin Panel

Sistemi yönetebilmek için Admin tarafında:

 - Uygun API'leri kullanarak kullanıcılar ile yapılan paylaşımları otomasyona ile yapan,
 - Her bir kullanıcı için üretilmesi gereken konfigürasyon dosyalarını otomatik oluşturan
   bir yazılımdır.

*Bir yönetim programı olduğundan buradan bir arayüz görüntüsü paylaşmıyorum*


## Sonuçlar

<details style="border: 0px solid #ccc; padding: 10px; border-radius: 0px; cursor: pointer;  ">
  <summary><b>Ancak Add-in'ler ile başarılabilecek konular hakkıda bilgi edinin <i class="fas fa-arrow-right"></i></b></summary>

> OpenRoads/OpenRail Designer'da aşağıdaki konularda hazır bir çözüm bulunmuyor. 
> 
> - Şev Tarama
>
> - Some, yatay eksen bilgilerinin çizdirilmesi ve güzergah tablolarının hazırlanması
>
> - Enkesit tablolarının oluşturulması ve yerleşimi
>
> - Menfezlerin "kesite" göre yerleşimi mümkün değil, alışageldiğimiz yapıda bir menfez yerleşimi ancak yazılım ile çözülebilir.
>
> - Edit gerektirmeyen "dever hesabı" mümkün değildir, proje hızından düşük kurplar için dever geçiş boyunun uygulandığı aralıkta edit kaçınılmazdır
>
> - Pafta detaylarının işlenebilmesi için yeterli otomasyon yoktur
>
> - Kotlu plan üretimi
>
> Bu konular ancak add-in geliştirerek gerçekleştirilebilir.
>

</details>


Aşağıda tüm süreç için geçiş planımı görüyorsunuz. Şu ana kadar tek başıma çalıştığım bir iş bütünü olduğundan, dallara sahip değil:

<div style="text-align: center;">
    <img src="../_static/connect_plan.png" alt="Connect Plan" style="margin: 5px auto; padding: 0px; height: auto; display: block;">
</div>


**Faz-1** Distribütör firma için çalıştığım dönemde ulaştığım noktayı temsil ediyor. Faz-1, herkesin (evet bütün tasarımcıların) bağlanabileceği, olmazsa olmaz kütüphaneleri, örnek bir projeyi ve proje şablonunu içerisinde barındıran, **BIM**'in kaynak yönetimi mekanizmasını sağlayabilen, aktivasyona hazır bir sistemdir. Bundan sonraki tüm üretimler bu sistemin içerisine yerleştirilebilir. Tasarımcılar bir örnek projeyi deneyimleyebilir, geliştirebilir. 

**Faz-2**'ye ulaşıldığında program ile proje üretebilmek mümkün olacak. Bu faza **Hibrit Dönem** denebilir çünkü **Şev Tarama**, **Some ve Eksen Bilgileri**, **menfez plan yerleşimi ve menfez kesitleri** konularını InRoads ve Select Serisi VBA kodları ile tamamlamak gerekecek. Connect serisi güzergahları ve terrain'leri kolayca InRoads'a alınabiliyor. Faz-2 ve Faz-3 arasında bu alışverişten faydalanarak proje üretimi sürebilir.

**Faz-3**'e ulaşıldığında ise artık InRoads'a ve eski teknolojiye ihtiyaç kalmadan proje üretilebilecek ve geçiş tamamlanmış olacak.



## Son Söz

Bentley Systems, ortak bir çatı altında yönetilebilen, kullanıcıların yalnızca projelerine odaklandığı, tüm ayar ve gereksinimlerin arka planda tüm kullanıcılara aynı havuzdan sunulduğu bir mekanizmayı hedefleyerek Connect Serisi 'ni oluşturdu. Fakat herkes için gerekli sistemi, ayarları ve kütüphaneleri elbette hazır olarak sunmuyor, yalnızca program kurulumunda gelen basit örneklerini kullanıcılara iletiyor.  Ülkemizde yıllardır Connect Serisi programları satılmasına rağmen, konu ile ilgili herhangi bir uzman ekibin görevlendirilmemesi nedeniyle, ne idareler ne de proje firmalarının yöneticileri, temel gereksinimler konusunda bilgi sahibi olamamıştır. Tasarımcılar da ayarları tamamlanmış bir sistemde programları test edemediğinden programlar ile yapılabileceklerin farkına varamamıştır. Dünyadaki Connect Serisi'ne geçiş süreci ise uzman ekiplerin arka plan çalışmalarıyla yıllar içerisinde olgunlaşmıştır.

Distribütör firmada çalıştığım dönemde, meslek tecrübemi, yazılım geliştirme bilgimi ve Connect Serisi programlarının varoluş amacını bir araya getirerek, aktive edilebilecek durumda bir sistem kurdum ve "Faz-1" olarak isimlendirdiğim aşamaya ulaştım. Bir örnek olmadığından, var olan bir çalışma üzerinden hareket etmedim, örneği oluşturdum.

Distribütör firmanın, firma için yaptığım çalışmaları nasıl kullanacağı veya sistemi nasıl işleteceği konusunda bilgi sahibi değilim. Şunu unutmamak gerekir: Connect serisi programları arka planda sistemi canlı tutmaya, sorunlarını gidermeye ve eklentiler yapmaya çalışan uzmanlar kadar güçlüler. 

</div>


